# Styra

Styra is the product name of the owner's personal AI Shopping Assistant design project. The owner confirmed on 18 October 2026 that both names refer to this one project. This is its canonical project folder.

## Owner-confirmed direction

Help customers save time finding approximately three to four relevant products within their budget, across brands, non-branded shops, marketplaces, and second-hand sellers. Recommend fewer when enough suitable options are unavailable; do not fill slots with weak matches.

The intended shopping coverage includes clothing, shoes, bags, and accessories, with cosmetics a possibility rather than a settled launch commitment. The audience is broad across genders and professions. Clothing examples in the older draft and reports do not establish a narrower approved audience or launch category list.

Preserve the [project working agreement](codex-contract.md): consider delivery-inclusive total cost, seller reliability, and return conditions; disclose unavailable information; obtain the customer's explicit approval before ordering or payment. The owner retains final product and design direction.

## Documents and status

| Document | Scope and status |
| --- | --- |
| [Project working agreement](codex-contract.md) | Existing AI Shopping Assistant agreement, now filed under the confirmed product name; substantive content preserved |
| [Context](context.md) | Confirmed user goal and audience direction, with evidence and research gaps explicit |
| [Engagement status](engagement.md) | Current maintenance boundary and unagreed product delivery terms |
| [V1 client brief](brief-v1-client.md) | Existing draft for review; not revised during repository organization |
| [Original design review](design-review-original.md) | Start screen critique; decisions remain pending in that document |
| [Heuristic evaluation](heuristics-evaluation.md) | Original Start screen; static-screen observations with behavior and accessibility limits |
| [Persona acid test](personal-acid-test.md) | Historical six-screen critique using assumed personas; reports fixes to a recreated HTML copy |
| [Critique index](critique-notes.md) | Entry point to the existing reports; no new design decisions or screen review |
| [Design-system status](tokens.md) | Missing sources and bindings; no approved token values invented |
| [Session log](log.md) | Current factual handoff and unresolved next decisions |

Read the [shared working agreement](../../principles/codex-contract.md), [design taste](../../principles/design-taste.md), and [anti-AI-slop rules](../../principles/anti-ai-slop.md) alongside these documents.

These context, engagement, critique, token-status, and log files follow the [reference workspace pattern](../../docs/reference-alignment.md). They provide navigation and truthful status; they do not create a new brief, approve a design system, or establish research. IA, implementation tasks, a revised brief, and real screens should be created only when that work is requested.

## Evidence and next work

The repository currently contains the written reports, not the source design, screen PNGs, or recreated HTML described in them. Implementation and pixel-measurement statements remain historical claims. The exact color pairs stated in the persona report were recalculated during repository review; this verifies the arithmetic only. Preserve the remaining limitations. Review decisions in one report do not automatically resolve the pending decisions in another.

The persona report includes a historical attribution to “Hasib”; that attribution has been preserved and is not confirmation of the repository owner's name. Verify it against the original source before changing it.

The project agreement and shared [Codex agreement](../../principles/codex-contract.md) complement each other: one defines Styra's customer safeguards, while the other governs collaboration and the owner's authority. Consolidation does not approve every assumption in the older draft. Brief development remains deferred.

## Agreement and draft reconciliation

- **Cost and seller information:** The agreement requires delivery-inclusive cost, seller reliability, and return conditions. The draft discusses shipping information when available but does not fully restate these safeguards. Keep the agreement's requirements; unknown delivery or return details must remain unknown rather than being treated as verified or within budget.
- **Purchase boundary:** The agreement requires approval before any order or payment; the draft describes continuing to a retailer and does not assume in-app checkout in V1. These safeguards do not themselves require an in-app checkout feature. Decide the V1 purchase handoff and any ordering capability when the owner resumes scope work.
- **Categories and audience:** Use the owner-confirmed direction above. The draft's clothing examples and open category questions require a later brief reconciliation; they do not supersede that direction. The initial release categories and whether cosmetics belong in them remain undecided.

The draft itself is unchanged. These notes identify how to read it against confirmed direction and where a substantive decision is still needed.

## Decisions to revisit when design work resumes

- The brief explicitly includes text conversation in V1, while the persona report reviews a voice screen. Voice scope needs an owner decision; the report does not approve adding it to V1.
- Persona finding F02 resolves a black-versus-navy mismatch by changing the example request. That may be a valid demonstration edit, but it does not authorize dropping a real customer's color requirement.
- F04b assumes retailer placeholders bind to real names at build time, and F13 suggests deriving a budget increase from matching products. No implementation or data source is present to verify these assumptions. Treat them as proposals, not established behavior.
- The original critique's ten pending decisions and the persona report's seventeen findings use different identifiers and scopes. Reconcile overlapping findings with the owner before treating either report as the implementation plan; retain their existing decisions until then.
- The heuristic evaluation marks icon accessibility as requiring verification while also assigning a numeric severity. Establish evidence and a common severity scale before using these labels to prioritize implementation.

These are review notes, not changes to the brief, product scope, or recorded design decisions.
