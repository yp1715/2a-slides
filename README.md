# MSK & Trauma — FRCR 2A Question Bank

A self-contained, image-based radiology question bank built from the *Musculoskeletal and Trauma* deck. 668 cases across seven sources, with score tracking, a review-misses mode, flagging, and progress that persists in your browser.

- **Auto-graded (189):** all of Masterpass (Papers 1–3) — true single-best-answer. Pick A–E and it grades instantly against the answer key.
- **Self-graded (479):** Afaq, Barrett, Currie, Get Through, Gupta, Lindsay — spot-diagnosis cases. Read the case, reveal the answer slide, mark yourself right or wrong.

## How to run it

The app loads images from the `img/` folder, so it must be **served over http(s)**, not opened as a `file://` path (browsers block that).

### Option A — GitHub Pages (recommended)
1. Create a new repository and upload the whole folder (`index.html`, `questions.js`, `img/`, `README.md`).
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick `main` / root, save.
3. Wait ~1 min, then open the URL it gives you (`https://<you>.github.io/<repo>/`).

### Option B — Run locally
From inside the folder:
```
python3 -m http.server 8000
```
Then open `http://localhost:8000`.

## Controls
- **A–E** or **1–5** — answer (auto-graded cases)
- **Space / R** — reveal answer (self-graded cases), then **Y/N** to mark
- **← / →** — previous / next case
- **F** — flag a case
- Source and Paper dropdowns filter the set; the shuffle and reset icons are top-right.

## Notes on accuracy
- Masterpass answer keys were extracted by OCR from each answer slide and spot-checked, but it's worth a sanity check as you go.
- Spot-diagnosis pairing (question → answer slide) was done automatically; the odd mis-pair is possible. Use the flag button to mark anything that looks off.
- Some answers span more than one slide — use the ‹ › pager that appears on the answer view.

Built from a 1,596-slide source deck. Question/answer images are downscaled screenshots of the original slides.
