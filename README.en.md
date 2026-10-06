<h1 align="center">G-Labs Voice Studio</h1>

<p align="center"><b>A desktop AI voice app that runs on your own computer - clone a voice from a few seconds of audio, read text in 600+ languages, create multi-voice dialogue, transcribe audio/video to subtitles and translate subtitles with AI.</b></p>

<p align="center">
  <a href="README.md">Tiếng Việt</a> ·
  <b>English</b> ·
  <a href="README.pt-BR.md">Português</a> ·
  <a href="README.tr.md">Türkçe</a> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.hi.md">हिन्दी</a> ·
  <a href="README.bn.md">বাংলা</a> ·
  <a href="README.ur.md">اردو</a> ·
  <a href="README.ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G"><img alt="Download for Windows" src="https://img.shields.io/badge/Download-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta"><img alt="Download for macOS (Apple Silicon)" src="https://img.shields.io/badge/Download-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

---

## Install

### Step 1 - Choose the right build for your computer

Builds are distributed through the official Google Drive folders:

| Your computer | Google Drive | Note |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | [Windows](https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G) | A `.zip` - extract and run, no installer |
| 🍎 **Mac with Apple chip (M1/M2/M3/M4…)** | [macOS Apple Silicon](https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta) | A `.dmg`, requires macOS 12 or later |

> **Intel Macs are not supported** - there is only an Apple Silicon build. Not sure which chip your Mac has? Click the  menu → **About This Mac**: a **Chip** line reading "Apple M…" works; a **Processor** line reading "Intel…" does not.

### Step 2 - Install

<details open>
<summary><b>🪟 On Windows</b></summary>

1. Download the Windows `.zip` (for example `G-Labs-Voice-Studio-v2.0.2-win.zip`) and **extract** it to any folder - the drive needs at least 10 GB free (the AI models downloaded later take several GB).
2. Open the extracted folder and run **`G-Labs-Voice-Studio.exe`** (everything else lives in the `data` subfolder - don't move it).
3. If **"Windows protected your PC"** (SmartScreen) appears: click **More info** → **Run anyway**. *(The app isn't signed with a Microsoft certificate, so Windows warns about it - it is not a virus.)*
4. **Create a shortcut:** right-click `G-Labs-Voice-Studio.exe` → **Send to** → **Desktop (create shortcut)** so you can open it quickly next time.

> ⏳ **The first launch can take 30-60 seconds** (the splash screen sits still) while Windows security-scans the app and the graphics libraries. Wait, don't close it - later launches are faster.

</details>

<details open>
<summary><b>🍎 On macOS</b></summary>

1. Open the downloaded **`.dmg`**, then **drag the G-Labs Voice Studio icon onto the Applications folder**.
2. In **Applications**, **right-click** (or Control-click) **G-Labs Voice Studio** → **Open** → click **Open** again in the confirmation dialog. *(The app isn't notarized by Apple, so you open it this way the **first time**; afterwards it opens normally.)*
3. If macOS says the app **"is damaged / can't be opened"** or there is no Open button, open **Terminal**, paste this and press Enter:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"
   ```
   Then open the app again. Alternatively: **System Settings → Privacy & Security**, scroll to the bottom and click **Open Anyway** next to the message about G-Labs Voice Studio being blocked.

> ⏳ **The first launch can take 30-60 seconds** while macOS security-checks the whole app. Later launches are faster.

</details>

### Step 3 - Sign in & choose a plan

**You need to sign in with Google** (Settings ⚙️ → **License Accounts** tab → **Login with Google**) so the app can check your license. One account runs on **one computer at a time** - signing in on another device ends the session on the old one.

| Plan | Price | Includes |
|---|---|---|
| **Trial** | Free | Limited rows per generation (1 by default) - enough to check your machine runs well before buying |
| **Studio plan** | 1 month $5 · 6 months $25 · 1 year $50 (100,000đ / 500,000đ / 1,000,000đ by VietQR) | Unlimited rows, **Render queue**, **Translate** tab, **Webhook API** |

- Buy inside the app (Settings → **License Accounts**) by **VietQR bank transfer**, **PayPal** (international card) or **USDT**. Plans are time-based, don't auto-renew, and are activated on the Google account you sign in with.
- The Studio plan belongs to Voice Studio only and is **separate** from G-Labs Studio Plus/Max.
- Refunds are available within the first **24 hours** after payment - see the [Refund policy](https://duckspace.net/refunds.html#en). Run the free trial first to make sure your machine handles it smoothly.

---

## First run

1. **Open the app and pick an interface language** on the welcome screen (change it later in Settings).
2. **Sign in with Google** - Settings ⚙️ → **License Accounts** → **Login with Google**.
3. **Download the voice model** - open the **Model Manager** tab (or follow the app's prompt) and download the AI voice model (several GB, one time only). Speech-recognition models download separately the first time you use them.
4. **Open the Read Text tab**, choose the **output language** and pick a voice from the library (30 built-in voices).
5. Paste your text → **Add to Table** → **Start**. Preview each line, then click **Export Audio** to save the file (with an `.srt` subtitle by default).

---

## Features

<p align="center">
  <img alt="G-Labs Voice Studio interface" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
</p>

- **Runs on your computer** - once the models are downloaded, voice generation and transcription run locally (NVIDIA GPU, Apple Metal or CPU); your audio and text are not sent to a server. Only the Translate tab sends subtitle text to the AI provider you choose.
- **Voice cloning** - from a 5-10 second sample, read any text in exactly that voice.
- **Voice design** - create a new voice by gender, age, pitch, style and accent; no sample file needed.
- **600+ output languages** - Vietnamese, English, Chinese, Japanese, Korean, French, German, Spanish and many more.
- **Multi-voice dialogue** - `<Name>: line` scripts, each character with its own voice and speed.
- **Subtitle extraction** - transcribe MP3, WAV, M4A, FLAC, MP4, MOV…; export TXT or SRT with word-level timing.
- **AI subtitle translation** *(Studio plan)* - translate or proofread `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt`; timings and line count stay exactly the same.
- **Voice library** - 30 built-in voices, save your own, pin ⭐ favourites, back up/restore to a `.vcp` file.
- **Audio fine-tuning** - 6 processing modes, volume levelling, 13 expression tags, a pronunciation dictionary that remembers how to read `100%`, `25°C`, `m²`.
- **Flexible export** - WAV or MP3, one merged file or one file per sentence, with `.srt`; download a single line with its ⬇ button.
- **Render queue** *(Studio plan)* - queue several scripts; the app runs them one by one and saves the files.
- **Webhook API** *(Studio plan)* - a local REST server for n8n, Make, Zapier, Python/cURL or AI agents.
- **Handles your hardware** - an incompatible graphics card falls back to CPU with a clear notice; GPU memory is released automatically when idle.
- **9 interface languages** - Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## Pages

Pages live in the left sidebar. The three voice pages (Voice Clone, Read Text, Group Dialogue) share one rhythm: choose the **output language** → paste text or **Import** (`.txt`, `.srt`) → **Add to Table** (the app splits sentences by the **Split mode** you choose, with a row-count preview) → **Start** → preview → **Export Audio**.

### 🔊 Voice Clone

![Voice Clone](docs/screenshots/en/clone.webp)

Click **Select...** to load a sample audio file (clear voice, little background noise), then **drag the highlighted box on the waveform** to select the exact 3-30 second region to use - on release the edges snap to the nearest silence; files longer than 5 minutes / 50 MB use their first 30 seconds. The *Sample text* is **required** and must match the words in the sample exactly (punctuation and spelling included); **✨ AI suggest** transcribes it for you, but check it before generating. When cloning finishes, the app invites you to preview and save the voice to the library in one click.

### 🎛️ Read Text

![Read Text](docs/screenshots/en/tts.webp)

Pick a voice from the library, or open **Voice Design** to create a new one by *Gender, Age, Pitch, Style, Accent*. Like a designed voice? Select its row in the table → **Save** it to the library for reuse. The **Smart merge** split mode joins short sentences into flowing lines up to a character cap while always breaking at a sentence end. The **Expression tags** button lets you look up tags and **Insert** them at the cursor.

### 💬 Group Dialogue

![Group Dialogue](docs/screenshots/en/dialogue.webp)

Write a multi-character script - great for podcasts, audio drama and interviews:

```
<Host>: Welcome, everyone.
<Mai>: Hi, I'm really glad to be on the show.
<Minh>: Same here - what are we talking about today?
```

Put the character name in `< >` at the start of the line (the `:` is optional, names are case-insensitive). Click **Sample dialogue** for an example, then **Parse dialogue** - the **Voice assignment** panel opens so you can give each character a voice from the library and its own **Speed** slider (0.5× → 2×).

### 📝 Extract Subtitles

![Extract Subtitles](docs/screenshots/en/asr.webp)

Choose an audio/video file (MP3, WAV, M4A, FLAC, MP4, MOV…), the spoken language and a recognition model (Tiny → Large v3, each showing the VRAM it needs), then run it. Subtitle lines are built from word timestamps and break at real pauses / sentence ends / a character cap; change the *max characters, max seconds, pause threshold* boxes and the table updates instantly, no re-transcription needed. Edit right in the table and export `.txt` or `.srt`.

### 🌐 Translate *(Studio plan)*

![Translate](docs/screenshots/en/srt.webp)

Translate subtitles into another language or proofread spelling and line breaks - **only the text changes; timings and line count stay the same**.

1. One-time setup in **Model Manager → LLM**: choose **9Router** (a gateway running on your machine - enter its address + API key), **Claude CLI**, **Antigravity** (`agy`) or **Codex CLI** (install and sign in). Each row has a **Guide** button with the install command; after installing, click **Refresh list** and the app detects it and lists its models.
2. **Import** `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt` - or **From Extract Subtitles**. A `.txt` file has no timings, so the app assigns provisional ones and tells you.
3. Recommended: **Clean up text** joins fragments split mid-sentence (common in subtitles exported from video editors), with a preview such as *"120 lines → 68 lines"* before you **Apply**.
4. Choose **Translate**, **Edit** or **Translate + Edit**, pick the target language and model, then **Start**.
5. A **consistency table** locks names, terms and forms of address for the whole file and is sent with every chunk; you can edit it, and optionally stop to review it before translating.
6. Check the **Result** column (lines the AI missed are marked ⚠ and keep the original text), choose **SRT / VTT / TXT** and **Export**.

### 📚 Model Manager

![Model Manager](docs/screenshots/en/model.webp)

One row per model with its size and status: the AI voice model and the recognition sizes (Tiny, Base, Small, Turbo, Large v3). Download only what you need and change the **model folder** (for example to drive D to spare drive C - copy the old model folder across, or let the app download again). This is also where you set up the **LLM** provider for Translate and the **Auto-unload VRAM** timer.

### 🗒 Render queue *(Studio plan)*

Instead of generating one script and exporting by hand, click **Add to queue** to save the current script + voice + settings as a job with **its own name and output folder**. **Run queue** and the app works through them one by one, saving the files. Each job shows `X/N sentences` so you can see which one is missing lines due to errors; **Reload** brings a job back into its tab for fixing (failed lines are marked ❌). The queue survives closing and reopening the app.

### 🔗 Webhook API *(Studio plan)*

![Webhook API](docs/screenshots/en/webhook.webp)

A local REST server so n8n, Make, Zapier, Python/cURL or AI agents can generate voice automatically. Defaults to `127.0.0.1:8766` (this computer only), with an API key, a full **URL** box with a **Copy** button, an auto-start option and a live request log. Change the IP to `0.0.0.0` / a LAN IP to let other devices call it - the API key then travels over unencrypted HTTP. Full schema: [`docs/WEBHOOK_INTEGRATION.en.md`](docs/WEBHOOK_INTEGRATION.en.md).

---

## Tips

<details>
<summary><b>Audio mastering - 6 processing modes</b></summary>

In the **Audio mastering** section of the three voice tabs (change it in one tab and the others follow):

- 📻 **Broadcast** *(default)* - radio/podcast standard, warm, compressed.
- 🎬 **Cinematic** - spacious reverb, gentle compression.
- 🎙️ **Podcast** - close-mic, heavy compression, no reverb.
- ☀️ **Warm** - boosted low-mids, cozy.
- ✨ **Bright** - crisp highs, airy.
- 🔇 **Raw** - the model's output as-is.

**Even out volume between rows** levels by perceived loudness (RMS), so no more loud and quiet lines. For the model's untouched output, pick **Raw** and untick this box.

</details>

<details>
<summary><b>Expression tags</b></summary>

Type a tag into the text (keep the square brackets; on its own or mid-sentence, e.g. `That's so funny [laughter] I can't stop.`) - the voice makes the sound instead of reading the word. No need to memorise them: the **Expression tags** button lets you look them up and insert them.

| Tag | Sound |
|---|---|
| `[laughter]` | Laughter |
| `[sigh]` | Sigh |
| `[confirmation-en]` | Agreement - "mm-hmm" |
| `[question-en]` · `[question-ah]` · `[question-oh]` · `[question-ei]` · `[question-yi]` | Questioning intonation |
| `[surprise-ah]` · `[surprise-oh]` · `[surprise-wa]` · `[surprise-yo]` | Surprise |
| `[dissatisfaction-hnn]` | Annoyance - "hnn" |

How strongly they come through varies by language and voice - try a short sentence first.

</details>

<details>
<summary><b>Pronunciation dictionary</b></summary>

Text with `%`, `$`, `°C`, `m²`, brand names…? Click **Fix pronunciation** before generating: the app asks how to read each symbol/word, you type the spelling once (e.g. `%` → `percent`) and it remembers it per output language.

</details>

<details>
<summary><b>Speed & subtitles on export</b></summary>

- **Reading Speed** is in *Advanced Settings*; the **Speed** control on the player previews faster/slower playback, and the exported file keeps that exact speed without pitch distortion.
- **Also export subtitles (.srt)** writes a matching `.srt` next to the audio, with timings from each sentence's real length after the speed adjustment.
- **Fit speech to subtitle timing**: when the script came from an `.srt`, each line is sped up (max 1.8×) to fit its cue - never slowed down.

</details>

<details>
<summary><b>Automatic memory release</b></summary>

Leave the app idle for a while (5 minutes by default) and the AI model is unloaded from VRAM/RAM to lighten your machine; it reloads on your next action. Change the time or turn it off in **Model Manager → Auto-unload VRAM**.

</details>

---

## System requirements

|   | Minimum | Recommended |
|---|---|---|
| **Operating system** | Windows 10 (64-bit), macOS 12 on Apple Silicon | Windows 11, macOS 13 or later |
| **RAM** | 8 GB | 16 GB or more |
| **Disk** | 10 GB free (models + cache) | 20 GB or more, SSD |
| **GPU** | Optional - runs on CPU | NVIDIA RTX 20-series or newer, 8 GB VRAM · Macs use Metal |
| **Network** | Internet for sign-in/license checks and model downloads | |

- **Windows:** GPU acceleration needs an NVIDIA **RTX 20-series or newer** card (compute capability ≥ 7.0) and a driver supporting CUDA 12.8. Older cards such as the GTX 10-series are detected automatically and run on CPU.
- **macOS:** **Apple Silicon** only (M1/M2/M3/M4…), accelerated with Metal.
- CPU mode is roughly 5-10× slower than GPU but still fine for short voice-overs.

---

## Where your data lives

| What | Windows | macOS |
|---|---|---|
| Exported audio (default) | `output\` inside the folder you extracted the app to | `~/Documents/G-Labs Voice Studio/output` |
| Settings, sign-in session | `%APPDATA%\G-Labs Voice Studio` | `~/Library/Application Support/G-Labs Voice Studio` |
| Your voice library | `%APPDATA%\G-Labs Voice Studio\voice_studio\voices` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/voices` |
| AI models | `%APPDATA%\G-Labs Voice Studio\voice_studio\model` (or the folder you choose) | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/model` (or the folder you choose) |
| Render queue | `%APPDATA%\G-Labs Voice Studio\voice_studio\queue` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/queue` |

To move your voice library to another computer, use **backup/restore `.vcp`** in the voice library panel.

---

## Troubleshooting

**The first launch is very slow, the splash screen doesn't move** - Windows/macOS is running its first security scan; wait 30-60 seconds, don't close it. Later launches are faster.

**Windows stops at "Windows protected your PC"** - click **More info → Run anyway**. The app isn't signed with a Microsoft certificate; it is not a virus.

**macOS says the app is damaged / can't be opened** - it isn't notarized by Apple. Right-click → **Open** the first time, or run `xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"`.

**"Switched to CPU" notice** - your graphics card isn't compatible (e.g. GTX 10-series). Everything still works, just slower; for speed you need an NVIDIA RTX 20-series or newer, or an Apple Silicon Mac.

**Only 1 row is generated at a time** - you're on the trial. Buy the Studio plan for unlimited rows.

**Signed out with a message that the account logged in on another device** - one account runs on one computer at a time; sign in again on the computer you want to use.

**The cloned voice says the wrong words / drifts** - the *Sample text* must match the words in the sample exactly; pick a clear sample with little noise.

**Special characters are read wrong (`100%`, `25°C`…)** - add how to read them under **Fix pronunciation**.

**Drive C is filling up with models** - change the model folder in **Model Manager**, then copy the old model folder across or let the app download again.

**No models to choose in the Translate tab** - install and sign in to an LLM provider (9Router, Claude CLI, Antigravity, Codex) following its **Guide** button, then click **Refresh list**.

**Need detailed error information** - click **Detailed Logs** in the sidebar.

---

📖 [Product page](https://duckspace.net/en/voice-studio/) · [Guide](https://duckmartians.info/voice/guide/en/) · [Changelog](CHANGELOG.md) · [Discord](https://discord.gg/munMZEBMw5)

© 2026 Duck Martians AI Labs. All rights reserved.
