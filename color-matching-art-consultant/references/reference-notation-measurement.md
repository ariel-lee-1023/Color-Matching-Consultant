# Reference — Notation & Measurement

> Companion reference for the **Color-Matching Art Consultant** skill. Distilled from A. H. Munsell, *A Color Notation* (1905). Attribution is at chapter/concept level. This file is the disambiguation-and-comparison scaffold: it turns vague color talk into three measured dimensions and back again. The parent skill points here from its Notation layer (§4) and from Munsell-Style Formal Analysis mode (§8). Deploy it *lightly* — as a communication tool, never as a technical tax (see §8 below).

**Contents**
- [§1. The three measured dimensions](#1-the-three-measured-dimensions)
- [§2. The notation form `H V/C`](#2-the-notation-form-h-vc)
- [§3. The 10-hue wheel](#3-the-10-hue-wheel)
- [§4. The value scale](#4-the-value-scale)
- [§5. The chroma scale (and why it's uneven)](#5-the-chroma-scale-and-why-its-uneven)
- [§6. Sphere and tree; warm/cool with green at center](#6-sphere-and-tree-warmcool-with-green-at-center)
- [§7. Complementaries, balance, and area](#7-complementaries-balance-and-area)
- [§8. Estimating `H V/C` from a plain description](#8-estimating-h-vc-from-a-plain-description)
- [§9. When notation should NOT be forced](#9-when-notation-should-not-be-forced)

---

## §1. The three measured dimensions

Every color resolves into three independent, measurable scales (Munsell, Ch. I–II, "Color has three dimensions"). Leaving any one out leaves the color undefined:

- **Hue** — *the name of a color* (red vs. yellow vs. blue…). Says nothing about light or strength (Munsell, Ch. II).
- **Value** — *the light of a color* (how light or dark). Places the color between black and white (Munsell, Ch. II).
- **Chroma** — *the strength of a color* (how strong or weak, saturated or grayed). Its departure from neutral gray (Munsell, Ch. II).

The point of measuring all three is to escape the "topazy yellow / dull red" problem — vague names that mean a different color to each listener (Munsell, Ch. I, the Stevenson letter). Hue, value, and chroma vary independently: you can change one while holding the other two.

## §2. The notation form `H V/C`

Write a color as **hue initial, value above the line, chroma below the line** (Munsell, Ch. VI):

```
        VALUE
  HUE ─────────
        CHROMA        →  written inline as  H V/C
```

- Example: **R 5/9 ≈ vermilion** — hue red, value 5 (middle), chroma 9 (very strong) (Munsell, Ch. II / Ch. VI).
- Read it as: *which family* (H), *how light* (V, 0–10), *how strong* (C, 0 = neutral gray, upward = more saturated).
- The scales can be subdivided decimally when finer precision is wanted (e.g. R5.1/4.9) — but that precision is finer than the eye's own limit, so it is a recording convenience, not something to invent (Munsell, Ch. V).

## §3. The 10-hue wheel

The hue circle has **five principal hues** and **five intermediates** made by mixing neighbors (Munsell, Ch. III):

- Principal: **R, Y, G, B, P** (red, yellow, green, blue, purple).
- Intermediate: **YR, GY, BG, PB, RP** (yellow-red, green-yellow, blue-green, purple-blue, red-purple).
- Full circle order: **R → YR → Y → GY → G → BG → B → PB → P → RP → (back to R)**.
- Popular names for the intermediates: YR = orange, GY = "grass green," BG = "peacock blue," PB = violet, RP = plum (Munsell, Ch. III). Prefer the two-letter hue names in analysis; the popular names are loose.
- Each hue can be subdivided into ten steps (1R…10R, with **5R the middle of that hue**), giving 100 hue positions if needed (Munsell, Ch. VI). Ten steps are plenty for most work.

## §4. The value scale

- A vertical scale from **0 = black** to **10 = white**, with **5 = middle value**; neutral grays are written N1…N10 (Munsell, Ch. II, Ch. III).
- A color's value is the same idea as a neutral gray of the same lightness: R7 is neither lighter nor darker than the gray N7 (Munsell, Ch. III). This is the bridge that lets you compare the lightness of *any* two colors regardless of hue.
- Value is the dimension personal judgment gets **wrong** most easily — Munsell's photometer showed people's "middle" grays drifting well off 5, and estimates varying by more than 10% between individuals and even between a person's two eyes (Munsell, Ch. III, the photometer). Practical upshot: judge value deliberately (squint, or compare against a neutral), don't trust a snap read. (This is the same lesson Albers reaches from the perception side — see `reference-perception-interaction.md` §6.)

## §5. The chroma scale (and why it's uneven)

- Chroma runs from the **neutral gray axis (0)** outward: 0 = no color left (gray), rising numbers = stronger, purer color (Munsell, Ch. II).
- On the idealized color **sphere**, chroma reaches only about **5** at the equator. But real pigments can be far stronger, so the scale extends **6, 7, 8, 9 and beyond** for colors that project past the sphere (Munsell, Ch. II, Ch. V).
- Crucially, **different hues reach very different maximum chromas.** Munsell's own note: the strongest blue-green pigment (chromium sesquioxide) was only about *half* the chroma of its red complement (mercuric sulfide/vermilion) (Munsell, Ch. IV appendix). So "full strength" is not a single number across the wheel — never assume two hues at "max" are equal in chroma.

## §6. Sphere and tree; warm/cool with green at center

- The **color sphere** unites the three scales: white at the north pole, black at the south, hues around the equator, chroma increasing outward from the neutral axis (Munsell, Ch. I–II).
- The **color tree** is the more honest model, because pigment maxima are unequal. Each hue's strongest chroma sits at a *different value level*: **yellow's max is high and light**, purple's is low and dark, with green, red, and blue between — so the branches are unequal in both length and height (Munsell, Ch. II, the color tree). Use this to remember that "a strong yellow" is inherently light and "a strong purple" inherently dark; you cannot have a strong dark yellow or a strong light purple in pigment.
- **Warm / cool split with green at the balance point:** to the warm side lie **GY, Y, YR, R**; to the cool side **BG, B, PB, P**; **green (G) is neither** — it becomes warm or cool only by adding yellow or blue, so it sits at the center (Munsell, Ch. VI, "why green is given the centre of the score"). In wave terms, long waves (red end) read warm, short waves (violet end) read cool, with green midway (Munsell, Ch. VI, footnote). This grounds the warm-advance/cool-recede logic used in `reference-harmony-palette.md`.

## §7. Complementaries, balance, and area

- **True complements** are the pairs joined by a straight line through the neutral center; mixed, they balance to gray (Munsell, Ch. III). The five opposite pairs are: **R ↔ BG, Y ↔ PB, G ↔ RP, B ↔ YR, P ↔ GY.**
- Munsell insists the old **red-yellow-blue "primary"** scheme is a false basis: the true fundamental sensations are **red, green, and violet-blue**, and the R-Y-B wheel wrongly makes green the complement of red, etc. (Munsell, appendices to Ch. III & IV). Practical use: when you need a genuine neutralizing complement, reach for the pair that actually balances to gray (e.g. red ↔ blue-green), not the school-taught "red ↔ green."
- **Balance by area.** When two colors are unequal in chroma or value, you can still balance them by using **more of the weaker one** — a small patch of strong color balances a large field of weak color (Munsell, Ch. III, the buttercup-and-violet). This is the measurement-side basis for the parent skill's accent-proportion logic and matches Albers's quantity effect (`reference-perception-interaction.md` §8) and Sutton's accent ratios (`reference-harmony-palette.md`).

## §8. Estimating `H V/C` from a plain description

Notation is most useful as a *translation layer* for vague requests. Procedure:

1. **Name the hue family and its lean.** Which of R/YR/Y/GY/G/BG/B/PB/P/RP, and does it tip toward a neighbor? ("Dusty blue" → blue leaning slightly purple → **PB**.)
2. **Place the value 0–10.** Light, middle, or dark? Anchor to N5 = middle. ("Dusty" reads mid, maybe a touch light → ~5.)
3. **Place the chroma.** Grayed/soft, moderate, or strong? Neutral axis = 0, moderate ≈ 4–6, strong ≈ 8+. ("Dusty" signals *low* chroma → ~3.)
4. **Write it and sanity-check against the tree.** Is that value even reachable at that chroma for that hue? (A "strong dark yellow" fails the tree — flag it.)

Worked examples (consistent with the parent skill's own):
- **"dusty blue"** ≈ **PB 5/3** — mid value, low chroma, blue leaning purple.
- **"ceremonial / imperial red"** ≈ roughly **R 4/8** — a deep, strong red (pair with gold; cross-ref `reference-color-histories.md` → Reds/Yellows for what "imperial" means *where*).
- **Two greens, "how do they differ?"** — one reads **G 6/4** (mid-value, moderate chroma, slightly yellow-leaning), the other **BG 4/6** (darker, stronger, blue-leaning). The felt difference is mostly *value + temperature*, not "greenness."

Give these as **estimates**, not certified codes (see §9).

## §9. When notation should NOT be forced

Munsell built this as a *teaching and communication* scaffold, not a straitjacket — and its own logic sets the limits:

- **No pigment is a pure spectral hue.** Every real paint is impure, so no physical color has one exact "true" notation without measurement (Munsell, Ch. IV appendix). Any `H V/C` you assign from a description or a screen is an estimate — say so, and don't fabricate a decimal you didn't measure.
- **The decimal notation is finer than the eye.** Precision like R5.1/4.9 exceeds the visual limit (Munsell, Ch. V); quoting it as if observed is false precision.
- **Reproduction and light shift the reading.** A color's apparent value and chroma move with lighting and surround, so a single fixed notation can misrepresent how it will actually read in place (cross-ref `reference-perception-interaction.md`).
- **Don't tax novices.** Munsell introduced hue first, then value, then chroma, deploying notation only where it helped a learner (Munsell, Ch. II, the course of study). Mirror that: use `H V/C` to disambiguate or compare precisely; drop it the moment plainer language serves the user better.

---

*All content distilled from Munsell, *A Color Notation* (1905), at chapter/concept level. Use hue/value/chroma as a scaffold to disambiguate requests and compare colors — always as an estimate unless the user supplied measured input, and never as a mandatory technical tax.*
