# game8 · minigame arcade

A collection of small HTML game prototypes. One file per game, no build step,
three.js from a CDN. Made to be hosted on GitHub Pages.

## Games

| # | Game | Pitch |
|---|------|-------|
| 01 | [Last Train Home](games/last-train-home.html) | First-person sprint through a tiny station before the doors close. Obstacles reshuffle every attempt. |
| 02 | [Sword With Too Much Momentum](games/sword-momentum.html) | Top-down dungeon crawler. Your mouse swings a sword three times your weight, and its momentum drags your knight around. Slay monsters, smash crates, descend. |
| 03 | [Stay On The Train](games/stay-on-the-train.html) | Remain standing in a violently moving subway carriage for 60 seconds. Everything has physics. PS1 visuals. Brace for the final stop. |
| 04 | [Squish Circuit](games/squish-circuit.html) | Time-trial racing as a squishy jelly ball. Tilt the whole world to roll around a neon sky-circuit; boost pads, sector splits, best lap saved locally. |
| 05 | [Brinewick](games/brinewick.html) | A misty seaside dock village. Open-world fish deliveries: take a parcel from the pier stall, find the recipient, keep it fresh. Foghorns, gulls, no fail state. |

Start at [`index.html`](index.html) — the main menu.

## Running locally

Any static file server works (ES modules don't load from `file://`):

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Hosting on GitHub Pages

Settings → Pages → "Deploy from a branch" → pick the default branch, folder `/ (root)`.
The site is plain static files; `.nojekyll` is included so nothing gets mangled.

## Tech

- [three.js](https://threejs.org/) `0.180.0` via jsDelivr import maps
- [cannon-es](https://github.com/pmndrs/cannon-es) `0.20.0` for the carriage physics in Stay On The Train
- All sound effects are procedural WebAudio — no asset files anywhere
- Each game is a single self-contained `.html` file; desktop + mouse recommended
