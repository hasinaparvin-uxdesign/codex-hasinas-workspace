# Styra — Phase 1: Start Screen Critique

## 1. Purpose

This document records the first critique phase of Styra, an AI-powered shopping assistant.

The goal is to evaluate the original, pre-improvement Start screen before making any design changes. The review focuses on how clearly the screen communicates Styra’s value, how easily users can begin shopping, and whether the visual hierarchy supports a low-friction experience.

**Scope:** Start screen only  
**Source:** Original, pre-improvement screen and `projects/styra/brief-v1-client.md`  
**Review method:** Visual inspection using the `/design-review` skill  
**Implementation status:** No changes implemented yet

## 2. What Works

### 2.1 Low-pressure entry point

The screen communicates that users can start with a simple request and that additional details are optional. This supports Styra’s goal of making shopping feel effortless rather than like completing a questionnaire.

### 2.2 Helpful example prompts

The example prompts give users a starting point when they are unsure what to ask. They help demonstrate how a shopper can describe a product, occasion, or budget in natural language.

### 2.3 Clear initial direction

The screen establishes the basic action: describe what you are looking for. This provides a simple entry into the shopping experience without requiring users to provide every detail upfront.

## 3. Key Findings

### Finding 1.1 — The primary input lacks visual dominance

**Severity:** High  
**Area:** Visual hierarchy, Interaction

**Observation:**  
The main input field is visually less prominent than the surrounding example cards, detail chips, and links. Users may need to scan several elements before recognising where to begin.

**Recommendation:**  
Make the primary input the clearest starting point. Example prompts and optional details should support the main action rather than compete with it.

**Decision:** Pending

### Finding 1.2 — Interactive elements look too similar

**Severity:** Medium  
**Area:** Interaction, Clarity

**Observation:**  
Example prompts, detail chips, and the send action use similar outlined or rounded styles. The screen does not clearly communicate whether selecting an example submits it immediately or places it in the input field for editing.

**Recommendation:**  
Differentiate these elements visually and clarify their expected behaviour.

**Decision:** Pending

### Finding 1.3 — Optional details may feel like a required form

**Severity:** Medium  
**Area:** Interaction, Clarity

**Observation:**  
The detail chips resemble a filter bar, and their dropdown indicators suggest that users are expected to configure several options. This may conflict with the message that everything is optional.

**Recommendation:**  
Present these controls as optional assistance rather than required steps. Reconsider whether dropdown indicators are appropriate for a conversational experience.

**Decision:** Pending

### Finding 1.4 — Selected details lack visible feedback

**Severity:** Medium  
**Area:** Interaction

**Observation:**  
The screen does not clearly show how selected details would persist or combine with the user's typed request.

**Recommendation:**  
Provide a visible selected state and make it clear how additional details contribute to the final request.

**Decision:** Pending

### Finding 1.5 — Styra’s distinctive AI shopping value is unclear

**Severity:** High  
**Area:** Product identity, AI value

**Observation:**  
The headline “What are you looking for?” and the Styra wordmark could belong to almost any search product or AI assistant. The screen does not clearly communicate that Styra researches shopping options and helps users compare products and make more confident decisions.

**Recommendation:**  
Communicate Styra’s specific shopping value through the headline, supporting copy, or visual identity without adding unnecessary steps.

**Decision:** Pending

### Finding 1.6 — Product coverage and scope are unclear

**Severity:** Medium  
**Area:** Clarity

**Observation:**  
All three examples relate to clothing. The screen does not establish whether Styra supports other product categories or whether it can explore different types of sellers, including second-hand options.

**Recommendation:**  
Set realistic expectations about Styra’s product coverage and shopping sources.

**Decision:** Pending

### Finding 1.7 — Traditional search has competing entry points

**Severity:** Medium  
**Area:** Clarity, Interaction

**Observation:**  
The magnifying-glass icon and the “Prefer filters? Use classic search” link both appear to provide access to traditional search. The icon’s purpose is ambiguous, and the link has limited visual separation from the composer area.

**Recommendation:**  
Give each entry point a clear purpose, remove ambiguity, and ensure the link has sufficient spacing.

**Decision:** Pending

### Finding 1.8 — Detail-chip labels and layout are inconsistent

**Severity:** Low  
**Area:** Clarity, Visual hierarchy

**Observation:**  
Most chips use category labels such as “Occasion” and “Budget”, while “Second-hand OK?” uses a question. The wrapping also creates an uneven layout.

**Recommendation:**  
Use a consistent labelling pattern and improve the chip layout.

**Decision:** Pending

### Finding 1.9 — The placeholder explains input mechanics, not what to write

**Severity:** Low  
**Area:** Interaction

**Observation:**  
“Type or tap the mic to speak” explains how to enter information but does not help users understand what kind of request they can make.

**Recommendation:**  
Use the placeholder to encourage a useful shopping request, while keeping the instruction concise.

**Decision:** Pending

### Finding 1.10 — Icon-only controls and border styles need review

**Severity:** Low  
**Area:** Visual hierarchy, Accessibility

**Observation:**  
The microphone button has a heavier border than the adjacent input, which may make it appear to be in a different state. The search, microphone, and send controls have no visible text labels; their accessible names cannot be confirmed from a static screenshot.

**Recommendation:**  
Align the control styling and verify that all icon-only controls have appropriate accessible names.

**Decision:** Pending

## 4. Main Themes

The findings point to three priorities for the Start screen:

1. **Communicate Styra’s value:** Explain how the product helps users find and compare relevant shopping options.
2. **Strengthen the starting point:** Make the primary input obvious and ensure optional controls do not feel like a mandatory questionnaire.
3. **Clarify interaction:** Help users understand what is selectable, what each control does, and how their choices affect the request.

These priorities should guide the next decision-making step, but they do not automatically mean every finding needs to be implemented.

## 5. Decision Log

Each finding will be reviewed individually and assigned one of the following decisions:

- **FIX** — The finding identifies a meaningful problem that should be addressed.
- **ACCEPT** — The current design is reasonable, and no change is needed.
- **PUSH BACK** — The recommendation should be challenged because it conflicts with the product goals, scope, or intended experience.

| Finding | Severity | Decision | Rationale |
|---|---|---|---|
| 1.1 — Input hierarchy | High | Pending | To be decided |
| 1.2 — Similar interactive styles | Medium | Pending | To be decided |
| 1.3 — Optional details feel mandatory | Medium | Pending | To be decided |
| 1.4 — Selected-detail feedback | Medium | Pending | To be decided |
| 1.5 — Unclear Styra value | High | Pending | To be decided |
| 1.6 — Unclear product coverage | Medium | Pending | To be decided |
| 1.7 — Competing search entry points | Medium | Pending | To be decided |
| 1.8 — Inconsistent chip labels and layout | Low | Pending | To be decided |
| 1.9 — Placeholder guidance | Low | Pending | To be decided |
| 1.10 — Icon controls and borders | Low | Pending | To be decided |

## 6. Next Step

Review the findings against the original product brief and the intended Styra experience. Decide which findings deserve action, document the rationale for each decision, and implement only the items marked **FIX**.

Preserve the original screen as the **BEFORE** version. After implementing the agreed changes, capture the updated screen as the **AFTER** version.

This phase covers only the Start screen. The remaining screens and cross-cutting findings will be reviewed in subsequent phases.
