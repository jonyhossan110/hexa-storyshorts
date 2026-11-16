# Production workflow — storyboard to published Short

Run the steps in order. Do not skip the storyboard: it is the cheapest place to catch a broken style, a changed character, or a wrong caption.

## 1. Script (from `script-formula.md`)

Deliver the package in the SKILL.md output format: title, style, and per beat — caption, narration, scene prompt. One mechanism only; shock first.

## 2. Storyboard (one image)

- Generate the 2×2 storyboard with the chosen style's master prompt.
- Check before continuing: (a) same characters in all 4 frames, (b) captions spelled right and ≤5 words, (c) Beat 3 carries the red circle (both styles), (d) Style B — 4 visibly different backgrounds; Style A — white everywhere, red only in Beat 3.
- If a check fails, regenerate the storyboard, not the scenes.

## 3. Scene images (one per beat, 9:16)

- Generate each beat as its own vertical image with the style's per-scene pattern, reusing character descriptions **verbatim** from the storyboard prompt.
- Keep the approved storyboard open as the visual reference for faces, clothes colors and the key object's design.
- File naming: `<slug>-beat1.png … <slug>-beat4.png` plus `<slug>-storyboard.png`.

## 4. Voice

- Narration text = the script's narration lines, exactly as written.
- Default voice: calm male AI narrator. Recommended free route: Google AI Studio Gemini TTS (current Flash TTS model), TTSMaker as backup. Never use a free-tier voice whose licence forbids monetised use.
- Pace: natural storytelling, slight pause between beats. Total Short runtime target 40–55 s; if the voice runs long, trim narration words — never speed the voice up.

## 5. Captions

- Burn in **bold word-by-word captions from 0:01** (the caption-bar sentence, revealed word by word in sync with the narration). Viewers decide in the first 2 seconds, with the sound usually off.
- The static caption bar text and the burned-in captions must match exactly.

## 6. Assembly

- Beat order 1→4, each scene held for its narration (~10–13 s per beat in a Short).
- Simple push-in (slow zoom) on each still is enough motion; Beat 3 gets the slowest zoom — it is the reveal.
- Music: one quiet background track from a royalty-free library, low under the voice; same track across a series for identity.
- Export: 1080×1920, vertical, captions inside the safe area (not under the platform UI at the bottom — keep the caption bar above the lower fifth's bottom edge… in practice: bar sits at ~78–85% height).

## 7. QC checklist (all must pass before upload)

- [ ] Story understandable with sound OFF (captions + images only)
- [ ] Shock visible within the first 2 seconds
- [ ] Exactly one mechanism; Beat 3 highlight present
- [ ] Characters identical across all scenes
- [ ] Style rules kept (A: one red accent only · B: 4 different backgrounds, real object colors)
- [ ] Every factual claim in the script is true and checkable
- [ ] Title follows the formula and the video proves it
- [ ] Description: 2–3 lines + one question to the viewer
- [ ] 1% rule: name one thing this video does better than the previous one (pacing, hook, caption, background) and keep a log of it per series

## 8. Publishing notes

- Post the finished Short where the channel's audience actually is; keep the same title/caption system across platforms.
- Pin the first comment yourself: restate the mechanism as a question ("When did you last restart yours?") — comments are the cheapest reach.
- Log the video (date, title, style, mechanism, the 1% improvement) in the series tracker so the next angle of the same mechanism is easy to pick.
