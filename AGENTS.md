# Repository instructions for Codex

## Read before working

1. Read `README.md` and `projects/README.md` to understand the repository and select the intended project.
2. Read `principles/codex-contract.md`, `principles/design-taste.md`, and `principles/anti-ai-slop.md` before analysis, design recommendations, or substantive edits.
3. Read the selected project's README, context, engagement, working agreement, and relevant brief, reviews, tokens, and latest log when present. Check for more specific `AGENTS.md` instructions in the directories being edited. Match the reading to the task rather than loading unrelated projects.
4. Identify documented facts, draft proposals, assumptions, approved decisions, and unverified claims before acting. A finding marked FIX in a historical report does not establish that a source design was updated or the owner approved it.
5. Read the relevant procedure from `skills/` for substantial design or career work. `.agents/skills/` provides Codex entry points that route to these canonical files; do not maintain a competing copy of the procedure there.

## Authority and scope

- Follow the owner's current request and preserve their final product and design authority. Apply the shared working agreement and the selected project's requirements together. If they conflict materially, explain the conflict and obtain the owner's decision before dependent work.
- Make routine organization, link repairs, and authorized file updates directly. Do not ask the owner to copy changes manually when repository access allows the work.
- Do not invent research, personas presented as research, metrics, screenshots, implementation status, or product requirements. Preserve source limitations and distinguish historical claims from checks performed now.
- Do not silently change settled requirements or governing principles. Routine repository maintenance covers structural repairs, factual corrections, and navigation; substantive changes to design standards require owner approval.
- Styra is the owner's AI Shopping Assistant project. Its canonical folder is `projects/styra/`; read its `codex-contract.md` alongside the shared agreement and the owner-confirmed direction in its README. Keep future shopping-assistant work in that folder.
- Brief development remains deferred until the owner explicitly resumes it. The existing V1 brief is a draft; its examples and unresolved scope assumptions must not override newer owner-confirmed direction. Record consequential discrepancies for the owner instead of silently rewriting the brief.
- Shopping recommendations must preserve delivery-inclusive total cost, seller reliability, return conditions, honest handling of unavailable information, and explicit customer approval before ordering or payment. Do not infer that checkout belongs in V1 from this safeguard.
- Treat examples in shared principles as illustrations of design judgment. An example involving checkout or a particular device does not add that capability or device requirement to every project's scope.

## File placement

- Keep the repository root limited to entry points and repository-wide configuration or instructions.
- Store shared principles in `principles/`; keep one canonical copy of each agreement or standard and link to it.
- Store project-specific documents in `projects/<project-name>/`. Start with a project README that links to the brief, agreement, and reviews that actually exist.
- Use lowercase, hyphenated names and `.md` for Markdown. Retain meaningful existing names during moves; do not rename historical documents just to imply new status.
- If a project grows, group reviews in `reviews/` and supporting images in `assets/`; update every affected reference when moving files. Create folders when there is content to place in them.
- Keep source designs, before/after exports, and implementation artifacts distinguishable. Do not claim an asset is present until it is committed or linked to a verified source.
- Reusable procedures belong in `skills/`; career positioning, portfolio stories, applications, and interview preparation belong in `career-vault/`. Shared workspace images belong in `assets/`, and product images in that project's assets folder when supplied.
- Start a new project from `projects/_new-client/` only when requested. This template and the optional `_brief-bank/` index are not active clients or evidence of progress. Never fill them with fictional user facts or borrow another project's context.
- Unfilled career files are templates, not evidence for a resume or application. Do not import facilitator identity, course outcomes, market assumptions, or unrelated example clients into the owner's work.

## Continuity and design workflow

- Resume a named project with `skills/pick-up.md`: read its latest log and check current files before relying on a handoff. At the end of substantial authorized work, use `skills/wrap-up.md` to preserve a concise, factual entry without inventing decisions or requiring redundant approval for routine notes.
- Diagnose blockers using `skills/stuck.md` and available evidence. Make routine authorized repairs directly; ask only when the next step genuinely needs the owner's input or approval.
- For new design work, clarify context and scope, consolidate a brief when authorized, map the journey, reuse or define tokens, plan tasks, build, and review. Reuse completed work and adapt the sequence to the task. Repository maintenance does not authorize the deferred Styra brief or require generating screens.
- Templates explain what remains missing. An empty context, token record, career file, or log must not be described as completed research, an approved system, or a shipped result. Preserve original briefs and reports as sources when later work creates new versions.

## Maintenance and verification

- Inspect the working tree before edits and preserve unrelated work.
- Keep changes focused. Preserve substantive content and review decisions during organizational changes. Update navigation whenever a document moves or is added.
- Verify local Markdown links, referenced repository paths, file extensions, and obsolete setup labels. Compare moved documents with their originals so substantive deletions are caught.
- For documentation-only changes, use document and diff checks; do not invent an application build or test suite.
- For authorized publication, use a reviewable branch and pull request. Do not merge or push directly to the default branch without explicit authorization. If access is unavailable, preserve concrete local changes and report the exact blocker.
- Finish with a brief report of applied changes, actual checks, unresolved questions, and publication status. Never claim remote files were updated when changes exist only locally.
