# Styra — Heuristic Evaluation: Screen 01 (Start)

**Repository review — 18 October 2026:** This is a historical evaluation. The original screen and prototype are not in the repository, so the visual findings, behavior, and implementation status have not been independently verified here. Numeric severity labels in this report are separate from the High/Medium/Low labels in the other critiques; do not equate them without an agreed scale. See the [project evidence notes](README.md#evidence-and-next-work).

**Project:** Styra — AI Shopping Assistant  
**Screen:** 01 — Start  
**Evaluation type:** Usability heuristic evaluation  
**Reference brief:** `projects/styra/brief-v1-client.md`  
**Evaluation scope:** Original Start screen only  
**Method:** Nielsen’s 10 Usability Heuristics, with relevant accessibility and human–AI interaction considerations

---

## 1. Screen Purpose

The Start screen introduces users to Styra and provides the entry point for an AI-assisted shopping experience.

Its primary purpose is to help users express what they want to buy, provide optional preferences, and understand how to begin a shopping request without feeling pressured to complete a long form.

The evaluation focuses on whether the screen communicates its purpose clearly, supports the primary action, and gives users enough control and guidance to start confidently.

## 2. Heuristic Evaluation Criteria

The screen is evaluated against the following criteria:

1. **Visibility of system status:** Can users understand the current state of their input and what happens when they interact with the screen?
2. **Match with the real world:** Does the interface use familiar, shopper-friendly language?
3. **User control and freedom:** Can users change their approach or choose another way to search?
4. **Consistency and standards:** Are similar controls visually and functionally distinguishable?
5. **Error prevention:** Does the interface help users avoid unclear or unintended actions?
6. **Recognition rather than recall:** Are options and instructions visible when users need them?
7. **Flexibility and efficiency:** Can both exploratory shoppers and users who already know what they want get started efficiently?
8. **Aesthetic and minimalist design:** Does the visual hierarchy prioritise the main task?
9. **Error recognition and recovery:** Is there a clear path if the initial input is incomplete or the search cannot proceed?
10. **Help and documentation:** Does the screen explain what Styra does and how users can begin?

Only findings supported by the original screen should be treated as confirmed. Behaviour that cannot be determined from a static image requires prototype or implementation testing.

## 3. Findings

### S01-H1 — The primary interaction has unclear outcomes

**Heuristic:** H1 — Visibility of system status  
**Severity:** 2 — Minor  
**Evidence:** The example prompts appear selectable, but the screen does not make it clear whether selecting one immediately starts a search or fills the input field. The detail chips also lack an obvious selected state, and there is no visible summary of selected details.

**User impact:** Users may be uncertain about what an interaction will do or which preferences Styra has received.

**Recommendation:** Make the outcome of selecting an example clear and provide visible feedback for selected preferences.

**Validation needed:** Confirm the actual tap behaviour and selection states in a prototype.

---

### S01-H2 — The language does not fully explain the shopping experience

**Heuristic:** H2 — Match between the system and the real world  
**Severity:** 2 — Minor  
**Evidence:** The screen provides examples and optional detail chips, but it does not clearly explain what Styra will do with the information or what kinds of shopping sources it can explore.

**User impact:** First-time users may not understand the difference between Styra and a conventional search interface.

**Recommendation:** Explain the shopping assistance in concise, familiar language, setting realistic expectations about what Styra can search and compare.

---

### S01-H3 — The traditional-search shortcut is easy to overlook

**Heuristic:** H7 — Flexibility and efficiency of use  
**Severity:** 2 — Minor  
**Evidence:** The “Prefer filters? Use classic search” link is small and positioned close to the composer divider. The magnifier icon near the wordmark may also have an unclear purpose.

**User impact:** Users who already know what they want may struggle to discover the faster, more familiar search path.

**Recommendation:** Make the alternative search route easy to recognise and give the magnifier a clear, consistent purpose.

**Product consideration:** AI-assisted conversation should remain the primary experience, while traditional search remains available as an optional path.

---

### S01-H4 — Supporting options compete with the primary action

**Heuristic:** H8 — Aesthetic and minimalist design  
**Severity:** 2 — Minor  
**Evidence:** Three example cards, multiple preference chips, and the classic-search link appear before the input field at the bottom of the screen.

**User impact:** The number of competing elements may make it harder for users to identify the simplest way to begin.

**Recommendation:** Establish a clearer hierarchy between the main input action and supporting suggestions.

**Product consideration:** Preserve the low-pressure approach. Optional details should help users express their needs without making the screen feel like a questionnaire.

---

### S01-H5 — The screen provides limited explanation of Styra

**Heuristic:** H10 — Help and documentation  
**Severity:** 2 — Minor  
**Evidence:** The screen includes the Styra wordmark and shopping prompts but does not clearly explain the product’s role, capabilities, or the purpose of the optional detail chips.

**User impact:** New users may need to infer how the service works before deciding whether to use it.

**Recommendation:** Provide a brief, task-focused explanation of how Styra helps users discover and compare suitable products.

---

### S01-H6 — Icon-only controls need accessibility verification

**Heuristic:** Accessibility — supplementary WCAG 2.x review  
**Severity:** 2 — Requires verification  
**Evidence:** The magnifier and send arrow are presented as icons without visible text labels. A screenshot cannot establish whether these controls have accessible names, adequate focus indicators, or a logical keyboard and screen-reader order.

**User impact:** Users relying on assistive technologies may not receive sufficient information about these controls if accessible names or focus behaviour are missing.

**Recommendation:** Verify accessible names, keyboard focus, focus order, and touch-target usability in the prototype or implementation.

**Status:** Unverifiable from the static screen.

## 4. Positive Observations

- **Low-pressure entry:** “Everything here is optional” helps reduce the feeling of completing a mandatory form.
- **Example prompts:** Suggestions give users a starting point when they are unsure how to describe their needs.
- **Alternative route:** The classic-search link provides an option for users who prefer filters.
- **Contrast:** The supplied evaluation reports that the main text and brand colours pass WCAG AA contrast checks. This should be confirmed against the actual rendered interface.

## 5. Priority Summary

| ID | Issue | Severity |
|---|---|---:|
| S01-H1 | Unclear interaction outcomes | 2 |
| S01-H2 | Limited explanation of the shopping experience | 2 |
| S01-H3 | Traditional search is easy to overlook | 2 |
| S01-H4 | Supporting elements compete with the main action | 2 |
| S01-H5 | Limited product explanation | 2 |
| S01-H6 | Icon accessibility requires verification | 2 |

**Recommended focus:** First clarify the primary interaction and the purpose of Styra. Then improve the hierarchy of the main action and the discoverability of traditional search. Verify accessibility separately in a working prototype.

## 6. Limitations

This evaluation covers only the original Start screen. It is based on visual inspection, not observed user behaviour or usability testing. Tap outcomes, selected states, keyboard navigation, screen-reader behaviour, and error recovery cannot be confirmed from the screenshot alone.

No design changes have been implemented as part of this evaluation.

