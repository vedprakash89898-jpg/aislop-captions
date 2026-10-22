# Caption Maker

A single web page that adds captions (subtitles) to your video or audio files — right inside your browser.

No install. No sign-up. No upload. Your file never leaves your device.

## 👋 New here? Read this first (no coding needed)

**What this does:** You open the page, pick a video or audio file, and it listens to the talking and writes captions for you. You can restyle them and save the captioned video, or export subtitle files for editing apps.

**How it works, simply:**
- The page downloads a small "speech model" (a program that understands speech) **one time** — about 40 MB.
- After that first download, it **works offline**, entirely in your browser. Nothing is sent to any server, and your file is never uploaded anywhere.
- Everything runs on your own computer or phone. That's why there's no login and no waiting on a server.

**Which speech model it uses (plain English):**
- **English, fastest (about 40 MB)** — this is the one to use. It only understands English, but it's small and works well on normal computers and phones.
- **Many languages, slower (about 80 MB)** — an optional second model that can handle other languages like Hindi. It is bigger and heavier.

## ⚠️ Important honesty note

This tool was **vibe-coded** (built with the help of Claude AI, not hand-written by a trained engineer), so please treat it as a friendly experiment rather than a polished product.

**Only the small English model is reliable.** That is the "tiny" and faster version, and it's the one that actually runs well.

The bigger, multi-language options and other tools out there:
- Need a **much more powerful computer** (lots of memory, a strong processor) to run in the browser.
- Are **not confirmed to work well** — I can't promise they run correctly.
- Are very likely **why it didn't work on your computer or your phone**. Those devices are probably just not strong enough to run the bigger models, not because the page is broken.

So: **use the tiny English model. Expect the rest to be heavy or unreliable.**

## 🛠️ For developers

- **Single file:** everything is in one `Caption-maker-fixed.html` — open it in a browser, no build step.
- **Speech engine:** Transformers.js v3.0.2, loaded from a CDN, running Whisper via **ONNX Runtime Web on the WASM (CPU) backend**. No GPU required; it runs on the CPU inside the browser.
- **Models used:**
  - `Xenova/whisper-tiny.en` — English-only, ~40 MB, fastest (default).
  - `Xenova/whisper-base` — multilingual, ~80 MB, slower.
  - Loaded quantized as `dtype: 'q8'`, `device: 'wasm'`.
- **Offline after first load:** the model is cached by the browser; later runs need no internet.
- **Transcription:** `automatic-speech-recognition` pipeline with word-level timestamps (`return_timestamps: 'word'`, 30s chunks, 5s stride). Audio is decoded and downmixed to 16 kHz mono via the Web Audio API.
- **Export formats:** SRT, WebVTT, FCPXML, TXT, JSON, CSV, plus a real-time in-browser video recording (MediaRecorder) that burns captions into the video.
- **Privacy:** all processing is on-device. No uploads, no accounts, no analytics.

**Why bigger models struggle:** the WASM/CPU backend runs the model on your processor alone. Larger Whisper variants need far more memory and compute than most laptops and phones can spare in a browser tab, so they're slow, memory-hungry, or simply fail.
