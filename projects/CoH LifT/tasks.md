# Class 6 — acceptance tasks and results

24 October 2026. Statuses: PASS = criterion verified; FAIL = tested criterion not met; NOT TESTED = no sufficient execution evidence. No FAIL result was observed for the scoped checks. Existing responsive React application is preserved. Evidence starts with [initial audit](class-6-audit.md); current evidence is recorded below and in [build notes](build-notes.md).

## T1 — demonstrate one meaningful shopping flow

Dependency: running review site; initially empty cart; reference catalogue T2 priced at €1,499. No merchant stock or paid order required. Do not substitute this reference price for an approved commercial price.

| Action | Done when | Final result |
|---|---|---|
| Open collection | `#/bikes` shows T2 with €1,499 market-reference price and a working product link | PASS — hosted audit |
| Open T2 | Route ends `#/bikes/coh-lift-t2`; heading and reference price match collection | PASS — hosted audit |
| Select Gray | Gray is selected and matching product image is shown; finish is retained when added | PASS — desktop/mobile: Gray gallery image alt and selected finish verified; cart retains Gray |
| Add one | Cart shows T2, Gray, quantity 1, line amount and item subtotal €1,499 | PASS — hosted audit |
| Change to two | Quantity is 2; line amount and item subtotal are both €2,998 | PASS — hosted audit |
| Reload | After loading finishes, T2/Gray/2 and €2,998 amounts remain | PASS — hosted audit |
| Check commercial boundary | Delivery stays unquoted and taxes/duties unconfirmed; no payable shipping-inclusive total or stock is invented | PASS — hosted audit |
| Remove and recover | Cart is empty with Explore bikes; clicking it returns to collection | PASS — desktop and mobile, including recovery-link click |

## Other assignment tasks

| ID / task | Dependency | Done when | Current result |
|---|---|---|---|
| T2. IA mapping | Existing architecture/routes | Every numbered step has a screen/state, primary/recovery transition and explicit integration boundary; admin/research separated | PASS — [ia-map.md](ia-map.md) created from existing implementation |
| T3. Additional state documentation | Source and existing tests | Each of three safeguards records trigger, visible result, recovery, need, procedure/result and assumptions without fabricated UI/provider verification | PASS — [build-notes.md](build-notes.md) |
| T4. Responsive demonstration | T1; browser viewport controls | At desktop 1440×960 and mobile 390×844, T1 controls remain operable, chosen model/finish/amounts stay readable, and collection/detail/cart/empty state have no document horizontal overflow | PASS — fresh desktop/mobile flow and screenshot inspection; widths recorded below. Not a full-site accessibility audit |
| T5. Screenshot evidence | T1/T4 | Actual running desktop cart screenshot shows T2 Gray quantity 2 and €2,998; existing narrow cart and empty screenshot retained; manifest records actual viewport/action | PASS — desktop plus fresh mobile capture saved; both original audit screenshots retained |
| T6. Relevant checks | Unchanged source and configured dependencies | Existing 21 tests, TypeScript, production build and both HTML structural checks have successful recorded results; no unsupported provider claim | PASS — final pass reran 21/21 tests, TypeScript, production build and both HTML structural checks successfully |
| T7. Evidence/package review | T2–T6 | Three Markdown outputs and screenshots are linked, verification limits stated, local delivery distinguished from GitHub/Figma/live changes | PASS — files/relative links and screenshot PNGs checked; final package contains local evidence |

## Build-and-check record

Selected task: T1. Criterion is the fixed set above; it must not be weakened to accommodate a failure. Inspected brief, tokens and current source before testing. Initial hosted audit passed the cart arithmetic/persistence/removal subset. Desktop/mobile results are recorded below and in the manual test record. If a criterion fails, identify one targeted repair, retest that same criterion and stop after three failed repair rounds. No application repair or visual change has been needed so far.

## Completion update

T1 completed at both 1440×960 and 390×844: collection/T2 reference price €1,499; Gray selected with matching image; cart quantity 1 then 2; reload retained T2/Gray/2 and both €2,998 amounts; delivery/tax/setup notices remained; removal showed empty cart and Explore bikes returned to collection. Test cart restored to empty. Temporary viewport override reset.

For collection, detail, cart and empty cart, document scrollWidth was 1425px at desktop and 375px at mobile (below window.innerWidth 1440/390 respectively, allowing for the scrollbar). The inspected browser console returned no warn/error entries for this session. This does not establish complete browser compatibility, keyboard/screen-reader accessibility or all-site layout correctness.

No criterion was changed to accommodate a failed test; no implementation repairs or repair rounds were needed. The application and its visual design are unchanged.

Screenshots under workspace `outputs/class-6-audit/`: `desktop-cart-gray-quantity-2.png` (desktop viewport screenshot), `mobile-390-cart-gray-quantity-2.png` (mobile full-page capture), and the two original audit captures. See [build notes](build-notes.md) for provenance and limits.

## Short manual hand-in checklist

1. Review these three documents and the desktop/empty-state evidence, then upload them to the course submission location.
2. If asked for a live demonstration, repeat T1 on the hosted review and call €1,499 a reference price; explain that payment/delivery activation is outside the demonstrated flow.
3. Only if the course specifically requires the offline HTML to be demonstrated: open the existing HTML manually and repeat T1; automated direct file access was blocked. Report any discrepancy rather than treating hosted checks as an offline pass.

Malformed-storage UI, quote-edit UI and real provider outcomes remain NOT TESTED at UI/provider level where documented; the assignment state descriptions are complete without pretending these were demonstrated. Client merchant/catalogue/carrier approvals remain production work, not manual prerequisites for handing in this scoped assignment.

## Final verification and remaining state criteria

See [manual test record](manual-test-record.md) for viewport, steps, expected and actual results, and screenshot provenance.

| Criterion | Status | Evidence / limit |
|---|---|---|
| Three safeguard descriptions contain all requested fields and distinguish source/tests/UI/provider evidence | PASS | build-notes.md |
| Malformed saved data recovers safely in an injected browser scenario | NOT TESTED | Sanitizer unit test passed; UI injection not performed |
| Editing an accepted quote hides the old total/payment action in the browser | NOT TESTED | Code guard inspected; no successful configured quote/edit browser scenario |
| Real provider timeout/retry avoids duplicate outcomes and misleading success | NOT TESTED | Isolated server tests passed; real provider test not performed |
| Tablet, keyboard-only and offline HTML interactions pass | NOT TESTED | No execution evidence; structural HTML check is separate |
| Token/access documentation matches inspected CSS and hosting metadata | PASS | tokens.md reconciled; hosting read-only check reports active/public/version 12; settings unchanged |
| Final tests, TypeScript, production build and both HTML structural validations succeed | PASS | All rerun successfully on 24 October; 21 tests, 0 failures |

Fresh final desktop capture: outputs/class-6-audit/desktop-cart-gray-quantity-2-final.png. No application acceptance failure or repair round occurred. Code, visual design, Figma, GitHub and deployment settings unchanged.
