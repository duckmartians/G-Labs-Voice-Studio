<h1 align="center">G-Labs Voice Studio</h1>

<p align="center"><b>在你自己电脑上运行的 AI 语音桌面应用--用几秒音频克隆声音、以 600 多种语言朗读文本、制作多角色对话、把音视频转写成字幕，并用 AI 翻译字幕。</b></p>

<p align="center">
  <a href="README.md">Tiếng Việt</a> ·
  <a href="README.en.md">English</a> ·
  <a href="README.pt-BR.md">Português</a> ·
  <a href="README.tr.md">Türkçe</a> ·
  <b>简体中文</b> ·
  <a href="README.hi.md">हिन्दी</a> ·
  <a href="README.bn.md">বাংলা</a> ·
  <a href="README.ur.md">اردو</a> ·
  <a href="README.ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G"><img alt="下载 Windows 版" src="https://img.shields.io/badge/%E4%B8%8B%E8%BD%BD-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta"><img alt="下载 macOS 版（Apple Silicon）" src="https://img.shields.io/badge/%E4%B8%8B%E8%BD%BD-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>&nbsp;
  <a href="https://www.youtube.com/watch?v=3J8GdUEfFlI"><img alt="YouTube 教程视频" src="https://img.shields.io/badge/YouTube-%E6%95%99%E7%A8%8B%E8%A7%86%E9%A2%91-FF0000?style=for-the-badge&logo=youtube&logoColor=white"></a>
</p>

---

## 安装

### 第 1 步--为你的电脑选择正确的版本

安装包通过官方 Google Drive 文件夹发布：

| 你的电脑 | Google Drive | 说明 |
|---|---|---|
| 🪟 **Windows 10/11（64 位）** | [Windows](https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G) | `.zip` 压缩包--解压即用，无需安装 |
| 🍎 **Apple 芯片 Mac（M1/M2/M3/M4…）** | [macOS Apple Silicon](https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta) | `.dmg`，需要 macOS 12 或更高版本 |

> **不支持 Intel 芯片的 Mac**--只有 Apple Silicon 版本。不确定你的 Mac 是什么芯片？点击  菜单 →**关于本机**：**芯片**一栏显示 "Apple M…" 即可使用；**处理器**一栏显示 "Intel…" 则无法使用。

### 第 2 步--安装

<details open>
<summary><b>🪟 Windows</b></summary>

1. 下载 Windows 版 `.zip`（例如 `G-Labs-Voice-Studio-v2.0.3-win.zip`），**解压**到任意文件夹--磁盘至少需要 10 GB 可用空间（之后下载的 AI 模型会占用数 GB）。
2. 打开解压后的文件夹，运行 **`G-Labs-Voice-Studio.exe`**（exe 与它需要的文件放在这个文件夹里--请不要移动或删除它们）。
3. 如果出现 **"Windows 已保护你的电脑"**（SmartScreen）：点击 **更多信息** → **仍要运行**。*（应用没有 Microsoft 证书签名，所以 Windows 会提示--这不是病毒。）*
4. **创建快捷方式：**右键 `G-Labs-Voice-Studio.exe` → **发送到** → **桌面快捷方式**，以后可快速打开。

> ⏳ **首次启动可能需要 30-60 秒**（启动画面会停住一段时间），因为 Windows 正在对应用和显卡库进行安全扫描。请耐心等待，不要关闭--之后的启动会更快。

</details>

<details open>
<summary><b>🍎 macOS</b></summary>

1. 打开下载的 **`.dmg`**，然后**把 G-Labs Voice Studio 图标拖到"应用程序"文件夹**。
2. 在 **应用程序** 中**右键**（或按住 Control 点按）**G-Labs Voice Studio** → **打开** → 在确认对话框中再次点击 **打开**。*（应用未经 Apple 公证，所以**第一次**需要这样打开；之后可正常打开。）*
3. 如果 macOS 提示应用**"已损坏 / 无法打开"**，或者没有"打开"按钮，请打开 **终端**，粘贴以下命令并回车：
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"
   ```
   然后重新打开应用。另一种方法：**系统设置 → 隐私与安全性**，滚动到底部，在提示 G-Labs Voice Studio 被阻止的那一行旁点击 **仍要打开**。

> ⏳ **首次启动可能需要 30-60 秒**，因为 macOS 会对整个应用进行安全检查。之后的启动会更快。

</details>

### 第 3 步--登录并选择套餐

**你需要用 Google 登录**（设置 ⚙️ → **授权账号** 选项卡 → **用 Google 登录**），以便应用验证你的许可。一个账号**同一时间只能在一台电脑上**运行--在其他设备登录会结束旧设备上的会话。

| 套餐 | 价格 | 包含 |
|---|---|---|
| **试用** | 免费 | 每次生成的行数有限（默认 1 行）--足以在购买前确认你的电脑运行流畅 |
| **Studio 套餐** | 1 个月 $5 · 6 个月 $25 · 1 年 $50（VietQR 付款为 100,000đ / 500,000đ / 1,000,000đ） | 不限行数、**渲染队列**、**翻译字幕** 选项卡、**Webhook API** |

- 在应用内购买（设置 → **授权账号**），支持 **VietQR 银行转账**、**PayPal**（国际卡）或 **USDT**。套餐按时长计费，不会自动续费，并在你登录的 Google 账号上激活。
- Studio 套餐仅属于 Voice Studio，与 G-Labs Studio 的 Plus/Max **相互独立**。
- 付款后 **24 小时**内可申请退款--见 [退款政策](https://duckspace.net/refunds.html#en)。请先运行免费试用，确认你的电脑能流畅运行。

---

## 首次运行

1. **打开应用，在欢迎界面选择界面语言**（之后可在设置中更改）。
2. **用 Google 登录**--设置 ⚙️ → **授权账号** → **用 Google 登录**。
3. **下载语音模型**--打开 **模型管理** 选项卡（或按应用提示操作），下载 AI 语音模型（数 GB，只需一次）。语音识别模型会在你第一次使用时单独下载。
4. **打开 文字转语音 选项卡**，选择**输出语言**，并从声音库中挑选一个声音（内置 30 个声音）。
5. 粘贴文本 → **添加到表格** → **开始运行**。逐行试听，然后点击 **导出音频** 保存文件（默认附带 `.srt` 字幕）。

---

## 功能

<p align="center">
  <img alt="G-Labs Voice Studio 界面" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
</p>

- **在你的电脑上运行**--模型下载后，语音生成和转写都在本地运行（NVIDIA GPU、Apple Metal 或 CPU）；你的音频和文本不会发送到服务器。只有翻译选项卡会把字幕文本发送给你选择的 AI 服务商。
- **声音克隆**--用一段 5-10 秒的样本，以完全相同的声音朗读任何文本。
- **随机声音**--按性别、年龄和音高（英语还可选口音）描述一个新声音；无需样本文件，喜欢的声音可保存到声音库。
- **600 多种输出语言**--越南语、英语、中文、日语、韩语、法语、德语、西班牙语等。
- **多角色对话**--`<名字>: 台词` 格式的剧本，每个角色有自己的声音和语速。
- **换声与配音**--载入视频，识别语音或导入已翻译的字幕，在原来的时间段内给每一行重新配音；可导出音频或替换了声音的视频，并保留原有音乐。
- **字幕提取**--转写 MP3、WAV、M4A、FLAC、MP4、MOV…；导出带逐词时间轴的 TXT 或 SRT。
- **AI 字幕翻译** *（Studio 套餐）*--翻译或校对 `.srt`、`.vtt`、`.ass`、`.sbv`、`.txt`；时间轴和行数完全不变。
- **声音库**--独立页面：30 个内置声音，可保存自己的声音，输入一句话即可试听任意声音，⭐ 置顶收藏，备份/恢复为 `.vcp` 文件。
- **音频微调**--6 种处理模式、音量均衡、13 个表情标签，以及能记住 `100%`、`25°C`、`m²` 等读法的发音词典。
- **灵活导出**--WAV 或 MP3，合并为一个文件或每句一个文件，附带 `.srt`；用 ⬇ 按钮单独下载某一行。
- **渲染队列** *（Studio 套餐）*--把多个剧本排入队列；应用逐个运行并保存文件。
- **Webhook API** *（Studio 套餐）*--本地 REST 服务器，供 n8n、Make、Zapier、Python/cURL 或 AI 智能体调用。
- **自动适配硬件**--显卡不兼容时自动切换到 CPU 并明确提示；空闲时自动释放 GPU 显存。
- **9 种界面语言**--Tiếng Việt、English、Português、Türkçe、简体中文、हिन्दी、বাংলা、اردو、Русский。

---

## 页面

页面位于左侧边栏，分为 **生成配音**（文字转语音、多人对话、换声）· **字幕**（提取字幕、翻译字幕）· **声音**（声音克隆、声音库）· **系统**（模型管理、Webhook API、队列）。语音页面的流程相同：在工具栏选择**朗读语言** → 把文本粘贴到 **原文**，或 **导入文件**（`.txt`、`.srt`）→ **添加到表格**（应用按你选择的方式拆分句子，默认 **智能合并**）→ **生成** → 试听并修改单独的行 → **导出**。

### 🔊 声音克隆

![声音克隆](docs/screenshots/en/clone.webp)

点击 **选择...** 载入样本音频，然后在波形上拖动高亮框选出 3-30 秒的片段（松开后边缘会吸附到静音处），或点击 **自动选最佳片段**。

- **样本决定质量：**克隆不仅复制声音，也会复制样本里的噪音、回声和音乐。请使用最干净的 5-15 秒；如果人声后面有音乐，先点击 **去除背景音乐**。
- **文本必须与样本逐字一致**（包括标点和拼写）。**AI 建议** 可帮你转写，但请边听边对照，改正错误：文本错了，声音也会错。

输入一句测试文本，点击 **开始运行**，试听；然后在右侧面板给声音起名并点击 **保存到声音库**。

### 🎛️ 文字转语音

![文字转语音](docs/screenshots/en/tts.webp)

在右侧的 **声音** 选项卡中，从声音库选择一个 **已有声音**，或选择 **随机声音**，按*性别、年龄和音调*创建新声音（英语口音在 **设置 → 常规设置** 中）。单独重新生成某一行时会保持同一个声音；喜欢的声音点击 **保存** 存入声音库。

点击某一行可以修改文本、在它前面添加停顿（**句前停顿**），或只重新生成这一行（**重新生成**）；下方的时间线会播放整段内容，拖动播放头即可跳转。**发音词典** 教应用如何读 `25°C` 或 `100%` 这类内容（对之后所有剧本都生效）；**表情标签** 会把 `[laughter]`、`[sigh]`… 插入文本。朗读速度和 6 种声音风格在 **设置** 选项卡中。

### 💬 多人对话

![多人对话](docs/screenshots/en/dialogue.webp)

编写多角色剧本--适合播客、有声剧和访谈：

```
<主持人>: 欢迎各位。
<Mai>: 你好，很高兴来到节目。
<Minh>: 我也是--今天我们聊什么？
```

把角色名放在行首的 `< >` 中（`:` 可省略，名字不区分大小写）。点击 **示例对话** 查看示例，然后点击 **解析对话**--右侧的 **声音** 选项卡会为每个角色显示一张卡片，可从声音库指定声音并设置独立的 **语速**（0.5× → 2×）。时间线上每个声音占一行；把某句拖到另一行即可更换朗读它的角色。

### 🔁 换声

![换声](docs/screenshots/en/voicechange.webp)

载入视频或音频文件并点击 **识别语音**，或用 **送到换声** 按钮从提取字幕 / 翻译字幕页面接收字幕（源视频会一起带过来）。每条字幕都会变成一行，固定在原来的时间位置；选好新声音和朗读语言后点击 **生成**--**对齐字幕** 会让每一行保持在自己的时间段内。

监听区可对比 **原声 / 新配音 / 新配音 + 背景**（背景音乐通过 Demucs 从旧人声中分离，首次约需下载 80 MB）。共有 6 种导出方式：仅新配音、新配音 + 原音乐、新配音 + 轻声原声--可导出为音频，或直接写入视频。

> **把视频配音成另一种语言：**提取字幕 → **送到翻译字幕** → 翻译 → **送到换声** → 选择声音 + 朗读语言 → 生成 → 导出视频。

### 📝 提取字幕

![提取字幕](docs/screenshots/en/asr.webp)

选择音视频文件（MP3、WAV、M4A、FLAC、MP4、MOV…）、说话语言和识别模型（Tiny → Large v3，每个都标明所需显存），然后运行。字幕行根据逐词时间戳构建，并在真实停顿 / 句末 / 字符上限处断开；修改*最大字符数、最大秒数、停顿阈值*后表格立即更新，无需重新转写。可直接在表格中编辑，并导出 `.txt` 或 `.srt`。

### 🌐 翻译字幕 *（Studio 套餐）*

![翻译字幕 （Studio 套餐）](docs/screenshots/en/srt.webp)

把字幕翻译成其他语言，或校对拼写和断行--**只改文字，时间轴和行数保持不变**。

1. 在 **模型管理 → LLM** 中一次性设置：选择 **9Router**（运行在你电脑上的网关--填写地址和 API 密钥）、**Claude CLI**、**Antigravity**（`agy`）或 **Codex CLI**（安装并登录）。每行都有 **指南** 按钮列出安装命令；安装后点击 **刷新列表**，应用会检测并列出其模型。
2. 用 **导入文件** 打开 `.srt`、`.vtt`、`.ass`、`.sbv`、`.txt`--或使用 **从提取字幕导入**。`.txt` 没有时间轴，应用会分配临时时间并提示你。
3. 建议：**整理文本** 会把在句中被切断的片段重新拼接（常见于视频剪辑软件导出的字幕），应用前会显示类似 *"120 行 → 68 行"* 的预览。
4. 选择 **翻译**、**润色** 或 **翻译 + 润色**，选择目标语言和模型，然后点击 **开始运行**。
5. **一致性表** 为整个文件统一人名、术语和称谓，并随每一段一起发送；你可以编辑它，也可以选择在翻译前暂停审阅。
6. 检查 **结果** 列（AI 遗漏的行会标记 ⚠ 并保留原文），选择 **SRT / VTT / TXT** 并点击 **导出结果**。

### 🗂️ 声音库

![声音库](docs/screenshots/en/library.webp)

你的所有声音集中在一处：按名称 / 描述 / 标签搜索，用 **全部 / 我的 / 内置 / 收藏** 筛选，点击 ⭐ 置顶。选中一个声音可查看详情、播放原始样本（内置声音），或输入一句话后点击 **生成并播放** 试听；**在文本转语音中使用** 会跳转到文字转语音页面并选中该声音。导出 / 导入 `.vcp` 文件即可备份声音或转移到另一台电脑。

### 📚 模型管理

![模型管理](docs/screenshots/en/model.webp)

分为三个部分：**AI 模型**、**字幕 LLM** 和 **硬件**（选择 GPU / CPU，空闲时释放显存）。在 AI 模型下，每个模型一行，显示大小和状态：AI 语音模型以及各识别模型（Tiny、Base、Small、Turbo、Large v3）。只下载你需要的，并可更改**模型文件夹**（例如移到 D 盘以节省 C 盘空间--把旧模型文件夹复制过去，或让应用重新下载）。翻译用的 **LLM** 服务商和 **自动释放显存** 计时器也在这里设置。

### 🗒 渲染队列 *（Studio 套餐）*

不必生成一个剧本再手动导出--点击 **添加到队列**，把当前剧本 + 声音 + 设置保存为一个任务，**拥有独立名称和输出文件夹**。点击 **运行队列**，应用会逐个处理并保存文件。每个任务显示 `X/N 句`，让你看出哪个任务因出错缺句；**重新加载** 可把任务载回其选项卡进行修改（失败的行标记 ❌）。关闭并重新打开应用后队列依然保留。

### 🔗 Webhook API *（Studio 套餐）*

![Webhook API （Studio 套餐）](docs/screenshots/en/webhook.webp)

本地 REST 服务器，让 n8n、Make、Zapier、Python/cURL 或 AI 智能体自动生成语音。默认 `127.0.0.1:8766`（仅本机），带 API 密钥、带复制按钮的完整 **URL** 框、随应用自动启动选项和实时请求日志。把 IP 改为 `0.0.0.0` / 局域网 IP 可让其他设备调用--此时 API 密钥通过未加密的 HTTP 传输。完整接口说明：[`docs/WEBHOOK_INTEGRATION.en.md`](docs/WEBHOOK_INTEGRATION.en.md)。

---

## 使用技巧

<details>
<summary><b>音频母带处理--6 种处理模式</b></summary>

在三个语音选项卡的 **音频母带处理** 区域（在一个选项卡中修改，其他选项卡会同步）：

- 📻 **广播** *（默认）*--广播/播客标准，温暖、压缩紧凑。
- 🎬 **电影**--宽广混响，轻度压缩。
- 🎙️ **播客**--近距离麦克风，强压缩，无混响。
- ☀️ **温暖**--增强中低频，温暖感。
- ✨ **明亮**--高频清晰，通透。
- 🔇 **原始**--保留模型原始输出。

**统一各句音量** 按人耳感知响度（RMS）均衡，不再忽大忽小。若想要模型未处理的输出，请选择 **原始** 并取消勾选此项。

</details>

<details>
<summary><b>表情标签</b></summary>

在文本中输入标签（保留方括号；可单独放置或放在句中，例如 `太好笑了 [laughter] 我忍不住了。`）--声音会发出对应的声音，而不是把单词读出来。不必背：**表情标签** 按钮可查阅并插入。

| 标签 | 声音 |
|---|---|
| `[laughter]` | 笑声 |
| `[sigh]` | 叹气 |
| `[confirmation-en]` | 赞同--"mm-hmm" |
| `[question-en]` · `[question-ah]` · `[question-oh]` · `[question-ei]` · `[question-yi]` | 疑问语调 |
| `[surprise-ah]` · `[surprise-oh]` · `[surprise-wa]` · `[surprise-yo]` | 惊讶 |
| `[dissatisfaction-hnn]` | 不满--"hnn" |

表现强度因语言和声音而异--建议先在一句短句上试试。

</details>

<details>
<summary><b>发音词典</b></summary>

文本中有 `%`、`$`、`°C`、`m²`、品牌名…？生成前点击 **调整发音**：应用会询问每个符号/词的读法，你只需输入一次（例如 `%` → `百分之`），应用会按输出语言记住。

</details>

<details>
<summary><b>导出时的语速与字幕</b></summary>

- **朗读速度** 位于 *高级设置*；播放器上的 **速度** 控件可加快/放慢试听，导出的文件保持该速度且不改变音高。
- **同时导出字幕** 会在音频旁写入同名 `.srt`，时间轴取自调整语速后每句的实际时长。
- **语音适配字幕时间轴**：当剧本来自 `.srt` 时，每行会加速（最多 1.8×）以适配其字幕时段--绝不放慢。

</details>

<details>
<summary><b>自动释放内存</b></summary>

应用空闲一段时间（默认 5 分钟）后，AI 模型会从显存/内存中卸载以减轻电脑负担；下次操作时自动重新加载。可在 **模型管理 → 自动释放显存** 中修改时间或关闭。

</details>

---

## 系统要求

|   | 最低 | 推荐 |
|---|---|---|
| **操作系统** | Windows 10（64 位）、Apple Silicon 上的 macOS 12 | Windows 11、macOS 13 或更高 |
| **Windows** | 支持 CUDA 的 NVIDIA 显卡，**RTX 2060** 或更高；8 GB 内存 | **RTX 3060（12 GB 显存）** 或更高；16 GB 内存 |
| **Mac** | Apple Silicon **M1** 或更新，**16 GB 内存** | M2 / M3 / M4，更大内存 |
| **磁盘** | 10 GB 可用空间（模型 + 缓存） | 20 GB 或以上，SSD |
| **网络** | 登录/许可验证和下载模型需要联网 | |

- **Windows：**需要支持 CUDA 的 NVIDIA 显卡，**RTX 2060** 或更新（compute capability ≥ 7.0），并安装支持 CUDA 12.8 的驱动；要流畅稳定地运行，请使用 **12 GB 显存的 RTX 3060** 或更高。GTX 10 系列等较旧显卡会被检测到并改用 CPU 运行--大约慢 5-10 倍，仅适合试用。
- **macOS：**需要 **Apple Silicon M1 或更新、16 GB 内存或以上**，使用 Metal 加速。

---

## 数据存放位置

| 内容 | Windows | macOS |
|---|---|---|
| 导出的音频（默认） | 解压应用所在文件夹内的 `output\` | `~/Documents/G-Labs Voice Studio/output` |
| 设置、登录会话 | `%APPDATA%\G-Labs Voice Studio` | `~/Library/Application Support/G-Labs Voice Studio` |
| 你的声音库 | `%APPDATA%\G-Labs Voice Studio\voice_studio\voices` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/voices` |
| AI 模型 | `%APPDATA%\G-Labs Voice Studio\voice_studio\model`（或你选择的文件夹） | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/model`（或你选择的文件夹） |
| 渲染队列 | `%APPDATA%\G-Labs Voice Studio\voice_studio\queue` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/queue` |

要把声音库迁移到另一台电脑，请使用声音库面板中的 **`.vcp` 备份/恢复**。

---

## 故障排除

**首次启动非常慢，启动画面不动**--Windows/macOS 正在进行首次安全扫描；请等待 30-60 秒，不要关闭。之后的启动会更快。

**Windows 停在"Windows 已保护你的电脑"**--点击 **更多信息 → 仍要运行**。应用没有 Microsoft 证书签名，不是病毒。

**macOS 提示应用已损坏 / 无法打开**--应用未经 Apple 公证。第一次请右键 → **打开**，或运行 `xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"`。

**提示已切换到 CPU 运行**--你的显卡不兼容（例如 GTX 10 系列）。所有功能照常可用，只是较慢；想要速度需要 NVIDIA RTX 20 系列或更新显卡，或 Apple Silicon Mac。

**每次只生成 1 行**--你正在使用试用版。购买 Studio 套餐即可不限行数。

**被登出，提示账号已在其他设备登录**--一个账号同一时间只能在一台电脑上运行；请在你要使用的电脑上重新登录。

**克隆的声音读错字 / 声音跑偏**--*样本文本* 必须与样本中的话完全一致；请选择清晰、噪音少的样本。

**特殊字符读错（`100%`、`25°C`…）**--在 **调整发音** 中添加读法。

**C 盘被模型占满**--在 **模型管理** 中更改模型文件夹，然后复制旧模型文件夹过去或让应用重新下载。

**翻译字幕 选项卡中没有可选模型**--按照 **指南** 按钮安装并登录一个 LLM 服务商（9Router、Claude CLI、Antigravity、Codex），然后点击 **刷新列表**。

**需要查看详细错误信息**--点击侧边栏中的 **详细日志**。

---

📖 [产品页面](https://duckspace.net/en/voice-studio/) · [使用指南](https://duckmartians.info/voice/guide/en/) · [更新日志](CHANGELOG.md) · [Discord](https://discord.gg/munMZEBMw5)

© 2026 Duck Martians AI Labs. 保留所有权利。
