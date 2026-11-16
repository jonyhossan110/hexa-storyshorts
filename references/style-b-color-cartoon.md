# Style B — Color Cartoon

Reference image: `../examples/router-storyboard-style-b-color.png` — study it before generating.

## Look

- Polished **full-color flat cartoon**, bold outlines, warm friendly character designs (real faces, hair, clothes — not stick figures).
- **Realistic colors for every object and device**: a black router with green blinking lights and a red reset button; a silver laptop; an orange sofa. If it exists in real life, it wears its real color.
- **Detailed, designed backgrounds** — a living room has the sofa, lamp, TV, rug, plant and shelves; a street has houses and sky. No empty color-wash backgrounds.
- **The background changes completely in every scene**, and each scene carries its own color mood. Default mood ladder for a 4-beat story:
  1. Shock — deep blue/purple night (the threat thrives in the dark)
  2. Cause — warm yellow/orange morning light (ordinary, neglected everyday)
  3. Mechanism — dark charcoal with a single spotlight on the secret object
  4. Payoff — bright fresh teal/mint daytime (clean, safe, resolved)
- The mechanism in Beat 3 still gets the red circle + red arrow (borrowed from Style A) — it is the one graphic device shared by both styles.
- Caption bar: solid black strip at the bottom of every frame, bold white ALL-CAPS text, max 5 words — identical to Style A so a channel can mix styles.

## Characters

- Design the family/person once: age, hair, glasses, signature clothes colors (e.g. father in blue, mother in yellow). The threat character keeps one signature look (dark hoodie + beanie).
- Reuse the character description **verbatim** in every prompt, storyboard and scene.

## Composition rules

- Beat 1 must establish place AND threat in one frame (family asleep inside; stranger connected outside the window).
- Beat 3 is a close-up: the object fills the frame, spotlight, family small and worried at the edge.
- Beat 4 shows the fix being physically done (a hand pressing the button) and the threat's defeat in the same frame (red X / NO SIGNAL on his screen, visible through the door or window).
- Props tell time and neglect: calendar, clock, cobwebs, dust — drawn, not captioned.

## Master storyboard prompt (paste, then replace the bracketed parts)

```
One single storyboard image: a 2x2 grid of four vertical 9:16 phone-video frames, polished full-color flat cartoon style with bold outlines, like screenshots from one high-quality animated YouTube Short. IMPORTANT: every frame has a COMPLETELY DIFFERENT background scene and color mood. Same [family/hero description] and the same [key object with its real colors] in every frame. Very large bold caption bars at the bottom of each frame: black bar, white capital letters. Frame 1 background: [night scene, deep blue-purple, detailed room], [shock scene], caption '[CAPTION 1]'. Frame 2 background: [warm morning scene, yellow-orange light, detailed room], [cause scene with neglect props], caption '[CAPTION 2]'. Frame 3 background: dramatic dark charcoal scene lit by a single spotlight; extreme close-up of [mechanism object] with [mechanism text] circled twice in bright red with a red arrow, caption '[CAPTION 3]'. Frame 4 background: [bright teal-mint daytime scene], [payoff scene — fix being done, threat visibly defeated], caption '[CAPTION 4]'. Bright, clear, detailed, no other text anywhere.
```

## Per-scene prompt pattern (for the individual 9:16 frames)

```
Vertical 9:16 frame, polished full-color flat cartoon style with bold outlines, realistic colors for all objects and devices. Background: [this beat's unique scene + color mood, fully described — never reuse another beat's background]. [Character descriptions verbatim]. Scene: [this beat's single scene]. A solid black caption bar at the bottom with bold white capital text: '[CAPTION]'. [Only in Beat 3: the mechanism is circled twice in bright red with a red arrow.] No other text anywhere.
```

## When to choose Style B

- The channel's premium/main style; best perceived quality and strongest thumbnails.
- Best for: home/family stories, anything emotional, and series intended to run long (the changing backgrounds keep 20 episodes from looking identical).

## Failure modes to check

- Two scenes sharing a background or mood (regenerate — the change is the style's signature).
- Devices in fantasy colors (a purple router fails; restate real colors).
- Background detail swallowing the hero object in Beat 3 (the spotlight close-up must stay clean).
- Captions misspelled or over 5 words (regenerate the frame; never ship a wrong caption).
