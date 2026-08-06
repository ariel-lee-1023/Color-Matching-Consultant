# Changelog

All notable changes to the **Color-Matching Art Consultant** skill are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html). The authoritative version number lives in `color-matching-art-consultant/SKILL.md` frontmatter (`metadata.version`).

---

## v3.0.2 — Standard skill layout

No change to the skill's behavior, logic, or reference content. Layout only:

- Moved the five reference files into a **`references/`** subfolder, so the skill now matches the conventional agent-skill layout:

  ```
  $SKILLS_HOME/<library-name>/
  ├── SKILL.md
  └── references/
  ```

- Re-pointed all 35 reference citations in `SKILL.md` (frontmatter `metadata.sources`, the intro manifest, and §3–§12) from `reference-*.md` to `references/reference-*.md`.
- Reference filenames are unchanged, and the reference files' cross-references to *each other* still resolve untouched, since all five remain siblings inside `references/`.
- Updated the repository-structure tree, the reference-file table, and the co-location note in `README.md`.

## v3.0.1 — Repository packaging

No change to the skill's behavior, logic, or reference content. Packaging only, for public release:

- Added `README.md`, `LICENSE` (MIT), and `.gitignore`.
- Moved the skill and its five reference files into a self-contained `color-matching-art-consultant/` directory so the folder can be zipped and installed directly.
- Renamed the skill file from `color-matching-art-consultant.md` to **`SKILL.md`**, matching the agent-skill convention. Historical entries below refer to it by its former name. The five reference filenames are unchanged, and all internal cross-references still resolve, since every file remains a sibling in the same directory.
- Standardized this changelog on the Keep a Changelog format.

## v3.0 — Reference-file refactor

**Shape change:** the skill went from one self-contained file (operating logic + two embedded appendices) to a **lean orchestration file + five standalone reference files**, one per source book. This follows the progressive-disclosure pattern: the host AI loads the small skill always, and pulls a reference file only when a request needs that book's depth. The skill dropped from 408 lines to **202** (well under the 500-line lean target).

### What moved (migration — no content lost)
- **Appendix A — Pigment Mixing Reference (Sidaway)** → **`reference-pigment-mixing.md`.** Content migrated as-is (§1 core principles through §8 problems-and-fixes table), refined for standalone use: added a provenance header, a table of contents, and a closing caveat. Section numbers changed from `A§1…A§8` to `§1…§8`; the skill's pointers were updated to match (e.g. "Appendix A §3" → "`reference-pigment-mixing.md` §3").
- **Appendix B — Color Histories (St. Clair)** → **`reference-color-histories.md`.** All ~75 entries migrated verbatim across the ten color families, plus a standalone header, a family-level table of contents, and the situated-not-universal caution promoted to the top. Skill pointers updated (e.g. "Appendix B, Reds" → "`reference-color-histories.md` → Reds").

### What's new (three references built to match the migrated depth)
The three books that were only briefly summarized in §4 and §11 now have full reference files, at the same depth and format as the migrated two. Every claim is attributed at chapter/concept level so it stays traceable, not generic color theory.
- **`reference-perception-interaction.md` (Albers).** Simultaneous contrast, afterimage/successive contrast, "one color looks like two," "two look like one," value/lightness deception, vibrating vs. vanishing boundaries, quantity/proportion and film-vs-surface color, transparency/space illusion, and a fast **composition-diagnostics table** for "it looks wrong but the pigment is fine."
- **`reference-notation-measurement.md` (Munsell).** The full 10-hue wheel (5 principal + 5 intermediate, circle order), value scale (0–10, N-grays, middle 5), chroma scale and why it's uneven across hues, the sphere/tree models, warm/cool with green at center, the five true complementary pairs (and why R-Y-B "primary" is a false basis), area-balance, a **step-by-step method for estimating `H V/C` from a plain description** (with worked examples), and explicit rules for **when notation should NOT be forced**. Distilled directly from the uploaded Munsell text.
- **`reference-harmony-palette.md` (Sutton).** The full set of harmony families (monochromatic, analogous, complementary, split-complementary, triadic, tetradic, square, near-neutral, warm/cool-dominant) with build steps and watch-outs, proportion/accent ratios (~60/30/10 as a heuristic, not a law), warm-advance/cool-recede logic, spectral balance, **mood-to-palette associations framed as suggestive and culturally situated**, a step-by-step palette-build tied to the skill's role vocabulary, and a palette-failure table.

### What changed in the skill file (`color-matching-art-consultant.md`)
- **Frontmatter:** `metadata.version` → `3.0`; `metadata.sources` now lists all five books **and** the five reference files by name; the `description` clause that claimed content was "embedded" was corrected to "ships with five companion reference files," since it no longer is (the description is the skill's triggering text and must stay accurate).
- **Intro:** the "this file is self-contained / two appendices follow" paragraph was replaced with a five-file manifest and a "pull the specific fact, don't inline a whole reference" instruction.
- **§4 Knowledge Model:** added `→ read …` pointers to the three new reference files (Perception, Notation, Harmony layers) and re-pointed the two existing ones (Mixing, Historical) to their new filenames; the diagnostic layer now points at both `reference-pigment-mixing.md` §8 and `reference-perception-interaction.md`.
- **§8 Recommendation Modes:** re-pointed Paint-Mixing Troubleshooting and Historical Palette Advisor to the new filenames, and added pointers so Studio Critique → perception diagnostics, Munsell-Style Formal Analysis → notation reference, Harmony Exploration → harmony reference.
- **§3, §5, §9, §10, §11, §12:** every "Appendix A/B" citation re-pointed to the corresponding reference file (15 references to pigment-mixing, 11 to color-histories across the body); §11 distillation notes for Albers/Munsell/Sutton now name their new reference files; the §12 final-prompt closing sentence names all five files.
- **Appendices A and B removed** from the skill file and replaced with a short footer manifest.

### What was preserved unchanged
All existing constraints and structures are intact: no fake precision (no invented pigment names, brands, or Munsell/hex codes), no universalized historical/cultural claims, always medium-anchored mixing advice, subtractive-vs-additive disambiguation, **value-checked-before-hue** discipline, the seven palette roles, the six Recommendation Modes, and the ten worked examples in §10 (re-pointed only, not shrunk).

### Why
- **Keeps the always-loaded file small.** Deep pigment tables and 75 histories don't belong in the context on every trigger; they load on demand.
- **Levels the depth across sources.** v2.0 gave Sidaway and St. Clair full appendices but left Albers, Munsell, and Sutton as thin summaries. v3.0 gives all five equal, traceable depth.
- **Traceability.** Concept-level attribution in every reference file keeps claims tied to their source book rather than reading as generic color theory, and makes future updates (swap one book, re-distill one file) a local edit instead of surgery on a monolith.

---

## Earlier versions

- **v2.0** — a single self-contained file (408 lines): operating logic plus two embedded appendices (Sidaway pigment mixing, St. Clair color histories). Albers, Munsell, and Sutton were present only as short summaries in §4 and §11.
- **v1.0** — initial release, predating this changelog.
