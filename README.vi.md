<p align="right">
🇻🇳 Tiếng Việt ·
<a href="./README.md">🇬🇧 English</a> ·
<a href="./README.pt-BR.md">🇧🇷 Português</a> ·
<a href="./README.tr.md">🇹🇷 Türkçe</a> ·
<a href="./README.zh-CN.md">🇨🇳 简体中文</a> ·
<a href="./README.hi.md">🇮🇳 हिन्दी</a> ·
<a href="./README.bn.md">🇧🇩 বাংলা</a> ·
<a href="./README.ur.md">🇵🇰 اردو</a> ·
<a href="./README.ru.md">🇷🇺 Русский</a>
</p>

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

**G-Labs Voice Studio** là ứng dụng máy tính tổng hợp giọng nói đa ngôn ngữ: sao chép giọng từ mẫu âm thanh, thiết kế giọng mới theo thuộc tính, tạo hội thoại nhiều nhân vật, và nhận dạng giọng nói thành văn bản. Giao diện nền tối, mô hình chạy trực tiếp trên máy của bạn — sau khi tải mô hình về, không có dữ liệu âm thanh hay văn bản nào được gửi lên máy chủ.

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="Giao diện G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
  </a>
</p>

---

## Tính năng

- **🔊 Sao chép giọng nói** — cung cấp một đoạn âm thanh mẫu 5–10 giây, ứng dụng sẽ đọc bất kỳ văn bản nào bằng đúng giọng đó.
- **🎛️ Văn bản sang giọng nói** — mô tả giọng theo thuộc tính (giới tính, độ tuổi, cao độ, phong cách, khẩu âm) mà không cần âm thanh mẫu.
- **💬 Hội thoại nhiều giọng** — viết kịch bản nhiều nhân vật theo cú pháp `<Tên>: lời thoại`, gán mỗi nhân vật một giọng riêng từ kho.
- **📝 Giọng nói sang văn bản** — nhận dạng lời nói từ tệp âm thanh/video. Hỗ trợ MP3, WAV, M4A, FLAC, MP4, MOV…
- **🗂 Kho giọng + 30 giọng mẫu sẵn** — ứng dụng đi kèm 30 giọng mẫu sẵn (nam/nữ, nhiều chất giọng), bạn cũng có thể lưu giọng tự tạo. Đánh dấu ⭐ yêu thích để pin lên đầu danh sách, **sao lưu & phục hồi** ra file `.vcp` để chia sẻ.
- **🎚 Thanh tốc độ + xuất theo tốc độ** — chỉnh tốc độ phát thử trên thanh sóng, file xuất ra sẽ đúng tốc độ đó (không bị méo cao độ).
- **📄 Xuất kèm phụ đề SRT** — chế độ xuất gộp 1 file mặc định kèm `.srt` để tiện làm video, không phải transcribe lại.
- **🔤 Từ điển phát âm cá nhân** — gặp ký tự đặc biệt như `100%`, `25°C`, `m²`? Gõ phiên âm một lần, ứng dụng tự nhớ và dùng lại cho lần sau.
- **✨ AI gợi ý văn bản mẫu** — tự động nhận dạng nội dung đoạn âm thanh mẫu, giúp bạn không phải gõ từ đầu (vẫn cần dò lại chính tả).
- **⬇ Tải riêng từng dòng** — mỗi câu trong bảng có nút tải riêng, không phải chờ xuất cả batch.
- **Hỗ trợ hơn 600 ngôn ngữ đầu ra** — đọc được hơn 600 ngôn ngữ khác nhau (Việt, Anh, Hoa, Nhật, Hàn, Pháp, Đức, Tây Ban Nha và nhiều ngôn ngữ thiểu số).
- **Xử lý hàng loạt** — nhập kịch bản dạng `.txt` hoặc `.srt`, chạy hàng loạt và xuất âm thanh giữ nguyên dấu thời gian.
- **Tự động nhận diện GPU tương thích** — nếu card đồ hoạ không chạy được, ứng dụng **tự chuyển sang CPU đa nhân** và báo rõ cho bạn biết, thay vì crash với lỗi kỹ thuật.
- **Giao diện 9 ngôn ngữ** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

<details open>
<summary><b>🆕 Có gì mới ở v1.0.8</b></summary>

- **🗒 Hàng chờ tạo (mới)** — thay vì ngồi tạo từng cái rồi bấm xuất tay, giờ bạn **xếp nhiều việc vào hàng chờ**: mỗi việc là một kịch bản + giọng + cài đặt riêng, độc lập hoàn toàn. Bấm chạy một lần, app **tự làm lần lượt và tự lưu file** ra thư mục cho từng việc — rảnh tay làm chuyện khác. Đặt **tên + thư mục riêng** cho mỗi việc; **đóng app mở lại vẫn còn nguyên hàng chờ**. *(Tính năng của bản trả phí.)*
- **📊 Xem tiến độ trực quan (X/N câu)** — mỗi việc trong hàng chờ hiển thị rõ **đã tạo được bao nhiêu trên tổng số câu** (ví dụ `8/10`), nên bạn thấy ngay việc nào chạy đủ, việc nào bị **thiếu câu do lỗi** — khỏi phải mở ra kiểm từng cái.
- **📂 Mở lại việc đã chạy để sửa** — bấm **Mở lại** một việc trong hàng chờ để nạp nguyên kịch bản + giọng + cài đặt về lại tab Văn bản → Giọng, câu lỗi được **đánh dấu ❌**, rồi tạo lại cho gọn.
- **✨ Giao diện gọn hơn** — các mục cài đặt gập/mở kiểu accordion (mở mục này thì mục kia tự đóng) cho đỡ dài; thêm vài biểu tượng cho dễ nhìn.

</details>

---

<details>
<summary><b>🆕 Có gì mới ở v1.0.7</b></summary>

- **🔊 Tab Sao chép giọng làm lại cho dễ dùng** — kho giọng chia 2 cột rõ ràng (**Giọng có sẵn** / **Giọng của bạn**), ô nhập gọn lại còn 1 câu. Sao chép xong app tự nhắc nghe thử rồi hỏi có muốn lưu vào kho không — lưu chỉ 1 chạm. Đoạn âm thanh mẫu dài hơn 30 giây sẽ **tự cắt gọn** ở chỗ im lặng cho giọng chuẩn hơn.
- **🎛 Tab Văn bản → Giọng gọn lại** — gộp "Kho giọng" và "Thiết kế giọng" vào **chung 1 khung**, gạt qua lại giữa **Dùng giọng có sẵn** ↔ **Giọng ngẫu nhiên**, không còn rối.
- **▶ Nghe thử giọng có sẵn** — bấm nút ▶ cạnh mỗi giọng mẫu trong kho để nghe ngay trước khi dùng.
- **⭐ Yêu thích đồng bộ mọi nơi** — đánh dấu ⭐ một giọng ở tab nào thì các tab khác cũng thấy.
- **🐛 Sửa lỗi đổi tốc độ làm méo tiếng / không xuất được file** — đã bỏ ô chỉnh tốc độ ở khung nghe thử (chính nó gây méo tiếng và lỗi khi xuất). Muốn đọc nhanh/chậm thì dùng thanh **Tốc độ đọc** trong *Cài đặt nâng cao* — giữ giọng tự nhiên, không lỗi.
- **✨ Vài tinh chỉnh nhỏ** — khoảng nghỉ giữa câu mặc định ngắn lại (100ms) cho liền mạch hơn; nút xóa hiển thị đồng nhất; giao diện gọn gàng hơn ở nhiều chỗ.
- **🎙 Tab Giọng nói → văn bản: chọn được model nhận dạng** — chọn từ bản nhỏ đến lớn (Tiny → Turbo) tùy sức máy: máy yếu chọn bản nhỏ cho nhẹ & nhanh, máy mạnh chọn bản lớn cho chính xác hơn (mỗi bản ghi rõ **VRAM cần dùng** để dễ chọn). Bản mặc định có sẵn ngay sau khi cài; bản khác tải thêm 1 chạm và **lưu về máy**, lần sau dùng lại không cần mạng.
- **🌍 Chọn ngôn ngữ khi nhận dạng** — chỉ rõ ngôn ngữ đang nói (~100 thứ tiếng) để nhận dạng đúng hơn, không bị nhầm ngôn ngữ giữa chừng; kèm vài cải tiến giúp ít sai/lặp chữ ở những đoạn khó.

</details>

---

<details>
<summary><b>🆕 Có gì mới ở v1.0.6</b></summary>

- **🔗 Webhook API (mới)** — server REST cục bộ cho phép n8n, Zapier, Python/cURL hoặc bất kỳ HTTP client nào gọi sinh giọng tự động. Tích hợp panel tìm kiếm giọng + ngôn ngữ ngay trong app, nháy đúp để copy. Có khóa API che dạng `xxxx***xxxx`, autostart, log request realtime.
- **🚀 Xuất file nhanh hơn nhiều + thanh tiến độ thật** — ghép nhạc + chỉnh tốc độ chạy song song nhiều core, dự án 50 phút xuất xong trong vài chục giây thay vì vài phút. Thanh tiến độ inline đi mượt 0→100% với nút **Dừng** cắt được giữa chừng.
- **🧹 Tab Sao chép giọng + Giọng nói sang văn bản (ASR) gọn hơn** — Clone bỏ các nút trùng với tab Văn bản → Giọng. ASR tự ghép fragment ngắn thành câu hoàn chỉnh, giữ nguyên timeline gốc.
- **💾 Đồng bộ cài đặt giữa các tab** — *Số câu đồng thời* (batch size) giờ dùng chung cho cả 3 tab + webhook concurrency limit, đổi ở đâu các nơi còn lại tự update. Tab Sao chép giọng / Văn bản → Giọng nhớ giọng đã chọn trong kho qua các lần restart.
- **🐛 Sửa nhiều lỗi tồn đọng** — crash khi xuất file sau khi hết phiên (`AttributeError: NoneType`), trạng thái "model đã tải" sai khi mạng đứt giữa chừng làm safetensors thiếu, nút "Lưu giọng" sáng sớm trước khi clone xong.

</details>

---

<details>
<summary><b>🆕 Có gì mới ở v1.0.5</b></summary>

- **🎚 Chế độ âm thanh chuyên nghiệp (mới)** — chọn 1 trong 6 chế độ xử lý (Phát thanh / Điện ảnh / Podcast / Ấm / Sáng / Nguyên bản) để file giọng đọc nghe "chuẩn studio" hơn. Có sẵn trong cả 3 tab Sao chép giọng / Văn bản sang giọng / Hội thoại — đổi ở 1 tab thì 2 tab còn lại tự cập nhật theo.
- **🌐 Tách câu tốt hơn cho tiếng Trung / Hindi / Ả Rập / Urdu** — trước đây các ngôn ngữ này hay bị dồn cả đoạn thành 1 dòng, giờ tách câu chính xác theo dấu câu của từng ngôn ngữ.
- **🧠 Tự động giải phóng bộ nhớ khi nhàn rỗi** — nếu để máy không dùng 5 phút (mặc định), app tự thả mô hình AI ra cho máy nhẹ bớt. Vào tab Cài đặt có thể đổi thời gian hoặc tắt hẳn.
- **⚙ Ổn định hơn khi vừa tạo giọng vừa nhận dạng** — máy yếu trước đây có thể bị lỗi giữa chừng, giờ app tự sắp xếp để không xung đột.

> ⚠️ **Đổi nhẹ ở file giọng đọc:** Mặc định bật chế độ **📻 Phát thanh** và **Cân đều âm lượng các câu**, nên file ở phiên bản này nghe **rõ và đầy hơn** so với phiên bản cũ. Muốn giữ y như cũ: vào 1 trong 3 tab tạo giọng → mở mục **Tinh chỉnh âm thanh** → chọn **🔇 Nguyên bản** và bỏ tích ô **Cân đều âm lượng các câu**.

</details>

---

<details>
<summary><b>🆕 Có gì mới ở v1.0.4</b></summary>

- **💬 Tab Hội thoại nhiều giọng (mới)** — viết kịch bản nhiều nhân vật, mỗi người một giọng. Có nút **📋 Mẫu hội thoại chuẩn** để xem ví dụ.
- **🗂 30 giọng mẫu sẵn** — đi kèm app, dùng được ngay không cần tự thu mẫu.
- **⭐ Ngôi sao yêu thích** — bấm vào ⭐ cạnh tên giọng trong kho để pin lên đầu danh sách.
- **🎚 Thanh tốc độ trong player** — chỉnh tốc độ phát thử (0.5x → 2x), xuất file giữ đúng tốc độ đó.
- **📄 Tự xuất phụ đề SRT** — khi xuất gộp 1 file, app kèm luôn file `.srt` cùng tên (có thể tắt nếu không cần).
- **🔤 Từ điển phát âm ký tự đặc biệt** — không bao giờ phải sửa "100%" thành "100 phần trăm" thủ công nữa: gõ phiên âm một lần, app nhớ mãi.
- **🌐 9 ngôn ngữ giao diện** — thêm Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский (ngoài Việt/Anh).
- **⏳ Hiển thị thời gian từng dòng** — biết ngay câu nào đang tạo và đã chạy bao lâu.
- **🌍 Bắt buộc chọn ngôn ngữ đầu ra** — không còn "Auto" để tránh đọc sai phát âm.

</details>

---

## Cài đặt

| Hệ điều hành | Tệp tải về | Dung lượng |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.8-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.8-arm64.dmg` | ~2 GB |

### Windows (chạy trực tiếp, không cần cài đặt)

1. Tải tệp `GLabsVoiceStudio-v1.0.8-win.zip`.
2. Giải nén ra thư mục bất kỳ (ổ cứng cần còn trống ít nhất 10 GB).
3. Mở thư mục vừa giải nén, chạy trực tiếp `GLabsVoiceStudio.exe`.

> Muốn tạo lối tắt ngoài màn hình? Chuột phải vào `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ Lần đầu mở ứng dụng có thể mất 30–60 giây (màn hình chờ dừng lâu ở khoảng 90%) — bạn cứ chờ, đừng tắt đi.** Windows cần quét ứng dụng và các tệp card đồ hoạ (đây là bước bảo mật tự động, lần đầu rất chậm). Từ lần thứ 2 trở đi, ứng dụng sẽ mở nhanh như bình thường.

### 🍎 macOS Apple Silicon

1. Tải tệp **`GLabsVoiceStudio-v1.0.8-arm64.dmg`** từ nguồn phân phối chính thức.
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

### Phần 1 — Lần đầu mở app (làm một lần)

1. Mở app — màn hình chào hiện 9 lựa chọn ngôn ngữ giao diện. Chọn ngôn ngữ bạn muốn dùng.
2. **Đăng nhập** — bấm biểu tượng bánh răng ⚙️ ở thanh bên trái → tab *Bản quyền* → **"Đăng nhập bằng Google"**.
3. **Tải mô hình AI** — chuyển sang tab *Cài đặt môi trường* (hoặc app tự nhắc) → bấm **"Tải mô hình"**. Khoảng vài GB, chờ hoàn tất là xong phần chuẩn bị.
4. Đóng Cài đặt.

> 💡 Đổi ngôn ngữ giao diện sau này: vào Cài đặt → Ngôn ngữ.

### Phần 2 — Sao chép giọng nói 🔊

Nhân bản một giọng nói từ mẫu âm thanh.

1. Mở tab **Sao chép giọng nói**.
2. Chọn **ngôn ngữ đầu ra** ở đầu tab (vd: Vietnamese, English...).
3. Ở ô *Tệp âm thanh mẫu*, bấm **"Chọn..."** → chọn tệp âm thanh mẫu (khuyến nghị 5–10 giây, giọng rõ ràng, ít tạp âm).
4. **Bắt buộc:** nhập *Văn bản mẫu* — gõ chính xác lời nói trong đoạn âm thanh mẫu (đủ dấu câu, đúng chính tả).
    > 💡 Bấm **"✨ AI gợi ý"** để Whisper tự nhận dạng giúp bạn — vẫn cần dò lại trước khi tạo.
5. Dán văn bản cần đọc vào ô *Nội dung văn bản* (hoặc **"📂 Nhập tệp"** từ `.txt` / `.srt`).
6. Bấm **"📋 Nhập vào bảng"** — app tự tách thành từng câu.
7. (Tuỳ chọn) Mở **🔤 Phát âm** để xem từ điển phát âm — nếu trong văn bản có ký tự đặc biệt (vd `100%`), app sẽ hỏi cách đọc.
8. Bấm **"▶ Bắt đầu tạo"** → app hỏi xác nhận văn bản mẫu → đồng ý để chạy.
9. Khi xong, bấm **"💾 Xuất âm thanh"** (gộp 1 file kèm `.srt`) hoặc **⬇** ở từng dòng để tải riêng.

### Phần 3 — Văn bản sang giọng nói 🎛️

Tạo giọng đọc mới theo mô tả, không cần tệp mẫu.

1. Mở tab **Văn bản sang giọng nói**.
2. Chọn **ngôn ngữ đầu ra**.
3. Mở khung **Thiết kế giọng** và chọn các thuộc tính: *Giới tính*, *Độ tuổi*, *Cao độ*, *Phong cách*, *Khẩu âm*.
    > 💡 Muốn dùng lại một giọng đã lưu trong **Kho giọng**? Chọn thẳng trong dropdown — app bỏ qua bước sinh giọng mẫu, chạy ngay từ câu 1.
4. Dán văn bản, bấm **"📋 Nhập vào bảng"**.
5. Bấm **"▶ Bắt đầu tạo"**.
6. Sau khi tạo xong: click vào dòng bạn muốn lưu trong bảng → bấm **"💾 Lưu"** trong khung *Kho giọng* để dùng lại sau.
7. Bấm **"💾 Xuất âm thanh"** để lấy kết quả.

### Phần 4 — Hội thoại nhiều giọng 💬 *(mới)*

Tạo audio hội thoại nhiều nhân vật, mỗi người một giọng riêng — phù hợp làm podcast, audio drama, video kịch bản phỏng vấn.

1. Mở tab **Hội thoại nhiều giọng**.
2. Chọn **ngôn ngữ đầu ra**.
3. Bấm nút **📋 Mẫu hội thoại chuẩn** (góc phải khung văn bản) để xem ví dụ — app sẽ paste mẫu và mở khung chỉnh sửa chi tiết.
4. Viết kịch bản theo cú pháp:
    ```
    <MC>: Xin chào quý vị và các bạn.
    <Mai>: Em chào anh chị, em rất vui khi được tham gia chương trình.
    <Minh>: Em cũng vậy, hôm nay chúng ta sẽ nói về gì ạ?
    ```
    > 💡 Tên nhân vật đặt trong dấu `< >`, theo sau là `:` rồi đến lời thoại. Có thể bỏ `:` cũng được. Tên không phân biệt hoa thường.
5. Bấm **"🎭 Phân tích hội thoại"** — app tách thành từng dòng, hiện cột "Nhân vật".
6. Khung **Phân vai giọng đọc** tự mở ra — chọn một giọng từ kho cho mỗi nhân vật.
7. (Tuỳ chọn — *mới*) Với mỗi nhân vật trong khung **Phân vai giọng đọc**, có thanh **Tốc độ** riêng (0.5x → 2x). Mỗi nhân vật nói với tốc độ độc lập trong cùng 1 lần tạo — phù hợp để MC nói chậm, khách mời nói nhanh hơn.
8. Bấm **"▶ Bắt đầu tạo"** — mỗi câu được đọc bằng giọng của nhân vật tương ứng.
9. **"💾 Xuất âm thanh"** để lấy file (có kèm `.srt`).

### Phần 5 — Giọng nói sang văn bản 📝

Nhận dạng lời nói từ tệp âm thanh/video sẵn có.

1. Mở tab **Giọng nói sang văn bản**.
2. Bấm **"Chọn tệp..."** → chọn tệp âm thanh/video (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. Bấm **"▶ Bắt đầu tạo"** — app phân tích, tự tách đoạn theo giọng nói, rồi nhận dạng từng đoạn.
4. Kết quả hiển thị dạng bảng (có dấu thời gian từng câu). Có thể chỉnh sửa trực tiếp.
5. Bấm **"💾 Xuất"** để lưu ra `.txt` (văn bản thuần) hoặc `.srt` (có dấu thời gian, dùng làm phụ đề).

---

## 💡 Mẹo dùng nâng cao

### Tinh chỉnh âm thanh chuyên nghiệp *(mới)*
- Trong 3 tab tạo giọng (Sao chép giọng / Văn bản sang giọng / Hội thoại) có mục **Tinh chỉnh âm thanh** thu gọn ở giữa khung.
- 6 chế độ sẵn:
  - 📻 **Phát thanh** *(mặc định)* — chuẩn radio/podcast, ấm và nén gọn.
  - 🎬 **Điện ảnh** — vang rộng, nén nhẹ, chất lượng phim.
  - 🎙️ **Podcast** — mic gần, nén mạnh, không vang.
  - 🔇 **Nguyên bản** — giữ nguyên đầu ra của mô hình, không xử lý.
  - ☀️ **Ấm** — trầm dày, cảm giác ấm áp.
  - ✨ **Sáng** — cao sắc nét, thoáng đãng.
- Đổi chế độ ở 1 tab → 2 tab còn lại tự đồng bộ. Nếu muốn file giống hệt phiên bản cũ (v1.0.4): chọn **🔇 Nguyên bản** + bỏ tích **Cân đều âm lượng các câu**.

### Tự động giải phóng bộ nhớ *(mới)*
- Mặc định: nếu để app không dùng **5 phút**, mô hình AI sẽ tự được dỡ ra khỏi VRAM/RAM để máy nhẹ bớt.
- Lần thao tác kế tiếp app sẽ nạp lại mô hình (~30-60s).
- Vào tab **Cài đặt môi trường** → mục **Tự động giải phóng VRAM** để chỉnh thời gian (0 = tắt hẳn, 1-120 phút).

### Kho giọng & ngôi sao yêu thích
- Mỗi giọng trong kho có ngôi sao ☆ ở đầu. Bấm vào → biến thành ★ → giọng đó nhảy lên đầu danh sách (cho lần mở sau).
- Bấm ★ lần nữa để bỏ yêu thích.
- 30 giọng mẫu sẵn (Achernar, Aoede, Mai, MC…) đều có thể đánh dấu yêu thích.

### Từ điển phát âm
- Khi trong văn bản có `%`, `$`, `°C`, `m²`, tên thương hiệu... bấm **🔤 Phát âm** trước khi tạo.
- Lần đầu gặp, app hỏi cách đọc cho từng ký tự/từ → bạn gõ phiên âm (vd `%` → ` phần trăm`).
- Mỗi từ chỉ cần gõ **một lần** — app nhớ theo ngôn ngữ đầu ra. Lần sau gặp lại, tự áp dụng.
- Cùng từ ở ngôn ngữ khác (vi vs en) sẽ có phiên âm riêng.

### Thẻ cảm xúc & âm thanh phi ngôn ngữ
- Gõ thẳng các thẻ này vào văn bản cần đọc, giọng sẽ phát ra âm thanh phi ngôn ngữ tương ứng. Dùng được ở cả **Sao chép giọng**, **Văn bản sang giọng** và **Hội thoại nhiều giọng**.
- Viết thẻ đúng như bên dưới, **giữ nguyên dấu ngoặc vuông**, đặt riêng hoặc xen giữa câu (vd: `Buồn cười quá [laughter] mình không nhịn được.`).

| Thẻ | Âm thanh |
|---|---|
| `[laughter]` | Tiếng cười |
| `[sigh]` | Tiếng thở dài |
| `[confirmation-en]` | Đồng tình — "mm-hmm" |
| `[question-en]` | Ngữ điệu hỏi |
| `[question-ah]` | Ngữ điệu hỏi — "ah?" |
| `[question-oh]` | Ngữ điệu hỏi — "oh?" |
| `[question-ei]` | Ngữ điệu hỏi — "ei?" |
| `[question-yi]` | Ngữ điệu hỏi — "yi?" |
| `[surprise-ah]` | Ngạc nhiên — "ah!" |
| `[surprise-oh]` | Ngạc nhiên — "oh!" |
| `[surprise-wa]` | Ngạc nhiên — "wa!" |
| `[surprise-yo]` | Ngạc nhiên — "yo!" |
| `[dissatisfaction-hnn]` | Khó chịu — "hnn" |

> 💡 Thẻ được hiểu là tín hiệu biểu cảm, không đọc thành chữ. Mức độ thể hiện thay đổi tùy ngôn ngữ và giọng — nên thử trên một câu ngắn trước.

### Tốc độ phát + xuất
- Sau khi tạo audio, dưới thanh sóng có **dropdown tốc độ** (0.5x → 2x).
- Đổi tốc độ → preview ngay trên player.
- File xuất ra sẽ giữ đúng tốc độ đó, **không bị méo cao độ** (dùng kỹ thuật time-stretch giữ pitch).

### Xuất file kèm SRT
- Trong khung *Cài đặt xuất file*, mặc định tích **"Xuất kèm phụ đề (.srt)"**.
- Khi xuất gộp 1 file, app tự tạo `tên.srt` cùng thư mục với `tên.wav`.
- Mốc thời gian trong SRT phản ánh độ dài thực tế của từng câu (đã bao gồm hiệu chỉnh tốc độ).

---

## Yêu cầu hệ thống

|   | Tối thiểu | Khuyến nghị |
|---|---|---|
| **Hệ điều hành** | Windows 10 (64-bit), macOS 12 Monterey | Windows 11, macOS 13 trở lên |
| **RAM** | 8 GB | 16 GB trở lên |
| **VRAM (GPU)** | 4 GB (tự chuyển TTS sang CPU khi thiếu) | 8 GB trở lên (NVIDIA RTX 3060+) |
| **Ổ cứng** | 10 GB trống (mô hình + cache) | 20 GB trở lên, SSD |
| **GPU** | Không bắt buộc — CPU vẫn chạy được | NVIDIA CUDA · Apple Silicon (Metal) |

> 💡 **Mẹo:** Với card đồ hoạ ≤ 8 GB VRAM, ứng dụng tự động chuyển phần tổng hợp giọng nói (TTS) sang CPU trong lúc nhận dạng — không cần chỉnh cấu hình. Máy không có GPU rời vẫn chạy được toàn bộ pipeline trên CPU (chỉ chậm hơn).

### Lưu ý theo nền tảng

**Windows x64**
- **Card đồ hoạ NVIDIA** đời **RTX 20-series trở lên** (compute capability ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). Các card cũ hơn như GTX 10-series (GTX 1060/1070/1080) **không chạy được phần tăng tốc**; ứng dụng sẽ tự phát hiện và chuyển sang CPU.
- Driver NVIDIA mới hỗ trợ CUDA 12.8.

**macOS**
- Chỉ hỗ trợ **Apple Silicon** (M1/M2/M3/M4…) — dùng công nghệ tăng tốc Metal của Apple. Bản Intel Mac không được hỗ trợ.

> Máy không có GPU tương thích sẽ **tự động chạy bằng CPU** đa nhân (ứng dụng đã tối ưu số luồng theo số nhân thật). Chậm hơn GPU khoảng 5–10 lần nhưng vẫn dùng được cho voice-over ngắn.

---

© 2026 Duck Martians AI Labs. Tất cả các quyền được bảo lưu.
