<h1 align="center">G-Labs Voice Studio</h1>

<p align="center"><b>Ứng dụng desktop giọng nói AI chạy ngay trên máy bạn — sao chép giọng từ mẫu vài giây, đọc văn bản hơn 600 ngôn ngữ, hội thoại nhiều giọng, tách phụ đề từ audio/video và dịch phụ đề bằng AI.</b></p>

<p align="center">
  <b>Tiếng Việt</b> ·
  <a href="README.en.md">English</a> ·
  <a href="README.pt-BR.md">Português</a> ·
  <a href="README.tr.md">Türkçe</a> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.hi.md">हिन्दी</a> ·
  <a href="README.bn.md">বাংলা</a> ·
  <a href="README.ur.md">اردو</a> ·
  <a href="README.ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G"><img alt="Tải về cho Windows" src="https://img.shields.io/badge/T%E1%BA%A3i%20v%E1%BB%81-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta"><img alt="Tải về cho macOS (Apple Silicon)" src="https://img.shields.io/badge/T%E1%BA%A3i%20v%E1%BB%81-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

---

## Cài đặt

### Bước 1 — Chọn đúng bản cho máy của bạn

Bản cài được phát hành qua thư mục Google Drive chính thức:

| Máy của bạn | Google Drive | Ghi chú |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | [Windows](https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G) | Tệp `.zip`, giải nén là chạy, không cần cài đặt |
| 🍎 **Mac chip Apple (M1/M2/M3/M4…)** | [macOS Apple Silicon](https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta) | Tệp `.dmg`, cần macOS 12 trở lên |

> **Mac chip Intel không được hỗ trợ** — chỉ có bản cho Apple Silicon. Không chắc Mac của bạn chip gì? Bấm biểu tượng  → **About This Mac**: dòng **Chip** ghi "Apple M…" là dùng được; dòng **Processor** ghi "Intel…" là không.

### Bước 2 — Cài đặt

<details open>
<summary><b>🪟 Trên Windows</b></summary>

1. Tải tệp `.zip` bản Windows (ví dụ `G-Labs-Voice-Studio-v2.0.2-win.zip`) và **giải nén** ra một thư mục bất kỳ — ổ đĩa cần còn trống ít nhất 10 GB (mô hình AI tải sau sẽ chiếm vài GB).
2. Mở thư mục vừa giải nén và chạy **`G-Labs-Voice-Studio.exe`** (các tệp còn lại nằm trong thư mục con `data`, đừng di chuyển chúng).
3. Nếu hiện bảng **"Windows protected your PC"** (SmartScreen): bấm **More info** → **Run anyway**. *(App chưa ký chứng chỉ của Microsoft nên bị cảnh báo — không phải virus.)*
4. **Tạo lối tắt:** chuột phải vào `G-Labs-Voice-Studio.exe` → **Send to** → **Desktop (create shortcut)** để lần sau mở nhanh.

> ⏳ **Lần đầu mở có thể mất 30–60 giây** (màn hình chờ dừng lâu) vì Windows quét bảo mật ứng dụng và thư viện card đồ hoạ. Cứ chờ, đừng tắt — các lần sau mở nhanh hơn.

</details>

<details open>
<summary><b>🍎 Trên macOS</b></summary>

1. Mở tệp **`.dmg`** vừa tải, rồi **kéo biểu tượng G-Labs Voice Studio thả vào thư mục Applications**.
2. Vào **Applications**, **bấm chuột phải** (hoặc giữ Control rồi bấm) lên **G-Labs Voice Studio** → chọn **Open** → bấm **Open** lần nữa ở hộp xác nhận. *(App chưa được Apple chứng thực nên phải mở kiểu này ở **lần đầu**; những lần sau mở bình thường.)*
3. Nếu macOS báo **"bị hỏng / không thể mở"** hoặc không thấy nút Open, mở **Terminal**, dán lệnh sau rồi Enter:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"
   ```
   Sau đó mở lại app. Cách khác: **System Settings → Privacy & Security**, kéo xuống cuối và bấm **Open Anyway** cạnh dòng báo G-Labs Voice Studio bị chặn.

> ⏳ **Lần đầu mở có thể mất 30–60 giây** vì macOS kiểm tra bảo mật toàn bộ ứng dụng. Các lần sau mở nhanh hơn.

</details>

### Bước 3 — Đăng nhập & chọn gói

**Bạn cần đăng nhập bằng Google** (Cài đặt ⚙️ → tab **Tài khoản Bản Quyền** → **Đăng nhập bằng Google**) để app kiểm tra bản quyền. Một tài khoản chạy trên **một máy tại một thời điểm** — đăng nhập ở máy khác thì phiên trên máy cũ kết thúc.

| Gói | Giá | Gồm |
|---|---|---|
| **Dùng thử** | Miễn phí | Giới hạn số dòng mỗi lượt tạo (mặc định 1 dòng) — đủ để kiểm tra máy bạn chạy ổn trước khi mua |
| **Gói Studio** | 1 tháng 100.000đ ($5) · 6 tháng 500.000đ ($25) · 1 năm 1.000.000đ ($50) | Tạo không giới hạn dòng, **Hàng chờ tạo**, tab **Dịch phụ đề**, **Webhook API** |

- Mua ngay trong app (Cài đặt → **Tài khoản Bản Quyền**) bằng **chuyển khoản VietQR**, **PayPal** (thẻ quốc tế) hoặc **USDT**. Gói theo thời hạn, không tự gia hạn, kích hoạt trên tài khoản Google bạn đăng nhập.
- Gói Studio là gói **riêng** của Voice Studio, tách khỏi Plus/Max của G-Labs Studio.
- Hoàn tiền trong **24 giờ** đầu sau khi thanh toán — xem [Chính sách hoàn tiền](https://duckspace.net/refunds.html#vi). Hãy chạy thử bản miễn phí trước để chắc máy bạn chạy mượt.

---

## Lần chạy đầu tiên

1. **Mở app và chọn ngôn ngữ giao diện** ở màn hình chào (đổi lại sau trong Cài đặt).
2. **Đăng nhập bằng Google** — Cài đặt ⚙️ → **Tài khoản Bản Quyền** → **Đăng nhập bằng Google**.
3. **Tải mô hình giọng đọc** — mở tab **Quản lý Model** (hoặc làm theo lời nhắc của app) và tải mô hình giọng đọc AI (vài GB, chỉ tải một lần). Mô hình nhận dạng giọng nói tải riêng khi bạn dùng lần đầu.
4. **Mở tab Đọc văn bản**, chọn **ngôn ngữ đầu ra**, chọn một giọng trong kho (có sẵn 30 giọng mẫu).
5. Dán văn bản → **Nhập vào bảng** → **Bắt đầu chạy**. Nghe thử từng dòng, rồi bấm **Xuất âm thanh** để lưu file (mặc định kèm phụ đề `.srt`).

---

## Tính năng

<p align="center">
  <img alt="Giao diện G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
</p>

- **Chạy trên máy bạn** — sau khi tải mô hình, tạo giọng và nhận dạng đều chạy cục bộ (GPU NVIDIA, Apple Metal hoặc CPU); âm thanh và văn bản không gửi lên máy chủ. Riêng tab Dịch phụ đề gửi nội dung phụ đề tới nhà cung cấp AI bạn chọn.
- **Sao chép giọng** — từ một mẫu âm thanh 5–10 giây, đọc bất kỳ văn bản nào bằng đúng giọng đó.
- **Thiết kế giọng** — tạo giọng mới theo giới tính, độ tuổi, cao độ, phong cách, khẩu âm; không cần tệp mẫu.
- **Hơn 600 ngôn ngữ đầu ra** — Việt, Anh, Trung, Nhật, Hàn, Pháp, Đức, Tây Ban Nha và nhiều ngôn ngữ khác.
- **Hội thoại nhiều giọng** — kịch bản `<Tên>: lời thoại`, mỗi nhân vật một giọng và tốc độ riêng.
- **Tách phụ đề** — nhận dạng lời nói từ MP3, WAV, M4A, FLAC, MP4, MOV…; xuất TXT hoặc SRT với mốc thời gian theo từng từ.
- **Dịch phụ đề bằng AI** *(gói Studio)* — dịch hoặc biên tập `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt`; mốc thời gian và số dòng giữ nguyên tuyệt đối.
- **Kho giọng** — 30 giọng mẫu sẵn, lưu giọng tự tạo, ghim ⭐ yêu thích, sao lưu/phục hồi ra tệp `.vcp`.
- **Tinh chỉnh âm thanh** — 6 chế độ xử lý, cân đều âm lượng, 13 thẻ biểu cảm, từ điển phát âm nhớ cách đọc `100%`, `25°C`, `m²`.
- **Xuất linh hoạt** — WAV hoặc MP3, gộp 1 file hoặc mỗi câu 1 file, kèm `.srt`; tải riêng từng dòng bằng nút ⬇.
- **Hàng chờ tạo** *(gói Studio)* — xếp nhiều kịch bản, app tự chạy lần lượt và tự lưu file.
- **Webhook API** *(gói Studio)* — máy chủ REST cục bộ cho n8n, Make, Zapier, Python/cURL hay AI agent.
- **Tự xử lý phần cứng** — card đồ hoạ không tương thích thì tự chuyển sang CPU và báo rõ; tự giải phóng bộ nhớ GPU khi nhàn rỗi.
- **Giao diện 9 ngôn ngữ** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## Các trang

Các trang nằm ở thanh bên trái. Ba trang tạo giọng (Sao chép giọng, Đọc văn bản, Hội thoại nhóm) có chung một nhịp: chọn **ngôn ngữ đầu ra** → dán văn bản hoặc **Nhập tệp** (`.txt`, `.srt`) → **Nhập vào bảng** (app tách câu theo **Kiểu tách câu** bạn chọn, có xem trước số dòng) → **Bắt đầu chạy** → nghe thử → **Xuất âm thanh**.

### 🔊 Sao chép giọng

Bấm **Chọn...** để nạp tệp âm thanh mẫu (giọng rõ, ít tạp âm), rồi **kéo khung sáng trên sóng âm** để chọn đúng đoạn 3–30 giây làm mẫu — thả tay là mép khung tự khớp vào khoảng lặng gần nhất; tệp dài quá 5 phút/50 MB thì app lấy 30 giây đầu. **Bắt buộc** nhập *Văn bản mẫu* khớp chính xác lời trong đoạn mẫu (đủ dấu câu, đúng chính tả); nút **✨ AI gợi ý** nhận dạng giúp bạn, nhưng vẫn cần dò lại. Tạo xong, app mời nghe thử và lưu giọng vào kho bằng một chạm.

### 🎛️ Đọc văn bản

Chọn một giọng đã có trong kho, hoặc mở **Thiết kế giọng** để tạo giọng mới theo *Giới tính, Độ tuổi, Cao độ, Phong cách, Khẩu âm*. Giọng thiết kế ưng ý thì chọn dòng trong bảng → **Lưu** vào kho để dùng lại. Kiểu tách câu **Gộp thông minh** gộp các câu ngắn thành dòng liền mạch tới trần ký tự nhưng luôn ngắt đúng điểm kết câu. Nút **Mẫu thẻ biểu cảm** cho tra và **Chèn** thẻ vào đúng vị trí con trỏ.

### 💬 Hội thoại nhóm

Viết kịch bản nhiều nhân vật — hợp với podcast, audio drama, phỏng vấn:

```
<MC>: Xin chào quý vị và các bạn.
<Mai>: Em chào anh chị, em rất vui khi được tham gia chương trình.
<Minh>: Hôm nay chúng ta sẽ nói về gì ạ?
```

Tên nhân vật đặt trong `< >` ở đầu dòng (dấu `:` có thể bỏ, tên không phân biệt hoa thường). Bấm **Mẫu hội thoại chuẩn** để xem ví dụ, rồi **Phân tích hội thoại** — khung **Phân vai giọng đọc** mở ra để gán mỗi nhân vật một giọng trong kho và một thanh **Tốc độ** riêng (0.5× → 2×).

### 📝 Tách phụ đề

Chọn tệp âm thanh/video (MP3, WAV, M4A, FLAC, MP4, MOV…), chọn ngôn ngữ đang nói và model nhận dạng (Tiny → Large v3, mỗi bản ghi rõ VRAM cần dùng), rồi bấm chạy. Dòng phụ đề được dựng theo mốc thời gian từng từ, ngắt ở chỗ nghỉ hơi thật / hết câu / trần ký tự; ba ô *ký tự tối đa, giây tối đa, ngưỡng nghỉ* đổi số là bảng cập nhật ngay, không cần nhận dạng lại. Sửa trực tiếp trong bảng, xuất `.txt` hoặc `.srt`.

### 🌐 Dịch phụ đề *(gói Studio)*

Dịch phụ đề sang ngôn ngữ khác hoặc biên tập lại chính tả, ngắt câu — **chỉ phần chữ thay đổi, mốc thời gian và số dòng giữ nguyên**.

1. Chuẩn bị một lần ở **Quản lý Model → LLM**: chọn **9Router** (gateway chạy trên máy, điền địa chỉ + API key), **Claude CLI**, **Antigravity** (`agy`) hoặc **Codex CLI** (cài và đăng nhập). Mỗi hàng có nút **Hướng dẫn** ghi lệnh cài; cài xong bấm **Làm mới danh sách** để app dò và liệt kê model.
2. **Nhập tệp** `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt` — hoặc **Lấy từ Tách phụ đề**. Tệp `.txt` không có mốc thời gian thì app tính giờ tạm và báo rõ.
3. Nên bấm **Tối ưu dữ liệu**: nối các mảnh bị ngắt giữa câu (hay gặp ở phụ đề xuất từ app dựng phim), có bảng xem trước kiểu *"120 dòng → 68 dòng"* trước khi **Áp dụng**.
4. Chọn chế độ **Dịch**, **Biên tập** hoặc **Dịch + Biên tập**, chọn ngôn ngữ đích và model, bấm **Bắt đầu chạy**.
5. **Bảng nhất quán** chốt tên riêng, thuật ngữ và cách xưng hô cho cả file rồi gửi kèm mọi đoạn; sửa tay được, và có tuỳ chọn dừng cho bạn duyệt trước khi dịch.
6. Kiểm lại cột **Kết quả** (dòng AI trả thiếu có dấu ⚠ và giữ chữ gốc), chọn **SRT / VTT / TXT** rồi **Xuất kết quả**.

### 📚 Quản lý Model

Mỗi model một hàng kèm dung lượng và trạng thái: mô hình giọng đọc AI và các bản nhận dạng (Tiny, Base, Small, Turbo, Large v3). Tải riêng bản nào cần, đổi được **thư mục lưu model** (ví dụ sang ổ D cho nhẹ ổ C — chép thư mục model cũ sang, hoặc để app tải lại). Ở đây cũng cài đặt nhà cung cấp **LLM** cho tab Dịch phụ đề và thời gian **Tự động giải phóng VRAM**.

### 🗒 Hàng chờ tạo *(gói Studio)*

Thay vì tạo từng kịch bản rồi xuất tay, bấm **Thêm hàng chờ** để lưu kịch bản + giọng + cài đặt hiện tại thành một việc có **tên và thư mục lưu riêng**. **Chạy hàng chờ** — app tự làm lần lượt và tự lưu file. Mỗi việc hiện tiến độ `X/N câu` để biết việc nào thiếu câu do lỗi; **Mở lại** nạp việc về tab để sửa (câu lỗi được đánh dấu ❌). Đóng app mở lại vẫn còn nguyên hàng chờ.

### 🔗 Webhook API *(gói Studio)*

Máy chủ REST cục bộ để n8n, Make, Zapier, Python/cURL hoặc AI agent gọi tạo giọng tự động. Mặc định `127.0.0.1:8766` (chỉ máy này gọi được), có khoá API, ô **URL** đầy đủ kèm nút **Sao chép**, tuỳ chọn tự khởi động cùng app và log request trực tiếp. Đổi IP sang `0.0.0.0` / IP LAN để máy khác gọi vào — khi đó khoá API đi qua HTTP không mã hoá. Lược đồ đầy đủ: [`docs/WEBHOOK_INTEGRATION.vi.md`](docs/WEBHOOK_INTEGRATION.vi.md).

---

## Mẹo dùng

<details>
<summary><b>Tinh chỉnh âm thanh — 6 chế độ xử lý</b></summary>

Trong mục **Tinh chỉnh âm thanh** của ba tab tạo giọng (đổi ở một tab, hai tab kia tự đồng bộ):

- 📻 **Phát thanh** *(mặc định)* — chuẩn radio/podcast, ấm, nén gọn.
- 🎬 **Điện ảnh** — vang rộng, nén nhẹ.
- 🎙️ **Podcast** — mic gần, nén mạnh, không vang.
- ☀️ **Ấm** — trầm dày, cảm giác ấm áp.
- ✨ **Sáng** — cao sắc nét, thoáng đãng.
- 🔇 **Nguyên bản** — giữ nguyên đầu ra của mô hình.

**Cân đều âm lượng các câu** cân theo độ to tai người nghe (RMS) nên hết câu to câu nhỏ. Muốn âm thanh thô của mô hình: chọn **Nguyên bản** và bỏ tích ô này.

</details>

<details>
<summary><b>Thẻ biểu cảm</b></summary>

Gõ thẻ vào văn bản (giữ nguyên ngoặc vuông, đặt riêng hoặc xen giữa câu, ví dụ `Buồn cười quá [laughter] mình không nhịn được.`) — giọng phát ra âm thanh tương ứng thay vì đọc thành chữ. Không cần nhớ: nút **Mẫu thẻ biểu cảm** cho tra và chèn thẳng.

| Thẻ | Âm thanh |
|---|---|
| `[laughter]` | Tiếng cười |
| `[sigh]` | Tiếng thở dài |
| `[confirmation-en]` | Đồng tình — "mm-hmm" |
| `[question-en]` · `[question-ah]` · `[question-oh]` · `[question-ei]` · `[question-yi]` | Ngữ điệu hỏi |
| `[surprise-ah]` · `[surprise-oh]` · `[surprise-wa]` · `[surprise-yo]` | Ngạc nhiên |
| `[dissatisfaction-hnn]` | Khó chịu — "hnn" |

Mức độ thể hiện thay đổi theo ngôn ngữ và giọng — nên thử trên một câu ngắn trước.

</details>

<details>
<summary><b>Từ điển phát âm</b></summary>

Văn bản có `%`, `$`, `°C`, `m²`, tên thương hiệu…? Bấm **Chỉnh phát âm** trước khi tạo: app hỏi cách đọc từng ký tự/từ, bạn gõ phiên âm một lần (ví dụ `%` → `phần trăm`) và app nhớ theo từng ngôn ngữ đầu ra.

</details>

<details>
<summary><b>Tốc độ & phụ đề khi xuất</b></summary>

- **Tốc độ đọc** nằm trong *Cài đặt nâng cao*; thanh **Tốc độ** trên trình phát cho nghe thử nhanh/chậm và file xuất giữ đúng tốc độ đó, không méo cao độ.
- **Xuất kèm phụ đề (.srt)** tạo file `.srt` cùng tên cạnh file âm thanh, mốc thời gian lấy từ độ dài thực của từng câu sau khi chỉnh tốc độ.
- **Khớp thời lượng phụ đề**: khi kịch bản nhập từ `.srt`, mỗi câu được đọc nhanh lại (tối đa 1.8×) để vừa ô phụ đề — không bao giờ kéo chậm.

</details>

<details>
<summary><b>Tự động giải phóng bộ nhớ</b></summary>

Để app không dùng một lúc (mặc định 5 phút), mô hình AI tự được dỡ khỏi VRAM/RAM cho máy nhẹ; lần thao tác kế tiếp app nạp lại. Chỉnh thời gian hoặc tắt hẳn trong **Quản lý Model → Tự động giải phóng VRAM**.

</details>

---

## Yêu cầu hệ thống

|   | Tối thiểu | Khuyến nghị |
|---|---|---|
| **Hệ điều hành** | Windows 10 (64-bit), macOS 12 trên Apple Silicon | Windows 11, macOS 13 trở lên |
| **RAM** | 8 GB | 16 GB trở lên |
| **Ổ cứng** | 10 GB trống (mô hình + cache) | 20 GB trở lên, SSD |
| **GPU** | Không bắt buộc — CPU vẫn chạy được | NVIDIA RTX 20-series trở lên, 8 GB VRAM · Mac dùng Metal |
| **Mạng** | Cần Internet để đăng nhập/kiểm tra bản quyền và tải mô hình | |

- **Windows:** tăng tốc GPU cần card NVIDIA đời **RTX 20-series trở lên** (compute capability ≥ 7.0) và driver hỗ trợ CUDA 12.8. Card cũ hơn như GTX 10-series được tự phát hiện và chạy bằng CPU.
- **macOS:** chỉ hỗ trợ **Apple Silicon** (M1/M2/M3/M4…), tăng tốc bằng Metal.
- Chạy bằng CPU chậm hơn GPU khoảng 5–10 lần nhưng vẫn dùng được cho voice-over ngắn.

---

## Nơi lưu dữ liệu

| Gì | Windows | macOS |
|---|---|---|
| Âm thanh xuất ra (mặc định) | `output\` trong thư mục bạn giải nén app | `~/Documents/G-Labs Voice Studio/output` |
| Cài đặt, phiên đăng nhập | `%APPDATA%\G-Labs Voice Studio` | `~/Library/Application Support/G-Labs Voice Studio` |
| Kho giọng của bạn | `%APPDATA%\G-Labs Voice Studio\voice_studio\voices` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/voices` |
| Mô hình AI | `%APPDATA%\G-Labs Voice Studio\voice_studio\model` (hoặc thư mục bạn chọn) | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/model` (hoặc thư mục bạn chọn) |
| Hàng chờ tạo | `%APPDATA%\G-Labs Voice Studio\voice_studio\queue` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/queue` |

Muốn chuyển kho giọng sang máy khác, dùng **sao lưu/phục hồi `.vcp`** trong khung Kho giọng.

---

## Khắc phục sự cố

**Mở lần đầu rất lâu, màn hình chờ đứng yên** — Windows/macOS đang quét bảo mật lần đầu; chờ 30–60 giây, đừng tắt. Các lần sau nhanh hơn.

**Windows chặn ở "Windows protected your PC"** — bấm **More info → Run anyway**. App chưa ký chứng chỉ của Microsoft, không phải virus.

**macOS báo ứng dụng bị hỏng / không mở được** — app chưa được Apple chứng thực. Chuột phải → **Open** ở lần đầu, hoặc chạy `xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"`.

**Thông báo "Đã chuyển sang chạy bằng CPU"** — card đồ hoạ không tương thích (ví dụ GTX 10-series). Mọi tính năng vẫn chạy, chỉ chậm hơn; muốn nhanh cần NVIDIA RTX 20-series trở lên hoặc Mac Apple Silicon.

**Mỗi lần chỉ tạo được 1 dòng** — bạn đang ở bản dùng thử. Mua gói Studio để tạo không giới hạn dòng.

**Bị đăng xuất, báo tài khoản đăng nhập ở thiết bị khác** — một tài khoản chỉ chạy một máy tại một thời điểm; đăng nhập lại trên máy bạn muốn dùng.

**Giọng sao chép đọc sai lời / lạc giọng** — *Văn bản mẫu* phải khớp chính xác lời trong đoạn mẫu; chọn đoạn mẫu rõ, ít tạp âm.

**Ký tự đặc biệt bị đọc sai (`100%`, `25°C`…)** — thêm cách đọc trong **Chỉnh phát âm**.

**Ổ C bị đầy vì mô hình** — đổi thư mục lưu model trong **Quản lý Model**, rồi chép thư mục model cũ sang hoặc để app tải lại.

**Tab Dịch phụ đề không có model để chọn** — cài và đăng nhập một nhà cung cấp LLM (9Router, Claude CLI, Antigravity, Codex) theo nút **Hướng dẫn**, rồi bấm **Làm mới danh sách**.

**Cần xem lỗi chi tiết** — bấm nút **Log Chi Tiết** ở thanh bên.

---

📖 [Trang giới thiệu](https://duckspace.net/voice-studio/) · [Hướng dẫn](https://duckmartians.info/voice/guide/) · [Nhật ký thay đổi](CHANGELOG.md) · [Discord](https://discord.gg/munMZEBMw5)

© 2026 Duck Martians AI Labs. Tất cả các quyền được bảo lưu.
