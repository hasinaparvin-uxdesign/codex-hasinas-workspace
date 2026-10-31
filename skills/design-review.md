# Review the design

## 1. Establish the evidence

Locate the actual artifact and version, project brief, context, approved decisions, relevant user evidence, and owner principles before asking for files already available. Read `principles/design-taste.md` and `principles/anti-ai-slop.md` and apply them as judgment aids, not mechanical style bans.

If the artifact or source version is absent, state what cannot be inspected. Separate documented facts, direct observations, hypotheses, assumptions, and unknowns. A screenshot cannot prove runtime behavior, keyboard or screen-reader support, or real-user outcomes.

## 2. Review the experience, not only the screenshot

Assess the dimensions that apply to the artifact and task:

- User problem, task success, and fit with the brief.
- Information architecture, content clarity, hierarchy, and primary/secondary actions.
- Visual specificity, brand fit, typography, color, spacing, and component consistency.
- Interaction behavior and relevant default, focus, selected, disabled, loading, empty, success, error, and recovery states.
- Accessibility, keyboard operation, focus visibility, contrast, semantics, reduced motion, and touch use as applicable.
- Responsive layouts, realistic content, long labels, and relevant device/performance constraints.
- Implementation completeness, maintainability, and truthful product claims.

Do not mark irrelevant states as missing when the product cannot produce them. Do not treat any visual style as wrong solely because it is common. Judge whether it serves the actual user and product.

## 3. Rate findings by impact

Use these severity levels consistently:

- **P0 — Must fix:** blocks core task completion, creates a serious accessibility or usability barrier, misleads users about material capabilities or outcomes, risks money/data, or breaks a critical flow.
- **P1 — Should fix:** causes significant confusion, friction, inconsistency, or unnecessary visual noise.
- **P2 — Refinement:** lower-impact craft improvement.

For each finding, record:
1. Severity and dimension.
2. Exact element, state, and artifact/version inspected.
3. Evidence or observed behavior.
4. User impact and why it matters.
5. Specific recommended correction.
6. Verification needed and whether it has actually been completed.

Use Pass, Needs work, Fail, or Not verified for each reviewed dimension. Do not turn an assumption into a finding. Compute contrast only from known color values and distinguish the calculation from rendered evidence. Verify applicable standard thresholds rather than treating one font size or target size as universal.

## 4. Separate recommendations from decisions and implementation

Keep findings and recommendations separate from owner decisions and implemented changes. Explain important trade-offs. The owner retains final authority over design direction and consequential product decisions.

Prioritize meaningful P0/P1 issues before P2 polish. If a correction is implemented, inspect the changed artifact and relevant behavior again. Do not imply that a recommendation has been implemented just because it appears in review notes.

## 5. Close with a truthful review summary

Record:
- Artifact and version reviewed.
- Review scope and evidence inspected.
- Highest-priority findings and recommended fixes.
- Checks performed and their results.
- What remains Not verified.
- Owner decisions needed, if any.
- The next validation step where uncertainty remains.

Never claim that real users validated a design unless user testing actually occurred. Never claim accessibility, responsiveness, production readiness, or successful runtime behavior without the corresponding checks.
