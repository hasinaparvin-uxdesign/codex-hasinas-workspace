# Styra — Persona Acid Test
Consolidated critique notes · 6 mobile screens · 17 October 2026 · Prepared for Hasib

**Repository review — 18 October 2026:** This historical report describes a recreated HTML copy; that HTML, the source design, and the screen images are not present here. Its FIX/ACCEPT/PUSH BACK decisions and claims of applied fixes are preserved, not newly approved or verified. References to unavailable repository access describe the original review, not the current connection. Only the contrast arithmetic correction below has been independently recalculated. See the [project evidence and decision notes](README.md#evidence-and-next-work).

## Review status

Verdict: Partly complete. The six supplied screens were reviewed: 17 findings logged, 12 FIX applied and shown before/after, 3 ACCEPT, and 2 PUSH BACK. The review is not fully complete because the personal GitHub repository could not be checked, and the review used static PNGs; screen-reader behaviour, text zoom, and real voice states remain unverified. Fixes were applied to a recreated HTML copy of the screens, not to the source design file.
## 1. Personas used

These are working personas defined for this test. They are assumptions, not research data about Styra’s real users. Replace them with validated research personas when available.

| ID | Persona | Profile | Design stress | S1 | S2 | S3 | S4 | S5 | S6 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P1 | Marta, 67 | Low vision; large text / zoom; reads slowly and carefully | Legibility, hidden controls, copy that can be taken literally | ✓ | ✓ | ✓ | ✓ | ✓ | ~ |
| P2 | Rui, 34 | Motor impairment; voice-first, large targets | Voice feedback, tap targets, forgiving flows | ✓ | ✓ | ✓ | ~ | ✓ | ✓ |
| P3 | Ana, 29 | Deal-hunter, sceptical of AI claims | Truthful copy, verifiable facts, price clarity | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| P4 | João, 52 | Low digital confidence; unsure about chat UIs | Escape hatches, plain labels, one obvious next step | ✓ | ✓ | ✓ | ~ | ✓ | ✓ |
| P5 | Sofia, 38 | Time-poor, one-handed on the commute | Thumb reach, scan speed, no re-reading | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |


Legend: ✓ = no open issue after fixes · ~ = passes on paper, but residual risk needs a real test.
## 2. Findings and decisions

| ID | Screen | Finding | Personas | Severity | Decision | Reasoning and evidence / resolution |
| --- | --- | --- | --- | --- | --- | --- |
| F01 | Start | “Prefer filters? Use classic search” is the only escape hatch from chat and is cut off by the fixed input bar; there is no bottom padding under the scroll content. | P1, P4 | High | FIX | Hidden fallback control leaves users who distrust chat with no visible way out. Added bottom spacing so the link sits fully above the bar. |
| F02 | Start | Example 1 promises “elegant black dress”, but the next screen echoes “elegant dress”, the understood chips drop “Black”, and the shortlist returns a navy dress. | P3, P4 | High | FIX | Trust break at the first interaction. The consistent fix was to make the example match the brief used through the flow. Example 1 now reads “elegant dress”; screens 1, 2, and 6 use the same brief. |
| F03 | Shortlist | Satin dress is justified as “Lowest price that suits the occasion”, yet the sheath dress is €34 versus €39. | P3 | High | FIX | Factually false rationale. Scoped the claim to what is true: copy now says “Lowest-priced new option.” |
| F04 | Shortlist | Cards say “Retailer A/B/C” in square brackets and the compare footer says “Visit A/B/C”; nothing ties letters to products, and brackets look unfinished. | P1, P4, P5 | Medium | FIX | The letter mapping is a usability gap even with real store names. Added A/B/C badges to shortlist cards and compare headers; footer buttons now match. |
| F04b | Shortlist | Square-bracket retailer placeholders. | — | Low | ACCEPT | These are design-file placeholders that bind to real retailer names at build time. No UI change needed; after images show the bound state without brackets. |
| F05 | Compare | Price row uses dark bars of different heights with top-aligned text, resembling a chart without a scale and offering no cue for the cheapest option. | P1, P3 | Medium | FIX | Price is the key comparison and should be scannable. Changed to uniform tinted cells of equal height and added “Lowest price” under €34. |
| F06 | Compare | Compare headers have unequal widths and image sizes, so columns do not line up with the grid below. | P1, P5 | Medium | FIX | Unequal columns bias attention and break comparison. Changed to three equal columns and equal image heights. |
| F07 | Shortlist | Vocabulary drifts between “Delivery unverified” / “Not confirmed”, “Second-hand” / “Used, seller-described”, and “Few reviews” / “Few”. | P3, P4 | Medium | FIX | Same facts had multiple labels. Standardised terminology to “Unverified” and “Second-hand, seller-described.” |
| F08 | Compare | “Fit for your brief” shows Strong / Good / Good without an explanation. | P3 | Medium | FIX | An unexplained rating is difficult to trust. Added a one-line reason under each rating. |
| F09 | Compare | The dashed-chip legend appears only after the Compare table and never on Shortlist, where dashed chips first appear. | P1, P4 | Medium | FIX | Users should see a legend before first encountering a symbol. Moved the legend above content on both screens. |
| F10 | Adaptive question | The size question is separated from answers by a large gap; “Where I’ll look” chips look tappable but are not; the helper line sits in the wrong card. | P2, P4, P5 | Medium | FIX | Keep question and answers together within thumb reach and avoid making informational chips look interactive. Moved size chips under the question; changed “Where I’ll look” to a sentence with a Change link; moved helper text beside the chips. |
| F11 | No match, refine | “Keep searching as it is” is ambiguous after a failed search and has the same visual weight as constructive options. | P1, P4 | Medium | FIX | Sounds like a loop. Renamed it “Keep my brief unchanged” and made it visually secondary. |
| F12 | Voice input | Voice screen has no live transcript or elapsed time; “Try saying” is small, grey, and far from the waveform. | P2, P4 | Medium | FIX | Voice-first users need confirmation that speech is being captured. Added a live “I’m hearing” transcript and elapsed time, and moved the hint beside the waveform. |
| F13 | No match, refine | “Raise my budget to €60” uses a fixed number. | P3 | Low | ACCEPT | Reasonable as a design placeholder; the real number should come from the cheapest matching silk result. Track as a data-spec item; no UI change. |
| F14 | Shortlist | “Compare these 3” has no per-item selection. | P5 | Low | PUSH BACK | With exactly three options, selection adds a step without benefit. Revisit if shortlists grow beyond three. |
| F15 | Start | Header search icon is unexplained in a chat-first product. | P4 | Low | ACCEPT | Cannot determine from a static image what it opens. Open question for the owner; no change made. |
| F16 | Start | Mic button has a near-black outline while other secondary controls are blue. | P2 | Low | PUSH BACK | The distinct outline improves differentiation and contrast for P1/P2. Keep it. |


## 3. Reported checks and contrast correction

- Text contrast for the exact stated color pairs: #4B6275 on #FFFFFF = 6.36:1; #025D8F on #E3EFF6 = 6.05:1. The original report gave 7.27:1 for the blue pair; this was corrected on 18 October 2026 using the [WCAG contrast formula](https://www.w3.org/TR/WCAG22/#dfn-contrast-ratio). Both exact pairs exceed the 4.5:1 AA threshold for normal text. This recalculates the stated hex values only; the original PNG pixel samples, any other colors in the “family,” and the rendered interface remain unverified.
- Touch targets: Chips, size buttons, option buttons, and footer CTAs are approximately 44–52 px high at 390 px width.
- Honest empty state: Screen 5 does not pad results with weak matches and keeps the €50 budget unless the user changes it.
## 4. Before and after

The “Before” version is a recreation of the supplied PNGs in HTML using Poppins and the same palette, so both versions share one rendering pipeline. It is close, not pixel-identical. The Compare “After” screen is taller (900 px) because it adds a legend and reasons.
| Screen | Name | Fixes shown |
| --- | --- | --- |
| Screen 1 | Start | F01, F02 |
| Screen 2 | Adaptive question | F10 |
| Screen 3 | Shortlist | F03, F04, F07, F09 |
| Screen 4 | Compare | F05, F06, F08, F09 |
| Screen 5 | No match, refine | F11 |
| Screen 6 | Voice input | F12 |


The original, recreated-before, and fixed-after screen images are embedded in the source HTML. They are not automatically embedded in this Markdown conversion; add exported image assets to the repository if you want them displayed on GitHub.

## 5. Not verified

- Screen-reader labels, focus order, and landmarks (PNG-only review; no markup supplied).
- Text zoom at 200% and operating-system large-text behaviour.
- Real voice states: permission prompt, denied permission, no speech detected, and errors.
- Loading, error, and slow-network states for search.
- Whether the dashed style is distinguishable without colour at small sizes (visual check only).
- Files in the personal GitHub repository (repository access was not available during this review).
## Source and scope

Source: six supplied Styra mobile-screen PNGs referenced by the original HTML report. Contrast values were computed from sampled pixels. This is a static-screen critique, not validated user research or a complete accessibility audit.
