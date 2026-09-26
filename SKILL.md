---
name: mojo-plate-design
description: "Engraved-atlas / plate-book design language distilled from mojo.trade — near-black warm paper, bone-cream ink, acid-lime accent, Instrument Serif display italics, JetBrains Mono micro-labels, etched sunburst/starburst SVG motifs, film grain, steps() stamp animations, and 'Plate I/II/III' sectioned narrative. Use when the user asks to design or build a landing page / hero / waitlist / launch page in the style of mojo.trade, an 'engraved atlas', 'botanical plate', 'celestial chart', 'letterpress dark editorial' aesthetic, or asks to reuse this design system, its tokens, motifs, or copy voice."
---

# Mojo Plate Design — Engraved Atlas Design Language

Design system reverse-engineered from https://www.mojo.trade/ ("Mojo — The Agentic Trading OS").
Treat the page as a **printed atlas of engraved plates**, not a SaaS landing: dark warm paper,
bone ink, one acid accent, specimen illustrations, plate numbers, and print-shop micro-copy.

## When building with this language

1. Copy [references/tokens.css](references/tokens.css) into the project — it is the full token
   set plus core utility classes (`.plate-cap`, `.stamp`, `.boil`, `.grain`, divider `.rule`).
2. Paste [references/motifs.svg](references/motifs.svg) as the first child of `<body>` — it
   defines the `boil` turbulence filter and the `<symbol>` library (`#sunburst`, `#evstar`,
   `#rule`). Reference with `<svg><use href="#sunburst"/></svg>`.
3. Follow [references/sections.md](references/sections.md) for the four section blueprints
   (hero plate, celestial timeline, letterpress colophon, inverse-accent CTA) and copy voice.
4. A complete working example lives in [replica/index.html](replica/index.html) — open it to
   see every pattern assembled. Plate illustration crops live in `assets/`.

## Non-negotiables (what makes it read as "Mojo")

- **Palette discipline**: near-black warm paper `#0b0b09`, bone ink `#e9e5d4`, ONE accent
  acid-lime `#cdf546` (used for rules, etchings, button fill, italic emphasis). Never add a
  second accent. Deep variant `#b8e032` for italic serif emphasis only.
- **Type trio**: Instrument Serif (display, italic accent words), Inter 300 (body),
  JetBrains Mono (micro-labels, ALL-CAPS, letter-spacing .22–.42em).
- **Print-shop framing**: sections are "Plates" (Plate I, Plate II …) captioned with
  `❦ PLATE N ❦` fleurons; hero is boxed by a double hairline frame; everything sits on
  1–1.5px hairlines, not cards with radius.
- **No border-radius anywhere.** Shadows are hard offset (`4px 4px`, `6px 7px`), never blurred.
- **Steps() easing**: entrances and hovers use `steps(2–4, end)` for a printed/flip-book
  feel — no smooth ease-out.
- **Film grain** overlay: fixed SVG turbulence layer, opacity .22, `mix-blend-mode: screen`.
- **Boil filter**: `feTurbulence + feDisplacementMap(scale 3.2)` on wordmark/etchings so
  lines look hand-etched.
- **Slow celestial spin**: sunburst/starburst motifs rotate over 70–90s linear infinite.
- **Copy voice**: terse, second-person, present tense; one italic serif keyword per headline
  ("Invest with *taste* mode.", "Your *edge* is waiting."); timestamps and monospaced
  micro-notes instead of marketing bullets.

## Adaptation knobs

- Accent swap: change `--lime`/`--terra`/`--terra-deep`/`--gold` together (original CSS also
  shipped a terracotta variant — same structure, warmer hue).
- Light inverse section: the CTA inverts to accent background with near-black text
  (`#0d0d0a`) — reuse this pattern for any final CTA.
- Specimen art: swap `assets/*.jpg` crops for any vintage botanical/entomological engraving;
  apply the duotone filter recipe in tokens.css (`.spec`, `.chip`) to make any image match.
