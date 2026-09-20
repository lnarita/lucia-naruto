# Luc(IA) Naruto — emotion pack

A tiny ninja with big feelings. One SVG, six eye states, eight animations,
zero dependencies.

**[▶ Live character sheet](https://lnarita.github.io/lucia-naruto)** — every expression runs on the
vector rig, right in your browser. Nothing to install, nothing loaded from
anywhere.

## Expressions

| Animation | Plays | Notes |
|---|---|---|
| Surprise | once | smash-cut wide eyes, rays flicker |
| Angry stomp | once | anticipation → stomp, vein lands on impact |
| Happy bounce | loop | two decaying hops |
| Tired sigh | loop | eyes close before the sigh escapes — always |
| Idle blink | loop | one calm blink, then two rapid ones for personality |
| Good morning | once | slow surfacing, long calm tail |
| Tired → sleep | once | the second blink is heavier than the first |
| Fighting sleepiness loop | loop | drifts off, jolts awake, drifts off again |

## How it works

No GIFs, no video, no animation library. The page samples the six drawn eye
states at load time (`getPointAtLength`, 30 points each), then tweens between
them as raw polylines — a little path-morph engine in ~40 lines. On top of
that:

- **spring follow-through** on the hair tufts, driven by lagged head velocity,
  for anything with a jolt in it
- **staggered sine breeze** for the calm loops
- open eye shapes are auto-closed as out-and-back loops so morphs never curl
  the wrong way

The whole thing is one self-contained HTML file. View source; that's all of it.

## Palette

| | name | hex |
|---|---|---|
| 🟨 | sand | `#e0cda8` |
| ⬛ | ink | `#17191c` |
| 🟦 | sigh | `#e6f4fa` |
| 🟥 | vermilion | `#c9483a` |

Chosen to survive both light and dark mail clients. Warm surfaces are for
reading.

## Status

This is **v1** and the design is still in the making — expressions get recast,
geometry gets redrawn, and the model sheet will change under you. Please don't
build derivatives on wet paint; watch the repo instead and come see her when
she's settled.

## License

- **Code** (the player, the morph engine, everything in `<script>`):
  [MIT](LICENSE)
- **Character & artwork** (the SVG, the expressions, the GIF exports):
  [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) —
  share with credit, no commercial use, no derivatives (see **Status** for why,
  and feel free to ask)

---

*Her first name is a mishearing. Her surname is a typo. She has been gainfully employed ever since.*


