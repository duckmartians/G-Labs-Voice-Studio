# G-Labs Voice Studio — Webhook API Integration Guide

> Audience: developers, technical integrators, and AI agents.
> Goal: everything needed to integrate the local Voice Studio Webhook REST API
> correctly — endpoints, auth, request/response schemas, voice presets,
> parameters, error handling, and the async (submit → poll → download) workflow.

This document describes the API exposed by the **Webhook** tab of the **G-Labs
Voice Studio** desktop app (a zero-shot text-to-speech / voice-cloning studio).
It lets external tools (n8n, Make.com, Zapier, custom scripts, AI agents) generate
speech audio from text using voices you saved in the app's **Voice Bank**.

> ⚠️ This is a **voice/TTS** API. It is different from the G-Labs *Automation*
> (image/video) webhook — endpoints, body fields, and default port differ.

---

## 1. Overview & key concepts

- **Local-only server.** The API runs on `http://127.0.0.1:<port>` (loopback). It
  binds to `127.0.0.1` only — it is **not** reachable from other machines unless
  you add your own tunnel/reverse proxy. Your integration must run on the same
  machine, or you must expose it yourself.
- **Default port:** `8766` (configurable in the Webhook tab).
- **You must start the server.** Open the app → **Webhook** tab → **Start**. The
  tab shows/copies the **API key** and lets you change the port.
- **You must save voices first.** Generation always uses a **`preset_id`** that
  points to a voice saved in the app's **Voice Bank**. List them with
  `GET /api/voices`; create them in the Voice Studio UI.
- **Asynchronous by design.** Generation takes time, so the API is
  **submit → poll → download**:
  1. `POST /api/voice/design` → get a `task_id` immediately (HTTP `202`).
  2. `GET /api/status/{task_id}` repeatedly until `status` is `completed` or `failed`.
  3. On `completed`, download the audio from the returned `results` URL.
- **Generation is serialized.** Requests are queued and run on a single shared TTS
  model (GPU/CPU). Even when several jobs are submitted at once, inference happens
  **one at a time** (a shared model mutex). Expect throughput of one generation at a time.
- **First request may be slow.** The first job after launch lazily loads (and may
  download) the TTS model. If the model can't be loaded (no model / cancelled
  download), queued tasks `fail` with a clear message.

---

## 2. Authentication

Auth applies to all endpoints **except** `GET /api/health` and
`GET /api/files/{name}`. Send the key as **either** header:

```
X-API-Key: <your-api-key>
```
or
```
Authorization: Bearer <your-api-key>
```

- A key is **auto-generated on first launch** and shown in the **Webhook** tab.
- **If the operator has not set any key, the server is open** (no auth) — but the
  default is that a key exists. Treat the key as required.
- Wrong/missing key (when one is configured) → `401 {"error": "Invalid or missing API key"}`.

CORS is enabled (`Access-Control-Allow-Origin: *`) with `OPTIONS` preflight handled.

---

## 3. Endpoints

| Method | Path | Auth | Purpose |
|--------|------|:----:|---------|
| `GET`  | `/api/health` | ❌ | Server health / uptime / queue counts |
| `GET`  | `/api/voices` | ✅ | List voice presets saved in the Voice Bank |
| `POST` | `/api/voice/design` | ✅ | Submit a text-to-speech generation task |
| `GET`  | `/api/status/{task_id}` | ✅ | Poll task status; returns result or error |
| `GET`  | `/api/result/{task_id}` | ✅ | Get result (only once `completed`) |
| `GET`  | `/api/files/{name}` | ❌ | Download a generated audio file |
| `GET`  | `/api/tasks` | ✅ | List the 50 most recent tasks |

Trailing slashes are tolerated (e.g. `/api/health/`).

---

## 4. The async workflow (step by step)

### Step 1 — Discover voices

`GET /api/voices` returns the presets you can use as `preset_id`:

```json
{
  "voices": [
    { "id": "spk_a1b2c3", "name": "Calm Narrator", "tags": ["male", "warm"], "is_factory": false, "is_favorite": true }
  ],
  "count": 1
}
```

> If `count` is `0`, no voices are saved yet — create one in the Voice Studio app
> (Voice Bank) before calling `/api/voice/design`.

### Step 2 — Submit

`POST /api/voice/design` with a JSON body (see §5). Response is **HTTP 202**:

```json
{
  "task_id": "a1b2c3d4e5f6",
  "status": "pending",
  "message": "Voice design task queued",
  "poll_url": "/api/status/a1b2c3d4e5f6"
}
```

> `task_id` is a 12-char hex string. The server validates JSON synchronously, so a
> malformed body returns `400` immediately instead of a `failed` task later.

### Step 3 — Poll status

`GET /api/status/{task_id}`. Possible `status`: `pending` → `running` →
`completed` | `failed`.

**Running:**
```json
{ "task_id": "a1b2c3d4e5f6", "type": "voice_design", "status": "running", "created_at": 1707782400.0 }
```

**Completed:**
```json
{
  "task_id": "a1b2c3d4e5f6",
  "type": "voice_design",
  "status": "completed",
  "created_at": 1707782400.0,
  "results": ["http://127.0.0.1:8766/api/files/voice_20260610_120000_a1b2c3d4e5f6.wav"],
  "completed_at": 1707782460.0
}
```

**Failed:**
```json
{
  "task_id": "a1b2c3d4e5f6",
  "type": "voice_design",
  "status": "failed",
  "created_at": 1707782400.0,
  "error": "Preset 'spk_xxx' not found. Call GET /api/voices to list available preset_ids."
}
```

> Suggested poll interval: every 2–4 seconds. Generation time scales with script
> length and `num_step`. Because the model is shared and serialized, a queued job
> also waits for earlier jobs to finish.

### Step 4 — Download the audio

`results` is an array with **one** URL:
`http://127.0.0.1:<port>/api/files/<urlencoded-name>`. `GET` it (no API key needed)
to download the raw audio bytes. `Content-Type` is set by extension
(`audio/wav` or `audio/mpeg`). The file is stored locally on the machine running
the app (`output/webhook/`).

---

## 5. Request body — `POST /api/voice/design`

JSON body. **`script` and `preset_id` are both required.**

| Field | Type | Required | Default | Notes |
|-------|------|:--------:|---------|-------|
| `script` | string | ✅ | — | The text to speak. Long text is auto-split into sentences; the output is one continuous audio file (sentences joined with ~0.3 s gaps). |
| `preset_id` | string | ✅ | — | A voice id from `GET /api/voices` (saved in the Voice Bank). Unknown id → task fails. |
| `language` | string | ❌ | `Auto` | `Auto` = auto-detect, or a language name (e.g. `"english"`, `"vietnamese"`). The model supports 600+ languages. |
| `speed` | number | ❌ | `1.0` | Speech speed factor. `>1.0` faster, `<1.0` slower. |
| `output_format` | string | ❌ | `wav` | `"wav"` (PCM 16-bit) or `"mp3"` (192 kbps). Any other value → `wav`. |
| `num_step` | int | ❌ | `50` | Diffusion steps. Higher = potentially better quality but slower; lower = faster. |
| `guidance_scale` | number | ❌ | `2.0` | Classifier-free guidance scale (adherence vs. naturalness). |

```json
{
  "preset_id": "spk_a1b2c3",
  "script": "Hello world. This is a sample sentence. And another one.",
  "language": "english",
  "speed": 1.0,
  "output_format": "wav"
}
```

Notes:
- `script` is required and trimmed — an empty/whitespace-only `script` fails the
  task with `` `script` is required ``.
- `preset_id` is required — a missing/empty value fails with a message pointing you
  to `GET /api/voices`.
- `num_step` and `guidance_scale` are advanced quality controls; leave them at the
  defaults unless you know you need to tune them.
- Output is **always a single audio file** per request.

---

## 6. Voices (`GET /api/voices`)

Returns every preset in the Voice Bank:

| Field | Type | Meaning |
|-------|------|---------|
| `id` | string | Use this as `preset_id`. |
| `name` | string | Human-friendly name. |
| `tags` | string[] | Free-form tags (e.g. gender, style). |
| `is_factory` | bool | True for built-in presets. |
| `is_favorite` | bool | True if the user starred it. |

Top-level: `{ "voices": [...], "count": <int> }`.

> Presets are created in the Voice Studio desktop app (record/clone a voice and
> save it to the Voice Bank). The webhook can only **use** presets, not create them.

---

## 7. Responses & status reference

### POST `/api/voice/design` → `202`
```json
{ "task_id": "a1b2c3d4e5f6", "status": "pending", "message": "Voice design task queued", "poll_url": "/api/status/a1b2c3d4e5f6" }
```

### GET `/api/status/{task_id}` → `200`
- `pending` / `running`: `{ task_id, type, status, created_at }`
- `completed`: adds `results` (array with one file URL) and `completed_at` (unix seconds).
- `failed`: adds `error` (string).
- Unknown task id → `404 {"error": "Task <id> not found"}`.

### GET `/api/result/{task_id}` → `200`
- If not yet completed: `{ task_id, status, message: "Task not yet completed" }`.
- If completed: `{ task_id, status: "completed", results: [...], completed_at }`.

### GET `/api/health` → `200`
```json
{ "status": "ok", "service": "G-Labs Voice Studio Webhook", "uptime": 123, "tasks_pending": 0, "tasks_running": 1 }
```

### GET `/api/tasks` → `200`
```json
{ "tasks": [ { "task_id": "...", "type": "voice_design", "status": "completed", "created_at": 1707782400.0 } ] }
```
(Newest first, max 50.)

### Error responses
| HTTP | Body | When |
|------|------|------|
| `400` | `{"error": "Empty body"}` | POST with no body |
| `400` | `{"error": "Invalid JSON body: ..."}` | POST with malformed JSON |
| `401` | `{"error": "Invalid or missing API key"}` | Missing/invalid key (when one is set) |
| `404` | `{"error": "Not found"}` | Unknown route |
| `404` | `{"error": "Task <id> not found"}` | Unknown task in status/result |
| `404` | `{"error": "File not found: <name>"}` | Unknown/expired file |
| `500` | `{"error": "Failed to list voices: ..."}` | Voice Bank read error on `/api/voices` |

---

## 8. Error handling

When a task fails, the status response carries a single **`error`** string (this
API does **not** split it into a numeric code like the Automation webhook does).
Branch on the message text. Common failures:

| `error` (text) | Cause | Fix |
|----------------|-------|-----|
| `` `script` is required `` | Empty/missing `script` | Provide non-empty `script`. |
| `` `preset_id` is required. ... `` | Missing `preset_id` | Call `GET /api/voices`, pass a valid `id`. |
| `Preset '<id>' not found. ...` | `preset_id` not in Voice Bank | Use a valid id from `GET /api/voices`. |
| `Failed to load preset '<id>': ...` | Preset data unreadable | Re-save the voice in the app. |
| `Voice model not loaded ...` / `Model load did not complete ...` | TTS model unavailable / download cancelled | Open Voice Studio, run any generation once, retry. |
| `MP3 encode failed: ...` | ffmpeg error during MP3 export | Use `"output_format": "wav"`, or check the app's ffmpeg. |
| `Internal: could not read request body` | Temp body lost before processing | Resubmit the request. |

HTTP-level validation errors (`400`) are returned synchronously at submit time
(empty body, bad JSON), so you don't need to poll to detect them.

---

## 9. Constraints & gotchas

- **Localhost only.** Run your integration on the same machine, or tunnel
  `127.0.0.1:<port>` yourself.
- **Serialized generation.** One generation at a time (shared TTS model). Submitting
  many jobs is fine — they queue — but don't expect parallel speedup.
- **Voice Bank required.** You must have at least one saved voice; `preset_id` is
  mandatory. There is no "design from text attributes" field in this webhook — it
  always clones a saved preset.
- **First-call model load.** The first request after launch may take longer (model
  load / download) and can fail if no model is available.
- **Tasks are in-memory.** Task state and the `task_id` → result mapping live in the
  running app; they are lost if the app restarts. Submit, poll, and download within
  the same app session.
- **Files are local** (`output/webhook/`) and may be cleaned up over time; download
  promptly after `completed`.
- **Determinism:** the same `script` is not guaranteed to produce byte-identical
  audio across runs.

---

## 10. End-to-end examples

### 10.1 cURL

```bash
# 1) List available voice presets → pick an "id"
curl http://127.0.0.1:8766/api/voices \
  -H "X-API-Key: YOUR_API_KEY"

# 2) Submit a voice generation job
curl -X POST http://127.0.0.1:8766/api/voice/design \
  -H "Content-Type: application/json" \
  -H "X-API-Key: YOUR_API_KEY" \
  -d '{"preset_id": "spk_a1b2c3", "script": "Hello world.", "language": "english"}'
# → {"task_id":"a1b2c3d4e5f6","status":"pending","poll_url":"/api/status/a1b2c3d4e5f6"}

# 3) Poll until done
curl http://127.0.0.1:8766/api/status/a1b2c3d4e5f6 -H "X-API-Key: YOUR_API_KEY"

# 4) Download the audio (no key needed)
curl -o out.wav "http://127.0.0.1:8766/api/files/voice_20260610_120000_a1b2c3d4e5f6.wav"

# Bearer-token style also works:
curl http://127.0.0.1:8766/api/voices -H "Authorization: Bearer YOUR_API_KEY"
```

### 10.2 Python (discover → submit → poll → download)

```python
import time, requests

BASE = "http://127.0.0.1:8766"
KEY  = "YOUR_API_KEY"
H    = {"X-API-Key": KEY, "Content-Type": "application/json"}

# 1) Pick a voice
voices = requests.get(f"{BASE}/api/voices", headers=H, timeout=30).json()["voices"]
if not voices:
    raise SystemExit("No voices saved — create one in the Voice Studio Voice Bank first.")
preset_id = next((v["id"] for v in voices if v.get("is_favorite")), voices[0]["id"])

# 2) Submit
def synth(script, preset_id, fmt="wav", language="Auto", poll=3, timeout=600):
    body = {"preset_id": preset_id, "script": script, "language": language, "output_format": fmt}
    r = requests.post(f"{BASE}/api/voice/design", json=body, headers=H, timeout=30)
    r.raise_for_status()
    task_id = r.json()["task_id"]

    deadline = time.time() + timeout
    while time.time() < deadline:
        s = requests.get(f"{BASE}/api/status/{task_id}", headers=H, timeout=30).json()
        if s["status"] == "completed":
            return s["results"][0]                 # single audio URL
        if s["status"] == "failed":
            raise RuntimeError(s.get("error"))
        time.sleep(poll)
    raise TimeoutError(f"task {task_id} did not finish in {timeout}s")

url = synth("Hello world. This is a test.", preset_id, fmt="mp3", language="english")

# 3) Download
audio = requests.get(url, timeout=120).content      # /api/files needs no key
open("out" + url[url.rfind("."):], "wb").write(audio)
```

### 10.3 JavaScript (Node, fetch)

```js
const BASE = "http://127.0.0.1:8766";
const KEY  = "YOUR_API_KEY";
const H = { "X-API-Key": KEY, "Content-Type": "application/json" };

async function synth(script, presetId, { fmt = "wav", language = "Auto", poll = 3000, timeout = 600000 } = {}) {
  const r = await fetch(`${BASE}/api/voice/design`, {
    method: "POST", headers: H,
    body: JSON.stringify({ preset_id: presetId, script, language, output_format: fmt }),
  });
  if (!r.ok) throw new Error(`submit ${r.status}: ${await r.text()}`);
  const { task_id } = await r.json();

  const end = Date.now() + timeout;
  while (Date.now() < end) {
    const s = await (await fetch(`${BASE}/api/status/${task_id}`, { headers: H })).json();
    if (s.status === "completed") return s.results[0];   // audio URL
    if (s.status === "failed") throw new Error(s.error);
    await new Promise(r => setTimeout(r, poll));
  }
  throw new Error(`task ${task_id} timed out`);
}

// Discover a voice, then synthesize
const { voices } = await (await fetch(`${BASE}/api/voices`, { headers: H })).json();
const url = await synth("Hello world.", voices[0].id, { fmt: "wav", language: "english" });
console.log(url);
```

---

## 11. Quick checklist for an integrator / AI agent

1. Make sure at least one voice is saved in the app's **Voice Bank**.
2. Start the Webhook server in the app; copy the **port** (default `8766`) and **API key**.
3. `GET /api/voices` → choose a `preset_id`.
4. `POST /api/voice/design` with `{ preset_id, script, ... }` (both `script` and `preset_id` required).
5. Read `task_id` from the `202` response.
6. Poll `GET /api/status/{task_id}` every 2–4 s until `completed` or `failed`.
7. On `completed`: `GET` `results[0]` to download the audio file.
8. On `failed`: read the `error` string (e.g. preset not found, model not loaded).
9. Remember: generation is **serialized** (one at a time), and tasks live only in
   the current app session.
