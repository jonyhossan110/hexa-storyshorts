# Style A-Color — Colorized Doodle

Reference image: `../examples/router-storyboard-style-a-color.png` — the Style A router storyboard after the colorize pass. Study it alongside the black-and-white original (`router-storyboard-style-a-whiteboard.png`): the drawing is identical; only color was added.

## What it is

Style A-Color is not a separate drawing style — it is **Style A plus a colorize pass**. You keep the whiteboard doodle's simplicity, speed and clarity, and add flat color to everything: people, home, devices, sky. It exists for channels that find pure black-and-white too plain but do not want Style B's heavier, fully-rendered look.

## The system (two passes)

1. **Pass 1 — draw it in Style A.** Build the storyboard and scenes exactly per `style-a-whiteboard-doodle.md`: black marker doodle, white background, one red accent on the mechanism, black caption bars.
2. **Pass 2 — colorize, change nothing else.** Fill the existing art with color. The composition, characters, captions, caption bars and the red circle/arrow stay exactly as drawn. Only the fills change:
   - **People:** natural skin tones; hair in natural colors; each character keeps ONE signature clothes color across all frames (e.g. father green, mother pink, son yellow, stranger blue hoodie).
   - **Home & rooms:** warm wall tones, wooden browns for shelves/furniture, soft colors for sofa/blanket; night scenes get a deep blue sky through the window.
   - **Devices & objects:** realistic colors — grey/black router with green indicator lights, silver laptop, light-grey cobwebs, pale calendar with a blue grid.
   - **The red accent stays red** and stays unique to the mechanism — do not introduce a second red object competing with it (a small red reset button on the device itself is fine, it is part of the device's real colors).

## Colorize prompt (for an image-editing model, storyboard or single scene)

```
Colorize this exact black-and-white storyboard image. Keep the same drawing, the same frames, the same characters, the same captions and the same composition — change nothing about the art itself, just add colors to everything: the people's skin tones, hair and clothes in different natural colors, the home interior with warm wall and furniture colors, the router and laptop and every device in their realistic colors, the night sky through the window deep blue. Keep the red circle and red arrow around the mechanism red. Keep the black caption bars with white text exactly as they are. Flat cartoon coloring, clean and bright, like a hand-drawn doodle that has been fully colored in.
```

(For a single scene, replace "storyboard image / frames" with "frame" and name the scene's caption.)

## Direct-generation alternative

If the image model handles it well, Style A-Color can be generated in one pass by taking the Style A master/scene prompt and replacing "minimal stick-figure whiteboard doodle style, thick black marker lines on a clean white background" with "hand-drawn doodle style with thick black outlines, fully colored with flat bright colors, warm colored backgrounds". The two-pass route is more reliable: the doodle pass locks the story and captions, the colorize pass cannot break them.

## Rules

- Color is added **after** the storyboard is approved in black-and-white — never colorize an unapproved board.
- Character signature colors are fixed at the first colorized frame and reused verbatim in every later prompt of the series.
- Caption bars are never recolored: black bar, white text, always.
- If the colorize pass changes any caption letter, object or character design, reject it and re-run the pass — color is the only allowed change.

## When to choose Style A-Color

- You want Style A's clarity with a warmer, more clickable look.
- Thumbnails and first frames benefit most: the colorized Beat 1 frame is the strongest single image this style produces.
