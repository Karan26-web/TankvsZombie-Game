# Tank vs Zombie — Angle Academy (game only)

The game on its own: the opening story, five rounds of finding the angle with
sin, cos and tan, and the ending in the safe zone. A single static page — no
build step, nothing to install.

This is the **game-only** build. The complete project, which also carries
the learning section that NEXT opens after the story, its design documents
and its asset tools, is kept separately; this copy differs from it only in
leaving the lesson out (`LESSON_SRC = null` in `index.html`).

## Run it

Serve the folder and open it — any static server will do:

```
python3 -m http.server 8000      # then http://localhost:8000
```

`?lan=hi` picks the language (`en hi mr te or gu`).

## Deploy

It deploys to Vercel as a static site: import the repository at
https://vercel.com/new — framework preset **Other**, no build command, no
output directory — and every push to `main` redeploys it.

## What's in it

- `index.html` — the whole game
- `i18n/strings.json` — every line of screen text, in six languages
- `assets/` — the art (WebP) and the commander's voice-over (Ogg Opus,
  `assets/vo/<lang>/`; English is recorded)

## Voice and browsers

The voice-over is Ogg Opus. It plays in Chrome, Edge, Firefox and on
Android; Safari plays Ogg only from 18.4 (iOS 18.4). Where a browser can't
play it (older iPhones and iPads, or a language not yet recorded), the game
carries on without her voice, pacing her lines by their length instead.
