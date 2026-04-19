<p align="right">🇻🇳 Tiếng Việt · <a href="./README.en.md">🇬🇧 English</a></p>

<h1 align="center">G-Labs Voice Studio</h1>
<p align="center">Ứng dụng giọng nói AI cho creators</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G">
    <img src="https://img.shields.io/badge/Download%20Windows-%F0%9F%92%BB-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  </a>
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta">
    <img src="https://img.shields.io/badge/Download%20macOS-%F0%9F%8D%8E-000000?style=for-the-badge&logo=apple&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://duckmartians.info">
    <img src="https://img.shields.io/badge/Homepage-Visit-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio** là ứng dụng desktop tổng hợp giọng nói đa ngôn ngữ với khả năng sao chép giọng (voice cloning), thiết kế giọng theo thuộc tính, và nhận dạng giọng nói thành văn bản. Giao diện dark-theme, chạy model ngay trên máy người dùng — không gửi audio/văn bản lên cloud sau khi model đã tải về.

<p align="center">
  <a href="https://duckmartians.info/g-labs">
    <img alt="Giao diện G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/0fe19f01-4e8e-46c9-bb8b-80bd9e347130" />
  </a>
</p>

---

## Tính năng

- **🔊 Sao chép giọng nói (Voice Cloning)** — cung cấp một đoạn audio mẫu 5–10 giây, app sẽ tạo giọng mới giống hệt với văn bản bất kỳ.
- **🎛️ Văn bản sang giọng nói (Voice Design / TTS)** — mô tả giọng theo thuộc tính (giới tính, độ tuổi, cao độ, phong cách, khẩu âm) mà không cần audio mẫu.
- **📝 Giọng nói sang văn bản (ASR)** — nhận dạng lời nói từ file audio/video. Hỗ trợ MP3, WAV, M4A, FLAC, MP4, MOV…
- **Xử lý hàng loạt** — nhập script dạng `.txt` hoặc `.srt`, chạy batch và xuất audio hàng loạt giữ nguyên timestamp.
- **Chỉnh giọng chi tiết** — độ chi tiết (diffusion steps), mức bám sát text (guidance scale), tốc độ đọc, khoảng nghỉ giữa câu.
- **Đa ngôn ngữ** — giao diện tiếng Việt / tiếng Anh, model hỗ trợ đa ngôn ngữ cho cả TTS và ASR.

---

## Cài đặt

| Nền tảng | File | Kích thước |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.0-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.0-arm64.dmg` | ~2 GB |

### Windows (portable, không cần cài đặt)

1. Tải file `GLabsVoiceStudio-v1.0.0-win.zip`.
2. Giải nén ra thư mục bất kỳ (khuyến nghị ổ có ít nhất 10 GB trống).
3. Mở thư mục vừa giải nén, chạy trực tiếp `GLabsVoiceStudio.exe`.
4. Đăng nhập bằng tài khoản Google để kích hoạt license.
5. App sẽ tải model AI lần đầu (~vài GB).

> Muốn tạo shortcut? Chuột phải `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ Lần đầu mở app có thể mất 30–60 giây (màn hình splash dừng lâu ở ~90%) — bạn cứ chờ, đừng tắt đi.** Windows cần quét qua app và các file GPU (đây là bước bảo mật tự động, lần đầu rất chậm). Từ lần thứ 2 trở đi, app sẽ mở nhanh như bình thường.

### macOS Apple Silicon

1. Tải file `GLabsVoiceStudio-v1.0.0-arm64.dmg`.
2. Mở file DMG, kéo biểu tượng app vào thư mục `Applications`.
3. Mở app từ Launchpad hoặc Applications. Lần đầu mở có thể cần vào *System Settings → Privacy & Security* để cho phép (app chưa được Apple notarize).
4. Đăng nhập bằng tài khoản Google để kích hoạt license.
5. App sẽ tải model AI lần đầu (~vài GB).

> **⏳ Lần đầu mở app có thể mất 30–60 giây (splash dừng lâu ở ~90%) — bạn cứ chờ, đừng tắt đi.** macOS cần kiểm tra bảo mật toàn bộ app lần đầu. Từ lần thứ 2 trở đi, app mở nhanh bình thường.

---

## Yêu cầu hệ thống

### Windows x64
- Windows 10 / 11 (64-bit)
- **NVIDIA GPU** driver hỗ trợ CUDA 12.8 (RTX 20-series trở lên khuyến nghị) — app tự động dùng CUDA nếu có, fallback CPU nếu không có GPU NVIDIA.
- 8 GB RAM (16 GB khuyến nghị khi batch)
- 10 GB dung lượng ổ cứng (bao gồm model)

### macOS
- macOS 12 (Monterey) trở lên
- **Apple Silicon** (M1/M2/M3/M4) — dùng Metal Performance Shaders (MPS)
- 8 GB RAM
- 10 GB dung lượng ổ cứng

> Máy Windows không có GPU NVIDIA hoặc macOS Intel sẽ chạy ở CPU mode — chậm hơn nhiều, chỉ phù hợp test.

---

© 2026 Duck Martians AI Labs. Tất cả các quyền được bảo lưu.
