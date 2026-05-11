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
  <a href="https://duckmartians.info/voice">
    <img alt="Homepage" src="https://img.shields.io/badge/Homepage-Visit-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio** is a desktop app for multilingual voice synthesis: clone voices from a short reference clip, design new voices by attributes, write multi-speaker dialogues, and transcribe speech to text. Dark-themed UI, models run locally on your machine — no audio or text leaves the device once the model is downloaded.

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="G-Labs Voice Studio UI" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
  </a>
</p>

---

## Features

- **🔊 Voice Cloning** — provide a 5–10 second reference clip; the app reads any text in that voice.
- **🎛️ Voice Design / TTS** — describe a voice by attributes (gender, age, pitch, style, accent) with no reference audio needed.
- **💬 Multi-Voice Dialogue** — write a multi-character script using the `<Name>: line` syntax and assign a library voice to each character.
- **📝 Speech-to-Text (ASR)** — transcribe audio/video files. Supports MP3, WAV, M4A, FLAC, MP4, MOV…
- **🗂 Voice Library + 30 factory voices** — the app ships with 30 ready-made voices (male/female, varied tones). You can also save your own. Star ⭐ a voice to pin it to the top, and **back up & restore** as portable `.vcp` files for sharing.
- **🎚 Speed control + speed-aware export** — change the preview speed under the waveform; the exported file plays back at exactly that speed (pitch preserved).
- **📄 Subtitle (SRT) export** — when exporting as a single merged file, the `.srt` is auto-generated alongside, ready for video editing.
- **🔤 Personal phonetic dictionary** — encounter `100%`, `25°C`, `m²`? Type the pronunciation once, the app remembers it for next time (per output language).
- **✨ AI sample-text suggestion** — Whisper auto-transcribes the reference clip so you don't have to retype it from scratch (still proofread before generating).
- **⬇ Per-row download** — every row in the script table has its own download button — no waiting for the full batch.
- **600+ languages supported** — speak more than 600 languages (Vietnamese, English, Chinese, Japanese, Korean, French, German, Spanish, and many minority languages).
- **Batch processing** — import `.txt` or `.srt` scripts, run batches, export audio preserving the timestamps.
- **Smart GPU compatibility check** — if your GPU can't run accelerated kernels, the app **auto-falls back to multi-core CPU** and tells you plainly, instead of crashing with a CUDA error.
- **9-language UI** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## 🆕 What's new in v1.0.4

- **💬 Multi-Voice Dialogue tab (new)** — write multi-character scripts, one voice per speaker. Click **📋 Sample dialogue** for a working example.
- **🗂 30 factory voices included** — ready to use out of the box, no need to record a sample first.
- **⭐ Favorite star** — click ☆ next to a voice to pin it to the top of the library.
- **🎚 Speed slider on the player** — preview at 0.5x → 2x, and the export keeps that exact speed.
- **📄 Auto SRT export** — when exporting as a merged file, the app drops a matching `.srt` next to the `.wav` (can be disabled).
- **🔤 Phonetic dictionary for special characters** — you'll never have to manually rewrite "100%" as "one hundred percent" again: type the pronunciation once, the app remembers it forever.
- **🌐 9 UI languages** — added Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский (on top of Vietnamese / English).
- **⏳ Per-row elapsed time** — see at a glance which line is currently generating and how long it's been running.
- **🌍 Output language must be selected explicitly** — the "Auto" option was removed to avoid mispronunciations.

---

## Installation

| Platform | File | Size |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.4-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.4-arm64.dmg` | ~2 GB |

### Windows (portable, no install needed)

1. Download `GLabsVoiceStudio-v1.0.4-win.zip`.
2. Extract to any folder (the drive needs at least 10 GB free).
3. Open the extracted folder and double-click `GLabsVoiceStudio.exe`.

> Want a desktop shortcut? Right-click `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** Windows needs to scan the app and GPU files (an automatic security step, only slow the first time). From the second launch onward, the app opens quickly.

### 🍎 macOS Apple Silicon

1. Download **`GLabsVoiceStudio-v1.0.4-arm64.dmg`** from the official distribution.
2. Double-click the `.dmg` file to open it.
3. Drag the **G-Labs Voice Studio** icon into the **Applications** folder.
4. Open **Applications**, **right-click** on **G-Labs Voice Studio** → choose **Open**.

> ⚠️ **First launch:** macOS may show *"App from an unidentified developer"*. Right-click the app → **Open** → click **Open** in the dialog. Only needed once.

> 📁 **Output files** (audio, scripts) are saved to `~/Documents/G-Labs Voice Studio/output/` by default.

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** macOS performs a full security check on first launch. From the second launch onward, the app opens quickly.

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

This clears all extended attributes (including the quarantine flag) from the app bundle. After running it, open the app normally. You only need to do this **once** per downloaded version.

**Method 3: System Settings → Privacy & Security**

1. Try to open the app normally (it will be blocked).
2. Open **System Settings** → **Privacy & Security**.
3. Scroll to the bottom, find *"G-Labs Voice Studio was blocked…"* → click **Open Anyway**.
4. Confirm with Touch ID or admin password.

---

## Getting Started

### Step 1 — First launch (one-time setup)

1. Open the app — a welcome screen offers 9 UI languages. Pick the one you want.
2. **Sign in** — click the ⚙️ gear icon in the left sidebar → *License* tab → **"Sign in with Google"**.
3. **Download the AI model** — switch to the *Environment* tab (or let the app prompt you) → click **"Download model"**. A few GB; wait for it to finish.
4. Close Settings.

> 💡 Change the UI language later: Settings → Language.

### Step 2 — Voice Cloning 🔊

Clone a voice from a sample recording.

1. Open the **Voice Cloning** tab.
2. Select the **output language** at the top of the tab (e.g. Vietnamese, English…).
3. In the *Reference audio* field, click **"Browse…"** and pick a sample clip (5–10 seconds, clear voice, low background noise).
4. **Required:** enter the *Reference text* — the exact transcript of the sample audio (correct punctuation and spelling).
    > 💡 Click **"✨ AI suggest"** and Whisper will transcribe it for you — still proofread it before generating.
5. Paste the target text into *Input text* (or click **"📂 Import file"** to load from `.txt` / `.srt`).
6. Click **"📋 Add to table"** — the app splits your text into individual sentences.
7. (Optional) Click **🔤 Pronunciation** to review the phonetic dictionary — if your text contains special characters (e.g. `100%`), the app will ask how to read them.
8. Click **"▶ Start"** → a confirmation dialog appears to verify the sample transcript → confirm to run.
9. When finished, click **"💾 Export audio"** (single merged file with companion `.srt`), or use **⬇** on a row to download just that line.

### Step 3 — Voice Design (TTS) 🎛️

Create a new voice from attribute descriptions — no sample needed.

1. Open the **Voice Design** tab.
2. Select the **output language**.
3. Open the **Voice Design** panel and pick: *Gender*, *Age*, *Pitch*, *Style*, *Accent*.
    > 💡 Want to reuse a saved voice from the **Voice Library**? Pick it straight from the dropdown — the app skips the first-row warmup and starts straight from row 1.
4. Paste your text and click **"📋 Add to table"**.
5. Click **"▶ Start"**.
6. After generation: click a row in the table you want to keep → click **"💾 Save"** in the *Voice Library* panel to reuse it later.
7. Click **"💾 Export audio"** to save the result.

### Step 4 — Multi-Voice Dialogue 💬 *(new)*

Generate multi-character dialogue audio, one voice per speaker — perfect for podcasts, audio drama, and interview-style videos.

1. Open the **Multi-Voice Dialogue** tab.
2. Select the **output language**.
3. Click **📋 Sample dialogue** (top-right of the text area) to see a working example — the app pastes the sample and opens the detail editor.
4. Write your script using this syntax:
    ```
    <Host>: Welcome everyone, today we have a very special conversation lined up.
    <Anna>: Hi, I'm really glad to be part of the show today.
    <Ben>: Same here, thanks for having us on. What's the topic?
    ```
    > 💡 Speaker name goes inside `< >`, followed by `:` then the line. The colon is optional — `<Anna> Hi there` also works. Names are case-insensitive.
5. Click **"🎭 Parse dialogue"** — the app splits the script into rows and shows a "Speaker" column.
6. The **Voice Assignment** panel opens automatically — pick a library voice for each speaker.
7. Click **"▶ Start"** — each line is read in the voice of its assigned speaker.
8. Click **"💾 Export audio"** to save the result (a matching `.srt` is included).

### Step 5 — Speech-to-Text 📝

Transcribe speech from an existing audio/video file.

1. Open the **Speech-to-Text** tab.
2. Click **"Choose file…"** and pick an audio/video file (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. Click **"▶ Start"** — the app analyses the audio, chunks it by speech segments, and transcribes each.
4. Results appear in a table with per-sentence timestamps. You can edit them directly.
5. Click **"💾 Export"** to save as `.txt` (plain text) or `.srt` (with timestamps, ready for subtitles).

---

## 💡 Power-user tips

### Voice Library & favorite star
- Every voice in the library has a ☆ at the start of its row. Click it → it turns ★ → that voice jumps to the top of the list (and stays there next time).
- Click ★ again to unfavorite.
- All 30 factory voices (Achernar, Aoede, Kore, Puck…) can be favorited too.

### Phonetic dictionary
- When your text contains `%`, `$`, `°C`, `m²`, brand names… click **🔤 Pronunciation** before generating.
- The first time the app sees a token it asks you how to read it (e.g. `%` → ` percent`).
- Each token only needs to be typed **once** — the app remembers it per output language. Next time it's applied automatically.
- The same token in different languages keeps separate pronunciations (e.g. Vietnamese vs English).

### Playback speed + export
- After audio is generated, the bar under the waveform has a **speed dropdown** (0.5x → 2x, in steps).
- Change the speed → preview updates immediately in the player.
- The exported file keeps that exact speed and **pitch is preserved** (no chipmunk effect — uses time-stretching).

### SRT export
- In the *Export settings* panel, **"Export subtitles (.srt)"** is on by default.
- When you export as a single merged file, the app creates `name.srt` next to `name.wav`.
- Timestamps in the SRT reflect the actual per-line duration (after the speed adjustment).

---

## System Requirements

### Windows x64
- Windows 10 / 11 (64-bit)
- **NVIDIA GPU, RTX 20-series or newer** (compute capability ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). Older cards like the GTX 10-series (GTX 1060/1070/1080) **can't run the accelerated kernels**; the app detects this and auto-falls-back to CPU.
- NVIDIA driver with CUDA 12.8 support.
- 8 GB RAM (16 GB recommended for batch workloads or CPU mode).
- 10 GB free disk space (including the AI model).

### macOS
- macOS 12 (Monterey) or newer
- **Apple Silicon** (M1/M2/M3/M4/…) — uses Apple's Metal acceleration
- 8 GB RAM
- 10 GB free disk space

> Machines without a compatible GPU **automatically run on multi-core CPU** (the app tunes PyTorch / BLAS thread counts to your physical core count). Roughly 5-10× slower than GPU but still usable for short voice-over jobs.

---

© 2026 Duck Martians AI Labs. All rights reserved.
