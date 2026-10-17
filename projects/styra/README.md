# Styra

Existing product design documents for a conversational AI shopping assistant.

## Documents and status

| Document | Scope and status |
| --- | --- |
| [V1 client brief](brief-v1-client.md) | Existing draft for review; not revised during repository organization |
| [Original design review](design-review-original.md) | Start screen critique; decisions remain pending in that document |
| [Heuristic evaluation](heuristics-evaluation.md) | Original Start screen; static-screen observations with behavior and accessibility limits |
| [Persona acid test](personal-acid-test.md) | Historical six-screen critique using assumed personas; reports fixes to a recreated HTML copy |

Read the [shared working agreement](../../principles/codex-contract.md), [design taste](../../principles/design-taste.md), and [anti-AI-slop rules](../../principles/anti-ai-slop.md) alongside these documents.

## Evidence and next work

The repository currently contains the written reports, not the source design, screen PNGs, or recreated HTML described in them. Implementation and pixel-measurement statements remain historical claims. The exact color pairs stated in the persona report were recalculated during repository review; this verifies the arithmetic only. Preserve the remaining limitations. Review decisions in one report do not automatically resolve the pending decisions in another.

The persona report includes a historical attribution to “Hasib”; that attribution has been preserved and is not confirmation of the repository owner's name. Verify it against the original source before changing it.

The separate [AI Shopping Assistant working agreement](../ai-shopping-assistant/codex-contract.md) covers related subject matter. Confirm the project relationship with the owner before merging folders or treating either brief as the other's approved requirements. Brief development is deferred for the current task.

## Decisions to revisit when design work resumes

- The brief explicitly includes text conversation in V1, while the persona report reviews a voice screen. Voice scope needs an owner decision; the report does not approve adding it to V1.
- Persona finding F02 resolves a black-versus-navy mismatch by changing the example request. That may be a valid demonstration edit, but it does not authorize dropping a real customer's color requirement.
- F04b assumes retailer placeholders bind to real names at build time, and F13 suggests deriving a budget increase from matching products. No implementation or data source is present to verify these assumptions. Treat them as proposals, not established behavior.
- The original critique's ten pending decisions and the persona report's seventeen findings use different identifiers and scopes. Reconcile overlapping findings with the owner before treating either report as the implementation plan; retain their existing decisions until then.
- The heuristic evaluation marks icon accessibility as requiring verification while also assigning a numeric severity. Establish evidence and a common severity scale before using these labels to prioritize implementation.

These are review notes, not changes to the brief, product scope, or recorded design decisions.
