# Caption Maker — Version 6.2

A free tool that adds captions (subtitles) to your video or audio — right inside your
web browser.

You open one file, choose your video, and the app listens to the sound and writes the
words for you. Then you make the captions look how you want and save them.

**Everything happens on your own computer. Nothing is uploaded. No account, no login,
no internet needed after the first time.**

---

## How to use it

1. **Open the file** `caption-maker_6.2.html` in your browser (for example Chrome).
2. Click **Choose file** and pick a video or an audio file.
3. Click **Create captions**. The app listens to the sound and writes the words.
   The first time, it downloads a "speech model" — this may take a few minutes.
   After that it is much faster.
4. Make the captions look how you like (see below).
5. Click **Save video with captions**, or export a subtitle file for your video editor.

That's it.

---

## What happens when you click "Create captions"

Your device uses a speech-recognition system called **Whisper** — the same kind of
technology used by many voice tools. It is a small "brain" that was trained to turn
speech into text. It runs on your own machine, so your file never leaves your device.

You can choose which version of Whisper to use. Bigger versions are more accurate but
slower; smaller versions are faster but less accurate:

| Choice in the app | Good for |
| --- | --- |
| **English · Small** (recommended) | Everyday English videos. Good speed and accuracy. |
| **Best accuracy · any language** | The highest quality, any language. Big download, needs a newer computer. |
| **Multilingual · Small** | Hindi, English, and other languages. |
| **Multilingual · Base** | A faster multilingual option. |
| **English · Tiny** | The fastest, for quick and simple jobs. |

If your video is in Hindi or another language, pick a **Multilingual** model and set
the **Language** to *Auto-detect*, *English*, or *Hindi*.

If your computer cannot use its graphics chip, the app quietly switches to the normal
processor. It still works — just a little slower.

---

## Making the captions look good

**Styles** — Pick one of 22 ready-made looks. Each one shows a small moving preview, so
you can see it before you choose. Names like *Bold pop*, *Karaoke*, *Typewriter*,
*Glitch*, *Cinema*.

**Customize** — Fine-tune the look:

- How many words show at once (1 to 6)
- Text size
- Where the text sits on screen (top, middle, bottom)
- Font (typeface)
- ALL CAPITALS on or off
- Whether words appear one by one as they are spoken
- Colors: the spoken word, the words already said, and the highlight box

**Speakers / people** — If two or more people talk, you can create a "person" for each
one with their own color, then select the words and tap that person to assign them.
The app does **not** guess who is speaking — you decide.

**Words and timeline** — Below, you can fix any word or timing by hand. Drag to move
captions, drag the edges to stretch them, or click to type a correction.

---

## Saving your work

You can save in several ways:

- **Save video with captions** — a new video with the captions built in. This records
  in real time, so keep the window open and on screen until it finishes.
- **SRT** or **WebVTT** — subtitle files that almost any video player or editor
  understands.
- **FCPXML** — for professional video editors (each caption becomes an editable clip).
- **TXT, JSON, CSV** — the plain text and the timings, for other uses.

You can choose how many words go in each subtitle, and set the frame rate to match your
editing program.

---

## Handy things

- **Undo / Redo** — the arrows at the top.
- **Light / dark mode** — the switch at the top.
- **Keyboard shortcuts** — press the **⌨ Shortcuts** button. Space to play or pause,
  arrow keys to move, and more. You can change any shortcut to whatever you like.
- The app remembers your theme, layout, style, people, and shortcuts for next time.

---

## Good to know

- **Private by design.** Your video and audio stay on your device. The only time the app
  uses the internet is the very first download of the speech model. After that, it can
  run offline.
- **Best in Chrome** (or another Chromium browser). Other browsers work too, but may be
  slower, and saving a video may not work in all of them.
- **The first run is the slow one.** The model is downloaded once, then kept by your
  browser for next time.

---

## The file

`caption-maker_6.2.html` — the whole app in a single file. Open it in a browser and
start captioning.
