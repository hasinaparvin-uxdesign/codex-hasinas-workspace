# Class 6 — additional safeguards and verification

24 October 2026. Implementation evidence: `storefront/src/App.tsx`, `src/commerce.mjs`, `src/Commerce.tsx`, `server/commerce.mjs`, `tests/commerce.test.mjs` and `tests/server.test.mjs`. Current runnable source also exists at workspace `outputs/e-bike-review/storefront`.

These three specific safeguards are not explicitly named in the original brief. The brief already requests generic empty/loading/error states, checkout validation and cart feedback; those alone are not counted as unrequested work. This document explains existing safeguards without adding new features or business rules.

## 1. Malformed saved cart

- **Trigger:** Stored `ebike-review-cart-v1` contains invalid JSON, a non-array value, unknown products, invalid finish indexes, non-integer/non-positive quantities, or duplicate/excess lines.
- **Implemented behavior:** App.tsx catches JSON/read failures and initializes an empty cart. `sanitizeCart` drops invalid lines, merges matching product/finish lines and caps quantity at 10. A storage-write failure is caught; the current in-memory cart remains usable. Ten is the existing browser cart limit, not evidence of stock availability.
- **Customer-visible result:** Valid retained items appear normally; if none remain, the normal empty cart offers Explore bikes. There is no special corruption warning. A silent recovery may lose the customer's earlier selection. Browser UI under injected malformed data is UNVERIFIED.
- **Recovery:** Browse and add the intended model/finish again. Storage unavailability can prevent persistence after closing/reloading even though the current session works.
- **Need addressed:** Brief cart quantity/removal/subtotal behavior and trustworthy review step (IA step 6); bad local data must not crash the flow or inject a price/product.
- **Test procedure:** Run `node --test tests/commerce.test.mjs`. Existing test supplies unknown/invalid lines and duplicated excess quantities; expects one valid line capped at 10 and a non-array input to return an empty array. For browser validation in a disposable local/test session, back up this one key, set it to invalid JSON, reload `#/cart`, confirm normal empty recovery, then restore the original key. Repeat with a JSON array containing invalid lines. Do not alter real customer carts.
- **Observed result:** Existing sanitizer test PASS in the audit's 21/21 run. Ordinary empty cart and recovery control were observed separately; invalid JSON catch/storage failure are code-inspected, not exercised in browser. No assertion that corrupted-storage UI has passed.
- **Unresolved assumptions:** No customer-approved recovery-message requirement; no cross-device persistence. Existing quantity cap does not replace server stock validation.

## 2. Stale delivery quote after an edit

- **Trigger:** Address or cart changes after a successful checkout quote.
- **Implemented behavior:** CheckoutForm fingerprints `JSON.stringify({address,lines:cart})`; a quote is accepted for display/payment only while its stored fingerprint matches. `acceptedQuote` becomes null after edits, so the old total and payment action are not rendered; `pay()` also returns without a matching quote. Re-entering exactly the prior values may restore the old matching quote; no time-based expiry is implemented. Server checkout independently recalculates current stock/prices/rules.
- **Customer-visible result:** Edited state returns to the instruction to enter delivery details/check the complete total. The form offers Review total and delivery. The former total/payment action should disappear. This transition exists in code; successful quote → edit UI is UNVERIFIED because the hosted review has no approved stock/rates.
- **Recovery:** Request a new quote after the final address/quantity is chosen. Resolve validation or coverage errors rather than assume delivery is free/available.
- **Need addressed:** Brief clear delivery charges and checkout validation; IA steps 7–8. Prevent paying against a total for the wrong destination or selection.
- **Test procedure:** In an isolated authorized test setup with clearly labeled inventory/rate fixtures, add a bike, fill a valid address and obtain a quote. Change postcode, country, street or quantity separately; each time verify the old accepted total/payment action disappears, request a new quote and compare its response with configured fixture rules. Change quantity by returning to cart, then reopen checkout. Also test restoring prior values and a price/stock change before payment. Never seed fixtures into merchant inventory.
- **Observed result:** Source fingerprint guard inspected. Existing backend quote test PASS with fixture database prices and permitted/excluded postcodes; that test does not exercise the React edit transition. No carrier/API or current UI quote-edit pass is claimed.
- **Unresolved assumptions:** Client-approved quote lifetime, actual carrier charges/coverage and message wording remain open. The implementation is a configured-rule engine, not a carrier integration.

## 3. Uncertain payment outcome / repeated request

- **Trigger:** Request times out or provider response is unclear while opening checkout; customer retries or returns from payment before server confirmation.
- **Implemented behavior:** Browser requests have a 20-second timeout. CheckoutForm persists/reuses a request UUID for the same address/cart fingerprint when sessionStorage works; a changed fingerprint gets a new attempt. Server idempotency/reservation logic prevents repeated identical requests from creating a second order or reservation. An uncertain request keeps reserved stock until safely reconciled rather than immediately releasing it. OrderStatus only says Payment confirmed for server status `paid`; cancelled return explicitly says it does not confirm payment.
- **Customer-visible result:** Checkout failure displays an alert and clears busy state for retry. Status page shows the server status/error and Check status again; it does not treat redirect as proof of payment. Error wording depends on the actual failure; a dedicated reassuring timeout message is not claimed. Timeout/paid/pending UI under real provider conditions is UNVERIFIED.
- **Recovery:** Retry with unchanged details to reuse the attempt; authorized store management can reconcile uncertain orders. A known order reference can be checked again. If checkout-session creation never returned a reference, the customer cannot independently recover it through order lookup; store investigation is needed. Do not advise placing another order to resolve uncertainty.
- **Need addressed:** Brief reliable cart/checkout feedback and confirmation/error behavior; IA steps 8–9. Avoid duplicate charges/reservations and misleading success claims.
- **Test procedure:** Run `node --test tests/server.test.mjs`. Tests inject a throwing provider transport, repeat an identical checkout request, verify one order/reservation, verify safe reconciliation, reject unsigned/incorrect payment messages and handle expiry/late success. Real provider tests must separately cover timeout, decline, cancellation, webhook delay and retry in the client's authorized test mode before sales open.
- **Observed result:** Those server tests PASS in the audit's 21/21 run with isolated SQLite and injected transport. The uncertain-provider test receives 500, retains stock, blocks premature reconciliation and later safely releases its no-session reservation. Repeat-request test returns the same checkout URL with one order. These are fixture results, not verified Stripe/network behavior.
- **Unresolved assumptions:** Client merchant account, test/live secrets, webhook setup, customer communications and operational reconciliation are pending. Blocked sessionStorage/changed browser or changed details may prevent request reuse; no unlimited duplicate-payment guarantee is claimed. Refund synchronization and transaction emails remain release work.

## Validation and screenshot record

The [initial audit](class-6-audit.md) records successful 21-test, TypeScript, production build and desktop/mobile HTML structural checks on 24 October 2026. The 21-test command was rerun during completion: 21 PASS, 0 failed (4 frontend integrity tests and 17 server tests); SQLite experimental warning only. No application code changed for this documentation task; successful build/type/HTML results were reused rather than repeated. Fixtures never establish commercial prices, actual inventory or delivery promises.

Existing evidence at workspace `outputs/class-6-audit/`:

| File | Action shown | Viewport / provenance |
|---|---|---|
| `cart-gray-quantity-2.png` | Hosted T2 Gray after reload, quantity 2, line and subtotal €2,998 | Audit recorded window.innerWidth 425 CSS px; screenshot bitmap 410 px wide; height was not recorded, so not inferred from full-page image |
| `empty-cart.png` | Hosted empty cart after removing test item | Same narrow browser session; exact viewport height not recorded |
| `desktop-cart-gray-quantity-2.png` | Hosted cart after Gray selection, quantity change and reload; line and item subtotal €2,998 | Fresh viewport override 1440×960 CSS px; normal viewport screenshot, visually inspected |
| `mobile-390-cart-gray-quantity-2.png` | Same hosted cart flow after reload at mobile size | Fresh viewport override 390×844 CSS px; full-page screenshot, visually inspected |

Desktop and mobile flow PASS for the fixed T1 criterion in [tasks.md](tasks.md), including final removal and the Explore bikes recovery link. For collection/detail/cart/empty cart, document scroll widths were 1425px (desktop) and 375px (mobile), below the respective 1440/390 window widths. Captured console had no warn/error entries in this session. The browser capture output may exclude the scrollbar; bitmap dimensions are not substituted for the recorded CSS viewport. Full-page image height is content height, not viewport height. Original screenshots were preserved unchanged. Test cart restored to empty and viewport override reset.

No screenshot required for the scoped assignment remains missing: main desktop flow plus empty state are available, with additional mobile evidence. The three special safeguard UI states have no dedicated screenshots and remain unverified at UI/provider level as described above. Offline HTML interaction testing remains separate and UNVERIFIED because direct file:// browser access was blocked; no bypass is attempted. This documentation/evidence pass required no application repair.

## Scope and release boundaries

This assignment demonstrates the existing frontend shopping flow, not an activated store. Actual catalogue/stock, final VAT-inclusive prices, commercial imagery/model approval, client-owned payment account, real provider tests, carrier rules, legal policies and contact details remain dependencies. Existing historical documents/UI may still use private-review wording; it is not proof of current hosting access restrictions. No application styling, token values, stock records, payment gates, Figma or deployment were changed by this documentation work.

## Final reconciliation pass — 24 October 2026

All 21 tests, TypeScript, production build and desktop/mobile HTML structural validation were rerun successfully (exit 0). This supersedes the earlier choice to reuse build/type results. See manual-test-record.md for exact commands and limits. Fresh desktop screenshot: outputs/class-6-audit/desktop-cart-gray-quantity-2-final.png, viewport 1440x960, T2 Gray quantity 2 after reload with EUR 2,998 line/subtotal; removal and recovery retested. The prior mobile record remains valid for unchanged code.

Token documentation now reflects existing final CSS: labels 16/24px weight 600; values 14/22px weight 400; helper notes 14/22px #60747B; text buttons 140x48px; existing fonts/gradients preserved. Hero no longer uses a CSS reflection; review photo lettering was edited. No CSS changed. Read-only hosting metadata confirms public/active/version 12; historical private-review UI/metadata wording does not guarantee access restriction. Setup/readiness/current README descriptions reconciled without changing permissions. Dedicated malformed-storage UI, accepted-quote/edit UI, actual provider outcomes, tablet, keyboard and offline HTML interactions remain NOT TESTED. No production integration is newly verified.
