---
created: 2026-10-31
type: working-standard
status: active
tags: [design-principles, anti-ai-slop, product-design, ux, accessibility, codex]
---

# Anti-AI-Slop — Product Design Quality Checks

## Purpose

This file identifies design and implementation patterns that should not be accepted without a clear reason. Use it alongside `design-taste.md`.

**The standard is not “avoid anything popular” or “make everything unusual.” The standard is “every important decision must serve the user, product, context, or brand.”**

A familiar pattern can be excellent when it fits the task. A fashionable visual effect can be appropriate when it has a purpose. Reject unjustified choices—not techniques simply because AI often uses them.

## How to use this checklist

Apply checks during design generation, implementation, and final review. Do not mechanically ban a pattern without considering context.

### Severity levels

- **P0 — Must fix:** Blocks task completion, creates a serious accessibility or usability barrier, misrepresents the product, risks user data or money, or makes a critical flow unsafe or unreliable.
- **P1 — Should fix:** Creates significant confusion, inconsistency, friction, or visual noise that weakens the experience.
- **P2 — Refinement:** A lower-impact polish issue that still has a meaningful improvement path.

Prioritize by user impact and risk. Do not spend time polishing P2 details while P0 or P1 issues remain.

For each concern, identify the pattern, explain why it matters, propose a specific correction, and verify the correction in context.

---

## 1. Visual sameness and decoration

### P1 — Trend-first visual styling

**Pattern:** Default purple-pink gradients, glowing orbs, abstract “AI” geometry, random particles, glass cards everywhere, or fashionable effects added without a product-specific reason.

**Why it fails:** The interface looks interchangeable and decoration competes with product meaning.

**Better response:** Start with the product's users, content, brand, and desired feeling. Keep an effect only when it strengthens identity, hierarchy, comprehension, or a meaningful interaction.

**Appropriate exception:** A brand-led campaign or creative product may intentionally use expressive gradients, blur, or abstract imagery when it is coherent and usable.

### P1 — Generic hero imagery

**Pattern:** Stock-photo-style teams, generic laptop mockups, floating lightbulbs, abstract tech illustrations, or unrelated AI-generated scenes used to fill a hero.

**Why it fails:** The image could belong to almost any product and does not help the user understand the offer.

**Better response:** Prefer authentic product UI, relevant real-world context, accurate product imagery, or a purposeful illustration. Check image accuracy, licensing/provenance where relevant, crop, accessibility text, and loading performance.

**Appropriate exception:** Stock or abstract imagery can be suitable when it serves a clear editorial or brand purpose and is not pretending to depict actual customers or product capabilities.

### P1 — Repetitive card grids

**Pattern:** Every section becomes three identical cards with an icon, heading, paragraph, and button; every content item has the same visual weight.

**Why it fails:** Repetition replaces information architecture, obscures priority, and makes different content feel falsely equivalent.

**Better response:** Choose the structure based on the content and task: lists, tables, editorial layouts, comparison views, timelines, featured items, or cards where cards genuinely help.

**Appropriate exception:** Consistent grids are useful for comparable items such as products or search results. Keep the consistency when it supports scanning and comparison.

### P1 — Everything is centered or equally emphasized

**Pattern:** Long body copy is centered, all headings and buttons compete for attention, or every section has the same visual hierarchy.

**Why it fails:** Reading becomes harder and users cannot easily identify what matters.

**Better response:** Use alignment, spacing, scale, grouping, and contrast to reflect content relationships. Center alignment can be right for short hero messages or compact empty states; it is not the default for every layout.

### P2 — Unnecessary visual effects

**Pattern:** Multiple shadows, decorative borders, faux-3D buttons, arbitrary outlines, oversized radii, icons beside every heading, or decorative elements with no meaning.

**Why it fails:** The interface accumulates visual noise and loses a clear visual system.

**Better response:** Remove the effect unless it supports hierarchy, affordance, grouping, state, or brand. Use elevation and borders consistently rather than stacking them by default.

### P1 — Novelty over usability

**Pattern:** Unfamiliar navigation, hidden gestures, unusual controls, or custom interactions chosen mainly to make the product feel unique.

**Why it fails:** Users must learn a new interaction without receiving enough value in return.

**Better response:** Use established patterns when they fit. Introduce a novel pattern only when it materially improves the task, and make the behavior discoverable, accessible, and testable.

---

## 2. Hierarchy, content, and trust

### P0 — Misleading product claims or fabricated proof

**Pattern:** Invented customer quotes, testimonials, review counts, logos, awards, metrics, certifications, research findings, usability-test outcomes, or product capabilities.

**Why it fails:** It damages trust and can mislead users, clients, or decision-makers.

**Better response:** Use only supplied or verified claims. Label illustrative data and placeholders clearly. If evidence is missing, state what is unknown and what should be collected; never fill the gap with invented proof.

### P1 — Vague marketing language

**Pattern:** “Empower,” “seamlessly,” “leverage,” “robust,” “intuitive,” “revolutionary,” “delight,” or “next-generation” used instead of explaining what the product actually does.

**Why it fails:** The copy sounds generic and forces users to infer the value.

**Better response:** Describe the capability, action, outcome, constraint, or benefit in concrete language. These words are not automatically forbidden; use them only when precise and justified.

### P1 — Placeholder content presented as final

**Pattern:** Repeated lorem ipsum, generic labels, unrealistic product names, implausibly short text, or sample data that hides real layout problems.

**Why it fails:** It prevents a meaningful review of hierarchy, wrapping, density, trust, and task flow.

**Better response:** Use realistic content based on supplied requirements. Mark invented examples as illustrative. Test long names, missing fields, different prices, varied descriptions, and relevant edge cases.

### P1 — Unnecessary copy patterns

**Pattern:** Every section has exactly three bullets, every feature is described with the same sentence template, or copy repeats the heading without adding meaning.

**Why it fails:** The structure feels generated rather than shaped around the information.

**Better response:** Let the number and format of points follow the content. Remove repetition and say only what helps the user decide or act.

### P1 — Hierarchy without a clear user purpose

**Pattern:** A hero has a title, subtitle, two CTAs, signup form, social proof, badges, and multiple decorative elements all competing for attention.

**Why it fails:** Users cannot easily tell what the product offers or what to do next.

**Better response:** Identify the page's primary purpose and prioritize the elements that support it. Do not apply an arbitrary maximum number of elements; include secondary content when it serves a real need.

---

## 3. Interaction and product behavior

### P0 — Dead or misleading controls

**Pattern:** Buttons that do nothing, links to nowhere, controls that imply a capability that does not exist, or actions with no meaningful feedback.

**Why it fails:** Users lose confidence and cannot complete the task.

**Better response:** Implement the intended behavior, use a clearly disabled state when unavailable, or label the element as a non-interactive example in a prototype. Verify every visible primary action.

### P0 — Unsafe destructive or financial actions

**Pattern:** Deleting, purchasing, submitting, or changing important data without appropriate clarity, confirmation, validation, or recovery when the risk warrants it.

**Why it fails:** Users can lose money or data through mistakes or ambiguity.

**Better response:** Make the action and consequences clear, prevent accidental activation, validate inputs, provide appropriate confirmation or undo, and design recovery paths. Do not add unnecessary confirmation steps to every harmless action.

### P1 — Toasts for every event

**Pattern:** A toast for every click, keystroke, or minor state change.

**Why it fails:** Frequent transient messages interrupt work and disappear before users can act on them.

**Better response:** Use inline feedback for local changes, persistent status for important outcomes, and toasts for brief, useful notifications that do not require sustained attention. Choose the feedback pattern based on importance and context.

### P1 — Modals used as default containers

**Pattern:** Long, complex, navigable, or multi-step content placed in a small modal simply because it is easy to implement.

**Why it fails:** It constrains space, harms orientation, and can make navigation and accessibility harder.

**Better response:** Use a dedicated page or route for substantial content. Use dialogs for focused tasks that benefit from temporary interruption and preserve sensible focus management and dismissal behavior.

### P1 — Unhelpful empty states

**Pattern:** “No data yet,” a sad cloud illustration, or a blank screen without explanation or next steps.

**Why it fails:** Users do not know whether the system is working, why there is no content, or how to proceed.

**Better response:** Explain the relevant reason when known and offer a useful next action. Distinguish a genuinely empty state from loading, an error, no search results, or a permission problem.

### P0 — Infinite or ambiguous loading

**Pattern:** An indefinite spinner with no feedback, no timeout handling, or no recovery when a request fails.

**Why it fails:** Users cannot tell whether to wait, retry, or leave.

**Better response:** Show appropriate progress or status, handle delays and failures, preserve user input where possible, and provide a recovery action. Use progress percentages only when the system can support them; do not invent progress.

### P0 — Generic or blameful errors

**Pattern:** “Something went wrong,” raw technical exceptions, or messages that blame users without explaining what to do.

**Why it fails:** Users cannot recover and may lose work.

**Better response:** Explain the problem at the level that is known, tell users what they can do next, preserve their input when possible, and provide support details where useful. Do not expose secrets or sensitive technical information.

### P1 — Missing interaction states

**Pattern:** Only the ideal/default state is designed; focus, pressed, selected, disabled, loading, validation, success, error, and recovery states are ignored.

**Why it fails:** The design is incomplete when users interact with it or the system behaves unexpectedly.

**Better response:** Define the relevant states for each component and flow. Do not mechanically create every possible state when it cannot occur; cover the states that are meaningful for the product.

---

## 4. Accessibility and responsive quality

### P0 — Accessibility barriers

**Pattern:** Insufficient text contrast, color as the only status signal, missing keyboard access, invisible focus, unlabeled controls, inaccessible dialogs, or information available only through hover.

**Why it fails:** Some users cannot understand or operate the product.

**Better response:** Check semantic structure, keyboard navigation, visible focus, contrast, labels, error associations, target size, zoom/reflow, reduced motion, and assistive-technology behavior as appropriate. Verify with automated checks and manual testing; automated results alone are not proof of accessibility.

### P1 — Desktop-only design

**Pattern:** Layouts that break at narrow widths, clipped controls, horizontal overflow, tiny tap targets, or fixed dimensions that assume one viewport.

**Why it fails:** Real users and real content do not match the designer's ideal screenshot.

**Better response:** Check representative viewport sizes, long text, realistic content, keyboard and touch interaction, and relevant device constraints. Responsive design means preserving task quality, not merely shrinking the desktop layout.

### P1 — Low-quality language and content handling

**Pattern:** Hard-coded text sizes or containers that break when labels are longer, translations expand, or supported scripts render differently.

**Why it fails:** Localization and real-world content expose layout and comprehension problems.

**Better response:** Test the product's supported languages, font coverage, wrapping, date/number formats, and text expansion. Do not claim language support that has not been checked.

---

## 5. Implementation and delivery

### P0 — Visual mockup mistaken for a working product

**Pattern:** A polished screen is presented as complete when interactions are placeholders, data is static, routes are broken, or core behavior is missing.

**Why it fails:** Visual completeness creates a false impression of functional readiness.

**Better response:** State whether the output is a concept, prototype, implemented feature, or tested flow. Verify behavior separately from appearance.

### P1 — Inconsistent components and tokens

**Pattern:** Similar buttons, forms, spacing, colors, and states are independently invented on different screens.

**Why it fails:** The product feels fragmented and becomes harder to maintain.

**Better response:** Reuse shared tokens and components where the role and behavior match. Document intentional exceptions. Do not force distinct components into one abstraction merely to maximize reuse.

### P0 — Unverified claims of testing

**Pattern:** Saying the design is responsive, accessible, production-ready, or tested without actually checking it.

**Why it fails:** Stakeholders cannot distinguish verified quality from assumption.

**Better response:** Report precisely what was inspected, executed, tested, or measured. List important unverified areas and the next validation step.

### P1 — Overengineering a visual idea

**Pattern:** Heavy animation, complex effects, unnecessary dependencies, or elaborate code used for a minor visual benefit.

**Why it fails:** It increases implementation and maintenance cost, can harm performance, and makes iteration harder.

**Better response:** Prefer the simplest implementation that delivers the intended experience. Consider performance, reduced motion, maintainability, and whether the visual benefit justifies the cost.

---

## 6. Specificity test

Ask:

**What would change in this design if we knew the real user's goal, constraints, environment, and level of familiarity?**

If the answer is “almost nothing,” investigate whether the design is too generic.

Use known user and product details, not stereotypes. If important context is unknown, document assumptions or plan research rather than inventing a persona.

---

## Hasina's context-specific checks

- **Purposeful motion is not automatically slop.** I value motion when it explains a product, demonstrates how something works, or makes a transition easier to understand. Reject motion when it is decorative by default, delays an essential task, harms accessibility, or costs more than it contributes.
- **Specificity example, not a universal requirement:** for an ecommerce flow, a first-time customer might use an Android phone on a slow connection and need to understand product price, delivery costs, order summary, payment status, and order confirmation. A review should inspect those concerns only when they belong to the actual product scope.
- **Copy:** be cautious with “empower,” “seamlessly,” “leverage,” “robust,” “intuitive,” and “beautifully crafted” when they are vague or unsupported. Prefer concrete user actions, product capabilities, and verifiable outcomes. These are not forbidden when used precisely.
- **Visual taste:** do not ban glassmorphism, gradients, card grids, or any other style categorically. Ask what job it performs, whether the context supports it, and whether a simpler option would work better.

## 7. Final quality gate

Before presenting work for review, check the following:

- [ ] The design addresses a clear user problem or task.
- [ ] The hierarchy reflects what users need to understand or do.
- [ ] Visual style and imagery have a product-specific reason.
- [ ] Copy and product claims are accurate; unknowns and placeholders are labeled.
- [ ] Primary controls work or are clearly identified as prototype elements.
- [ ] Relevant loading, empty, error, success, and recovery states are covered.
- [ ] Keyboard, focus, contrast, semantics, and responsive behavior have been considered.
- [ ] Realistic content and relevant viewport sizes have been inspected.
- [ ] Components and design tokens are consistent where appropriate.
- [ ] The most serious P0/P1 issues are resolved or explicitly disclosed.
- [ ] Testing claims match the checks actually performed.
- [ ] The next validation step is clear where uncertainty remains.

## Record personal patterns over time

After reviewing real work, add a new entry only when it captures a useful lesson. Record:
1. The concrete pattern observed.
2. The context and user impact.
3. Why the pattern was inappropriate in that case.
4. The correction.
5. Any exception where the pattern could be appropriate.
6. How the correction was or could be verified.

Do not add rules merely because a style is trending or because a generated output used it. The purpose is to improve judgment, not to create a longer list of prohibitions.

**Final rule:** specificity beats generic polish, but user outcomes beat novelty. Make the experience useful, truthful, accessible, coherent, and appropriate before optimizing for visual impressiveness.
