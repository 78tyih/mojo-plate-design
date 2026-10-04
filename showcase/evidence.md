# Evidence — mojo-plate-design

Updated: 2026-10-05

## Observed（实查）

| 声明 | 证据 |
|---|---|
| 八条非协商规则 | SKILL.md「Non-negotiables」原文（palette/type trio/print framing/no radius/hard shadows/steps/grain/boil/copy voice） |
| 色板四值 | references/tokens.css：--paper #0b0b09 / --ink #e9e5d4 / --lime #cdf546 / --terra-deep #b8e032 |
| 四个 section 蓝图 | references/sections.md 目录：Plate I hero / Plate II celestial timeline / Colophon / Plate III inverse-accent CTA |
| replica 自包含 | replica/index.html 仅引用同目录三张 jpg + Google Fonts（grep 核对，无 ../ 引用） |
| 在线渲染 | docs/replica/ 副本经 GitHub Pages 提供服务；showcase iframe 直接加载（上线后 curl 200 核验） |
| 标本图版素材 | assets/（→docs/replica/）papillons.jpg 340K / bugs.jpg 336K / urania.jpg 220K；replica hero .spec-l/r、时间线 .urania-card、CTA .chip 印章三处实际使用 |
| 标本图版 + duotone 在线演示 | showcase.html 03 · SPECIMEN PLATES：三张图版卡（.spec 同款奶油衬底/双细线框/硬偏移阴影/歪斜）+ chip-duotone 滤镜实时开关演示（配方逐字取自 tokens.css 77–83 行；headless 截图核验渲染） |
| 商用替换声明 | README Credits 节 + SKILL.md：字标与插图归原作者，商用前替换（showcase 03 节亦注明） |

## Inferred（推断，附复核方式）

| 声明 | 复核方式 |
|---|---|
| 「换 accent 四件套一起换」 | SKILL.md Adaptation knobs 自述（--lime/--terra/--terra-deep/--gold 联动）；未逐行验证全部引用点 |
| duotone 滤镜配方适配任意图 | **已升级为 Observed**：showcase 03 节用 bugs.jpg 实测渲染（filter:grayscale(1) invert(.94) sepia(.9) saturate(2.6) hue-rotate(33deg) contrast(1.06) + mix-blend-mode:screen），酸绿版画效果成立 |

## Unknown

- 技能被 Agent 实际触发并产出页面的端到端记录（仓库内无运行样例输出）
