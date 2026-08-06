# Reference — Harmony & Palette

> Companion reference for the **Color-Matching Art Consultant** skill. Distilled from Tina Sutton, *The Complete Color Harmony, Deluxe Edition* (2024). Attribution is at concept level. This file builds and balances palettes: harmony families, proportion and accent ratios, warm/cool spatial logic, and mood associations. The parent skill points here from its Harmony layer (§4) and from Harmony Exploration mode (§8). **Mood associations are suggestive, not deterministic** — see §5.

**Contents**
- [§1. Harmony families](#1-harmony-families)
- [§2. Proportion & accent ratios](#2-proportion--accent-ratios)
- [§3. Warm-advance / cool-recede](#3-warm-advance--cool-recede)
- [§4. Spectral balance](#4-spectral-balance)
- [§5. Mood-to-palette associations (suggestive)](#5-mood-to-palette-associations-suggestive)
- [§6. Building a palette step by step](#6-building-a-palette-step-by-step)
- [§7. Palette failure modes](#7-palette-failure-modes)

---

## §1. Harmony families

Each family is a *relationship on the hue wheel*, with a characteristic feel and its own risks (Sutton — harmony schemes). Pick by the job, not by habit.

- **Monochromatic** — one hue, varied in value and chroma. Feel: calm, cohesive, refined. Build: hold hue fixed, spread value widely, vary chroma. Watch-out: can go flat/dull; rescue with a strong value range or one small chroma spike.
- **Analogous** — 2–4 neighbors on the wheel (e.g. YR–Y–GY). Feel: harmonious, natural, easy. Build: let one neighbor dominate, the others support. Watch-out: low contrast; needs value separation or a small complementary accent to avoid monotony.
- **Complementary** — two opposites (e.g. B / YR). Feel: high-energy, vibrant, stable. Build: one dominant, the other as a smaller accent; rarely 50/50. Watch-out: equal areas at full chroma buzz and fight (cross-ref `reference-perception-interaction.md` §7); mute one or shrink it.
- **Split-complementary** — a hue + the two neighbors of its opposite (e.g. B / YR-adjacent Y and R). Feel: complementary contrast with less tension; more forgiving. Build: one dominant, two accents. Watch-out: can feel unfocused if all three run equal.
- **Triadic** — three hues evenly spaced (e.g. R / Y / B). Feel: balanced, lively, playful. Build: **one dominant, two subordinate** — never three equals. Watch-out: three full-chroma hues = chaos; let one lead.
- **Tetradic / double-complementary** — two complementary pairs (a rectangle or square on the wheel). Feel: rich, complex. Build: pick one hue to dominate and keep the other three in support; balance warm against cool. Watch-out: the hardest to balance; easy to overload.
- **Square** — four hues evenly spaced. As tetradic but more evenly tense; same "let one lead" rule.
- **Near-neutral / achromatic** — grays, browns, off-whites, or one hue barely above neutral. Feel: quiet, elegant, sophisticated. Build: rely on value and subtle temperature shifts; add at most one saturated accent. Watch-out: can read drab without a clear value structure or a single accent.
- **Warm-dominant / cool-dominant** — a palette pulled mostly to one temperature. Feel: warm = cozy/active; cool = calm/distant. Build: commit to the temperature, then add a small opposite-temperature balancer so it doesn't feel one-note (see §4).

## §2. Proportion & accent ratios

- Palettes read best with a clear hierarchy, not equal thirds. A useful **starting heuristic is ~60 / 30 / 10** — dominant / secondary / accent — adjusted to taste, not a law (Sutton — proportion and dominance).
- The **accent carries the highest chroma in the smallest area.** A small patch of strong color energizes; the same color across a large field overwhelms (Sutton — accent color; this is the same effect Munsell frames as area-balance, `reference-notation-measurement.md` §7, and Albers as the quantity effect, `reference-perception-interaction.md` §8).
- Inverse rule for large areas: the bigger the area, the **lower the chroma** it can carry comfortably. Big fields want muted color; save full chroma for accents.
- Compensate unequal strength with area: to balance a weak color against a strong one, give the weak color **more space** (Sutton — balancing unequal colors).

## §3. Warm-advance / cool-recede

- **Warm hues (R, YR, Y) advance** — they feel nearer, more active, and draw the eye. **Cool hues (G, B, P) recede** — they feel farther, calmer, quieter (Sutton — warm/cool spatial behavior; grounded in Munsell's warm/cool split, `reference-notation-measurement.md` §6).
- Use it to build **depth and focal hierarchy:** warm accents on a cool ground jump forward; cool passages sink back. A warm focal point against cool surroundings is a reliable way to direct attention.
- Treat advance/recede as a **strong tendency, not a fixed law** — value and context can reverse it (a dark warm can recede behind a light cool). Albers makes the same caution from the perception side (`reference-perception-interaction.md` §9).

## §4. Spectral balance

- A palette that spans **both warm and cool** tends to feel resolved; an all-warm or all-cool palette can feel one-note (Sutton — spectral/temperature balance).
- Practical move: in a temperature-dominant palette, include a small **temperature balancer** (the parent skill's palette role) — a cool accent in a warm scheme, or a warm accent in a cool one — to give the eye relief and a point of contrast.
- This pairs with value structure: a resolved palette usually balances *both* temperature (warm/cool) *and* value (light/dark), not just hue.

## §5. Mood-to-palette associations (suggestive)

**These are cultural, contextual associations — not rules.** Sutton presents mood links as starting points, and the parent skill's constraint is explicit: never treat "this scheme = this emotion" as deterministic. Where a mood leans on cultural meaning (regal, ceremonial, mourning), cross-check `reference-color-histories.md` for *which* culture/era, and say so.

- **Calm / serene** — analogous cools (B, BG, PB), low-to-moderate chroma, mid-to-high value. Monochromatic blue or green reads restful.
- **Energetic / bold** — complementary or triadic, high chroma, warm-led (R, YR, Y). Strong value contrast adds punch.
- **Somber / grave** — low value, low chroma; cool or earth-dominant. Near-neutral darks.
- **Ceremonial / regal** — deep, saturated hues (often purple or red) with metallic/gold accents. *Which* hue reads "regal" is culturally specific — Tyrian purple in the Roman/Byzantine world, imperial yellow in Tang-and-later China (`reference-color-histories.md` → Purples, Yellows). Name the register.
- **Nostalgic / vintage** — muted, slightly warm, lowered chroma; sepia and faded earth tones (cross-ref sepia, `reference-color-histories.md` → Browns).
- **Fresh / natural** — green-led analogous with earth neutrals; moderate chroma, higher value.
- **Luxe / elegant** — near-neutral field (grays, off-whites, deep browns or black) with a single saturated accent; restraint reads as sophistication.
- **Cheerful / playful** — higher-value warms, moderate-to-high chroma, often multiple hues held in a triadic relationship with one dominant.

Offer these as options a user can accept or reject, phrased as "often reads as…," not "means."

## §6. Building a palette step by step

Ties directly to the parent skill's palette roles (anchor, accent, bridge, neutral, shadow, highlight, temperature balancer):

1. **Set the anchor.** Choose the dominant color as `H V/C` (hue, value, chroma) — this fixes the palette's identity and temperature.
2. **Choose a harmony family** (§1) based on the desired feel and the anchor.
3. **Assign roles.** Anchor (largest area), accent (small, highest chroma), bridge (a hue between anchor and accent to ease the transition), neutral (a grayed or earth tone for rest), plus shadow and highlight for value range, and a temperature balancer if the scheme is temperature-dominant (§4).
4. **Set proportions** (§2) — start ~60/30/10, adjust; give weaker colors more area to balance stronger ones.
5. **Check value spread and chroma hierarchy last.** Squint: is there a clear light-to-dark range, and does exactly one color carry the top chroma? If everything is mid-value or everything is full-chroma, fix that before finalizing (§7).

## §7. Palette failure modes

| Symptom | Cause | Fix |
|---|---|---|
| Chaotic / everything shouting | Chroma overload — too many colors at full strength | Keep one accent at full chroma; mute the rest |
| Flat / lifeless despite many hues | Value collapse — all mid-value | Spread values; add a dark and a light (cross-ref `reference-perception-interaction.md` §6) |
| One-note / airless | Temperature monotony — all warm or all cool | Add a small opposite-temperature balancer (§4) |
| No focal point | No dominant; colors in equal thirds | Impose a 60/30/10 hierarchy (§2) |
| Accent doesn't read as an accent | It's too large, or not the highest chroma | Shrink it and/or raise its chroma above the field |
| Complementary pair fights / buzzes | Equal areas, equal value, both full chroma | Make one dominant, mute or shift the other (cross-ref `reference-perception-interaction.md` §7) |

---

*All content distilled from Sutton, *The Complete Color Harmony, Deluxe Edition* (2024), at concept level. Harmony families and ratios are construction tools; mood associations are suggestive and culturally situated — offer them as options, cross-check `reference-color-histories.md` for cultural specificity, and never present a scheme-to-emotion mapping as deterministic.*
