# Tank vs Zombie — Angle Academy (game only)

The game on its own: START, and the tank rolls straight up to the first
zombie — five rounds of finding the angle with sin, cos and tan, on three
shells for the mission, and the ending in the safe zone. A single static
page — no build step, nothing to install.

This is the **game-only** build. The complete project is kept separately:
it also opens with the commander's story (the fly-over, her hatch scene and
the triangle's sides), hands over to the learning section after it, and
carries the design documents and asset tools. Neither the story nor the
lesson is in this copy.

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
carries on without her voice: her lines still show on screen.
