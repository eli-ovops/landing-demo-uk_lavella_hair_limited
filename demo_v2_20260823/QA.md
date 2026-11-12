# Owner QA - Lavella Hair v2 reset 3

Checked: 2026-08-23, local server `http://127.0.0.1:4178/`. This is owner QA only. It cannot substitute for the required independent visual review.

## Evidence

| Check | Result | Evidence |
|---|---|---|
| Desktop 1440 × 900 render | PASS | `qa/final/desktop-1440x900.png` - SHA-256 `5d4d00b82bd24f547e0c6e3c3cbd1be45231a8871b26abc911ff5645922110f5` |
| Mobile 390 × 844 render | PASS | `qa/final/mobile-390x844.png` - SHA-256 `16c91be39762ce844a52029f93c9174bfec06d83af5c556af5633e8e54483cba` |
| Horizontal overflow | PASS | Browser check: desktop scroll width 1425 ≤ 1440; mobile 375 ≤ 390. |
| Image loading | PASS | Browser check: all four rendered image elements complete with non-zero natural widths. |
| Booking path | PASS | Seven external CTAs point exactly to `https://lavellahairlimited.book.app/book-now`; read-only HTTP verification returned `200` on 2026-08-23. |
| Static scope | PASS | No form, booking embed, login, payment, CMS, backend, database, or custom JS flow. |
| Client-visible internal-text gate | PASS | Browser text scan found none of: AI-generated wording, stock/placeholder/mock wording, customer-authorization wording, internal-review wording, or sending-authorization wording. |
| Asset authenticity | PASS with authorization boundary | One constrained abstract ImageGen concept visual and three distinct evidence-led assets are recorded in `IMAGE_LEDGER.md`. The concept visual is not presented as a real business asset, location, staff member or result. `CUSTOMER AUTHORIZATION: NOT VERIFIED` remains an internal constraint for customer-origin assets. |
| Business fidelity | PASS for the narrow hair-only slice | Colour, extension and women’s hair replacement consultation wording are mapped to current public booking evidence in `BUSINESS_FIDELITY_MAP.md`. No medical, practitioner, price, availability, or outcome claims were added. |
| Cross-demo similarity | PASS - reset direction and post-render owner check | The concept material study, paper-based asymmetrical hero, actual salon scene, practical consultation notes and illustrated location close are unlike either historical demo’s generic hero/card/review-number rhythm. See `CROSS_DEMO_SIMILARITY_CHECK.md`. |
| Visual and motion reset | PASS locally | H1 is 52px at 1440px and 38px at 390px. The image carries the first-screen visual weight. GSAP loaded and performs one transform-and-opacity entrance sequence plus one-time in-view reveals; reduced motion disables the sequence. |

## Independent acceptance gate

`INDEPENDENT VISUAL ACCEPTANCE = AWAITING`

`CLIENT-SHOWABLE DEMO = FAIL (pending independent acceptance)`

The required reviewer is a different Owner. They must apply the eight-item visual rubric and only pass if the average is at least 8.0 and every item is at least 7.0. This owner has not made that decision.

## Boundaries retained

- Local v2 draft only; the old v1 directory was not modified.
- No deployment, public upload, sending, customer contact, login, payment, installation, deletion, or Git action occurred.
- External booking is a link to the existing Ovatu path, not a recreated booking experience.
