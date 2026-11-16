# Style A — Whiteboard Doodle

Reference image: `../examples/router-storyboard-style-a-whiteboard.png` — study it before generating.

## Look

- Hand-drawn **black marker on clean white**, thick confident outlines, stick figures with round heads and simple expressive faces.
- Lots of white space. Nothing shaded, nothing grey-washed; props are single-line doodles (router = box + two antennae + dots).
- **Exactly ONE color accent in the whole video: red**, used once — in Beat 3, to circle/arrow the mechanism (the password, the open setting, the hidden toggle). Red never appears anywhere else.
- Caption bar: solid black strip at the bottom of every frame, bold white ALL-CAPS text, max 5 words.

## Characters

- Heroes: a stick-figure family/person — same heads, same hair marks, same clothes marks in every frame.
- Threat: a stick figure with a laptop and a grin (hoodie scribble + backpack identifies the stranger in every appearance).
- Describe each character once in the production notes and reuse the description **verbatim** in every prompt.

## Composition rules

- One idea per frame; the frame's hero object is large and centered (the router fills Beat 3).
- Show connections as dotted lines (Wi-Fi line from router to stranger). Show defeat as the dotted line snapping/breaking.
- Emotion is drawn, not captioned: Zzz for asleep, sweat drops for shock, thumbs up for payoff.

## Master storyboard prompt (paste, then replace the bracketed parts)

```
One single storyboard image: a 2x2 grid of four vertical 9:16 phone-video frames, minimal stick-figure whiteboard doodle style, thick black marker lines on a clean white background, like screenshots from one simple animated YouTube Short. The ONLY color in the whole image is one red marker circle in frame 3. Same [hero description] and the same [key object description] in every frame. Very large, bold, easy-to-read caption bars at the bottom of each frame: black bar, white capital letters. Frame 1 (the shock first): [shock scene], caption '[CAPTION 1]'. Frame 2 (the cause): [cause scene], caption '[CAPTION 2]'. Frame 3 (the mechanism): extreme close-up of [mechanism object], circled twice in bright red marker with a red arrow pointing at it, caption '[CAPTION 3]'. Frame 4 (the payoff): [payoff scene — fix being done, threat defeated], caption '[CAPTION 4]'. Simple, charming, lots of white space, no other text anywhere.
```

## Per-scene prompt pattern (for the individual 9:16 frames)

```
Vertical 9:16 frame, minimal stick-figure whiteboard doodle style, thick black marker lines on a clean white background. [Character descriptions verbatim]. Scene: [this beat's single scene]. A solid black caption bar at the bottom with bold white capital text: '[CAPTION]'. [Only in Beat 3: The word/object '[mechanism]' is circled twice in bright red marker with a red arrow — the only color in the image.] No other text anywhere.
```

## When to choose Style A

- Fastest production, maximum clarity, smallest generation cost.
- Best for: single-object stories (router, password, one app, one setting), first tests of a new series, and any topic where the mechanism is a single visible thing.

## Failure modes to check

- Extra colors sneaking in (reject — only the one red accent).
- Captions longer than 5 words or misspelled (regenerate the frame; never ship a wrong caption).
- The stranger/hero changing design between frames (restate descriptions verbatim and regenerate).
