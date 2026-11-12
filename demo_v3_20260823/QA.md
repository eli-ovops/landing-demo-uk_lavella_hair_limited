# Owner QA - Lavella Hair v3

Checked locally on 2026-08-23 using `http://127.0.0.1:4179/`. This is implementation evidence only; it does not replace independent visual re-acceptance.

| Check | Result | Evidence |
|---|---|---|
| Final Desktop viewport | PASS | `qa/final/desktop-1440x900.png`, exact 1440 × 900, SHA-256 `d983dff0b9c1e8298ddc6f296ad01dfe62d1637e03179b3203658ae40a774f97` |
| Final Mobile viewport | PASS | `qa/final/mobile-390x844.png`, exact 390 × 844, SHA-256 `2a63cdf226ea136dfcbda2744980cf1a0d068212211a239858eb30827566730f` |
| Full page evidence | PASS | `qa/final/full-page-desktop.png`, separately named (1440 × 4194), SHA-256 `4fec39794749edba2dabf665780608ac7fc96d98e27da7f5d0e39d44bc51f5e8` |
| Horizontal overflow | PASS | Desktop scroll width 1425 ≤ 1440; mobile scroll width 375 ≤ 390. |
| Concept Preview visibility | PASS | Browser text check found one `Independent concept preview` at both 1440px and 390px. Mobile does not CSS-hide it. |
| Images | PASS | Logo plus three unique rendered image-to-image derivatives loaded with non-zero natural widths. No same image is reused across hero, place or close. |
| Image legibility | PASS | Hero is 1672 × 941; reception/corridor are 1448 × 1086; wash area is 1122 × 1402. Every displayed image and its factual anchor/use boundary is recorded in `IMAGE_LEDGER.md`. |
| Business fidelity | PASS | Each page claim and visual maps to a public source in `BUSINESS_FIDELITY_MAP.md`; no service outcome, price, medical, practitioner or availability claim was added. |
| External paths | PASS | Booking and live availability use `https://lavellahairlimited.book.app/book-now`; the separately labelled customer-review fact links to `https://lavellahairlimited.book.app/reviews`. Service-path links remain internal guide anchors. |
| Static product boundary | PASS | No form, booking embed, login, payment, database, backend, analytics or data collection. |
| Client-visible internal-text gate | PASS | No visible AI/source/rights/authorization/internal-governance wording was found in the final page. |
| Motion and visual-direction criteria | PASS locally | No Manrope, DM Mono, deep green/fluorescent yellow system, split hero, three-card CTA pattern, compact 411 proof block, or dark close plus bright CTA. The final page uses a guided decision spine and short GSAP transform/opacity entrances only; `prefers-reduced-motion` skips them. |

## Required independent gate

`INDEPENDENT VISUAL RE-ACCEPTANCE = AWAITING`

`CLIENT-SHOWABLE DEMO = FAIL (until independently re-accepted)`

The new reviewer must inspect `DESIGN_INTENT.md`, `CROSS_DEMO_SIMILARITY_CHECK.md`, `BUSINESS_FIDELITY_MAP.md`, `IMAGE_LEDGER.md`, `SOURCE_LEDGER.md`, this QA file and both final viewport PNGs. The owner has not assigned a visual-rubric score or claimed acceptance.

## Retained boundaries

- v1 and v2 were read-only comparison material and were not edited.
- v3 is local only. No deployment, upload, sending, contact, login, payment, installation, deletion or Git action occurred.
