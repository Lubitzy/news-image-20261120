# Design review — 20 November 2026

## Evidence and limits

- [evidence] Three actual 1024 × 1024 original designs were rendered with the same six sourced stories. A uses six equal light cards, B gives two stories lead-card treatment, and C uses a dark six-card layout.
- [evidence] The remote vision tool returned HTTP 403 `client_not_allowed`. It was not retried through another image route. Review used decoded pixels, known text geometry, measured color contrast and local Windows OCR, including actual 300-pixel-wide renditions.
- [evidence] The local OCR engine correctly recovered a rendered fixture containing the date and several topic words before design comparisons. OCR errors are retained in private review evidence; they are not treated as proof that a glyph is absent or a claim is wrong.
- [assumption] These are constrained editorial self-assessments, not verdicts from the official judge or a claim of direct visual/aesthetic inspection. Icon recognizability and fine low-resolution typography remain uncertain where OCR cannot assess them.

## Pairwise selection of the initial compositions

The rubric is applied in order: one named day; importance/breadth; understandable events; faithful attribution; craft around 300 px. All three use the same date and selected reporting, so criteria 1–2 do not distinguish the content.

### A versus B: A selected

- [evidence] Initial B allocates 202 px to secondary cards. Its 3-line trade description runs through the source area and beyond the intended card body, while its 300 px OCR fails to recover the complete food-aid headline.
- [evidence] A allocates 231 px to each card; native OCR recovers the full trade qualification. A still has an insufficient body/source gap in two cards and needs revision rather than being accepted unchanged.
- [assumption] Event clarity and preservation of qualifications favor A first, before considering whether B's larger lead pictures are aesthetically preferable.

### A versus C: A selected

- [evidence] Six icon colors measure approximately 4.63–6.04:1 against A's light card surface, compared with 1.91–2.49:1 against C's dark surface. These are luminance-contrast measurements, not an assertion that every icon was visually classified.
- [evidence] Native OCR recovers the same main copy in A and C. At 300 px, C misrecognizes COP31 while A recovers it.
- [assumption] A has the safer combination of text recovery and pictogram contrast. The main difference is readability/craft, not news selection.

### B versus C: C narrowly selected

- [evidence] C preserves the longer secondary descriptions within taller cards. Initial B loses the end of the trade qualification and several secondary-source labels in native OCR, consistent with its overflowing text geometry.
- [assumption] Preserving an event's qualification outweighs C's weaker icon contrast. This is a narrow self-assessment with no official score attached.

## Retained revisions of A

1. [evidence] Revision 1 shortened all six descriptions while preserving attribution and the distinction between MoUs, appeals and completed actions. Body text increased from 25 px to 30 px. Explicit layout guards were added. Every card then had a 15 px body/source clearance; native OCR recovered all six source labels.
2. [evidence] Revision 2 moved pictograms into the upper-right header area and gave headlines the card's full width, increasing headline size from 34 px to 40 px. It preserved a measured 13 px body/source clearance.
3. [evidence] Revision 3 increased headlines to 42 px, body text to 32 px and source labels to 17 px. An attempted overlong description was rejected by the renderer's line-limit guard before an image was saved. The Ukraine and climate descriptions were then shortened without changing their factual scope. The retained image has a 14 px headline/body gap and a 9 px body/source gap in every card.

## Final choice

- [evidence] Selected composition: A, retained revision 3, copied to `assets/entry.png`.
- [evidence] The date and all six headlines are recovered at native size. At actual 300 px, OCR recovers the date and most headline wording, plus more body content than the initial rendition; some words, symbols and digits are still misrecognized. No claim of perfect 300 px OCR is made.
- [evidence] Image size: 1024 × 1024, 307140 bytes.
- [evidence] SHA-256: `cff74b610b653628128d59372a08af60572d9cb8f23183f07a2a6c25b5fc624c`.
- [evidence] Initial candidates, 300 px comparisons, native OCR and revision reports are retained outside the entry repo under the sibling `design-review/` directory. They are original development artifacts, not downloaded competitor assets.
- [assumption] A clearer low-resolution hierarchy is preferable to adding more stories or decorative material. The official judge may weigh pictures and editorial selection differently; no placement or score is predicted.
