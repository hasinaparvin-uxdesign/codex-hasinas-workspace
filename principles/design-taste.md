---
created: 2026-10-31
type: working-standard
status: active
tags: [design-principles, design-taste, product-design, ux, accessibility, codex]
---

# Design Taste — Hasina's Working Standard

## Purpose

This file defines the design quality I aim to create across digital products. Use it when framing a design direction, creating or implementing an interface, and reviewing a result.

My goal is not to make every product look the same. It is to make each experience clear, useful, distinctive, accessible, and appropriate to its users and context.

**Guiding principle: solve the problem before designing the screen.**

These principles are working standards, not universal laws. Apply judgment, explain meaningful trade-offs, and refine the standards as real project evidence accumulates.

## How to use this file

Before design work, read the project brief and identify the user, task, context, constraints, and intended outcome. Then use this file to guide decisions. Use `anti-ai-slop.md` as the companion quality-control checklist.

Do not assume that a visual preference is evidence. Separate:
- **Verified facts:** supported by supplied research, analytics, requirements, or direct inspection.
- **Observations:** what can be seen in the product, interface, or provided material.
- **Hypotheses:** reasonable explanations or predictions that still need validation.
- **Unknowns:** information not yet available.

Never invent user research, product requirements, metrics, or validation results to justify a design.

## 1. Decision hierarchy

When goals conflict, use this hierarchy to structure the decision. It is a guide for reasoning, not permission to ignore context.

1. **User needs and task success:** Can the intended user understand what is happening and make progress on their real task?
2. **Accessibility and inclusive usability:** Can people with different abilities, devices, input methods, language needs, and levels of familiarity use the experience?
3. **Product goals and constraints:** Does the design support the actual product objective, business requirements, technical feasibility, and delivery constraints?
4. **Clarity and consistency:** Are content, hierarchy, terminology, patterns, and interaction behavior coherent?
5. **Visual craft and product identity:** Does the experience feel intentional, distinctive, polished, and appropriate for its audience?
6. **Decorative enhancement:** Does an extra visual effect or animation add meaning or improve the experience enough to justify its cost?

If a decision requires a trade-off, state what is being prioritized, what is being sacrificed, and how the decision could be validated.

## 2. Context before components

Do not choose a layout or visual style before understanding the situation.

Identify, where known:
- Primary users, their goals, needs, motivations, and barriers.
- The specific task and its importance or risk.
- Where, when, and on which devices the experience will be used.
- User familiarity, language, accessibility needs, and likely connectivity constraints.
- Product category, brand character, market expectations, and content.
- Business goals, technical constraints, existing design systems, and success measures.

Do not invent missing context. Ask a focused question when an unknown materially changes the solution; otherwise state a reasonable assumption and make it easy to revisit.

## 3. Hierarchy before decoration

Every screen or section should make its purpose legible. Identify the main task, decision, or message, then give it the right visual priority.

- Use size, position, spacing, contrast, grouping, and typography to show relationships.
- Make the primary action clear without making every secondary action compete with it.
- Match hierarchy to task importance, not to a desire to make every element look equally impressive.
- Use content structure to guide scanning and reading.
- Do not force a single primary CTA onto screens where users genuinely need to compare, explore, or choose among several equally important options.

**Review question:** Can a user quickly tell what this screen is for, what matters most, and what they can do next?

## 4. Specificity before generic polish

Design for the actual product, audience, task, and environment. A polished interface that could be reused unchanged for almost any product is not sufficiently considered.

- Use real product capabilities, meaningful content, relevant imagery, and accurate terminology when available.
- Make the visual direction express the product's character rather than defaulting to a fashionable AI aesthetic.
- Use examples and imagery that fit the audience and use case.
- Keep familiar interaction patterns when they help users. Distinctiveness does not require novelty everywhere.

**Review question:** What would change in this design because we understand this particular user and task?

## 5. Restraint with intention

Remove anything that competes with the task or adds complexity without enough value. Do not confuse restraint with blandness or minimalism.

- Avoid decoration that has no communicative, navigational, brand, or interaction purpose.
- Use shadows, gradients, borders, blur, icons, and illustration selectively.
- Prefer a clear, meaningful composition over a crowded collection of effects.
- Keep useful detail when it supports comparison, comprehension, trust, or decision-making.
- Do not remove information merely to achieve a minimalist appearance.

**Review question:** What can be removed without losing meaning, usability, identity, or trust? What must stay, even if it adds visual complexity?

## 6. Typography and content hierarchy

Typography must support reading, scanning, accessibility, and the product's character.

- Establish a deliberate type scale and clear roles for headings, body text, labels, metadata, and actions.
- Use a small, purposeful set of typefaces and weights as a starting point; use more only when the content or brand genuinely benefits.
- Check actual font rendering, language coverage, line length, line height, wrapping, and truncation.
- Do not use tiny or low-contrast text just to fit more content into a layout.
- Use real, specific interface copy. Prefer concrete descriptions of capabilities and actions over vague claims.
- Ensure typography remains legible across responsive sizes and supported languages.

There is no mandatory universal font count or type scale. Choose values that suit the product and verify them in context.

## 7. Color, contrast, and semantic tokens

Color should communicate hierarchy, state, meaning, and brand—not merely fill empty space.

- Define semantic tokens such as `surface.default`, `text.primary`, `text.secondary`, `border.default`, `action.primary`, `state.success`, and `state.danger`.
- Use consistent tokens across related screens and components.
- Check contrast and do not rely on color alone to communicate status or meaning.
- Use accent colors deliberately; preserve enough visual quiet for important actions and content.
- Choose palettes based on the brand, audience, product context, and accessibility—not on trend alone.
- Check light/dark surfaces, disabled states, focus indicators, and real content combinations where applicable.

A 60/30/10 palette or a particular color family can be a useful starting point, not a universal rule.

## 8. Layout, spacing, and responsive behavior

Layout should reflect the content and task, not a template that is applied indiscriminately.

- Use a coherent spacing scale and alignment system.
- Use grids when they improve scanning, comparison, and consistency; change composition when content or hierarchy calls for it.
- Preserve clear reading order and appropriate content density.
- Test narrow and wide viewports, long labels, empty and populated content, and realistic text.
- Avoid horizontal overflow, clipped controls, awkward wrapping, and layouts that work only with ideal placeholder content.
- Do not force desktop patterns onto mobile or assume mobile users always have less complex needs.

## 9. Interaction and state quality

A screen is only one part of an experience. Design and implement the behavior around it.

Consider the states relevant to each flow:
- Default, hover, focus, pressed, selected, and disabled.
- Loading, success, empty, error, offline, and recovery.
- Validation, confirmation, undo, and destructive-action safeguards where appropriate.
- Keyboard navigation, touch targets, visible focus, and assistive-technology semantics.
- Clear feedback after meaningful user actions.

Use notifications, modals, inline messages, and navigation according to the task. No component type is automatically wrong; its appropriateness depends on urgency, complexity, context, and user control.

## 10. Motion with purpose

Motion should communicate state changes, cause and effect, spatial relationships, or meaningful feedback. It should not obstruct the task.

- Keep feedback responsive and transitions appropriate to the interaction.
- Consider reduced-motion preferences, device performance, battery, and connectivity.
- Avoid animation that delays critical actions or makes content harder to read.
- Use longer motion only when it helps comprehension or supports a meaningful experience.
- Verify motion in the actual interface rather than assuming a duration is universally correct.

Treat specific durations such as 150ms as starting heuristics, not laws. Purpose, perceived responsiveness, accessibility, and real-device performance matter more than one number.

## 11. Consistency without rigidity

Use established product patterns and design tokens to reduce avoidable cognitive load.

- Reuse components when the role and behavior are genuinely the same.
- Keep terminology, spacing, states, and interaction behavior coherent.
- Create a new pattern when there is a clear user or product reason.
- Avoid both extremes: inconsistency without reason and uniformity that erases meaningful differences.

## 12. Design rationale and trade-offs

For consequential decisions, document:

- **Decision:** What are we choosing?
- **Reason:** Which user need, evidence, requirement, or principle supports it?
- **Trade-off:** What are we giving up or making harder?
- **Validation:** What observation, usability test, metric, or review could tell us whether it works?

Consider alternatives when the decision is high-impact or uncertain. Do not create long explanations for trivial choices. The goal is traceable reasoning, not paperwork.

## 13. Critique and refinement

Before presenting work as finished:

1. Compare the result with the brief and intended user task.
2. Review hierarchy, content, interaction, accessibility, responsive behavior, and visual consistency.
3. Identify the three most consequential weaknesses.
4. Fix issues by user impact and severity—not by personal preference alone.
5. Inspect realistic content and relevant states, not just the ideal first screen.
6. State what was actually tested and what remains unverified.

A first plausible output is a starting point, not proof of quality.

## 14. When to break a principle

Break a principle consciously when the project context or evidence supports it.

A defensible exception states:
- Which principle is being overridden.
- Why the context warrants the exception.
- What benefit is expected.
- What cost or risk is accepted.
- How the result will be checked.

For example, a visually expressive animation may be justified in a brand moment but inappropriate in a repeated, time-sensitive checkout action. The context determines the decision.

## 15. How this standard evolves

This file is a living working standard, not a claim that every preference has already been validated.

After meaningful project work, record:
- The design decision and its context.
- The evidence or hypothesis behind it.
- The alternative considered.
- The result of implementation or testing.
- What should be kept, changed, or tested next time.

Distinguish personal preference from a principle supported by repeated evidence. Update this file when real work teaches a better rule.

## Hasina's current visual preferences

These preferences are starting points to guide exploration, not rigid requirements for every product.

- **Overall direction:** balanced premium—considered, clear, mature, and visually distinctive without unnecessary decoration.
- **Typography:** begin with two or three purposeful typefaces at most, using a clear scale and deliberate roles. Add another only when the product has a defensible need. Verify script and language coverage.
- **Color:** use a dominant, supporting, and accent relationship as a starting point (a 60/30/10 split can help), then adjust to the actual content, brand, and accessibility needs.
- **Composition:** use grids, spacing, hierarchy, and contrast to create order. Do not force every screen into the same grid if the content calls for another structure.
- **Visual exploration:** restrained navy-and-white or monochrome directions can be useful references, but must not become a default palette for every product.
- **Motion:** routine interface transitions typically begin around 150–200ms; longer, expressive motion is appropriate when it tells a product-relevant story or improves understanding. Respect reduced-motion preferences and verify performance.
- **Learning references:** I admire Sohanul Habib's Figma-based UX work and Shadman Rahman's AI-assisted design expertise. Learn from the craft and reasoning, but do not copy their style blindly; build judgment that fits each project's users and identity.

When a preference conflicts with user needs, accessibility, evidence, or product requirements, explain the conflict and prioritize the experience over personal taste.

## Quick design review

Before sign-off, ask:

- Is the user problem clear, and does this design address it?
- Is the main task or decision easy to understand?
- Is the interface specific to its product and audience?
- Is every major visual choice intentional?
- Are typography, color, spacing, and components coherent?
- Are accessibility and responsive behavior considered?
- Are important interaction and system states covered?
- Does motion improve rather than interrupt the experience?
- Are claims, content, and product capabilities accurate?
- What is the biggest remaining weakness, and what evidence would help resolve it?

**Quality standard:** useful before beautiful, clear without being generic, distinctive without being decorative, and polished without sacrificing accessibility or task success.
