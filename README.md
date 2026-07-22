# Color-Matching Art Consultant

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-3.0.1-green.svg)](CHANGELOG.md)
[![Type: Agent Skill](https://img.shields.io/badge/type-agent%20skill-8A2BE2.svg)](#installation)

An AI agent skill for **color matching, palette construction, and pigment mixing** — for painting, illustration, concept art, interiors, and design.

It reasons like a hybrid of a color theorist, a notation-minded systematist, a working painter, a palette designer, and a careful visual historian. It leads with plain, actionable advice, reaches for technical language only when that sharpens precision, and treats paint, print, screen, and ambient light as genuinely different worlds.

---

## What it does

Give it a color, a palette, an artwork description, a mood, or a failing paint mix, and it will:

- **Build palettes** with every color assigned a structural role — anchor, accent, bridge, neutral, shadow, highlight, temperature balancer — plus rough proportions.
- **Diagnose failing mixes** ("my purple keeps coming out muddy") through pigment bias, medium behavior, and complementary-neutralization logic.
- **Explain perceptual effects** — simultaneous contrast, afterimage, "one color looks like two," value deception, buzzing and dissolving edges.
- **Translate vague descriptions** — "dusty blue," "ceremonial red," "older gold" — into structured hue / value / chroma terms.
- **Add situated historical notes**, drawn from ~75 color biographies, only when they improve the recommendation.

It always separates the three registers that get confused in color advice: **visual interaction** (the surround changed what the eye reports), **paint mixture** (the pigment physically changed), and **historical association** (a culture in a period meant something by it).

### Six recommendation modes

| Mode | For |
|---|---|
| Quick Match | "What goes with this?" — 1–3 pairings, fast |
| Studio Critique | Analyzing an existing palette or artwork and proposing fixes |
| Paint-Mixing Troubleshooting | Muddy, dull, or wrong-temperature mixes |
| Historical Palette Advisor | Period- or culturally-grounded palettes |
| Munsell-Style Formal Analysis | Precise hue/value/chroma description and comparison |
| Harmony Exploration | Several palette options across harmony families |

---

## Repository structure

```
.
├── README.md
├── LICENSE
├── CHANGELOG.md
├── .gitignore
└── color-matching-art-consultant/       ← the skill itself (upload this folder)
    ├── SKILL.md                          ← operating logic, §1–§12
    ├── reference-pigment-mixing.md
    ├── reference-color-histories.md
    ├── reference-perception-interaction.md
    ├── reference-notation-measurement.md
    └── reference-harmony-palette.md
```

`SKILL.md` is deliberately lean (~200 lines) and orchestration-focused. The deep content lives in five companion reference files — one per source book — that the agent loads **only when a request needs that book's depth**. This is the progressive-disclosure pattern: small always-loaded file, heavy content on demand.

> **Note:** the reference files cross-reference each other by bare filename. Keep all six files in the same directory.

### The five reference files

| File | Covers |
|---|---|
| `reference-pigment-mixing.md` | Named pigments and their biases, clean-vs-muddy secondaries, neutrals and darks, tints/shades/tones, per-medium behavior, target-color recipes, a troubleshooting table |
| `reference-color-histories.md` | ~75 situated color biographies across ten color families |
| `reference-perception-interaction.md` | Simultaneous contrast, afterimage, "one color as two / two as one," value deception, vibrating and vanishing boundaries, composition diagnostics |
| `reference-notation-measurement.md` | The 10-hue wheel, value and chroma scales, true complementary pairs, area balance, estimating `H V/C` from a plain description, and when *not* to force notation |
| `reference-harmony-palette.md` | Harmony families with build steps and watch-outs, proportion and accent ratios, warm-advance/cool-recede logic, mood associations framed as suggestive |

---

## Installation

### Claude (Skills)

Zip the skill folder and upload it:

```bash
zip -r color-matching-art-consultant.zip color-matching-art-consultant/
```

Then add it via **Settings → Capabilities → Skills** in the Claude app, or drop the folder into your skills directory for Claude Code:

```bash
git clone https://github.com/<your-username>/color-matching-art-consultant.git
cp -r color-matching-art-consultant/color-matching-art-consultant ~/.claude/skills/
```

The skill triggers on its own when a request matches its `description` — you don't have to invoke it by name.

### Any other LLM

`SKILL.md` §12 contains a self-contained **Final Skill Prompt** you can paste directly as a system prompt. Provide the reference files as attachments, retrieval documents, or context files so the model can consult them on demand.

---

## Design constraints

The skill is defined as much by what it refuses to do:

- **No fake precision.** It will not invent exact pigment names, brand formulations, or Munsell/hex codes that can't be reliably inferred. Asked for the exact hex of Vermeer's ultramarine, it declines and explains why any single value would be fabricated.
- **No universalized symbolism.** Color meanings are stated as situated — "in this culture, in this era" — never as global truths.
- **No medium-agnostic mixing advice.** A watercolour mix is not an oil mix is not a screen blend.
- **No confusing subtractive with additive.** In paint, red + green make a dull near-neutral; on screen they make yellow.
- **Value before hue.** Value structure is checked first, always.
- **No vague praise.** "This palette feels nice" without a reason is a failure mode, not an answer.

---

## Sources and attribution

The skill and its references are **original distillations** — synthesized concepts, restated in new language — of ideas from five books. They contain no reproduced text from those works, and are not a substitute for reading them:

- Josef Albers, *Interaction of Color* (Yale University Press, 2013 ed.) — the perception layer
- A. H. Munsell, *A Color Notation* (1905) — the notation layer
- Ian Sidaway, *The Color Mixing Bible* (Quarto, 2002) — the mixing layer
- Tina Sutton, *The Complete Color Harmony, Deluxe Edition* (2024) — the harmony layer
- Kassia St. Clair, *The Secret Lives of Color* (John Murray, 2017) — the historical/cultural layer

Attribution inside the reference files is kept at chapter/concept level so claims stay traceable to a source rather than reading as generic color theory. All named pigments are behavioral examples, not brand guarantees.

---

## Versioning

This project follows [Semantic Versioning](https://semver.org/). The current version lives in `SKILL.md` frontmatter (`metadata.version`) and the history is in [CHANGELOG.md](CHANGELOG.md).

Because the architecture is one reference file per book, updates are usually local: swapping a source or re-distilling one layer touches one file, not the whole skill.

---

## Contributing

Issues and pull requests are welcome. Useful contributions include:

- Corrections to pigment behavior, historical claims, or notation
- Additional worked examples in `SKILL.md` §10
- Failure cases where the skill over-reaches, gives false precision, or universalizes a cultural claim

Please keep `SKILL.md` lean — new depth belongs in a reference file, with a pointer added from §4 and §8.

---

## License

Released under the [MIT License](LICENSE). Copyright © 2026 Ariel Lee.

The license covers this repository's original text. It does not extend to the underlying source books, which remain the property of their respective copyright holders.
