# G-Labs Voice Studio — Hướng dẫn tích hợp Webhook API

> Đối tượng đọc: lập trình viên, người tích hợp kỹ thuật, và AI agent.
> Mục tiêu: cung cấp đầy đủ mọi thứ cần để tích hợp đúng Webhook REST API của Voice
> Studio — endpoint, xác thực, schema request/response, voice preset, tham số, xử lý
> lỗi, và quy trình bất đồng bộ (gửi → hỏi trạng thái → tải về).

Tài liệu này mô tả API do tab **Webhook** của ứng dụng desktop **G-Labs Voice Studio**
(studio chuyển văn-bản-thành-giọng-nói / nhân bản giọng zero-shot) cung cấp. Nó cho
phép các công cụ bên ngoài (n8n, Make.com, Zapier, script tự viết, AI agent) tạo audio
giọng nói từ văn bản bằng các giọng bạn đã lưu trong **Voice Bank** của app.

> ⚠️ Đây là API **giọng nói/TTS**. Nó **khác** với webhook của G-Labs *Automation*
> (ảnh/video) — endpoint, trường body, và port mặc định đều khác.

---

## 1. Tổng quan & khái niệm chính

- **Máy chủ chạy nội bộ.** API chạy ở `http://127.0.0.1:<port>` (loopback), chỉ bind
  vào `127.0.0.1` — **không** truy cập được từ máy khác trừ khi bạn tự dựng
  tunnel/reverse proxy. Tích hợp của bạn phải chạy **trên cùng máy**, hoặc bạn tự
  expose ra ngoài.
- **Port mặc định:** `8766` (đổi được trong tab Webhook).
- **Bạn phải bật máy chủ.** Mở app → tab **Webhook** → **Start**. Tab này hiển thị/sao
  chép **API key** và cho phép đổi port.
- **Phải lưu giọng trước.** Việc tạo luôn dùng một **`preset_id`** trỏ tới giọng đã
  lưu trong **Voice Bank** của app. Liệt kê bằng `GET /api/voices`; tạo giọng trong
  giao diện Voice Studio.
- **Bất đồng bộ theo thiết kế.** Việc tạo tốn thời gian, nên API theo mô hình
  **gửi → hỏi trạng thái → tải về**:
  1. `POST /api/voice/design` → nhận `task_id` ngay lập tức (HTTP `202`).
  2. `GET /api/status/{task_id}` lặp lại tới khi `status` là `completed` hoặc `failed`.
  3. Khi `completed`, tải audio từ URL trong `results`.
- **Tạo tuần tự.** Các request được xếp hàng và chạy trên **một** model TTS dùng chung
  (GPU/CPU). Dù gửi nhiều job cùng lúc, suy luận vẫn diễn ra **lần lượt từng cái** (một
  mutex dùng chung cho model). Hãy hình dung thông lượng là một lần tạo tại một thời điểm.
- **Request đầu tiên có thể chậm.** Job đầu sau khi mở app sẽ nạp (và có thể tải) model
  TTS. Nếu không nạp được model (không có model / hủy tải), các task đang chờ sẽ `fail`
  kèm thông điệp rõ ràng.

---

## 2. Xác thực

Xác thực áp dụng cho mọi endpoint **trừ** `GET /api/health` và `GET /api/files/{name}`.
Gửi key qua **một trong hai** header:

```
X-API-Key: <api-key-của-bạn>
```
hoặc
```
Authorization: Bearer <api-key-của-bạn>
```

- Key được **tự sinh khi mở app lần đầu** và hiển thị trong tab **Webhook**.
- **Nếu người vận hành chưa đặt key nào, máy chủ ở chế độ mở** (không xác thực) — nhưng
  mặc định là đã có key. Hãy coi key là bắt buộc.
- Key sai/thiếu (khi đã cấu hình) → `401 {"error": "Invalid or missing API key"}`.

CORS đã bật (`Access-Control-Allow-Origin: *`) và có xử lý preflight `OPTIONS`.

---

## 3. Danh sách Endpoint

| Method | Path | Auth | Mục đích |
|--------|------|:----:|----------|
| `GET`  | `/api/health` | ❌ | Tình trạng máy chủ / uptime / số task trong hàng đợi |
| `GET`  | `/api/voices` | ✅ | Liệt kê voice preset đã lưu trong Voice Bank |
| `POST` | `/api/voice/design` | ✅ | Đưa task chuyển văn-bản-thành-giọng vào hàng đợi |
| `GET`  | `/api/status/{task_id}` | ✅ | Hỏi trạng thái task; trả kết quả hoặc lỗi |
| `GET`  | `/api/result/{task_id}` | ✅ | Lấy kết quả (chỉ khi đã `completed`) |
| `GET`  | `/api/files/{name}` | ❌ | Tải file audio đã tạo |
| `GET`  | `/api/tasks` | ✅ | Liệt kê 50 task gần nhất |

Dấu `/` ở cuối được chấp nhận (vd `/api/health/`).

---

## 4. Quy trình bất đồng bộ (từng bước)

### Bước 1 — Tìm giọng

`GET /api/voices` trả về các preset bạn có thể dùng làm `preset_id`:

```json
{
  "voices": [
    { "id": "spk_a1b2c3", "name": "Calm Narrator", "tags": ["male", "warm"], "is_factory": false, "is_favorite": true }
  ],
  "count": 1
}
```

> Nếu `count` là `0`, chưa có giọng nào — hãy tạo một giọng trong app (Voice Bank)
> trước khi gọi `/api/voice/design`.

### Bước 2 — Gửi yêu cầu

`POST /api/voice/design` kèm JSON body (xem §5). Phản hồi là **HTTP 202**:

```json
{
  "task_id": "a1b2c3d4e5f6",
  "status": "pending",
  "message": "Voice design task queued",
  "poll_url": "/api/status/a1b2c3d4e5f6"
}
```

> `task_id` là chuỗi hex 12 ký tự. Máy chủ kiểm tra JSON ngay lập tức, nên body sai
> định dạng sẽ trả `400` ngay thay vì thành task `failed` sau đó.

### Bước 3 — Hỏi trạng thái

`GET /api/status/{task_id}`. Các giá trị `status`: `pending` → `running` →
`completed` | `failed`.

**Đang chạy:**
```json
{ "task_id": "a1b2c3d4e5f6", "type": "voice_design", "status": "running", "created_at": 1707782400.0 }
```

**Hoàn thành:**
```json
{
  "task_id": "a1b2c3d4e5f6",
  "type": "voice_design",
  "status": "completed",
  "created_at": 1707782400.0,
  "results": ["http://127.0.0.1:8766/api/files/voice_20260610_120000_a1b2c3d4e5f6.wav"],
  "completed_at": 1707782460.0
}
```

**Thất bại:**
```json
{
  "task_id": "a1b2c3d4e5f6",
  "type": "voice_design",
  "status": "failed",
  "created_at": 1707782400.0,
  "error": "Preset 'spk_xxx' not found. Call GET /api/voices to list available preset_ids."
}
```

> Khoảng thời gian hỏi đề xuất: mỗi 2–4 giây. Thời gian tạo tỉ lệ với độ dài `script`
> và `num_step`. Vì model dùng chung và xử lý tuần tự, job đang chờ còn phải đợi các
> job trước hoàn tất.

### Bước 4 — Tải audio

`results` là mảng có **một** URL: `http://127.0.0.1:<port>/api/files/<tên-đã-url-encode>`.
`GET` URL đó (không cần API key) để tải dữ liệu audio thô. `Content-Type` đặt theo phần
mở rộng (`audio/wav` hoặc `audio/mpeg`). File lưu nội bộ trên máy chạy app
(`output/webhook/`).

---

## 5. Body của request — `POST /api/voice/design`

JSON body. **`script` và `preset_id` đều bắt buộc.**

| Trường | Kiểu | Bắt buộc | Mặc định | Ghi chú |
|--------|------|:--------:|----------|---------|
| `script` | string | ✅ | — | Văn bản cần đọc. Văn bản dài được tự tách câu; đầu ra là một file audio liền mạch (các câu nối nhau, chèn khoảng lặng ~0.3 giây). |
| `preset_id` | string | ✅ | — | Một id giọng từ `GET /api/voices` (đã lưu trong Voice Bank). id không tồn tại → task thất bại. |
| `language` | string | ❌ | `Auto` | `Auto` = tự nhận diện, hoặc tên ngôn ngữ (vd `"english"`, `"vietnamese"`). Model hỗ trợ 600+ ngôn ngữ. |
| `speed` | number | ❌ | `1.0` | Hệ số tốc độ đọc. `>1.0` nhanh hơn, `<1.0` chậm hơn. |
| `output_format` | string | ❌ | `wav` | `"wav"` (PCM 16-bit) hoặc `"mp3"` (192 kbps). Giá trị khác → `wav`. |
| `num_step` | int | ❌ | `50` | Số bước diffusion. Cao hơn = có thể chất lượng tốt hơn nhưng chậm; thấp hơn = nhanh. |
| `guidance_scale` | number | ❌ | `2.0` | Hệ số guidance (bám sát vs. tự nhiên). |

```json
{
  "preset_id": "spk_a1b2c3",
  "script": "Hello world. This is a sample sentence. And another one.",
  "language": "english",
  "speed": 1.0,
  "output_format": "wav"
}
```

Ghi chú:
- `script` bắt buộc và được trim — `script` rỗng/chỉ-khoảng-trắng làm task thất bại với
  `` `script` is required ``.
- `preset_id` bắt buộc — thiếu/rỗng sẽ thất bại kèm thông điệp chỉ tới `GET /api/voices`.
- `num_step` và `guidance_scale` là điều khiển chất lượng nâng cao; cứ để mặc định trừ
  khi bạn thực sự cần tinh chỉnh.
- Đầu ra **luôn là một file audio** mỗi request.

---

## 6. Giọng (`GET /api/voices`)

Trả về mọi preset trong Voice Bank:

| Trường | Kiểu | Ý nghĩa |
|--------|------|---------|
| `id` | string | Dùng làm `preset_id`. |
| `name` | string | Tên dễ đọc. |
| `tags` | string[] | Nhãn tự do (vd giới tính, phong cách). |
| `is_factory` | bool | True nếu là preset dựng sẵn. |
| `is_favorite` | bool | True nếu người dùng đánh dấu sao. |

Cấp ngoài cùng: `{ "voices": [...], "count": <int> }`.

> Preset được tạo trong app desktop Voice Studio (thu/nhân bản một giọng rồi lưu vào
> Voice Bank). Webhook chỉ **dùng** được preset, không tạo được.

---

## 7. Tham chiếu Response & trạng thái

### POST `/api/voice/design` → `202`
```json
{ "task_id": "a1b2c3d4e5f6", "status": "pending", "message": "Voice design task queued", "poll_url": "/api/status/a1b2c3d4e5f6" }
```

### GET `/api/status/{task_id}` → `200`
- `pending` / `running`: `{ task_id, type, status, created_at }`
- `completed`: thêm `results` (mảng có một URL file) và `completed_at` (unix giây).
- `failed`: thêm `error` (string).
- task_id không tồn tại → `404 {"error": "Task <id> not found"}`.

### GET `/api/result/{task_id}` → `200`
- Nếu chưa xong: `{ task_id, status, message: "Task not yet completed" }`.
- Nếu đã xong: `{ task_id, status: "completed", results: [...], completed_at }`.

### GET `/api/health` → `200`
```json
{ "status": "ok", "service": "G-Labs Voice Studio Webhook", "uptime": 123, "tasks_pending": 0, "tasks_running": 1 }
```

### GET `/api/tasks` → `200`
```json
{ "tasks": [ { "task_id": "...", "type": "voice_design", "status": "completed", "created_at": 1707782400.0 } ] }
```
(Mới nhất trước, tối đa 50.)

### Các response lỗi
| HTTP | Body | Khi nào |
|------|------|---------|
| `400` | `{"error": "Empty body"}` | POST không có body |
| `400` | `{"error": "Invalid JSON body: ..."}` | POST với JSON sai định dạng |
| `401` | `{"error": "Invalid or missing API key"}` | Thiếu/sai key (khi đã đặt key) |
| `404` | `{"error": "Not found"}` | Route không tồn tại |
| `404` | `{"error": "Task <id> not found"}` | task không tồn tại ở status/result |
| `404` | `{"error": "File not found: <name>"}` | File không tồn tại/đã hết hạn |
| `500` | `{"error": "Failed to list voices: ..."}` | Lỗi đọc Voice Bank ở `/api/voices` |

---

## 8. Xử lý lỗi

Khi task thất bại, response trạng thái mang **một** chuỗi **`error`** (API này **không**
tách thành mã số như webhook Automation). Hãy rẽ nhánh theo nội dung chuỗi. Các lỗi phổ biến:

| `error` (chữ) | Nguyên nhân | Cách khắc phục |
|---------------|-------------|----------------|
| `` `script` is required `` | `script` rỗng/thiếu | Cung cấp `script` không rỗng. |
| `` `preset_id` is required. ... `` | Thiếu `preset_id` | Gọi `GET /api/voices`, truyền `id` hợp lệ. |
| `Preset '<id>' not found. ...` | `preset_id` không có trong Voice Bank | Dùng id hợp lệ từ `GET /api/voices`. |
| `Failed to load preset '<id>': ...` | Dữ liệu preset không đọc được | Lưu lại giọng trong app. |
| `Voice model not loaded ...` / `Model load did not complete ...` | Model TTS không sẵn / hủy tải | Mở Voice Studio, chạy tạo thử một lần, rồi thử lại. |
| `MP3 encode failed: ...` | Lỗi ffmpeg khi xuất MP3 | Dùng `"output_format": "wav"`, hoặc kiểm tra ffmpeg của app. |
| `Internal: could not read request body` | Mất file body tạm trước khi xử lý | Gửi lại request. |

Lỗi validate ở tầng HTTP (`400`) được trả **ngay** lúc gửi (body rỗng, JSON sai), nên
bạn không cần poll để phát hiện.

---

## 9. Ràng buộc & lưu ý

- **Chỉ localhost.** Chạy tích hợp trên cùng máy, hoặc tự tunnel `127.0.0.1:<port>`.
- **Tạo tuần tự.** Một lần tạo tại một thời điểm (model TTS dùng chung). Gửi nhiều job
  thì cứ gửi — chúng xếp hàng — nhưng đừng kỳ vọng nhanh hơn nhờ song song.
- **Cần Voice Bank.** Phải có ít nhất một giọng đã lưu; `preset_id` là bắt buộc. Webhook
  này **không** có trường "thiết kế giọng từ thuộc tính văn bản" — nó luôn nhân bản một
  preset đã lưu.
- **Nạp model ở lần gọi đầu.** Request đầu sau khi mở app có thể lâu hơn (nạp/tải model)
  và có thể thất bại nếu không có model.
- **Task lưu trong bộ nhớ.** Trạng thái task và ánh xạ `task_id` → kết quả nằm trong app
  đang chạy; sẽ mất nếu app khởi động lại. Hãy gửi, hỏi trạng thái và tải về trong cùng
  một phiên chạy app.
- **File lưu nội bộ** (`output/webhook/`) và có thể bị dọn theo thời gian; tải ngay sau
  khi `completed`.
- **Tính tái lập:** cùng một `script` không đảm bảo cho ra audio giống hệt từng byte.

---

## 10. Ví dụ đầu-cuối

### 10.1 cURL

```bash
# 1) Liệt kê voice preset → chọn một "id"
curl http://127.0.0.1:8766/api/voices \
  -H "X-API-Key: YOUR_API_KEY"

# 2) Gửi job tạo giọng
curl -X POST http://127.0.0.1:8766/api/voice/design \
  -H "Content-Type: application/json" \
  -H "X-API-Key: YOUR_API_KEY" \
  -d '{"preset_id": "spk_a1b2c3", "script": "Hello world.", "language": "english"}'
# → {"task_id":"a1b2c3d4e5f6","status":"pending","poll_url":"/api/status/a1b2c3d4e5f6"}

# 3) Hỏi trạng thái tới khi xong
curl http://127.0.0.1:8766/api/status/a1b2c3d4e5f6 -H "X-API-Key: YOUR_API_KEY"

# 4) Tải audio (không cần key)
curl -o out.wav "http://127.0.0.1:8766/api/files/voice_20260610_120000_a1b2c3d4e5f6.wav"

# Kiểu Bearer-token cũng được:
curl http://127.0.0.1:8766/api/voices -H "Authorization: Bearer YOUR_API_KEY"
```

### 10.2 Python (tìm giọng → gửi → hỏi → tải)

```python
import time, requests

BASE = "http://127.0.0.1:8766"
KEY  = "YOUR_API_KEY"
H    = {"X-API-Key": KEY, "Content-Type": "application/json"}

# 1) Chọn giọng
voices = requests.get(f"{BASE}/api/voices", headers=H, timeout=30).json()["voices"]
if not voices:
    raise SystemExit("Chưa có giọng nào — hãy tạo giọng trong Voice Bank của Voice Studio trước.")
preset_id = next((v["id"] for v in voices if v.get("is_favorite")), voices[0]["id"])

# 2) Gửi
def synth(script, preset_id, fmt="wav", language="Auto", poll=3, timeout=600):
    body = {"preset_id": preset_id, "script": script, "language": language, "output_format": fmt}
    r = requests.post(f"{BASE}/api/voice/design", json=body, headers=H, timeout=30)
    r.raise_for_status()
    task_id = r.json()["task_id"]

    deadline = time.time() + timeout
    while time.time() < deadline:
        s = requests.get(f"{BASE}/api/status/{task_id}", headers=H, timeout=30).json()
        if s["status"] == "completed":
            return s["results"][0]                 # một URL audio
        if s["status"] == "failed":
            raise RuntimeError(s.get("error"))
        time.sleep(poll)
    raise TimeoutError(f"task {task_id} chưa xong trong {timeout}s")

url = synth("Hello world. This is a test.", preset_id, fmt="mp3", language="english")

# 3) Tải về
audio = requests.get(url, timeout=120).content      # /api/files không cần key
open("out" + url[url.rfind("."):], "wb").write(audio)
```

### 10.3 JavaScript (Node, fetch)

```js
const BASE = "http://127.0.0.1:8766";
const KEY  = "YOUR_API_KEY";
const H = { "X-API-Key": KEY, "Content-Type": "application/json" };

async function synth(script, presetId, { fmt = "wav", language = "Auto", poll = 3000, timeout = 600000 } = {}) {
  const r = await fetch(`${BASE}/api/voice/design`, {
    method: "POST", headers: H,
    body: JSON.stringify({ preset_id: presetId, script, language, output_format: fmt }),
  });
  if (!r.ok) throw new Error(`submit ${r.status}: ${await r.text()}`);
  const { task_id } = await r.json();

  const end = Date.now() + timeout;
  while (Date.now() < end) {
    const s = await (await fetch(`${BASE}/api/status/${task_id}`, { headers: H })).json();
    if (s.status === "completed") return s.results[0];   // URL audio
    if (s.status === "failed") throw new Error(s.error);
    await new Promise(r => setTimeout(r, poll));
  }
  throw new Error(`task ${task_id} hết thời gian chờ`);
}

// Tìm giọng, rồi tổng hợp
const { voices } = await (await fetch(`${BASE}/api/voices`, { headers: H })).json();
const url = await synth("Hello world.", voices[0].id, { fmt: "wav", language: "english" });
console.log(url);
```

---

## 11. Checklist nhanh cho người tích hợp / AI agent

1. Đảm bảo có ít nhất một giọng đã lưu trong **Voice Bank** của app.
2. Bật máy chủ Webhook trong app; sao chép **port** (mặc định `8766`) và **API key**.
3. `GET /api/voices` → chọn một `preset_id`.
4. `POST /api/voice/design` với `{ preset_id, script, ... }` (cả `script` và `preset_id` bắt buộc).
5. Đọc `task_id` từ response `202`.
6. Hỏi `GET /api/status/{task_id}` mỗi 2–4 giây tới khi `completed` hoặc `failed`.
7. Khi `completed`: `GET` `results[0]` để tải file audio.
8. Khi `failed`: đọc chuỗi `error` (vd preset không tồn tại, model chưa nạp).
9. Nhớ: việc tạo là **tuần tự** (lần lượt từng cái), và task chỉ tồn tại trong phiên
   chạy hiện tại của app.
```
