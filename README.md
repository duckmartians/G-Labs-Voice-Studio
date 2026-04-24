<p align="right">🇻🇳 Tiếng Việt · <a href="./README.en.md">🇬🇧 English</a></p>

<h1 align="center">G-Labs Voice Studio</h1>
<p align="center">Ứng dụng giọng nói AI cho người sáng tạo nội dung</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G">
    <img alt="Tải bản Windows" src="https://img.shields.io/badge/T%E1%BA%A3i%20Windows-%F0%9F%92%BB-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  </a>
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta">
    <img alt="Tải bản macOS" src="https://img.shields.io/badge/T%E1%BA%A3i%20macOS-%F0%9F%8D%8E-000000?style=for-the-badge&logo=apple&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="Trang chủ" src="https://img.shields.io/badge/Trang%20ch%E1%BB%A7-Truy%20c%E1%BA%ADp-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio** là ứng dụng máy tính tổng hợp giọng nói đa ngôn ngữ, có khả năng sao chép giọng, thiết kế giọng theo thuộc tính, và nhận dạng giọng nói thành văn bản. Giao diện nền tối, mô hình chạy trực tiếp trên máy của bạn — sau khi tải mô hình về, không có dữ liệu âm thanh hay văn bản nào được gửi lên máy chủ.

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="Giao diện G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/0fe19f01-4e8e-46c9-bb8b-80bd9e347130" />
  </a>
</p>

---

## Tính năng

- **🔊 Sao chép giọng nói** — cung cấp một đoạn âm thanh mẫu 5–10 giây, ứng dụng sẽ đọc bất kỳ văn bản nào bằng đúng giọng đó.
- **🎛️ Văn bản sang giọng nói** — mô tả giọng theo thuộc tính (giới tính, độ tuổi, cao độ, phong cách, khẩu âm) mà không cần âm thanh mẫu.
- **📝 Giọng nói sang văn bản** — nhận dạng lời nói từ tệp âm thanh/video. Hỗ trợ MP3, WAV, M4A, FLAC, MP4, MOV…
- **🗂 Kho giọng** — lưu lại giọng vừa tạo với tên và mô tả, tái sử dụng cho cả tab Sao chép giọng nói và Văn bản sang giọng nói. Hỗ trợ **sao lưu & phục hồi** ra file `.vcp` để chia sẻ giữa các máy.
- **✨ AI gợi ý văn bản mẫu** — tự động nhận dạng nội dung đoạn âm thanh mẫu, giúp bạn không phải gõ từ đầu (vẫn cần dò lại chính tả trước khi tạo).
- **⬇ Tải riêng từng dòng** — mỗi câu trong bảng có nút tải riêng, không phải chờ xuất cả batch.
- **Hỗ trợ hơn 600 ngôn ngữ** — nhận dạng và đọc được hơn 600 ngôn ngữ khác nhau (bao gồm tiếng Việt, Anh, Hoa, Nhật, Hàn, Pháp, Đức, Tây Ban Nha và nhiều ngôn ngữ thiểu số).
- **Xử lý hàng loạt** — nhập kịch bản dạng `.txt` hoặc `.srt`, chạy hàng loạt và xuất âm thanh giữ nguyên dấu thời gian.
- **Tuỳ chỉnh giọng chi tiết** — số bước xử lý, mức độ bám sát văn bản, tốc độ đọc, khoảng nghỉ giữa các câu.
- **Tự động nhận diện GPU tương thích** — nếu card đồ hoạ không chạy được (cũ hoặc thiếu driver), ứng dụng **tự chuyển sang CPU đa nhân** và báo rõ cho bạn biết, thay vì crash với lỗi kỹ thuật.
- **Giao diện đa ngôn ngữ** — tiếng Việt và tiếng Anh.

---

## 🆕 Có gì mới ở v1.0.2

- **Kho giọng (Voice Library)** — lưu, phục hồi và chia sẻ giọng đã tạo.
- **AI gợi ý văn bản mẫu** — Whisper tự ghi lại lời nói trong đoạn âm thanh mẫu.
- **Cảnh báo kiểm tra văn bản mẫu** — trước khi tạo, ứng dụng hỏi xác nhận để tránh lỗi "AI đọc chèn quảng cáo/subscribe" do văn bản mẫu sai lệch so với âm thanh.
- **Tải riêng từng dòng** — nút ⬇ ngay trên từng hàng bảng.
- **Phát hiện GPU chính xác hơn** — không còn hiện "Hỗ trợ tốt" giả cho GPU quá cũ; tự chuyển CPU khi không chạy được.
- **Tối ưu CPU đa nhân** — khi chạy bằng CPU, tự cấu hình số luồng PyTorch/BLAS theo số nhân thật của máy để nhanh hơn đáng kể so với mặc định.

---

## Cài đặt

| Hệ điều hành | Tệp tải về | Dung lượng |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.2-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.2-arm64.dmg` | ~2 GB |

### Windows (chạy trực tiếp, không cần cài đặt)

1. Tải tệp `GLabsVoiceStudio-v1.0.2-win.zip`.
2. Giải nén ra thư mục bất kỳ (ổ cứng cần còn trống ít nhất 10 GB).
3. Mở thư mục vừa giải nén, chạy trực tiếp `GLabsVoiceStudio.exe`.

> Muốn tạo lối tắt ngoài màn hình? Chuột phải vào `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ Lần đầu mở ứng dụng có thể mất 30–60 giây (màn hình chờ dừng lâu ở khoảng 90%) — bạn cứ chờ, đừng tắt đi.** Windows cần quét ứng dụng và các tệp card đồ hoạ (đây là bước bảo mật tự động, lần đầu rất chậm). Từ lần thứ 2 trở đi, ứng dụng sẽ mở nhanh như bình thường.

### 🍎 macOS Apple Silicon

1. Tải tệp **`GLabsVoiceStudio-v1.0.2-arm64.dmg`** từ nguồn phân phối chính thức.
2. Nhấp đúp vào file `.dmg` để mở.
3. Kéo biểu tượng **G-Labs Voice Studio** vào thư mục **Applications**.
4. Mở **Applications**, **nhấp chuột phải** vào **G-Labs Voice Studio** → chọn **Open**.

> ⚠️ **Lần mở đầu tiên:** macOS có thể hiện cảnh báo *"Ứng dụng từ nhà phát triển không xác định"*. Nhấp chuột phải vào ứng dụng → **Open** → nhấn **Open** trong hộp thoại. Chỉ cần làm một lần duy nhất.

> 📁 **File đầu ra** (âm thanh, kịch bản) được lưu tại `~/Documents/G-Labs Voice Studio/output/` theo mặc định.

> **⏳ Lần đầu mở ứng dụng có thể mất 30–60 giây (màn hình chờ dừng lâu ở khoảng 90%) — bạn cứ chờ, đừng tắt đi.** macOS cần kiểm tra bảo mật toàn bộ ứng dụng lần đầu. Từ lần thứ 2 trở đi, ứng dụng mở nhanh bình thường.

#### 🍎 Xử lý lỗi *"Ứng dụng bị hỏng"* trên macOS

Khi tải file `.dmg` từ internet, macOS tự động gắn **cờ cách ly (quarantine)** vào file. Nếu ứng dụng chưa được chứng thực bởi Apple, macOS Gatekeeper sẽ chặn không cho chạy và có thể báo *"Ứng dụng bị hỏng, không thể mở"*.

**Cách 1: Nhấp chuột phải → Open** *(khuyến nghị)*

1. Mở **Applications**.
2. **Nhấp chuột phải** vào *G-Labs Voice Studio* → **Open**.
3. Nhấn **Open** lần nữa trong hộp thoại cảnh báo.

**Cách 2: Dùng Terminal** (nếu cách 1 vẫn báo lỗi)

Mở **Terminal** (Launchpad → Other → Terminal) rồi dán lệnh sau và nhấn Enter:

```bash
xattr -cr "/Applications/G-Labs Voice Studio.app"
```

Lệnh này gỡ bỏ tất cả thuộc tính mở rộng (bao gồm cờ cách ly) khỏi bundle ứng dụng. Sau khi chạy xong, mở lại ứng dụng bình thường. Chỉ cần làm **một lần duy nhất** cho mỗi phiên bản tải về.

**Cách 3: System Settings → Privacy & Security**

1. Thử mở ứng dụng bình thường (sẽ bị chặn).
2. Mở **System Settings** → **Privacy & Security**.
3. Kéo xuống cuối, tìm dòng *"G-Labs Voice Studio bị chặn…"* → bấm **Open Anyway**.
4. Xác nhận bằng Touch ID hoặc mật khẩu admin.

---

## Cách sử dụng

### Bước 1 — Đăng nhập và tải mô hình (làm một lần)

1. **Mở Cài đặt** — bấm biểu tượng bánh răng ⚙️ ở thanh bên trái.
2. **Đăng nhập** — trong tab *Bản quyền*, bấm **"Đăng nhập bằng Google"**. Trình duyệt sẽ tự mở để bạn chọn tài khoản Google.
3. **Tải mô hình AI** — chuyển sang tab *Cài đặt môi trường* (hoặc ứng dụng tự nhắc), bấm **"Tải mô hình"**. Lần đầu sẽ tải về khoảng vài GB, chờ hoàn tất là xong phần chuẩn bị.
4. Đóng Cài đặt.

### Bước 2 — Sao chép giọng nói 🔊

Nhân bản một giọng nói từ mẫu âm thanh.

1. Mở tab **Sao chép giọng nói**.
2. Ở ô *Tệp âm thanh mẫu*, bấm **"Chọn..."** → chọn tệp âm thanh mẫu (khuyến nghị 5–10 giây, giọng rõ ràng, ít tạp âm).
3. **Bắt buộc:** nhập *Văn bản mẫu* — gõ chính xác lời nói trong đoạn âm thanh mẫu (đủ dấu câu, đúng chính tả). Văn bản khớp với âm thanh là điều kiện then chốt để giọng được sao chép chuẩn.
    > 💡 Bấm **"✨ AI gợi ý"** cạnh ô văn bản mẫu để Whisper tự nhận dạng giúp bạn — vẫn cần dò lại trước khi tạo, vì AI có thể nghe nhầm vài chữ.
4. Dán hoặc gõ văn bản cần đọc vào ô *Nội dung văn bản*. Có thể bấm **"📂 Nhập tệp văn bản"** để nạp trực tiếp từ tệp `.txt` hoặc `.srt`.
5. Bấm **"📋 Nhập vào bảng"** — ứng dụng tự tách thành từng câu và đưa vào bảng phía dưới.
6. (Tuỳ chọn) Mở *Cài đặt nâng cao* để chỉnh độ chi tiết, mức độ bám sát, tốc độ đọc, khoảng nghỉ giữa câu.
7. Bấm **"▶ Bắt đầu tạo"** — ứng dụng hiện popup xác nhận văn bản mẫu; kiểm tra lần cuối rồi đồng ý để chạy.
8. Khi xong, bấm **"💾 Xuất âm thanh"** để ghép tất cả thành một tệp duy nhất, hoặc dùng nút **⬇** ở từng dòng để tải riêng câu đó.

### Bước 2b — Dùng Kho giọng 🗂 *(tuỳ chọn, có thể dùng chung ở cả tab Văn bản sang giọng nói)*

Giọng đẹp mà bạn vừa tạo xong có thể lưu lại để lần sau dùng lại trong vài giây — không cần chọn file âm thanh, không cần mã hoá lại.

1. Sau khi tạo ra âm thanh ưng ý, mở khung **Kho giọng** ở panel trái.
2. Phần **"Lưu giọng vừa tạo vào kho"**: bấm **"💾 Lưu"**, nhập tên (VD: "MC Nam trầm") và mô tả ngắn (VD: "Giọng trung niên, phù hợp voice-over tin tức") → **Lưu**.
3. Lần sau, chọn giọng từ dropdown **"Chọn giọng từ kho"** → không cần chọn tệp mẫu và văn bản mẫu nữa, chạy ngay được.
4. Nút **⋯** bên cạnh mở menu **Sao lưu / Phục hồi**:
    - **Sao lưu giọng đang chọn / toàn bộ kho** — xuất ra file `.vcp` để backup hoặc chia sẻ.
    - **Nạp backup từ file `.vcp`** — nhập nhiều file cùng lúc, không ghi đè file cũ.
5. Giọng lưu ở tab **Văn bản sang giọng nói** cũng dùng được ngay bên **Sao chép giọng nói** (và ngược lại) — không cần khởi động lại app.

### Bước 3 — Văn bản sang giọng nói 🎛️

Tạo giọng đọc mới theo mô tả, không cần tệp mẫu.

1. Mở tab **Văn bản sang giọng nói**.
2. Chọn thuộc tính giọng: *Giới tính*, *Độ tuổi*, *Cao độ*, *Phong cách*, *Khẩu âm*.
    > 💡 Muốn dùng lại một giọng đã lưu trong **Kho giọng**? Chọn thẳng trong dropdown "Chọn giọng từ kho" — ứng dụng bỏ qua bước sinh giọng mẫu từ câu đầu, chạy batch ngay từ câu 1 → **nhanh hơn đáng kể**.
3. Dán văn bản cần đọc vào ô *Nội dung văn bản*, hoặc **"📂 Nhập tệp văn bản"** từ `.txt` / `.srt`.
4. Bấm **"📋 Nhập vào bảng"** để tách câu.
5. (Tuỳ chọn) Chỉnh *Cài đặt nâng cao*.
6. Bấm **"▶ Bắt đầu tạo"**.
7. Bấm **"💾 Xuất âm thanh"** để lấy kết quả, hoặc **⬇** ở từng dòng để tải riêng.
8. Nếu thấy giọng hay, bấm **"💾 Lưu"** trong khung *Kho giọng* để dùng lại sau.

### Bước 4 — Giọng nói sang văn bản 📝

Nhận dạng lời nói từ tệp âm thanh/video sẵn có.

1. Mở tab **Giọng nói sang văn bản**.
2. Bấm **"Chọn tệp..."** → chọn tệp âm thanh/video (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. Bấm **"▶ Bắt đầu tạo"** — ứng dụng phân tích, tự tách đoạn theo giọng nói, rồi nhận dạng từng đoạn.
4. Kết quả hiển thị dạng bảng (có dấu thời gian từng câu). Có thể chỉnh sửa trực tiếp.
5. Bấm **"💾 Xuất"** để lưu ra `.txt` (văn bản thuần) hoặc `.srt` (có dấu thời gian, dùng làm phụ đề).

---

## Yêu cầu hệ thống

### Windows x64
- Windows 10 / 11 (64-bit)
- **Card đồ hoạ NVIDIA** đời **RTX 20-series trở lên** (compute capability ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). Các card cũ hơn như GTX 10-series (GTX 1060/1070/1080) **không chạy được phần tăng tốc** vì thiếu hỗ trợ kernel; ứng dụng sẽ tự phát hiện và chuyển sang CPU.
- Driver NVIDIA mới hỗ trợ CUDA 12.8.
- 8 GB RAM (khuyến nghị 16 GB khi xử lý hàng loạt hoặc chạy bằng CPU).
- 10 GB dung lượng ổ cứng (bao gồm mô hình AI).

### macOS
- macOS 12 (Monterey) trở lên
- **Apple Silicon** (M1/M2/M3/M4/...) — dùng công nghệ tăng tốc Metal của Apple
- 8 GB RAM
- 10 GB dung lượng ổ cứng

> Máy không có GPU tương thích sẽ **tự động chạy bằng CPU** đa nhân (ứng dụng đã tối ưu số luồng theo số nhân thật). Chậm hơn GPU khoảng 5-10 lần nhưng vẫn dùng được cho voice-over ngắn.

---

© 2026 Duck Martians AI Labs. Tất cả các quyền được bảo lưu.
