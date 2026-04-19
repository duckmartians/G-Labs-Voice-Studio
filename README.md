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
  <a href="https://duckmartians.info">
    <img alt="Trang chủ" src="https://img.shields.io/badge/Trang%20ch%E1%BB%A7-Truy%20c%E1%BA%ADp-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio** là ứng dụng máy tính tổng hợp giọng nói đa ngôn ngữ, có khả năng sao chép giọng, thiết kế giọng theo thuộc tính, và nhận dạng giọng nói thành văn bản. Giao diện nền tối, mô hình chạy trực tiếp trên máy của bạn — sau khi tải mô hình về, không có dữ liệu âm thanh hay văn bản nào được gửi lên máy chủ.

<p align="center">
  <a href="https://duckmartians.info/g-labs">
    <img alt="Giao diện G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/0fe19f01-4e8e-46c9-bb8b-80bd9e347130" />
  </a>
</p>

---

## Tính năng

- **🔊 Sao chép giọng nói** — cung cấp một đoạn âm thanh mẫu 5–10 giây, ứng dụng sẽ đọc bất kỳ văn bản nào bằng đúng giọng đó.
- **🎛️ Văn bản sang giọng nói** — mô tả giọng theo thuộc tính (giới tính, độ tuổi, cao độ, phong cách, khẩu âm) mà không cần âm thanh mẫu.
- **📝 Giọng nói sang văn bản** — nhận dạng lời nói từ tệp âm thanh/video. Hỗ trợ MP3, WAV, M4A, FLAC, MP4, MOV…
- **Hỗ trợ hơn 600 ngôn ngữ** — nhận dạng và đọc được hơn 600 ngôn ngữ khác nhau (bao gồm tiếng Việt, Anh, Hoa, Nhật, Hàn, Pháp, Đức, Tây Ban Nha và nhiều ngôn ngữ thiểu số).
- **Xử lý hàng loạt** — nhập kịch bản dạng `.txt` hoặc `.srt`, chạy hàng loạt và xuất âm thanh giữ nguyên dấu thời gian.
- **Tuỳ chỉnh giọng chi tiết** — số bước xử lý, mức độ bám sát văn bản, tốc độ đọc, khoảng nghỉ giữa các câu.
- **Giao diện đa ngôn ngữ** — tiếng Việt và tiếng Anh.

---

## Cài đặt

| Hệ điều hành | Tệp tải về | Dung lượng |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.0-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.0-arm64.dmg` | ~2 GB |

### Windows (chạy trực tiếp, không cần cài đặt)

1. Tải tệp `GLabsVoiceStudio-v1.0.0-win.zip`.
2. Giải nén ra thư mục bất kỳ (ổ cứng cần còn trống ít nhất 10 GB).
3. Mở thư mục vừa giải nén, chạy trực tiếp `GLabsVoiceStudio.exe`.

> Muốn tạo lối tắt ngoài màn hình? Chuột phải vào `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ Lần đầu mở ứng dụng có thể mất 30–60 giây (màn hình chờ dừng lâu ở khoảng 90%) — bạn cứ chờ, đừng tắt đi.** Windows cần quét ứng dụng và các tệp card đồ hoạ (đây là bước bảo mật tự động, lần đầu rất chậm). Từ lần thứ 2 trở đi, ứng dụng sẽ mở nhanh như bình thường.

### macOS Apple Silicon

1. Tải tệp `GLabsVoiceStudio-v1.0.0-arm64.dmg`.
2. Mở tệp DMG, kéo biểu tượng ứng dụng vào thư mục `Applications`.
3. Mở ứng dụng từ Launchpad hoặc Applications. Lần đầu mở có thể cần vào *System Settings → Privacy & Security* để cho phép chạy (ứng dụng chưa được Apple chứng thực).

> **⏳ Lần đầu mở ứng dụng có thể mất 30–60 giây (màn hình chờ dừng lâu ở khoảng 90%) — bạn cứ chờ, đừng tắt đi.** macOS cần kiểm tra bảo mật toàn bộ ứng dụng lần đầu. Từ lần thứ 2 trở đi, ứng dụng mở nhanh bình thường.

---

## Cách sử dụng

Sau khi mở ứng dụng lần đầu, **bắt buộc phải đăng nhập tài khoản bản quyền thì mới dùng được** các tính năng:

1. **Mở Cài đặt** — bấm vào biểu tượng bánh răng ⚙️ ở thanh bên trái.
2. **Đăng nhập** — trong tab *Bản quyền*, bấm nút **"Đăng nhập bằng Google"**. Trình duyệt sẽ tự mở để bạn chọn tài khoản Google đã mua bản quyền.
3. **Chờ kích hoạt** — ứng dụng xác thực với máy chủ và hiển thị trạng thái tài khoản (gói, hạn sử dụng).
4. **Tải mô hình AI** — lần đầu ứng dụng sẽ tải mô hình (~vài GB). Chờ tải xong là dùng được.
5. **Bắt đầu tạo** — đóng Cài đặt, chọn một trong các tab *Sao chép giọng nói* / *Văn bản sang giọng nói* / *Giọng nói sang văn bản* tuỳ nhu cầu.

> Chưa có tài khoản bản quyền? Liên hệ qua [Discord](https://discord.gg/munMZEBMw5) hoặc [trang chủ](https://duckmartians.info) để được hướng dẫn mua.

---

## Yêu cầu hệ thống

### Windows x64
- Windows 10 / 11 (64-bit)
- **Card đồ hoạ NVIDIA** có trình điều khiển hỗ trợ CUDA 12.8 (khuyến nghị dòng RTX 20-series trở lên) — ứng dụng tự dùng card đồ hoạ nếu có, nếu không thì chuyển sang dùng CPU.
- 8 GB RAM (khuyến nghị 16 GB khi xử lý hàng loạt)
- 10 GB dung lượng ổ cứng (bao gồm mô hình AI)

### macOS
- macOS 12 (Monterey) trở lên
- **Apple Silicon** (M1/M2/M3/M4/...) — dùng công nghệ tăng tốc Metal của Apple
- 8 GB RAM
- 10 GB dung lượng ổ cứng

> Máy Windows không có card đồ hoạ NVIDIA hoặc máy Mac đời Intel sẽ chạy bằng CPU — chậm hơn nhiều, chỉ phù hợp để dùng thử.

---

© 2026 Duck Martians AI Labs. Tất cả các quyền được bảo lưu.
