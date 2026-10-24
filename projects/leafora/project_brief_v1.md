# LEAFORA — PRODUCT & UX BUILD BRIEF
## Version 1.0 | Codex Implementation Handoff

**Project:** Leafora  
**Document type:** Product requirements, UX/UI specification, implementation brief  
**Initial market:** Portugal  
**Languages:** Portuguese and English  
**Platform:** Responsive e-commerce web application  
**Primary audience:** Individual customers, households, office managers, business buyers  
**Status:** Initial build brief; some commercial, technical, and operational decisions remain open.

---

# 1. Purpose of This Document

Build Leafora as a premium, practical, trustworthy plant-selling e-commerce platform that solves real customer problems and delivers a complete, low-friction shopping experience.

This document consolidates the product requirements and UX decisions discussed so far. Use it as the initial source of truth for implementation.

The project must not be treated as merely a collection of attractive UI screens. It must account for:

- Real customer needs and purchasing behaviour.
- Clear information architecture and intuitive navigation.
- Product discovery, selection, pricing, cart, checkout, and post-purchase support.
- Plant-care services, recurring plans, business customers, and partner sellers.
- Loading, success, empty, error, validation, and recovery states.
- Accurate prices, availability, delivery information, and promotion calculations.
- Accessibility, privacy, security, maintainability, and production readiness.
- A defensible UX rationale suitable for a professional design portfolio and interviews.

**Important:** Do not confuse Leafora with any other project the owner may be developing. Leafora is the plant-selling e-commerce platform.

# 2. Product Vision

Leafora helps people discover, choose, purchase, and care for plants suited to their spaces and needs.

The platform combines:

1. Plant shopping.
2. Guided plant discovery.
3. Curated and customizable plant bundles.
4. Plant-care guidance.
5. Professional plant-care services.
6. Recurring care plans.
7. Business and workplace greenery.
8. Selected partner-seller products.
9. Delivery, collection, and post-purchase support.

The intended experience should feel premium, botanical, calm, welcoming, clear, and easy to use.

## Primary homepage message

**“Discover beautiful plants”**

The homepage should primarily support browsing collections and shopping. Plant-care services and business offerings should remain accessible through clear, distinct navigation.

## Business model

Use a hybrid model comprising:

- Products sold directly by Leafora.
- Products from selected, Leafora-approved partner shops.
- Professional plant-care services.
- Curated plant packages and customizable bundles.
- Eligible recurring care plans.
- Business purchases and workplace greenery services.

Leafora controls partner approval, listing quality, pricing rules, and customer-facing standards.

Do not assume partner sellers require a self-service portal in the first implementation. Staff-managed partner records and inventory are the current requirement.

## Brand status

Leafora is the working brand name. Trademark, company-name, and domain availability have not been confirmed.

# 3. Non-Negotiable Product and UX Principles

Every major feature must have a clear purpose and a defensible rationale.

## 3.1 Solve real problems

Do not invent customer research, user interviews, statistics, pain points, or business evidence.

Distinguish clearly between:

- Confirmed product requirements.
- Research-backed findings.
- Hypotheses that need validation.
- Implementation assumptions.
- Future opportunities.

Where evidence is missing, identify what should be researched or tested.

## 3.2 Keep the experience simple

- Use clear, familiar navigation.
- Reduce unnecessary steps.
- Use understandable language.
- Keep important information visible at the decision point.
- Use progressive disclosure when it reduces complexity.
- Avoid unnecessary pop-ups, forced account creation, and distracting promotions.
- Preserve user input during recoverable errors.
- Make the next action obvious.

## 3.3 Make every feature meaningful

Do not add features simply because competitors have them.

For each feature, document:

- Customer problem.
- Intended user and context.
- Evidence or hypothesis.
- Design decision.
- Alternatives considered.
- Applicable UX principles.
- Trade-offs.
- Validation approach.

## 3.4 Build the complete experience

A screen is not complete merely because its ideal state looks good.

For each relevant component, implement and test:

- Default and success states.
- Loading and pending states.
- Empty states.
- Validation states.
- Error and failure states.
- Missing-data states.
- Unavailable and out-of-stock states.
- Recovery actions.
- Disabled and permission-restricted states.
- Responsive and accessible behaviour.

## 3.5 Never mislead customers

Never fabricate:

- Live stock or availability.
- Delivery dates or fees.
- Payment confirmations.
- Order tracking.
- Reviews or verified-purchase badges.
- Customer testimonials.
- Service appointments.
- Partner data.
- Product claims or plant-care facts.
- Discounts, reference prices, or savings.

Demo data must be identified as illustrative where necessary. Demo functionality must not be presented as a real production integration.

# 4. Reference Materials and Visual Direction

## Figma reference

Use the following supplied Figma file as a design reference:

https://www.figma.com/design/uNAidTwsR7aBBWyR5gmiMF/Figma-Pro_Hasina?node-id=0-1&t=7d8xBCG7zzKNUCI9-1

The owner has also supplied a reference image named `Frame 134.png`, containing four mobile reference screens:

1. Onboarding.
2. Product details.
3. Cart.
4. Home.

The owner will provide or attach reference images to Codex as necessary.

**Implementation requirement:** Inspect the actual reference images and available Figma material before implementing the relevant screens. Do not claim to have inspected Figma nodes or extracted design tokens unless that inspection actually occurred.

## Visual direction

The intended visual language is:

- Premium botanical aesthetic.
- Deep emerald and forest-green accents.
- Muted sage and olive tones.
- High-quality botanical photography.
- Elegant, serif-like headline typography where supported by the reference.
- Rounded cards and panels.
- Subtle translucent or glass-like surfaces where present in the reference.
- Calm spacing and strong visual hierarchy.
- Clear plant-care and suitability information.
- Mobile-friendly navigation, including bottom navigation where shown in the reference.
- Consistent spacing, typography, controls, imagery, and interaction states.

Exact colours, font families, spacing values, radii, and other design tokens must be extracted from the available reference where possible. Do not invent token values and attribute them to Figma.

## Fidelity requirements

- Implement the four supplied reference screens closely.
- Do not perform a major redesign without approval.
- Preserve the established identity, hierarchy, and composition.
- Extend the design system consistently to desktop and tablet.
- Do not simply stretch mobile layouts across desktop.
- Add necessary functional states without compromising the reference design.
- Use licensed, approved, or otherwise appropriately sourced imagery.
- Use genuine seller-approved product images for real launch listings.
- Clearly distinguish AI-generated concept images from genuine product photography.

# 5. Platform and Localization

Build one responsive web application for desktop, tablet, and mobile.

Do not create separate native iOS and Android apps as part of this scope.

Support:

- Portuguese.
- English.
- Language switching from a visible location.
- Browser-language suggestions for new visitors.
- Manual language selection.
- Remembered language preferences where appropriate.
- Localized dates, number formats, and currency display.
- Accessible navigation and controls across screen sizes.

The initial market is Portugal. EUR pricing is expected, but the actual tax, accounting, and pricing configuration must be verified before production.

Do not hard-code text throughout components. Use a maintainable localization system.

# 6. Information Architecture and Navigation

Proposed primary navigation:

- Home.
- Shop by Space.
- Shop by Plant Type.
- Plant Care Services.
- Promotions.
- For Businesses.
- Search.
- Wishlist.
- Cart.
- Account.
- Language selector.

Adjust the exact navigation presentation to match the reference design and responsive requirements.

## Shop by Space

Support distinct, meaningful categories such as:

- Home.
- Office.
- Garden.
- Rooftop.
- Indoor Spaces.
- Outdoor Spaces.

Avoid redundant categories or unnecessary duplication.

## Shop by Plant Type

Possible categories include:

- Flowering plants.
- Succulents.
- Herbs.
- Trees.
- Other verified catalog categories.

The final taxonomy should reflect actual inventory and user research, not arbitrary assumptions.

## Navigation principles

- Customers should understand where a navigation item will lead.
- Product discovery should not depend on knowing botanical terminology.
- The plant finder should complement, not replace, category browsing.
- Plant Care Services must be clearly separate from ordinary shopping.
- For Businesses must be visible without making the consumer shopping experience complicated.

# 7. Homepage

The homepage should communicate Leafora's value and help customers begin shopping quickly.

Required elements, adapted to the reference design:

- Premium botanical hero section.
- Primary message: “Discover beautiful plants”.
- Clear primary shopping action.
- Shop by Space.
- Shop by Plant Type.
- Curated plant collections.
- Featured products or collections based on actual catalog data.
- Relevant promotional offers.
- Plant bundle discovery.
- Plant-care guidance or services entry point.
- For Businesses entry point.
- Trust-building information based on genuine policies and capabilities.
- Responsive footer with relevant support, privacy, and policy links.

Do not fill the homepage with every feature. Prioritize the shopping journey and use a clear visual hierarchy.

Include loading, unavailable-content, and image-failure behaviour where applicable.

# 8. Guided Plant Finder

Provide an optional guided discovery experience for customers who are unsure which plants to choose.

Possible questions:

- What type of space are you decorating?
- What are the light conditions?
- How much space is available?
- What is your plant-care experience?
- What is your budget?

Use the answers to recommend plants only when relevant catalog and plant-care data supports the recommendation.

Each recommendation should explain why the plant may be suitable, such as its light requirements or size.

## Required states

- Introduction.
- Question and answer selection.
- Missing-answer validation.
- Back and edit answers.
- Loading recommendations.
- Successful recommendations.
- No suitable matches.
- Insufficient plant data.
- Recommendation failure.
- Retry or return to browsing.

Do not claim that a plant is suitable without supporting care and suitability data. Avoid presenting recommendations as guaranteed outcomes.

# 9. Product Catalog and Product Detail Pages

Product listings and details must combine attractive imagery with useful, decision-making information.

## Product listing information

Where available:

- Product image.
- Clear plant name.
- Price.
- Product size or variant.
- Relevant care or suitability attributes.
- Availability.
- Seller information where appropriate.
- Product details link.
- Add-to-cart action when valid.

Filtering, sorting, and category navigation should work consistently.

## Product detail page

Include:

- High-quality product imagery.
- Product name and price.
- Plant size and available variants.
- Light requirements.
- Care requirements.
- Suitable spaces.
- Availability.
- Seller and fulfilment information.
- Delivery or collection information when reliable.
- Quantity selection.
- Compatible pot options, where available.
- Add-to-cart action.
- Wishlist action.
- Verified reviews when genuine review data exists.
- Related products or bundles where relevant.

## Pots and product options

Customers may purchase plants without pots.

Where compatible pots are available:

- Show compatible choices.
- Explain whether a pot is included.
- Display any additional price.
- Update the product total when a paid option changes.
- Carry the selection through the cart and checkout.
- Validate compatibility and availability.

Do not imply that a pot is included when it is sold separately.

## Product states

Include:

- Loading.
- Missing image.
- Missing or incomplete product data.
- Out of stock.
- Variant unavailable.
- Invalid option combination.
- Failed add-to-cart action.
- Successful add-to-cart action.
- Changed price or availability.
- No reviews.
- Review-loading or review-submission failure.

# 10. Plant Bundles and Packages

Plant bundles are a confirmed part of the intended product offering.

Support both fixed curated bundles and customizable bundles.

## 10.1 Fixed curated bundles

Examples of possible bundle concepts:

- Three plants in small, medium, and large sizes.
- Plants selected for a living room.
- Plants selected for an office.
- Coordinated botanical packages.
- Seasonal collections.

These are illustrative concepts until actual bundle contents are approved.

## 10.2 Custom bundles

Allow customers to select from eligible plants or sizes where the configured business rules support customization.

The interface should show:

- Available selections.
- Plant names and sizes.
- Individual prices where applicable.
- Bundle eligibility.
- Current bundle price.
- Discount or savings.
- Remaining selections, if a bundle requires a specific number of items.
- Availability of each selected item.
- Clear add-to-cart action.

## 10.3 Bundle pricing

Calculate package prices using configured, valid rules.

Example only:

| Item | Illustrative price |
|---|---:|
| Small plant | €9.99 |
| Medium plant | €15.00 |
| Large plant | €25.00 |
| Separate-purchase total | €49.99 |
| Example bundle price | €44.99 |
| Example saving | €5.00 |

Do not hard-code these example prices.

The system must correctly calculate:

- The total of eligible individual prices.
- The bundle price.
- Discount amount.
- Discount percentage where useful.
- Tax treatment.
- Any applicable additional options.
- Final cart and checkout totals.

If a customer changes a selection or size, recalculate the bundle price and eligibility.

Do not silently substitute an unavailable plant.

## 10.4 Bundle states

Include:

- Initial selection.
- Incomplete bundle.
- Complete eligible bundle.
- Invalid combination.
- Loading availability.
- Out-of-stock selection.
- Changed bundle price.
- Discount applied.
- Discount no longer eligible.
- Add-to-cart success or failure.

Bundle contents and pricing must remain identifiable in the cart, order confirmation, and relevant refund calculations.

# 11. Wishlist and Saved Collections

Support:

- A default wishlist.
- Custom collections such as “Living Room”, “Office”, and “Garden Project”.
- Moving saved items into the cart.
- Using eligible saved items when creating a plant package.

Design and document:

- Empty wishlist.
- Successful save.
- Failed save.
- Duplicate saved item handling.
- Unavailable saved product.
- Guest persistence.
- Sign-in requirements, if applicable.
- Collection creation, editing, and deletion.

Guest persistence, sharing, and cross-device synchronization remain technical decisions to assess.

# 12. Cart and Transparent Pricing

The cart must provide complete, understandable pricing.

Customers must always be able to see:

- Which products they selected.
- The quantity of each product.
- The unit price.
- The line total for each product.
- Selected pots and paid options.
- Applied discounts.
- Product subtotal.
- Delivery or collection charges.
- Other applicable charges.
- Estimated or confirmed final total, clearly distinguished.
- Total number of units.
- Number of distinct cart line items.

## Core calculation

For each line:

**Line total = quantity × applicable unit price, including selected paid options where relevant.**

The cart subtotal is the sum of all applicable line totals, after applying the configured product-level pricing rules.

The final amount is calculated from:

**Final total = applicable merchandise subtotal − applicable discounts + delivery charges + other applicable charges.**

Taxes must be handled correctly for the chosen pricing model. Do not add tax twice if displayed product prices already include it.

## Quantity controls

- Provide clear increase and decrease controls.
- Recalculate line totals and order totals when quantity changes.
- Prevent quantities below the allowed minimum.
- Validate stock and any maximum order quantity.
- Explain when a quantity cannot be fulfilled.
- Avoid losing the rest of the cart when one line fails.

## Multiple sellers

The cart must support products from multiple sellers.

Display relevant seller and fulfilment details. Make seller-specific delivery estimates and fees understandable.

The customer should see the combined order total before committing to payment.

## Cart states

- Empty cart.
- Cart with one or more products.
- Loading.
- Quantity update in progress.
- Quantity update failure.
- Stock conflict.
- Price change.
- Product unavailable.
- Invalid bundle.
- Coupon applied.
- Coupon rejected or expired.
- Delivery estimate unavailable.
- Seller fulfilment restriction.
- Network failure.
- Successful transition to checkout.

Never silently remove, substitute, or reprice a product without explaining the change.

# 13. Checkout UX

Design a guided checkout that is simple, transparent, accessible, and resilient to failure.

Recommended flow:

1. Cart review.
2. Contact details and delivery or collection.
3. Payment.
4. Final order review and placement.
5. Order confirmation.

The exact step arrangement may be adapted to the reference and validated against usability goals, but the customer must always understand their progress.

## Guest checkout and accounts

Support guest checkout and optional account creation.

Do not force customers to register before purchasing unless a specific verified business or operational requirement necessitates it.

Potential account capabilities:

- Order history.
- Saved addresses.
- Wishlists.
- Service bookings.
- Recurring plans.
- Plant-care history.

The exact account dashboard scope can be refined during implementation.

## Contact and delivery

Collect only the information required for the chosen fulfilment method.

Support applicable delivery or collection options, customer contact details, and delivery addresses.

Validate input accessibly and preserve entered details during recoverable errors.

## Final review

Before placing the order, show:

- Products and quantities.
- Unit prices and line totals.
- Pots and options.
- Discounts.
- Subtotal.
- Delivery or collection charges.
- Applicable additional charges.
- Final payable total.
- Delivery address or collection details.
- Payment method.
- Relevant purchase terms.

Make it easy to return to an earlier step and correct details.

## Checkout error and recovery states

Include:

- Missing required field.
- Invalid email or postal code.
- Invalid or incomplete address.
- Unsupported delivery location.
- Delivery price unavailable.
- Seller cannot fulfil the selected method.
- Stock changed.
- Price changed.
- Coupon rejected.
- Session expired.
- Network failure.
- Payment declined.
- Payment pending.
- Payment outcome unknown.
- Payment succeeded but order confirmation is delayed.
- Order submission failure.
- Duplicate submission prevention.

Errors must explain the problem and provide the next safe action.

Do not clear the customer's entire checkout because one field is invalid.

# 14. Payments

Requested payment methods:

- Debit and credit cards.
- MB WAY.
- Cash on delivery or collection where supported.
- Corporate invoicing for eligible business customers.

These are requirements, not confirmed integrations.

Assess suitable providers and actual support for each method before implementation.

## Payment safety requirements

- Never store raw card details unnecessarily.
- Use the selected provider's secure payment flow.
- Confirm transaction status through trusted provider responses.
- Protect payment operations against duplicate submissions.
- Use appropriate idempotency mechanisms where supported.
- Do not mark an order paid because the browser displays a success message.
- Handle delayed and asynchronous payment confirmation.
- Reconcile payment and order status.
- Explain whether an order is confirmed, pending, failed, or paid but awaiting order reconciliation.

## Payment messages

Illustrative copy:

**Declined**

“We couldn’t complete your payment. Try another payment method or contact your payment provider if you need help.”

**Pending**

“Your payment is still being confirmed. Please wait while we check its status.”

**Unknown outcome**

“We couldn’t verify your payment status. Your payment may still be processing. Please check its status before trying again.”

**Confirmed**

“Payment confirmed. We’ll show your order confirmation once your order has been successfully recorded.”

Do not tell a customer that payment failed if the transaction outcome is unknown.

Do not permit an unsafe retry until the prior transaction status has been checked where necessary.

# 15. Delivery and Fulfilment

Support delivery and collection where operationally available.

Requirements:

- Location-based fulfilment availability.
- Seller-specific fulfilment options.
- Accurate delivery estimates where supported.
- Configurable delivery fees.
- Seller-specific delivery charges.
- Collection options where available.
- Clear delivery information before order placement.
- Revalidation when addresses, quantities, sellers, or fulfilment methods change.

Delivery fees may depend on:

- Seller.
- Delivery location.
- Delivery area.
- Order size.
- Fulfilment method.
- Other configured business rules.

Do not invent free-delivery thresholds, rates, carrier names, collection hours, or delivery dates.

Open decisions include delivery zones, carriers, collection points, cut-off times, inventory synchronization, and mixed-seller fee calculation.

If delivery cannot be calculated, explain the limitation and the next step rather than displaying a fabricated estimate.

# 16. Promotions, Discounts and Abandoned Cart Recovery

Leafora will support a configurable promotions system.

## Promotion types

- Abandoned-cart offers.
- First-order offers.
- Seasonal sales.
- Bundle discounts.
- Coupon codes.
- Eligible free-delivery offers if introduced later.
- Other approved campaigns.

The system must support:

- Start and end dates.
- Eligible products or collections.
- Customer eligibility.
- Minimum purchase conditions where applicable.
- Exclusions.
- Discount limits.
- Coupon validation.
- Discount stacking rules.
- Tax treatment.
- Refund and cancellation behaviour.
- Clear promotional terms.

Do not permanently hard-code a 10% discount.

## Abandoned-cart recovery

Where supported, preserve carts so customers can resume shopping.

An abandoned cart may qualify for a reminder after a configurable period, but merely adding an item to a cart does not automatically authorize marketing messages.

Requirements:

- Determine eligibility before sending.
- Suppress reminders after a completed purchase.
- Respect applicable privacy, marketing, and consent requirements.
- Use appropriate frequency limits.
- Respect unsubscribe requests.
- Avoid repeated unnecessary messages.
- Use genuine, valid offers only.
- Revalidate prices and inventory when the customer returns.
- Make the cart link restore the customer's selection where technically supported.

An abandoned-cart reminder containing a promotional discount must be evaluated for applicable marketing-consent requirements. Do not assume that every cart reminder is permissible under the same rules as transactional communication.

## Example promotional message

Subject: Your plants are waiting for you

“ You left a few favourites in your cart. Whenever you're ready, you can return to your selection and pick up where you left off.”

An eligible campaign may offer a configured discount, such as 10% off qualifying products, subject to clear terms and expiry.

This copy and discount are illustrative. The actual message must reflect a real campaign.

## Promotional UX

- Show applicable offers clearly.
- Do not imply an offer is guaranteed when it is conditional.
- Do not use fake urgency, invented scarcity, or misleading countdowns.
- Show the actual saving.
- Explain expired or ineligible coupons.
- Recalculate totals correctly.
- Make exclusions and stacking rules understandable.

# 17. Order Confirmation and Post-Purchase Experience

Provide a complete post-purchase experience.

Required features:

- Order confirmation.
- Unique order reference.
- Itemized order summary.
- Payment status.
- Delivery or collection details.
- Order status and tracking where genuinely available.
- Relevant order-change notifications.
- Issue-reporting options.
- Plant-care guidance after delivery.

Do not show a confirmed order number before an order has been recorded successfully.

Do not show fabricated tracking events.

If tracking is not connected, clearly explain the available status information rather than simulating live carrier data without a demo label.

## Order states

- Order submitted.
- Awaiting payment.
- Payment pending.
- Payment confirmed.
- Order confirmed.
- Processing.
- Preparing for fulfilment.
- Dispatched or ready for collection, where applicable.
- Delivered or collected, where confirmed.
- Cancelled.
- Refund pending.
- Refunded.

Use only states that the actual system can support. Map them to real operational events.

Transactional notifications must be separated from optional marketing communications.

# 18. Returns, Issues and Customer Support

Provide clear workflows for:

- Damaged delivery.
- Missing items.
- Incorrect items.
- Unhealthy plants on arrival.
- Ordinary return requests.
- Order or payment issues.
- Delivery issues.
- Service-related complaints.

Offer possible resolutions such as replacement or refund where appropriate under the actual policy and applicable law.

Do not invent blanket rules such as “plants can never be returned” or promise unlimited free replacements.

Policies must be reviewed for Portuguese and applicable EU consumer-law requirements.

## Support channels

Requested channels:

- Contact form.
- Email.
- Live chat during published support hours.

Support hours, email provider, and live-chat integration remain open decisions.

If live support is closed, show actual published hours and provide a genuine fallback.

Do not present a demo chat as a live agent.

## Support states

- Form validation.
- Submission in progress.
- Submission successful.
- Submission failed.
- Attachment upload failed, if attachments are supported.
- Live chat unavailable.
- Support outside opening hours.
- Issue received and awaiting response.
- Resolution pending.

Do not claim a support request has been received unless it has actually been recorded or submitted successfully.

# 19. Reviews and Trust

Support verified-purchase reviews with optional customer-uploaded photos.

Requirements:

- Only assign a verified-purchase badge when backed by a real eligible order.
- Clearly label demo reviews.
- Do not invent real customer reviews.
- Provide understandable review submission and moderation states.
- Handle failed photo uploads.
- Explain when reviews are awaiting moderation.
- Show genuine product and care information.
- Avoid unsupported claims about plant health, suitability, or outcomes.

Trust should be established through accurate information and reliable functionality, not decorative trust badges.

# 20. Inventory and Partner Sellers

Support seller-specific inventory and fulfilment information.

Requirements:

- Track inventory by seller and product or variant.
- Prevent overselling.
- Revalidate stock before order placement.
- Display availability accurately.
- Handle inventory synchronization failures.
- Track seller-specific fulfilment options.
- Explain stock changes.
- Avoid silent substitutions.

Automatic out-of-stock substitutions have not been approved.

Leafora staff manage partner records and seller inventory initially. A full self-service partner portal is not a confirmed requirement.

Partner integrations and synchronization methods remain open technical decisions.

# 21. Plant Care Services and Recurring Plans

Provide a dedicated Plant Care Services section.

## Service types

- Standard services that customers can book directly online.
- Larger or complex projects that require a quote request.
- Fixed, predefined care packages.
- Customizable care plans.

Actual service names, prices, provider coverage, and availability must be configured from verified business information.

## Booking

Support:

- Service information.
- Price or quote explanation.
- Available appointment options.
- Booking submission.
- Confirmation.
- Rescheduling or cancellation where permitted.
- Provider availability checks.
- Booking failure and recovery.

Do not claim an appointment is confirmed until availability has been verified and the booking recorded.

## Recurring care plans

Support self-service views of:

- Plan details.
- Upcoming charges.
- Upcoming visits.
- Eligible plan changes.
- Pause where permitted.
- Cancellation under clear terms.

Replacement benefits apply only to eligible plans and must have defined conditions, exclusions, and limits. Do not promise unlimited free replacements.

Plan billing, cancellation terms, renewal rules, service responsibilities, provider assignment, and replacement eligibility remain open business decisions.

Real recurring billing, scheduling, and reminders require appropriate integrations.

# 22. Business Customers

Provide a visible For Businesses entry point.

Support relevant capabilities such as:

- Workplace and office plant purchases.
- Business account registration.
- Corporate invoicing for eligible customers.
- Business users and business approvers as distinct roles.
- Optional purchase approval workflows.
- Configurable approval requirements for businesses that need them.

Small businesses may be allowed to order directly, while larger businesses may configure approvals.

Do not require an approval workflow for every business customer.

Business verification, invoice and tax workflows, approval thresholds, and detailed approval rules remain open decisions.

# 23. Admin Dashboard and Role-Based Access

Build an operations dashboard that supports:

- Products.
- Inventory.
- Partner sellers.
- Orders.
- Promotions.
- Customer support.
- Plant-care bookings.
- Recurring care plans.
- Business accounts.

Advanced analytics and financial reporting are not confirmed requirements for the initial scope.

## Roles

The role model should accommodate:

- Shopper.
- Business user.
- Business approver.
- Partner seller.
- Support staff.
- Service manager.
- Administrator.

Implement role-based access and secure authorization for sensitive actions.

Do not rely solely on hiding interface elements. Enforce access restrictions at the appropriate server or data layer.

A separately configurable, granular permission-management system has not been selected.

Define a practical initial permission matrix before implementing sensitive operations.

# 24. Privacy and Data Protection

Leafora must follow a privacy-first approach.

Requirements:

- Collect only necessary information.
- Provide clear privacy notices and consent choices where required.
- Separate marketing preferences from essential transactional communication.
- Provide accessible privacy settings.
- Support applicable access, correction, and deletion rights.
- Evaluate cookie and tracking technologies.
- Do not activate non-essential tracking without appropriate consent.
- Protect personal data and account information.
- Avoid collecting customer data solely for promotional purposes without an appropriate legal basis.
- Respect marketing opt-outs.
- Document retention and deletion rules.

Assess applicable GDPR and Portuguese legal requirements.

Do not claim legal compliance merely because a privacy page exists. Legal review and correct implementation are required.

# 25. Accessibility

The owner has not yet confirmed a formal accessibility target.

Recommended implementation target: **WCAG 2.2 AA**, subject to validation and testing.

Include:

- Semantic HTML.
- Keyboard-accessible interactions.
- Visible focus indicators.
- Appropriate screen-reader labels.
- Accessible form labels and errors.
- Sufficient text and interface contrast.
- Touch-friendly controls.
- Responsive text and layouts.
- Accessible dialogs and menus.
- Status announcements for asynchronous actions.
- Reduced-motion support.
- Meaningful alternative text.
- Accessible progress indicators and checkout steps.
- No reliance on colour alone to communicate meaning.

Do not claim WCAG compliance without appropriate testing.

# 26. Complete UI State System

State design is a core requirement across the application, not a final polish task.

Each relevant page and component must consider:

1. Default state.
2. Loading state.
3. Skeleton or progress state where appropriate.
4. Success state.
5. Empty state.
6. Validation state.
7. Error state.
8. Missing-data state.
9. Unavailable state.
10. Permission-restricted state.
11. Pending state.
12. Recovery state.

Not every component needs every state. Include the states relevant to its actual behaviour.

## State behaviour requirements

- Explain what happened.
- Use clear, non-technical language.
- Provide a safe next action where possible.
- Preserve valid user input.
- Prevent duplicate submissions.
- Avoid exposing sensitive internal details.
- Announce important changes accessibly.
- Avoid infinite loading.
- Provide a retry action when retrying is safe.
- Distinguish unknown outcomes from confirmed failures.
- Use consistent visual treatment throughout Leafora.

## Representative examples

### Plant recommendations loading

“Finding plants that suit your space…”

If the request fails, provide a retry option and allow the customer to return to browsing.

### Empty wishlist

“Your wishlist is waiting for its first plant.”

Provide a relevant action to browse products.

### Product unavailable

“This plant is no longer available. Review the item or explore available alternatives.”

Do not silently replace it.

### Delivery estimate unavailable

“We can’t estimate delivery for this address yet. Check your details or contact our support team.”

Do not invent fees or dates.

### Payment failure

“We couldn’t complete your payment. Try another available payment method.”

Use this only when the transaction is confirmed to have failed.

### Payment outcome unknown

“We couldn’t verify your payment status. Your payment may still be processing. Please check its status before trying again.”

Verify the transaction before permitting an unsafe retry.

### Appointment unavailable

“This appointment time is no longer available. Choose another available time to continue.”

Recheck availability and prevent conflicting bookings.

### Support offline

“We’re currently offline. You can send us a message using the contact form.”

Use genuine support hours and a working fallback.

# 27. Cart and Checkout Calculation Requirements

These calculations must be consistent across the cart, checkout, order confirmation, and any applicable account order history.

## Required displayed amounts

- Quantity per product line.
- Unit price.
- Line total.
- Selected option prices.
- Merchandise subtotal.
- Applied discount.
- Delivery or collection fee.
- Applicable additional charges.
- Final payable total.
- Total product units.
- Number of distinct cart lines where useful.

## Calculation principles

- Recalculate line totals when quantities or paid options change.
- Apply only valid promotions.
- Apply bundle pricing and discount rules correctly.
- Revalidate stock and pricing before order placement.
- Handle taxes according to the configured pricing model.
- Keep server-side pricing authoritative.
- Prevent rounding inconsistencies.
- Explain price changes before the customer commits.
- Reconcile the amount authorized or charged with the actual order total.

The displayed final total must not contain hidden charges that appear only after the customer has committed to purchase.

# 28. Technical Implementation Guidance

## Inspect the existing repository first

Before choosing a stack or making major changes:

1. Inspect the repository structure.
2. Identify the existing framework and build tools.
3. Read the existing README and project instructions.
4. Inspect package manifests and installed dependencies.
5. Identify current routes, components, assets, design tokens, and test infrastructure.
6. Inspect supplied UI reference images.
7. Review the Figma reference where access and tools permit.
8. Determine what already exists and what must be implemented.
9. Report any blockers before replacing major architecture.

Do not replace an existing stack without a clear reason and approval.

## Architecture

Use a maintainable architecture compatible with the existing repository.

Prefer TypeScript if the existing stack supports it.

Separate concerns for:

- UI components.
- Page and route composition.
- Domain models.
- Pricing and promotion rules.
- Cart and checkout logic.
- Inventory and fulfilment.
- Authentication and authorization.
- Service bookings and recurring plans.
- Localization.
- Data access.
- External integrations.
- Error handling.

Avoid giant components and duplicated business logic.

## Data models

Plan appropriate models for:

- Product.
- Product variant or size.
- Plant-care attributes.
- Pot and compatible options.
- Seller.
- Inventory.
- Bundle.
- Promotion.
- Cart and cart line.
- Customer.
- Address.
- Business account.
- Role and authorization.
- Order and order line.
- Payment transaction.
- Fulfilment.
- Delivery estimate.
- Booking.
- Care plan and subscription.
- Review.
- Support request.

Use a suitable relational or equivalent data model based on the existing stack and actual operational requirements.

## Validation and reliability

- Validate user input.
- Treat server-side validation as authoritative.
- Handle network and service failures.
- Avoid duplicate order creation.
- Use appropriate transaction boundaries.
- Make retry behaviour safe.
- Do not expose secrets in source code.
- Use environment variables for secrets and environment-specific settings.
- Document configuration requirements.
- Provide useful setup instructions.
- Add tests for critical business logic.

## Integrations

Do not select payment, hosting, database, shipping, email, chat, or subscription providers without assessing the current project and relevant business requirements.

Where real integrations are unavailable, implement clean adapters and mock data.

Clearly identify mocked behaviour and list the steps required for a real integration.

# 29. Prototype Versus Production

A working prototype can demonstrate the experience, but it must not be misrepresented as a complete production system.

## Prototype scope

Demonstrate:

- Responsive homepage.
- Four reference screens.
- Category browsing.
- Guided plant finder.
- Product details.
- Pot selection.
- Fixed and customizable bundles.
- Wishlist and saved collections.
- Multi-seller cart.
- Accurate client-side demonstration of itemized totals.
- Guided checkout.
- Guest and account entry points.
- Illustrative delivery calculations.
- Payment states using safe mocks.
- Order confirmation and tracking states.
- Issue reporting.
- Plant-care guidance.
- Service booking and quote requests.
- Recurring care plan screens.
- Business account and approval flows.
- Support forms and clearly labelled demo chat.
- Review interface with clearly labelled demo data.
- Admin screens.
- Role-based navigation.
- Portuguese and English switching.
- Privacy controls.
- Accessibility behaviours.
- Loading, success, empty, error, validation, and recovery states.

The prototype must be internally coherent and interactive. Do not implement every control as a decorative placeholder.

## Production work still required

Depending on the final architecture and providers:

- Secure authentication and sessions.
- Persistent carts, accounts, wishlists, orders, and bookings.
- Real payment processing.
- MB WAY and card integration.
- Corporate invoicing.
- Reliable inventory and seller synchronization.
- Real delivery calculations and tracking.
- Email, chat, and notification integrations.
- Recurring billing.
- Real appointment scheduling.
- Verified-purchase reviews.
- GDPR-related workflows.
- Security review.
- Monitoring, backups, and operational support.
- Deployment configuration.

Document which functionality is mocked, which is working locally, and which requires external configuration.

# 30. UX Rationale and Portfolio Documentation

Leafora is intended to be part of the owner's professional UX/UI portfolio.

The implementation and design process should help the owner understand and explain the decisions confidently in interviews.

Use relevant UX principles where they genuinely inform the design, including:

- User-centred design.
- Nielsen's usability heuristics.
- Visibility of system status.
- Error prevention and recovery.
- Recognition rather than recall.
- Consistency and standards.
- User control and freedom.
- Hick's Law, applied carefully to unnecessary choice complexity.
- Cognitive-load reduction.
- Clear information scent.
- Accessibility and inclusive design.
- Progressive disclosure.
- Trust and pricing transparency.
- Familiar e-commerce conventions, where appropriate.

Do not insert principle names merely to make the project appear more sophisticated.

For major decisions, record:

1. Customer problem.
2. Evidence or hypothesis.
3. User goal and context.
4. Design alternatives.
5. Chosen approach.
6. Rationale and relevant principles.
7. Trade-offs.
8. Edge cases.
9. Validation approach.
10. Learning and possible iteration.

Do not invent research findings or claim testing occurred if it did not.

Where appropriate, propose usability tests around realistic tasks such as finding a suitable plant, selecting a bundle, understanding delivery costs, correcting an error, and completing checkout.

# 31. Implementation Priorities

Implement progressively without losing sight of the full scope.

## Priority 1 — Design fidelity and shopping foundation

- Inspect repository and references.
- Establish design tokens and reusable components.
- Implement the four reference screens.
- Build responsive homepage and navigation.
- Build category browsing.
- Build product details.
- Implement the plant finder.
- Implement cart and itemized pricing.
- Implement the primary checkout flow.
- Add essential states and accessibility behaviour.

## Priority 2 — Complete purchase and post-purchase

- Promotions and coupons.
- Plant bundles.
- Wishlist.
- Delivery and fulfilment logic.
- Payment-state handling.
- Order confirmation and status.
- Issue reporting.
- Plant-care guidance.
- Reviews and trust features.

## Priority 3 — Services and business workflows

- Plant-care services.
- Booking and quote requests.
- Recurring plans.
- Business accounts.
- Approval workflows.
- Admin and partner management.

## Priority 4 — Production integrations and validation

- Real integrations.
- Security and privacy review.
- Accessibility testing.
- Automated and manual testing.
- Operational reliability.
- Deployment readiness.

These priorities organise delivery; they do not remove agreed features from the product scope.

# 32. Acceptance Criteria

The work is not complete simply because the homepage renders.

## Design

- Supplied reference screens are faithfully implemented.
- Visual hierarchy and botanical identity remain consistent.
- Desktop, tablet, and mobile layouts work.
- No major unintended overflow or broken images.
- Reusable components and tokens are used consistently.
- Interactive states fit the visual system.

## Shopping

- Categories and navigation work.
- Product details use consistent data.
- Options and pot selections are validated.
- Bundles calculate prices and discounts correctly.
- Cart quantities and line totals update correctly.
- Subtotal and final total are accurate.
- Delivery charges are displayed transparently.
- Promotions apply only under valid rules.
- Stock and price changes are handled safely.

## Checkout

- Progress is clear.
- Guest checkout is supported.
- Required fields are validated.
- Errors preserve valid customer input.
- Payment outcomes are distinguished accurately.
- Duplicate submissions are handled safely.
- Order confirmation appears only after the required confirmation conditions are satisfied.

## Complete state coverage

- Loading, empty, success, validation, error, pending, and unavailable states are implemented where relevant.
- Recovery actions are clear.
- No important interaction leaves the customer without feedback.
- Accessible focus and status announcements are implemented.
- No fake tracking, payments, reviews, stock, or appointment confirmations.

## Privacy and access

- Role-based restrictions are enforced.
- Sensitive operations are protected.
- Marketing preferences are distinct from transactional notifications.
- Applicable privacy controls are represented honestly.
- No secrets are committed to source code.

## Engineering

- Critical pricing and promotion logic is tested.
- Important flows have appropriate automated or documented manual tests.
- No known critical console errors remain.
- The application can be set up using the README.
- Mock and live integrations are clearly distinguished.
- Remaining production work and open decisions are documented.

# 33. Open Decisions Register

Do not silently invent answers to the following:

1. Final typography, design tokens, and detailed responsive breakpoints, if not verifiable from references.
2. Exact product catalog, names, botanical facts, sizes, imagery, prices, and inventory.
3. Final plant taxonomy and category labels.
4. Bundle contents, sizes, prices, eligibility, and substitution rules.
5. Pot compatibility and availability.
6. Payment provider and live payment integration.
7. Tax and accounting configuration.
8. Delivery carriers, zones, rates, cut-off times, and collection locations.
9. Mixed-seller delivery-fee calculation.
10. Free-delivery threshold, if any.
11. Guest cart persistence and cross-device synchronization.
12. Account registration and authentication approach.
13. Promotion stacking, expiry, exclusions, and refund rules.
14. Abandoned-cart reminder timing and legally permissible channels.
15. Email and notification provider.
16. Customer-support hours and live-chat provider.
17. Returns and replacement policies.
18. Service catalog, provider coverage, and appointment capacity.
19. Subscription billing, pause, cancellation, and renewal rules.
20. Plant-replacement eligibility and limitations.
21. Business verification, invoicing, and approval rules.
22. Partner inventory synchronization.
23. Database, hosting, deployment, and monitoring choices.
24. Accessibility acceptance target and testing plan.
25. Trademark and domain availability.

Use explicit placeholders or mock data until decisions are made. Ask for clarification only when a decision is genuinely blocking or a choice could create substantial rework.

# 34. Instructions to Codex

Use this document as the initial product and UX specification for Leafora.

Before implementation:

1. Inspect the current repository.
2. Read the project-specific instructions.
3. Inspect the supplied reference images and Figma material available to you.
4. Identify the existing architecture, dependencies, and reusable assets.
5. Report what already exists, what is missing, and any significant blockers.
6. Propose an implementation sequence that respects the current codebase.

During implementation:

- Preserve the reference design.
- Build reusable components and consistent states.
- Implement real interactions, not just static screens.
- Prioritize the customer shopping journey.
- Include loading, success, empty, error, validation, unavailable, and recovery states where appropriate.
- Keep pricing, inventory, promotions, and order status logically consistent.
- Use honest demo data when live data is unavailable.
- Avoid unnecessary dependencies and major architectural changes.
- Keep localization and accessibility in mind from the beginning.
- Test the important customer journeys.
- Document open decisions and production integration requirements.
- Explain significant UX and technical decisions in clear language.

Do not claim that integrations, testing, compliance, or Figma inspection have occurred unless they actually have.

Deliver working increments, explain what was implemented, describe what was tested, and identify what remains.

# 35. Final Product Principle

Leafora should be a premium, trustworthy, genuinely useful plant-shopping experience—not a feature-heavy demonstration.

The product must make choosing plants easier, make prices and policies understandable, support customers when something goes wrong, and allow the business to grow without sacrificing usability.

**Every feature must have a purpose. Every price must be explainable. Every important interaction must provide feedback. Every failure must have a safe recovery path. Every significant design decision must have a reason the owner can confidently explain.**

This is the standard against which Leafora Version 1 should be designed, implemented, and reviewed.

---

**End of Leafora Product & UX Build Brief — Version 1.0**
