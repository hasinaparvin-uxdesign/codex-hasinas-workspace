# Class 6 — customer journey and screen map

24 October 2026. Assignment companion to [UX architecture](ux-architecture.md), not a replacement brief. Uses the existing responsive React application. Based on the [compliance audit](class-6-audit.md) and inspected routes in `storefront/src/App.tsx` and `Commerce.tsx`. The client is US-based; intended customers are in Portugal and selected European markets. No tutor-booking workflow applies.

## Numbered shopping journey

| Step / customer purpose | Existing screen or state | Primary transition | Recovery / boundary |
|---|---|---|---|
| 1. Discover bikes | `#/` Home | PRE ORDER or collection link → `#/bikes` | Hero model/specifications are reference content, not verified sale claims; PRE ORDER opens browsing, not a reservation |
| 2. Find a suitable model | `#/bikes` Collection | Search/filter/sort → matching product link | No matches → Clear filters → complete collection; reference prices do not establish merchant offers |
| 3. Inspect product and riding context | `#/bikes/coh-lift-t2` and other existing model routes; product gallery; optional `#/gallery` | Inspect images/specifications → choose finish | Image failure → fallback caption; close zoom dialog → gallery; source identity/image rights require client approval |
| 4. Compare, if needed | `#/compare` | Select Compare on cards/details → shortlist → product | Empty shortlist → Explore bikes; remove model → remaining shortlist. This step is optional |
| 5. Choose finish and review availability | Product detail; T2 Forest green / Gray | Select Gray → matching gallery image/selected state → Add to cart | Confirmed out-of-stock offer disables add; absent merchant offer says availability awaiting confirmation. Review cart remains possible without claiming stock |
| 6. Review and correct cart | `#/cart` | Check model/finish → quantity → subtotal → Review checkout | Remove → empty cart → Explore bikes; valid cart persists after reload; malformed saved cart is sanitized. Assignment demonstration ends here |
| 7. Check delivery and complete address | Product delivery checker, `#/delivery`, `#/checkout` | Country/postcode or full address → request server quote | Invalid postcode/address → correct fields; no configured coverage/stock → error, revise selection or destination; pending check → status. General delivery page directs exact pricing to checkout |
| 8. Review confirmed total and request payment | `#/checkout` | Accept current server quote → secure Stripe checkout when enabled | Address/cart change invalidates displayed quote; re-review required. Payments remain gated; carrier charges, actual inventory and approved prices are dependencies |
| 9. Understand payment outcome | Stripe return → `?session_id=…#/order`; cancellation → `#/checkout?cancelled=1` | Server-verified paid status → order preparation | Redirect alone never confirms payment. Pending/error/review → Check status again; missing reference → explanation. Actual provider outcome tests are unverified |
| 10. Track or resolve an issue | `#/order`, `#/support`, `#/parts` | Read verified dispatch reference or support/compatibility information | Tracking needs actual paid/fulfilled order; no account order history, transactional email or purchasable parts catalogue is claimed. Contacts/policies/parts need client data |

Main demonstrated path: **Collection → T2 → Gray → add one → cart → quantity two → reload → remove → empty cart → collection.** Existing €1,499 is a market-reference price; the arithmetic check is €1,499 × 2 = €2,998, not an approved sale quote.

## Cross-cutting states

- Initial application loading: `app/storefront.tsx` displays Loading the store… until the client application loads.
- Collection/cart/comparison empty states offer a return to browsing; unknown routes offer Explore the bikes.
- Labels and native required/email validation guide checkout; product delivery checks validate destination postcodes before requesting a quote.
- Request busy/error states appear in delivery/checkout; order status supports manual refresh. A global commerce connection failure is held in context but has no distinct site-wide retry banner; this remains an audit limitation.
- Additional safeguards, their actual evidence and UI verification limits are in [build notes](build-notes.md).

## Supporting screens and scope boundaries

| Route / element | Purpose and boundary |
|---|---|
| `#/gallery` | Customer decision support: posture, scale and everyday riding; returns to product browsing |
| `#/delivery`, `#/support`, `#/parts` | Customer purchase/support guidance; approved rates, terms, contact arrangements and sellable compatible parts remain external inputs |
| `#/admin` | Restricted operational inventory, shipping and order management; not part of the customer funnel; never seed fabricated client stock |
| `#/sources` | Research/provenance and client review record; not a normal purchase step |
| Login dialog | Truthful unavailable customer-account state, not a working account system; guest checkout form exists |
| Desktop/mobile HTML exports | Alternate previews of the same application, not two applications; offline commerce is deliberately unavailable |

Payment code, quote code and management screens exist; real Stripe transactions, refunds, carrier APIs, client stock, commercial prices, tax/policy correctness and launch readiness have not been established. Existing documents describing checkout/order screens purely as future work are historical; these implemented screens still depend on configuration and provider validation. See [production dependencies](production-readiness.md) and [commerce setup](commerce-setup.md). This map does not change those business decisions or any visual tokens.
