# Class 6 — manual test and evidence record

24 October 2026. Target: existing hosted review, version 12, https://ebike-client-review-hasina.ochreangel10.chatgpt.site/ . Expected values use the existing T2 €1,499 market-reference price, not an approved commercial price. Initial condition: empty cart. Browser viewport controls used; application code unchanged.

| Check | Viewport | Steps | Expected | Actual | Status |
|---|---|---|---|---|---|
| Collection and details | Desktop 1440×960; mobile 390×844 | Open collection → T2 → Gray | Correct T2/reference price; selected Gray and matching image; operable controls | T2/€1,499 present; Gray selection and matching Gray image verified; controls used successfully in prior completion pass | PASS |
| Cart and persistence | Desktop 1440×960; mobile 390×844 | Add one → cart → set 2 → reload and await hydration | T2/Gray/2 retained; line and item subtotal €2,998 | All expected values observed; desktop repeated again in final verification pass | PASS |
| Removal and recovery | Desktop 1440×960; mobile 390×844 | Remove → Explore bikes | Empty cart then collection; no test items left | Expected transitions observed at both sizes; desktop repeated in final pass | PASS |
| Commercial boundary | Same desktop/mobile sizes | Read cart summary | No invented delivery-inclusive total, taxes or stock claim | Delivery Not yet quoted; taxes/duties To be confirmed; availability/payment setup notices visible | PASS |
| Horizontal overflow | Same desktop/mobile sizes | Inspect collection, detail, cart, empty state | document scrollWidth ≤ window.innerWidth | 1425 ≤ 1440 desktop; 375 ≤ 390 mobile during completion pass; final desktop cart again 1425 ≤ 1440 | PASS |
| Visible controls/readability | Same desktop/mobile sizes | Use product link, Gray, Add, quantity select, Remove, recovery link; inspect captures | Required controls operable; chosen finish/quantity/amounts readable | Controls operated; desktop/mobile cart images inspected | PASS |
| Malformed-storage UI | Not exercised | Isolated malformed saved key → reload → recover | No crash; safe retained/empty cart | Sanitizer unit test passed; injected browser state not tested | NOT TESTED |
| Accepted quote edited | Not exercised | Obtain fixture quote → edit address/cart → re-review | Stale accepted total/payment action hidden | Fingerprint guard inspected; successful quote/edit browser scenario not tested | NOT TESTED |
| Uncertain real provider response | Not exercised | Authorized provider test timeout/retry/webhook | No false success or duplicate order | Isolated injected-transport tests passed; real provider/UI scenario not tested | NOT TESTED |
| Tablet / keyboard-only / screen reader | Not exercised | Dedicated device/accessibility checks | Applicable flow usable | No such test performed in this assignment pass | NOT TESTED |
| Offline HTML interactions | Not exercised | Manually open existing HTML and repeat cart flow | Same preview behavior within offline limits | Structural validation passed; direct file:// automation blocked previously | NOT TESTED |

## Screenshot manifest

Paths below are relative to the task workspace (`outputs/class-6-audit/`). Captures show actual hosted application behavior, not a mockup.

| Screenshot | Viewport and action |
|---|---|
| `desktop-cart-gray-quantity-2-final.png` | Fresh final-pass desktop 1440×960 CSS viewport screenshot; T2 Gray quantity 2 after reload, €2,998 line/subtotal |
| `desktop-cart-gray-quantity-2.png` | Prior completion desktop 1440×960 CSS viewport screenshot of the same verified flow |
| `mobile-390-cart-gray-quantity-2.png` | Completion mobile 390×844 CSS viewport, full-page capture of same cart after reload |
| `cart-gray-quantity-2.png` | Original audit narrow cart; window width 425 CSS px, viewport height not recorded |
| `empty-cart.png` | Original audit empty-cart recovery state; same narrow session, height not recorded |

Full-page image height is not viewport height. Screenshot bitmap width may exclude the scrollbar; recorded CSS viewport is not inferred from bitmap size. Existing screenshots were preserved. Temporary viewport reset and cart restored to empty. Required desktop/cart/empty evidence is available; no tablet, keyboard or offline interaction pass is claimed.

## Final technical checks

Run in `outputs/e-bike-review/storefront`: `node --test tests/commerce.test.mjs tests/server.test.mjs` → 21 passed / 0 failed; `node node_modules/typescript/bin/tsc --noEmit` → exit 0; `node scripts/run-framework.mjs build` → exit 0. From workspace root: `node work/validate-html.mjs` → exit 0 for desktop and mobile. SQLite experimental warning and Vinext timing/static-route classification notices did not fail the checks. No code repair or repair round was required. Document link/whitespace checks are recorded in the final handoff.
