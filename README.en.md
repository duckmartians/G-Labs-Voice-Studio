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
- **600+ languages supported** — recognize and synthesize over 600 languages (including Vietnamese, English, Chinese, Japanese, Korean, French, German, Spanish, and many minority languages).
- **Batch processing** — import `.txt` or `.srt` scripts, run batches, and export audio files preserving timestamps.
- **Fine-grained controls** — diffusion steps, guidance scale, playback speed, sentence gap.
- **Bilingual UI** — Vietnamese and English.

---

## Installation

| Platform | File | Size |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.0-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.0-arm64.dmg` | ~2 GB |

### Windows (portable, no install needed)

1. Download `GLabsVoiceStudio-v1.0.0-win.zip`.
2. Extract to any folder (pick a drive with at least 10 GB free).
3. Open the extracted folder and run `GLabsVoiceStudio.exe` directly.

> Want a desktop shortcut? Right-click `GLabsVoiceStudio.exe` → *Send to* → *Desktop (create shortcut)*.

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** Windows needs to scan the app and GPU files (an automatic security step that is slow on first run). From the second launch onward, the app opens quickly.

### macOS Apple Silicon

1. Download `GLabsVoiceStudio-v1.0.0-arm64.dmg`.
2. Open the DMG and drag the app icon into the `Applications` folder.
3. Launch the app from Launchpad or Applications. On first launch you may need to allow it in *System Settings → Privacy & Security* (the app is not Apple-notarized yet).

> **⏳ The first launch may take 30–60 seconds (the splash screen will pause around ~90%) — please wait, don't close it.** macOS performs a full security check on the app during first launch. From the second launch onward, it opens quickly.

---

## Getting Started

After launching the app for the first time, **you must sign in with your licensed account before any feature becomes usable**:

1. **Open Settings** — click the ⚙️ gear icon in the left sidebar.
2. **Sign in** — on the *License* tab, click **"Sign in with Google"**. Your browser will open so you can pick the Google account tied to your license.
3. **Wait for activation** — the app verifies with the server and displays your plan and expiry.
4. **Download the AI model** — on first launch the app downloads the model (~a few GB). Wait for it to finish.
5. **Start creating** — close Settings, then pick a tab: *Voice Cloning* / *Voice Design (TTS)* / *Speech-to-Text* depending on your task.

---

## System Requirements

### Windows x64
- Windows 10 / 11 (64-bit)
- **NVIDIA GPU** with a driver supporting CUDA 12.8 (RTX 20-series or newer recommended) — the app uses CUDA automatically when available and falls back to CPU if no NVIDIA GPU is detected.
- 8 GB RAM (16 GB recommended for batch workloads)
- 10 GB free disk space (including the model)

### macOS
- macOS 12 (Monterey) or newer
- **Apple Silicon** (M1/M2/M3/M4/...) — uses Metal Performance Shaders (MPS)
- 8 GB RAM
- 10 GB free disk space

> Windows machines without an NVIDIA GPU and Intel Macs will run in CPU mode — significantly slower, suitable for testing only.

---

© 2026 Duck Martians AI Labs. All rights reserved.
