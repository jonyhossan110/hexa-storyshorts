# Production workflow — storyboard to published Short

Run the steps in order. Do not skip the storyboard: it is the cheapest place to catch a broken style, a changed character, or a wrong caption.

## 1. Script (from `script-formula.md`)

Deliver the package in the SKILL.md output format: title, style, and per beat — caption, narration, scene prompt. One mechanism only; shock first. Then break every beat into STEPS (one step per narration sentence or distinct action) — the steps are the real shot list.

## 2. Storyboard (one image)

- Generate the 2×2 storyboard with the chosen style's master prompt.
- Check before continuing: (a) same characters in all 4 frames, (b) captions spelled right and ≤5 words, (c) Beat 3 carries the red circle (both styles), (d) Style B — 4 visibly different backgrounds; Style A — white everywhere, red only in Beat 3.
- If a check fails, regenerate the storyboard, not the scenes.

## 3. Step images (one per step, 9:16)

- Generate each STEP as its own vertical image with the style's per-scene pattern, reusing character descriptions **verbatim** from the storyboard prompt.
- Keep the approved storyboard open as the visual reference for faces, clothes colors and the key object's design.
- File naming: `<slug>-step1.png … <slug>-stepN.png` plus `<slug>-storyboard.png`.
- **Assembly may not begin until every step has an image.** A missing step image is generated, never faked: do not animate, stretch, crop-zoom or repeat another image to cover a missing step.

## 4. Voice

- Narration text = the script's narration lines, exactly as written.
- Default voice: calm male AI narrator. Recommended free route: Google AI Studio Gemini TTS (current Flash TTS model), TTSMaker as backup. Never use a free-tier voice whose licence forbids monetised use.
- Pace: natural storytelling, slight pause between beats. Total Short runtime target 40–55 s; if the voice runs long, trim narration words — never speed the voice up.

## 5. Captions

- Burn in **bold word-by-word captions from 0:01** (the caption-bar sentence, revealed word by word in sync with the narration). Viewers decide in the first 2 seconds, with the sound usually off.
- The static caption bar text and the burned-in captions must match exactly.

## 6. Assembly — step by step, exact images, NO motion

**The law: the finished video is the step images in order, each shown FULL-FRAME and STATIC for exactly its narration segment, joined by HARD CUTS only.**

- FORBIDDEN on stills: zoom/pan (ffmpeg `zoompan`), Ken Burns, parallax, drift, slow push-in, crossfades/dissolves, speed ramps. Motion effects on a still break the step-by-step clarity — the STORY moves by changing images, never by moving one image.
- Timing comes from the REAL voice audio: split the audio by narration lines; each step image lasts exactly its line (a step covering two lines lasts both). Never pad a step to a round number of seconds.
- ffmpeg pattern: one input per image (`-loop 1 -t <step seconds>`), each scaled/padded to 1080×1920 (`scale=1080:1920:force_original_aspect_ratio=decrease,pad=1080:1920:(ow-iw)/2:(oh-ih)/2`), concatenated in order, voice track added last. No `zoompan` anywhere in the filter chain.
- The image on screen must be the exact generated image — no cropping into it, no colour shift, no motion graphics moving on top of it (the burned-in captions excepted).
- Music: one quiet background track from a royalty-free library, low under the voice; same track across a series for identity.
- Export: 1080×1920, vertical, captions inside the safe area (caption bar at ~78–85% height, clear of the platform UI at the bottom).

### Agent instruction block (paste into Antigravity or any assembly agent)

```
Follow the hexa-storyshorts production-workflow assembly law exactly.
Build the video from the step images in this workspace, in order:
- Each image appears FULL-FRAME and STATIC for exactly the duration of its narration line in the voice track (measure the real audio; split by the script's lines).
- HARD CUTS only between images.
- Do NOT apply zoom, pan, Ken Burns, zoompan, parallax, crossfade or any other motion or transition effect to any image. Do not crop or recolour the images.
- Before assembling, list the steps from the script and check that an image exists for EVERY step. If a step image is missing, STOP and tell me which step is missing — do not fill the gap by animating or repeating another image.
- Output final.mp4 (1080x1920, 30 fps, H.264 + AAC) and verify with ffprobe.
```

## 7. QC checklist (all must pass before upload)

- [ ] Step-by-step test: every narration line has its own image; the image changes exactly when the story moves
- [ ] No-motion test: no zoom, pan, drift or transition effect on any still; every cut is a hard cut to a NEW image
- [ ] Step count = image count; no image repeats or stretches to fill time
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
