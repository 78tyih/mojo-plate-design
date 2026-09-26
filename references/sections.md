# Section blueprints & copy voice

Four section archetypes make up the mojo.trade page. Each is a "Plate" in an engraved atlas.
Full working code: `../replica/index.html`.

## Contents
- Global chrome: loader, header, footer
- Plate I — Hero (framed specimen plate)
- Plate II — Celestial timeline
- Colophon — Letterpress statement
- Plate III — Inverse-accent CTA
- Copy voice rules

## Global chrome

**Loader**: full-screen paper background, centered wordmark in accent color +
`Atlas of Intent · MMXXVI` plate number; snaps out with `steps(4,end)` after load.

**Header**: fixed, 72px, paper bg, hairline bottom border + a second offset hairline
(`box-shadow: 0 3px 0 -2px ink-15` and an `:after` 4px lower — the "double rule" print
effect). Nav links: JetBrains Mono 11px, uppercase, letter-spacing .22em, 13px icon.

**Footer**: paper strip on top of the CTA, mono 10px uppercase meta line + icon links.

## Plate I — Hero

- `min-height:100svh`, centered content, double hairline frame inset
  (`border:1px solid #cdf5468c` + inner `:after` at 5px, `#cdf54638`).
- Two sunburst etchings positioned in opposite corners, 90s counter-rotating spins.
- Two tilted specimen cards (`rotate(-2.6deg / 2deg)`) cropping a vintage butterfly
  engraving, cream backing, hard offset shadow with accent tint (`6px 7px #cdf5461a`).
- Headline: Instrument Serif, `clamp(54px,9.6vw,124px)`, weight 400, line-height 1;
  one word italic in `--terra-deep`.
- Engraved `#rule` divider under headline, then Inter 300 subline in `--ink-60`.
- Email form: 1.5px ink border, paper-2 fill, serif italic placeholder, accent button
  with mono uppercase label; hard shadow `4px 4px #cdf54624`; button disabled until
  valid email. Mono 11px micro-note underneath.
- Scroll cue: 14×22 chevron, `cue-bob` steps animation.

## Plate II — Celestial timeline

- Background `--slate` (#10141f), bordered top/bottom by 2px ink rules.
- Faint graph-paper grid: 84px linear-gradient gridlines at 5% cream alpha.
- Tilted urania (star atlas) card, top-left, rotated -3deg, deep soft shadow.
- Events alternate left/right (`nth-of-type` margins), max-width 470px.
- Each event: `#evstar` marker (inner `.burst` spins 70s), mono timestamp
  (letter-spacing .3em), then serif description `clamp(23px,3vw,34px)` with one
  italic accent phrase.
- Stars connected by a dashed curved SVG path ("constellation") drawn at runtime
  between star centers — `stroke-dasharray:0.5 6`, accent at 33% alpha.

## Colophon — Letterpress statement

- Paper background, near-full viewport, centered.
- Two serif lines `clamp(40px,6.8vw,88px)`; second line italic in `--terra-deep`.
- Words split into spans, each snaps in with `steps(3,end)` and 45ms stagger when
  the section scrolls into view (IntersectionObserver, threshold .35).
- One faint sunburst at low opacity in a corner.

## Plate III — Inverse-accent CTA

- Full accent (`--lime`) background, near-black text `#0d0d0a`; 2px ink top border.
- 56px grid overlay at 10% black alpha.
- Insect-plate "chips": square crops of specimen engravings on cream backing,
  1px dark border, hard shadow `4px 5px #0b0b0973`, scattered and slightly rotated.
- Headline serif `clamp(50px,8.8vw,116px)`; italic word underlined (2px) instead of
  recolored — color emphasis is unavailable on accent bg.
- CTA button: near-black fill, accent mono uppercase text, hard shadow
  `5px 5px #23221c59`; hover translates (2px,2px) and shrinks the shadow.
- Giant wordmark watermark cropped at bottom (`translateY(16%)`, ink at 28% alpha).

## Copy voice rules

- Headlines: short declarative, one italic serif keyword: "Invest with *taste* mode.",
  "Your *edge* is waiting."
- Timeline events: second person, present tense, timestamp-led, under 20 words, last
  clause italic: "*Mojo had it ready in 2 seconds.*"
- Micro-copy is mono lowercase/uppercase mix and plainly factual:
  "Follow the X first. We will open waitlist for email registry later"
- Section captions are plate numbers: "Plate I", "Plate II — 24h with Mojo", "Colophon".
- Meta line is lowercase with em dash: "mojo — the agentic trading os".
