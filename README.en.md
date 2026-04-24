<p align="right"><a href="./README.md">🇻🇳 Tiếng Việt</a> · 🇬🇧 English</p>

<h1 align="center">G-Labs Voice Studio</h1>
<p align="center">AI voice studio for creators</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G">
    <img alt="Download Windows" src="https://img.shields.io/badge/Download%20Windows-%F0%9F%92%BB-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  </a>
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta">
    <img alt="Download macOS" src="https://img.shields.io/badge/Download%20macOS-%F0%9F%8D%8E-000000?style=for-the-badge&logo=apple&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://duckmartians.info">
    <img alt="Homepage" src="https://img.shields.io/badge/Homepage-Visit-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio** is a desktop app for multilingual voice synthesis featuring voice cloning, attribute-based voice design, and speech-to-text. Dark-themed UI, models run locally on your machine — no audio or text is sent to the cloud once the model is downloaded.

<p align="center">
  <a href="https://duckmartians.info/g-labs">
    <img alt="G-Labs Voice Studio UI" width="900" src="https://github.com/user-attachments/assets/0fe19f01-4e8e-46c9-bb8b-80bd9e347130" />
  </a>
</p>

---

## Features

- **🔊 Voice Cloning** — provide a 5–10 second reference audio clip; the app generates a matching voice for any text.
- **🎛️ Voice Design / TTS** — describe a voice by attributes (gender, age, pitch, style, accent) with no reference audio needed.
- **📝 Speech-to-Text (ASR)** — transcribe audio/video files. Supports MP3, WAV, M4A, FLAC, MP4, MOV, and more.
- **🗂 Voice Library** — save any voice you've just generated under a name + short description, reuse it in both the Voice Cloning and Voice Design tabs. Supports **backup & restore** via portable `.vcp` files so you can share voices across machines.
- **✨ AI sample-text suggestion** — auto-transcribe the reference audio with Whisper so you don't have to type the whole thing from scratch (proofread before generating).
- **⬇ Per-row download** — every row in the script table has its own download button so you don't have to wait for the whole batch to export.
- **600+ languages supported** — recognize and synthesize over 600 languages (including Vietnamese, English, Chinese, Japanese, Korean, French, German, Spanish, and many minority languages).
- **Batch processing** — import `.txt` or `.srt` scripts, run batches, and export audio files preserving timestamps.
- **Fine-grained controls** — diffusion steps, guidance scale, playback speed, sentence gap.
- **Smart GPU compatibility check** — if your GPU is too old or driver mismatched, the app **auto-falls back to multi-core CPU** and tells you plainly, instead of crashing with a CUDA error.
- **Bilingual UI** — Vietnamese and English.

---

## 🆕 What's new in v1.0.2

- **Voice Library** — save, back up and share voices you've created.
- **AI sample-text suggestion** — Whisper transcribes the reference clip so you only need to proofread, not retype.
- **Pre-flight transcript check** — confirmation dialog before generating, to avoid the "voice says 'subscribe to our channel'" hallucination caused by mismatched transcripts.
- **Per-row download** — ⬇ button on each row of the script table.
- **Accurate GPU detection** — no more false "Supported" badge for old GPUs; auto-fallback to CPU when the GPU can't actually run the model.
- **Multi-core CPU optimization** — when running on CPU, the app configures PyTorch / BLAS thread counts to your true core count, significantly faster than the defaults.

---

## Installation

| Platform | File | Size |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.2-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.2-arm64.dmg` | ~2 GB |

### Windows (portable, no install needed)

1. Download `GLabsVoiceStudio-v1.0.2-win.zip`.
2. Extract to any folder (pick a drive with at least 10 GB free).
3. Open the extracted folder and run `GLabsVoiceStudio.exe` directly.

> Want a desktop shortcut? Right-click `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** Windows needs to scan the app and GPU files (an automatic security step that is slow on first run). From the second launch onward, the app opens quickly.

### 🍎 macOS Apple Silicon

1. Download **`GLabsVoiceStudio-v1.0.2-arm64.dmg`** from the official distribution.
2. Double-click the `.dmg` file to open it.
3. Drag the **G-Labs Voice Studio** icon into the **Applications** folder.
4. Open **Applications**, **right-click** on **G-Labs Voice Studio** → select **Open**.

> ⚠️ **First launch:** macOS may show *"App from an unidentified developer"*. Right-click the app → **Open** → click **Open** in the dialog. Only needs to be done once.

> 📁 **Output files** (audio, scripts) are saved to `~/Documents/G-Labs Voice Studio/output/` by default.

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** macOS performs a full security check on the app during first launch. From the second launch onward, it opens quickly.

#### 🍎 Fixing *"App is damaged"* on macOS

When you download a `.dmg` from the internet, macOS automatically attaches a **quarantine flag** to the file. If the app isn't Apple-notarized, Gatekeeper will block it and may report *"The app is damaged and can't be opened"*.

**Method 1: Right-click → Open** *(recommended)*

1. Open **Applications**.
2. **Right-click** on *G-Labs Voice Studio* → **Open**.
3. Click **Open** again in the warning dialog.

**Method 2: Use Terminal** (if method 1 still shows the error)

Open **Terminal** (Launchpad → Other → Terminal), paste the following command and press Enter:

```bash
xattr -cr "/Applications/G-Labs Voice Studio.app"
```

This command clears all extended attributes (including the quarantine flag) from the app bundle. After running it, open the app normally. You only need to do this **once** per downloaded version.

**Method 3: System Settings → Privacy & Security**

1. Try to open the app normally (it will be blocked).
2. Open **System Settings** → **Privacy & Security**.
3. Scroll to the bottom, find *"G-Labs Voice Studio was blocked…"* → click **Open Anyway**.
4. Confirm with Touch ID or admin password.

---

## Getting Started

### Step 1 — Sign in and download the model (one-time setup)

1. **Open Settings** — click the ⚙️ gear icon in the left sidebar.
2. **Sign in** — on the *License* tab, click **"Sign in with Google"**. Your browser opens so you can pick your Google account.
3. **Download the AI model** — switch to the *Environment* tab (or let the app prompt you), then click **"Download model"**. First-time download is a few GB; wait for it to finish.
4. Close Settings.

### Step 2 — Voice Cloning 🔊

Clone a voice from a sample recording.

1. Open the **Voice Cloning** tab.
2. In the *Reference audio* field, click **"Browse..."** and select a sample clip (5–10 seconds, clear voice, minimal background noise).
3. **Required:** enter the *Reference text* — the exact transcript of the sample audio (full punctuation, correct spelling). A matching transcript is the key to a clean voice clone.
    > 💡 Click **"✨ AI suggest"** next to the sample text box to let Whisper transcribe it for you — you'll still want to proofread because Whisper can miss a word or two.
4. Paste or type the text to be spoken into the *Input text* box. You can click **"📂 Import text file"** to load directly from `.txt` or `.srt`.
5. Click **"📋 Add to table"** — the app splits your text into individual sentences and fills the table below.
6. (Optional) Open *Advanced settings* to tune diffusion steps, guidance scale, speech speed, and sentence gap.
7. Click **"▶ Start"** — a confirmation dialog asks you to verify the sample transcript one last time; confirm to run.
8. When done, click **"💾 Export audio"** to merge everything into a single file, or use the **⬇** button on a row to download that single line.

### Step 2b — Using the Voice Library 🗂 *(optional, shared with Voice Design tab)*

A voice you like can be saved and reused in seconds next time — no file pick, no re-encoding.

1. After generating a voice you're happy with, open the **Voice Library** panel on the left.
2. Under **"Save current voice to library"**: click **"💾 Save"**, enter a name (e.g. "Deep Male MC") and a short description (e.g. "Warm middle-aged male — news voice-over") → **Save**.
3. Next time, pick the voice from the **"Load voice from library"** dropdown — no reference file or transcript needed, generation starts immediately.
4. The **⋯** menu offers **Backup / Restore**:
    - **Backup selected voice / entire library** — export as `.vcp` file(s) for backup or sharing.
    - **Restore from `.vcp`** — import multiple files at once; existing presets are never overwritten.
5. A voice saved on the **Voice Design** tab is instantly visible on the **Voice Cloning** tab (and vice versa) — no restart required.

### Step 3 — Voice Design (TTS) 🎛️

Create a new voice from attribute descriptions — no sample needed.

1. Open the **Voice Design** tab.
2. Pick voice attributes: *Gender*, *Age*, *Pitch*, *Style*, *Accent*.
    > 💡 Want to reuse a saved voice from the **Voice Library**? Pick it directly from the "Load voice from library" dropdown — the app skips the first-row warmup and **batches every sentence from row 1**, noticeably faster.
3. Paste the target text into *Input text*, or use **"📂 Import text file"** to load from `.txt` / `.srt`.
4. Click **"📋 Add to table"** to split into sentences.
5. (Optional) Adjust *Advanced settings*.
6. Click **"▶ Start"**.
7. Click **"💾 Export audio"** to save the result, or use the **⬇** button on a row to download that line alone.
8. If you like the generated voice, click **"💾 Save"** in the *Voice Library* panel to reuse it later.

### Step 4 — Speech-to-Text 📝

Transcribe speech from existing audio/video files.

1. Open the **Speech-to-Text** tab.
2. Click **"Choose file..."** and pick an audio/video file (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. Click **"▶ Start"** — the app analyses and chunks the speech, then transcribes each segment.
4. Results appear in a table with per-sentence timestamps. You can edit them directly.
5. Click **"💾 Export"** to save as `.txt` (plain text) or `.srt` (with timestamps, suitable for subtitles).

---

## System Requirements

### Windows x64
- Windows 10 / 11 (64-bit)
- **NVIDIA GPU, RTX 20-series or newer** (compute capability ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). Older GPUs such as GTX 10-series (GTX 1060/1070/1080) **can't run the accelerated attention kernels**; the app detects this and auto-falls-back to CPU.
- NVIDIA driver with CUDA 12.8 support.
- 8 GB RAM (16 GB recommended for batch workloads or CPU mode).
- 10 GB free disk space (including the model).

### macOS
- macOS 12 (Monterey) or newer
- **Apple Silicon** (M1/M2/M3/M4/...) — uses Metal Performance Shaders (MPS)
- 8 GB RAM
- 10 GB free disk space

> Machines without a compatible GPU **automatically run on multi-core CPU** (the app tunes PyTorch / BLAS thread counts to your physical core count). That's roughly 5-10× slower than GPU but still usable for short voice-over jobs.

---

© 2026 Duck Martians AI Labs. All rights reserved.
