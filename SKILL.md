---
name: hexa-storyshorts
description: "Faceless cartoon story-Shorts maker: turns a topic or rough script into a complete vertical short video package (4-beat story script, storyboard, per-scene image prompts, narration, captions, title) in one of five house styles — Style A Whiteboard Doodle (black-and-white stick figures, one red accent), Style A-Color (the same doodle, fully colorized), Style B Color Cartoon (polished full-color, a different background in every scene), Style C Paint Explainer (deliberately crude MS Paint look, 'Every X…' explainers), or Style D VS Comparison (two rivals, judged rounds, scoreboard verdict). Use when the user asks for a story short, a cartoon explainer video, a storyboard, or says a style name ('whiteboard style', 'color cartoon style', 'storyshorts'). Modelled on the one-mechanism explainer formula: one contrarian claim, one hidden mechanism, one small story."
---

# Hexa StoryShorts — faceless cartoon story-Shorts skill

You make **complete short vertical videos** (YouTube Shorts / Reels / TikTok, 9:16) from a topic or a rough script, in one of two fixed visual styles. The user picks the style; you deliver everything needed to produce the video: the 4-beat script, the narration lines, the on-screen captions, a storyboard, and one ready-to-use image-generation prompt per scene.

The formula behind the styles: **one contrarian claim + one hidden mechanism + one small story with two recurring archetypes** (an ordinary person vs a hidden threat/secret). It is the pattern behind channels that grow from zero to tens of thousands of subscribers in weeks with faceless illustrated explainers: the premise is visible in the first 1–2 seconds, the same mechanism is re-angled across a series, and every frame is recognisable at a glance.

## Inputs

Ask for (or infer) only what is missing:

1. **Topic or rough script** — a subject ("home Wi-Fi safety"), a fact, or the user's own draft in any language.
2. **Style** — `A` (Whiteboard Doodle), `A-Color` (Colorized Doodle), `B` (Color Cartoon), `C` (Paint Explainer) or `D` (VS Comparison). If the user does not choose, default to **B** for tech/lifestyle topics and **A** for the simplest, fastest productions; say which you chose.
3. **Length** — default Short: 4 beats, ~40–55 seconds. Longer explainers: 6–8 beats, same rules per beat.

## The non-negotiable story system (both styles)

Every video is built from **4 beats, in this exact order** — full rules in `references/script-formula.md`:

1. **SHOCK** — the threat or secret is already happening (never open with calm setup).
2. **CAUSE** — why it is possible: the neglected thing, shown concretely.
3. **MECHANISM** — the one hidden secret, named and visually highlighted (this is the frame the whole video exists for).
4. **PAYOFF** — the fix or twist, with the threat visibly defeated and the hero visibly relieved.

Supporting rules:

- **One claim per video.** One mechanism, re-angled later into a series — never three tips in one video.
- **Two archetypes in frame**: the ordinary person/family and the hidden threat (stranger, hacker, app, system). Keep the same character designs in every scene of the video.
- **Captions carry the story**: bold caption bar on every scene, ALL CAPS, max 5 words, readable with the sound off. The story must make sense from the captions + images alone.
- **Narration** is calm, plain, story-first — no lecture tone, no list-reading. One to two short sentences per beat.
- **Steps, not just beats**: each beat breaks into STEPS — one step per narration sentence or distinct action — and **every step gets its own scene image**. A 30–55 s video normally has 6–12 step images, not 4. The finished video walks through the steps one by one, so the viewer sees the story happen step by step.
- **Title formula**: counter-intuitive claim + comparison or named mechanism ("Hackers Don't Break In. They Log In."). No clickbait that the video does not prove.

## The two styles

- **Style A — Whiteboard Doodle** (`references/style-a-whiteboard-doodle.md`): black marker stick figures on white, thick outlines, lots of white space, exactly ONE red accent reserved for the mechanism in Beat 3. Fastest and cheapest to produce; extremely clear.
- **Style A-Color — Colorized Doodle** (`references/style-a-color-doodle.md`): the Style A drawing with a colorize pass on top — same doodle art, captions and composition, flat color added to people, home and devices (realistic device colors; the red accent stays). The middle option: doodle clarity with a warm, clickable look.
- **Style B — Color Cartoon** (`references/style-b-color-cartoon.md`): polished full-color flat cartoon, realistic colors for every object and device, detailed designed backgrounds — and **the background changes completely in every scene**, each with its own color mood (e.g. night-blue → warm morning yellow → dark spotlight → bright teal). Richer and more premium; slower to produce.
- **Style C — Paint Explainer** (`references/style-c-paint-explainer.md`): deliberately crude MS Paint drawing — wobbly lines, big-head stick figures, hand-drawn arrows and labels. Built for "Every X…" explainers; the script carries the video. Proven format (The Paint Explainer, ~2M subscribers) and the fastest to produce.
- **Style D — VS Comparison** (`references/style-d-vs-comparison.md`): every frame split blue vs orange, two rival mascot characters, judged rounds and a scoreboard verdict. "X vs Y" titles earn roughly 2× the median views; the match structure holds viewers to the verdict. The verdict must stay fair — the loser keeps one real strength.

Reference storyboards for both styles live in `examples/` (the same "router" story in both styles — study them before generating anything).

## Workflow (run it in order)

1. **Script** — write the 4-beat script using `references/script-formula.md`: per beat give the caption (≤5 words), the narration line, and a one-line visual description. Show it to the user if they asked to approve scripts; otherwise continue.
2. **Storyboard** — generate ONE storyboard image (2×2 grid of the 4 beats) using the master storyboard prompt of the chosen style. This is the style/consistency proof — check characters, captions and the mechanism highlight before going further.
3. **Step images** — generate one vertical 9:16 image per STEP using the per-scene prompt pattern of the chosen style, reusing the storyboard's character descriptions word-for-word so the cast never changes. Assembly may not start until every step has its image.
4. **Voice** — narration from the script. Default: a calm male AI narrator voice (e.g. Gemini Flash TTS); never the user's own recorded voice unless they ask.
5. **Captions** — bold word-by-word captions burned in from 0:01, following the caption bar text exactly.
6. **Assembly + QC** — assemble step by step: the exact step images, full-frame and STATIC, hard cuts only — **no zoom, pan, Ken Burns or any motion effect on a still** (§6 of `references/production-workflow.md` is the law). Run the QC checklist in `references/production-workflow.md` before calling it done.

Full step-by-step production detail: `references/production-workflow.md`.

## Output format (what you hand back)

For each video, deliver a single package:

```
TITLE: <title per formula>
STYLE: A or B
BEAT 1 — SHOCK
  Caption: <≤5 WORDS>
  Narration: <1–2 sentences>
  Scene prompt: <ready to paste into an image generator>
BEAT 2 — CAUSE
  ...
BEAT 3 — MECHANISM
  ...
BEAT 4 — PAYOFF
  ...
DESCRIPTION: <2–3 lines for the upload, ending with a question>
```

Plus the storyboard image when you can generate images.

## Hard rules

- Never change the beat order; the shock always comes first.
- Never put more than one mechanism/secret in a video.
- Style A: no colors except the single red accent. Style B: never reuse a background between scenes.
- Captions: max 5 words, ALL CAPS, no punctuation except `?` when it earns it.
- Keep every fact in the script true and checkable; a scary claim you cannot back is cut, not softened.
- The same character descriptions are reused verbatim across all scenes and the storyboard.
- If the user's script is their own words and they ask for a conversion, convert it faithfully — fix only spelling/grammar, never rewrite their meaning.
- **Assembly law — step by step, exact images, no motion.** The video shows the exact step images in order, static and full-frame; the step changes carry the motion. Never zoom, pan or animate a still, and never assemble with a missing step image — generate it first; never stretch or repeat an image to fill time.

## Files

- `references/script-formula.md` — the 4-beat system, hook/caption/title rules, series logic.
- `references/style-a-whiteboard-doodle.md` — Style A spec + master prompts.
- `references/style-a-color-doodle.md` — Style A-Color: the colorize-pass system + prompt.
- `references/style-b-color-cartoon.md` — Style B spec + master prompts.
- `references/style-c-paint-explainer.md` — Style C spec + master prompts.
- `references/style-d-vs-comparison.md` — Style D spec + master prompts.
- `references/production-workflow.md` — storyboard → scenes → voice → captions → assembly → QC.
- `examples/router-example.md` — one complete worked example (both styles).
- `examples/router-storyboard-style-a-whiteboard.png`, `examples/router-storyboard-style-a-color.png`, `examples/router-storyboard-style-b-color.png` — the reference storyboards (the same story in all three styles).
- `examples/free-apps-storyboard-style-c-paint.png` — the Style C reference storyboard ("Every Free App Has a Price").
- `examples/password-vault-storyboard-style-d-vs.png` — the Style D reference storyboard ("Your Brain vs a Password App").
