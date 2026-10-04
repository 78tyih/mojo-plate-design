# mojo-plate-design

A reusable **design reference skill** distilled from [mojo.trade](https://www.mojo.trade/) —
the "engraved atlas" design language: near-black warm paper, bone-cream ink, one acid-lime
accent, Instrument Serif display italics, JetBrains Mono micro-labels, etched sunburst SVG
motifs, film grain, and `steps()` print-block animations.

**Live:** [Interactive showcase](https://78tyih.github.io/mojo-plate-design/showcase.html) (ZH/EN × light/dark, live replica) · [Replica full page](https://78tyih.github.io/mojo-plate-design/replica/index.html)

## Contents

```
mojo-plate-design/
├── SKILL.md                 # skill entry: when/how to apply the language
├── references/
│   ├── tokens.css           # full token set + core utility classes
│   ├── motifs.svg           # boil filter + sunburst/evstar/rule symbol library
│   └── sections.md          # 4 section blueprints + copy voice rules
├── assets/                  # vintage specimen plate crops (papillons / bugs / urania)
└── replica/                 # full working replica of mojo.trade (open index.html)
```

## Use as an agent skill

Copy the folder into your skills directory (`~/.config/agents/skills/`, `~/.kimi/skills/`,
or `.agents/skills/` in a project). The skill triggers when asked to build a landing /
waitlist / launch page in the mojo.trade "engraved atlas" style.

## Use by hand

1. Inline `references/motifs.svg` as the first child of `<body>`.
2. Link `references/tokens.css` (fix the three `--img-*` paths to point at `assets/`).
3. Follow `references/sections.md` for layout recipes, or crib from `replica/index.html`.

## Credits

Design reverse-engineered from https://www.mojo.trade/ for study and reference. The Mojo
wordmark and specimen illustrations belong to their respective owners; replace them before
any commercial use.

## 四问速览 · Four questions

| 问 | 答 |
|---|---|
| **Problem** | 想要 mojo.trade 那种「雕版图谱」质感时，每次都要从零逆向。本技能把整套语言工程化：token、motif、蓝图、文案腔调、replica 参照，一次提炼反复使用 |
| **Scenario → Outcome** | 交易/金融产品的 launch 页、waitlist 页、编辑感 hero——对 Agent 说「用 Mojo Plate 做」即得整套印刷纪律；手写时抄 tokens.css + sections.md 直接开工 |
| **Architecture** | SKILL.md（触发 + 非协商规则）→ references/tokens.css（全 token + 工具类）→ references/motifs.svg（boil 滤镜 + symbol 库）→ references/sections.md（四蓝图 + 文案腔调）→ replica/（完整成品） |
| **Value & Reuse** | ① 整包复制进 skills 目录即触发；② tokens.css 独立可用（换 accent 四件套一起换）；③ duotone 滤镜配方让任何图变标本版画；④ Plate I/II/III 图册叙事可套任何内容 |
