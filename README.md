# SomaForm

**Poolside swimming technique analysis powered by AI.**

SomaForm uses your phone camera and the Claude AI vision API to analyse swimming technique in real time — grounded in the biomechanical framework of Dr. Ernest W. Maglischo (*Swimming Fastest*, 2003).

No app store. No subscription. Just open the HTML file, add your Anthropic API key, and start coaching.

---

## What it does

Point your phone at the end of the lane (front camera facing down the pool on a clear stand). SomaForm watches the swimmer approach the wall, turn, push off, and break out — then gives you instant feedback as simple, colour-coded cards:

- 🟢 **Good** — technique is solid
- 🟠 **OK** — minor adjustment needed
- 🔴 **Work on** — key area to focus on

Each card shows:
- A thumbnail of the actual rep frame analysed
- A simple diagram of the correct vs. observed body position for that phase
- A plain-English coaching cue (no jargon — as if you're standing poolside)
- A one-sentence observation of what was seen and why it matters

Phases analysed: **Approach · Into Wall · Turn · Push-Off · Breakout**

---

## Two versions

### `index.html` — Upload & Analyse
Upload a video or image from your camera roll. Best for reviewing saved footage or testing the tool.

### `somaform-live.html` — Live Session
Uses your phone camera with automatic motion detection. When a swimmer enters frame, SomaForm captures the rep and analyses it automatically. View feedback by skill (Freestyle, Backstroke, Breaststroke, Butterfly, Turn, Push-Off) with Last Rep / Average / Best / Worst breakdowns.

---

## Setup

1. Get an [Anthropic API key](https://console.anthropic.com/) — you'll need a Claude account
2. Clone or download this repo
3. Open `somaform-live.html` in Chrome on your phone (or deploy to a static host — see below)
4. Enter your API key on the setup screen
5. Mount your phone at the end of the lane on a clear stand, front camera facing the pool
6. Tap **Start Session**

> **Note:** The live camera version requires HTTPS for camera access. For poolside use, deploy to a static host (Netlify, GitHub Pages, etc.) rather than opening as a local file.

---

## Deployment (recommended for poolside use)

The easiest option is [Netlify Drop](https://app.netlify.com/drop) — drag the folder in and you get an instant HTTPS URL. Free tier is plenty.

Or connect your GitHub repo to Netlify and every push auto-deploys.

---

## Phone stand setup

Mount your phone at the end of the lane with:
- Front camera **and** screen facing down the lane
- Height roughly level with the water surface or slightly above
- A clear acrylic phone stand works well and doesn't block the view

---

## Framework

SomaForm's analysis is grounded in the work of **Dr. Ernest W. Maglischo** — *Swimming Fastest* (2003) — widely considered the definitive biomechanical reference for competitive swimming coaching. Phase benchmarks, turn mechanics, push-off depth, and breakout timing are all evaluated against Maglischo's documented principles.

---

## Tech

- Vanilla HTML/CSS/JS — no build step, no dependencies, no framework
- [Claude claude-sonnet-4-20250514](https://anthropic.com) vision API for image analysis
- Motion detection via canvas pixel diffing (no ML library required)
- Runs entirely in the browser — your video never leaves your device except as a single frame sent to the Anthropic API

---

## License

AGPL v3 — see `LICENSE` for details.

Free to use, modify, and self-host. If you build something with it, share it back.

---

## Feedback

Built by Mike Cardno. Questions, bugs, ideas, or footage you want analysed — reach out:

📧 **michael.cardno@gmail.com**
https://www.linkedin.com/in/mikecardno/

Pull requests welcome.
# SomaformFOSS
