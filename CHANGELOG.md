# Changelog

## v2.0.2 - duckmartians

### Sửa lỗi

- **Thiết kế giọng**: dấu phẩy toàn khổ `，` và phương ngữ (`河南话`…) bị hỏng mã → mô tả tiếng Trung báo lỗi, phương ngữ không ép tiếng Trung.
- **Tệp giọng `.vcp`**: nạp ở chế độ an toàn (tệp chia sẻ không chạy được mã); nhập lại giọng có sẵn đã xuất không còn bị che/không xoá được.
- **License**: nhiều nơi kiểm cùng lúc không còn gây đăng xuất oan.
- **Cài đặt**: `settings.json` không còn bị xoá trắng khi tệp lỗi/ghi chồng.
- **Xuất file**: không nạp hết audio vào RAM, RAM không còn tăng dần sau mỗi lần xuất; nút Xuất mở lại sau khi bấm Dừng hoặc gặp lỗi.
- **Tách phụ đề**: đổi model nhận dạng giữa chừng không còn làm cụt kết quả âm thầm; đoạn nhận dạng lỗi được báo ra.
- **Dịch phụ đề**: nạp tệp mới khi đang dịch bị chặn (trước ghi nhầm bản dịch cũ vào tệp mới); lỗi xác thực dừng job ngay; nhận phụ đề không có trường giờ (`00:01.000`, kiểu YouTube).
- **Hàng chờ tạo**: không sửa cấu hình mastering chung trong lúc chạy.
- **Bảng kịch bản**: khoá xoá/tách/nhập dòng khi đang tạo (trước audio có thể rơi nhầm dòng).
- **Webhook**: một client treo không còn chặn cả API; giới hạn thân request 1 MB; trạng thái `completed` luôn kèm `results`; URL kết quả đúng địa chỉ khi gọi qua LAN.
- **Cập nhật**: nút tải tự động tải được bản mới; tệp tải thiếu byte bị coi là lỗi.
- Mac: bộ mã hoá âm thanh ở lại CPU; App Nap không còn bị bật lại trong bản DMG.

### Nhanh & nhẹ hơn

- Splash hiện gần như ngay khi mở app (trước phải chờ nạp torch/transformers ~4-16 s).
- Tạo giọng tốn ít VRAM hơn (chỉ tính logits ở đoạn cần đọc); model nhận dạng được gỡ khỏi GPU khi phải nhường chỗ cho TTS.
- Hết đơ giao diện: dò phần cứng, dựng thanh nghe thử, tải MP3 từng dòng đều chạy nền; kho giọng không dựng lại danh sách mỗi lần chuyển tab.
- Ghép audio / cross-fade nhanh hơn nhiều lần với kịch bản dài.
- Gói cài nhẹ bớt: bỏ header C++ của torch, ~440 model transformers không dùng, onnxruntime; build nhanh hơn.

### Khác

- Bổ sung bản dịch còn thiếu cho 7 ngôn ngữ; launcher Windows chạy được trong thư mục có ký tự Unicode.

## v2.0.0 - duckmartians

### Dịch phụ đề (tab mới - gói Studio)

- **Dịch & biên tập SRT bằng LLM, khoá cứng theo cue**: LLM chỉ được đổi phần chữ; timing và số dòng bất biến. Cue nào model trả thiếu/rỗng thì giữ nguyên text gốc + cờ ⚠ (fail-per-cue, không fail cả job); mỗi chunk lỗi retry 1 lần.
- **Nhập nhiều định dạng**: `.srt`, `.vtt` (parser SRT đã chịu được dấu thập phân `.` và header WEBVTT), `.ass`/`.ssa` (đọc dòng `Format:` trong `[Events]` thay vì đếm dấu phẩy, xử lý centisecond + `\N` + khối `{\pos}`), `.sbv`, và `.txt` thuần (sinh mốc thời gian tạm 2.5s/dòng, UI báo rõ). Đuôi tệp chỉ dùng để đoán thứ tự thử - file SRT lưu nhầm `.txt` vẫn nhận đúng.
- **Bảng nhất quán (STORY ANCHORS)**: lượt 1 đọc toàn file (lấy mẫu đều nếu dài) chốt `{register, terms, address}`, lượt 2 nhét NGUYÊN bảng đó vào system prompt của MỌI chunk + 2 cue giáp ranh mỗi phía + 3 câu vừa dịch xong ở chunk trước. Bảng sửa được bằng bảng nhập liệu (không phải JSON thô), giữ nguyên khoá lạ do server trả về. Lượt 1 hỏng thì vẫn dịch tiếp, chỉ mất nhất quán.
- **Tuỳ chọn dừng sau bước lập bảng** để user duyệt trước khi tốn thời gian dịch cả file; không tick thì chạy liền mạch 2 lượt như cũ. Nút Chạy/Dừng gộp làm một.
- **Chế độ Biên tập không dùng bảng nhất quán**: giấu nút bảng + ô tick, và chặn ở worker - chạy Dịch trước rồi đổi sang Biên tập thì bảng cũ KHÔNG lọt vào prompt.
- **Tối ưu dữ liệu trước khi dịch**: gộp dòng bị ngắt giữa câu (khoảng lặng < ngưỡng **và** dòng trước chưa có dấu kết câu **và** gộp xong vẫn trong trần ký tự/thời lượng), rồi tách dòng vượt trần tại dấu kết câu → dấu phẩy → khoảng trắng, chia thời gian theo tỉ lệ ký tự. CJK nối không chèn dấu cách. Có bảng xem trước sống trong hộp thoại.
- **Xuất SRT / VTT / TXT**, tự thêm đuôi nếu user gõ thiếu.
- **Prompt hệ thống nằm ở server** (KV `srt_prompts`, kênh `rc` của `/login` + `/check_license`), không hardcode trong client; chỉ tài khoản gói Studio nạp được. Nút Chạy gác 2 lớp license (UI + worker).

### LLM (Quản lý Model)

- **Bốn nhà cung cấp**: 9Router (openai/anthropic/gemini, parse SSE phòng thủ, retry 429 backoff luỹ tiến ×4, 5xx retry 1 lần, 401/403 fail-fast), Claude CLI (prompt qua stdin né trần ~32KB CreateProcessW), Antigravity `agy`, và Codex CLI.
- **agy không cần PTY**: bản 1.1.x đã trả đủ output trên pipe thường và có `--output-format json` - bỏ hẳn pseudo-TTY + marker tự chế. Danh sách model lấy từ `agy models` (tách `id<TAB>Tên hiển thị`, dùng id cho `--model`).
- **Codex chạy headless bằng `codex exec`**: prompt qua stdin, `-o` ghi ra đúng câu trả lời cuối, sandbox read-only trong thư mục tạm.
- **stdin phải đóng khi spawn agy** - để pipe mở thì agy chờ vô hạn tới khi watchdog giết.
- Dialog **Hướng dẫn** cài đặt cho từng CLI (lệnh lấy từ tài liệu chính thức); nút **Làm mới** quét lại provider + hỏi Claude CLI tự khai model, cache qua restart.
- Dropdown model không bao giờ để trống: có danh sách thì chọn sẵn mục đầu và lưu lại, chưa có thì hiện dòng "- Chọn model -".

### Webhook

- Thêm ô **IP** (`WebhookServer.start(host=...)`, mặc định `127.0.0.1`), ô **URL** đầy đủ dạng chỉ-đọc + nút **Sao chép**. URL xem trước theo đúng IP + cổng đang đặt (trước hardcode `127.0.0.1`).
- **Khoá IP + Cổng khi server đang chạy** - trước đây spinbox vẫn xoay được nên URL hiện cổng khác cổng đang lắng nghe.
- **Tick "Tự động khởi động" chạy server ngay** thay vì phải mở lại app.
- **Autostart không còn trượt khi license về chậm**: cờ chỉ bị tiêu thụ khi thật sự khởi động, và cửa sổ chính gọi lại `try_autostart()` sau khi biết chắc tình trạng license (trước là hẹn giờ cứng 800ms).

### Sao chép giọng nói (Voice Clone)

- **Khung "Chọn lọc đoạn mẫu" mới**: hiển thị sóng âm của file mẫu, kéo khung chọn trực tiếp đoạn dùng để sao chép giọng (3-30 giây), có nút nghe thử đúng đoạn đang chọn - thay thế hoàn toàn cơ chế cắt tự động cũ.
- **Tự hít vào khoảng lặng**: thả tay kéo mép khung, mép tự khớp vào điểm im lặng gần nhất để không cắt giữa từ.
- **File dài/nặng xử lý êm**: file quá 5 phút hoặc 50 MB tự lấy 30 giây đầu làm mẫu (không từ chối), kèm thông báo rõ ràng.
- **Chống lệch văn bản mẫu**: đổi đoạn chọn hoặc đổi file sẽ tự xóa văn bản mẫu cũ - tránh transcript không khớp âm thanh làm hỏng chất lượng giọng.
- Gọn giao diện: "Cài đặt nâng cao" và "Tinh chỉnh âm thanh" mở luân phiên (mở khung này tự đóng khung kia).

### Giao diện

- **Sidebar dọc mới**: 6 tab chức năng chuyển từ tab bar ngang ra thanh bên trái, tên rút gọn (Sao chép giọng / Đọc văn bản / Hội thoại nhóm / Tách phụ đề / Dịch phụ đề / Quản lý Model), nằm trên mục Webhook. Sidebar 180px, nhãn vừa 1 dòng ở cả 9 ngôn ngữ. Thêm nút **Log Chi Tiết** vào thẳng tab Log trong Cài đặt.
- **Quản lý Model làm lại**: mỗi model 1 hàng (TTS + 5 bản nhận dạng) kèm dung lượng, trạng thái đã tải, nút tải riêng và nhãn "Khuyến nghị" (TTS + Turbo); toàn tab có vùng cuộn - cửa sổ thấp không còn ép vỡ bố cục. Bỏ tên model khỏi nhãn (Turbo / Tiny / Base / Small / Large v3) cho khớp dropdown bên tab Tách phụ đề.
- **Nút Mẫu thẻ biểu cảm** (tab Đọc văn bản + Hội thoại nhóm): bảng tra 13 thẻ ngay trong app thay vì chỉ nằm trong README, mỗi dòng có nút Chèn bỏ thẻ vào đúng vị trí con trỏ (tự thêm dấu cách khi cần, không nhân đôi).
- **Sửa danh sách giọng cao thấp so le**: `QLabel` bật word-wrap khiến chiều cao gợi ý phụ thuộc độ dài mô tả (đo được 34 / 48 / 61px trên cùng một danh sách) - tắt word-wrap và chốt cứng 48px mỗi hàng.
- **Popup combo giữ được icon**: `SearchableComboBox` dựng `QListWidgetItem` mới nên rơi mất icon - cả danh sách model trông giống hệt nhau, không phân biệt được 9Router / Claude CLI / Antigravity / Codex.
- Khung **Xuất file** chuyển xuống dưới **Hàng chờ tạo** cho đúng trình tự làm việc; nút *Phát âm* đổi thành **Chỉnh phát âm**; nút mở rộng ô văn bản dời về sát nhãn; nhãn "Khi nhàn rỗi" đổi thành **"Tự giải phóng bộ nhớ GPU sau: N phút không dùng"**; địa chỉ gateway + API key của 9Router gộp về một hàng hai cột.
- **Dropdown không còn bị cuộn chuột đổi giá trị** khi lăn qua (`NoWheelValueFilter` chuyển sự kiện cho vùng cuộn gần nhất).

### Nhận dạng & Tách phụ đề

- **Chuyển engine sang faster-whisper (CTranslate2)**: nhanh ~4x, VRAM giảm ~nửa (Turbo ~2.5GB), CPU chạy int8. Model CT2 là subfolder `ct2-whisper-*` của repo license, tải on-demand - gói tải đầu giảm ~4.9GB → ~3.3GB.
- **Dựng dòng phụ đề từ word timestamps**: ngắt tại nghỉ hơi thật / hết câu / hết mệnh đề khi gần trần / trần ký tự / trần giây; khử dòng lặp ảo giác; kẹp từ bị kéo dãn. Đo trên ghi âm 41 phút: cơ chế cũ cho dòng tệ nhất 104s/1.299 ký tự, cơ chế mới 0 dòng vượt trần.
- **3 tham số gộp/tách tự chỉnh** (ký tự tối đa / giây tối đa / ngưỡng nghỉ): đổi là bảng dựng lại ngay từ raw đã lưu temp, không cần nhận dạng lại; bảng có chỉnh sửa tay thì hỏi trước khi dựng đè.
- Fix VAD bị kéo lên CUDA sau chu kỳ offload VRAM (streaming mất VAD ngầm); nút AI gợi ý (tab Clone) vào chung mutex + swap VRAM với tab Tách phụ đề.

### Đọc văn bản / Hội thoại nhóm

- **Kiểu tách câu mới "Gộp thông minh (≤N ký tự)"**: tách bằng bộ Tự động rồi gộp câu tới trần N, luôn ngắt tại điểm kết câu; câu đơn quá dài cắt tại dấu mệnh đề/khoảng trắng; tôn trọng ranh giới đoạn văn. Mặc định 500 ký tự ≈ 29s (đo thật: model đọc chính xác 100% tới ~1.800 ký tự; 500 giữ mỗi dòng dưới ngưỡng 30s không bị cross-fade nội bộ).

### Tinh chỉnh âm thanh

- **Fix "Cân đều âm lượng"**: normalize theo RMS loudness (−20 dBFS) thay vì peak −2 dBFS - hết "câu to câu nhỏ" khi bật (peak normalize làm độ to trôi theo crest factor); câu gần im lặng không còn bị khuếch thành tiếng ồn; chốt trần đỉnh −1dB chống clip. Webhook đồng bộ cùng chuẩn.

### Hiệu năng

- **Audio đã tạo + raw nhận dạng lưu temp thay vì RAM**: mỗi câu tạo xong ghi `.npy` ra `voice_studio/temp/rowaudio` (tiết kiệm ~165MB/giờ audio), nghe thử/xuất file load lại đúng lúc cần; temp phiên trước tự dọn khi mở app.
- **Sửa rò VRAM ở đường webhook**: worker xong không được dọn nên model bị giữ tham chiếu - VRAM leo thang qua mỗi chu kỳ unload/reload (đo: 1947 → 3886 → 5825 MB). Sau fix, sàn VRAM đứng yên ở 1947 MB qua 3 chu kỳ. Teardown per-worker (`model = None`, graveyard + `deleteLater`), đánh dấu model-used ở cả lúc tạo worker lẫn lúc worker xong, thêm QTimer 60s phát hiện worker treo > 300s, và `/api/health` trả thêm `vram: {alloc_mb, reserved_mb}`.

### Tài liệu

- README (9 ngôn ngữ): mọi mục **Cách sử dụng** và **Mẹo dùng nâng cao** gói trong khối gập/mở - xem mục nào mở mục đấy. Thêm **Phần 6 - Dịch phụ đề**. Bước tạo lối tắt ra desktop nâng từ ghi chú lên thành bước có số. Bỏ tên model khỏi chữ người dùng đọc.
- `docs/WEBHOOK_INTEGRATION` (vi + en): sửa hai khẳng định đã thành sai - server không còn "chỉ bind 127.0.0.1" (đổi IP được, kèm cảnh báo API key đi qua HTTP trần), và **thứ tự hoàn thành không đảm bảo FIFO** khi có nhiều job cùng lúc → client phải ghép kết quả theo `task_id`.
