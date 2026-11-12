# Local QA — Lavella Hair v4

Checked: 2026-08-23. Local render target: `http://127.0.0.1:4178/`. The v10 local refinement uses a consultation-index middle section, two selected public Lavella work images, and an Ovatu-handoff booking panel.

| Check | Result | Evidence / boundary |
|---|---|---|
| Desktop viewport | PASS | `qa/final/desktop-1440x900.png` is exactly 1440 × 900 px; SHA-256 `0218dae4450cfe0a74d980fd38c89b6b81b0dddca80a0afcd361fead5ab9a238`. |
| Mobile viewport | PASS | `qa/final/mobile-390x844.png` is exactly 390 × 844 px; SHA-256 `eaef8f48bb9ed1181c6477b112be008fa15fb266aba556f5d9fafa9478d53d52`. |
| Mobile overflow | PASS | Rendered `innerWidth` and document `scrollWidth` were both 390. |
| Intermediate-width consultation index | PASS | `qa/final/tablet-820x900.png` and `qa/final/tablet-1000x900.png` were rendered. The service rows now use the same stable three-column grammar at 721px, 820px, 1000px and 1440px; the decorative fourth column is removed so “Hair replacement” cannot overlap its description. |
| Chrome-range consultation layout | PASS | `qa/final/chrome-range-1180x900.png` verifies the formerly failing range. Up to 1320px, the consultation index changes from a narrow two-column shell to a stacked intro plus full-width service rows; at 1180px the title column is 447.5px and copy begins at x=595.5px, with no overlap or horizontal overflow. |
| Browser-zoom stability | PASS | `qa/final/zoom-proof-3000x900.png` simulates Chrome’s low-zoom wide CSS viewport. Bounded `clamp()` gutters keep the consultation content at 1120px; its title and copy columns are 471.391px and 554.609px respectively, with zero horizontal overflow. |
| Full-page rhythm | PASS, Owner check | `qa/final/full-page-desktop.png` and `qa/final/full-page-mobile.png` show the full sequence without a repeated generic CTA or a text-only run after the appointment decision. The original non-person colour-material study is internally registered in `IMAGE_LEDGER.md` and is not asserted to be customer work. |
| External handoff | PASS | The visible links resolve in markup to the existing Lavella Ovatu booking route and public reviews route; no form, payment or self-hosted booking is present. |
| Console | PASS | Browser console reported 0 errors and 0 warnings on the final local render. |
| Motion | PASS, local technical check | GSAP loaded (`window.gsap === true`); the code exits before animation under `prefers-reduced-motion: reduce`. Motion is transform/opacity-based and contains no loop. |
| Client-visible text | PASS, manual source check | No visible AI/source/authorization/internal-review/placeholder language. “Independent concept preview” remains intentionally visible on desktop and mobile. |
| Content fidelity | PASS, bounded | Address, review count, booking and cookie-preference handoff are mapped in `BUSINESS_FIDELITY_MAP.md`; fixed hours and prices remain absent. |
| Real-work asset integration | PASS, bounded | Two visual placements now use distinct stills from the public, unauthenticated `@lavella_ltd` profile. Exact permalinks, retrieval date, checksums, usage and authorization boundary are in `IMAGE_LEDGER.md`. The unsuitable text-overlay clip is retained but not rendered. |
| v10 desktop viewport | PASS | `qa/final/desktop-1440x900-v10.png` is exactly 1440 × 900 px; SHA-256 `8c85dd147ce333022ce9c8ee27c2a2ff2cbb03ad7ca3fe1d8a0eec22fd4a95d2`. |
| v10 mobile viewport | PASS | `qa/final/mobile-390x844-v10.png` is exactly 390 × 844 px; SHA-256 `eaef8f48bb9ed1181c6477b112be008fa15fb266aba556f5d9fafa9478d53d52`. It preserves the visible concept-preview label, image-first opening and no horizontal overflow. |
| v10 work bridge | PASS, Owner technical check | `qa/final/desktop-work-proof-v10.png` and `qa/final/mobile-work-proof-v10.png` show the second public work in the intended desktop/mobile composition, without text overlays, duplicate images or false service-result claims. |
| v10 Chrome low-zoom range | PASS | `qa/final/zoom-proof-3000x900-v10.png` is exactly 3000 × 900 px. At this wide CSS viewport, `scrollWidth = innerWidth = 3000`, the consultation shell stays in its block layout and no service-row collision occurs. |
| v11 consolidated case gallery | PASS, Owner technical check | `qa/final/desktop-case-gallery-v11.png` and `qa/final/mobile-case-gallery-v11.png` show both selected public Lavella work images in one continuous gallery. At 1440 and 390 px, the gallery has two rendered figures and `scrollWidth = innerWidth`; cases are no longer split between the consultation intro and a separate half-width bridge. |
| v12 decision-desk composition | PASS, Owner technical check | `qa/final/desktop-consultation-v12.png` and `qa/final/mobile-consultation-v12.png` show the consultation title, one-sentence orientation and three live-menu routes as a composed decision desk. Verified at 1440, 390 and 3000 CSS px: `scrollWidth = innerWidth`; no overlap or horizontal overflow. |

## Non-passing gates

- `INDEPENDENT VISUAL ACCEPTANCE = AWAITING`
- `CLIENT-SHOWABLE DEMO = FAIL` until independent acceptance is recorded.
- No deployment, public release, submission, client contact or external send was performed or authorized.
