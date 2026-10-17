# Repository instructions for Codex

## Read before working

1. Read `README.md` and `projects/README.md` to understand the repository and select the intended project.
2. Read `principles/codex-contract.md`, `principles/design-taste.md`, and `principles/anti-ai-slop.md` before analysis, design recommendations, or substantive edits.
3. Read the selected project's README, working agreement if present, brief, and relevant reviews. Check for more specific `AGENTS.md` instructions in the directories being edited.
4. Identify documented facts, draft proposals, assumptions, approved decisions, and unverified claims before acting. A finding marked FIX in a historical report does not establish that a source design was updated or the owner approved it.

## Authority and scope

- Follow the owner's current request and preserve their final product and design authority. Apply the shared working agreement and the selected project's requirements together. If they conflict materially, explain the conflict and obtain the owner's decision before dependent work.
- Make routine organization, link repairs, and authorized file updates directly. Do not ask the owner to copy changes manually when repository access allows the work.
- Do not invent research, personas presented as research, metrics, screenshots, implementation status, or product requirements. Preserve source limitations and distinguish historical claims from checks performed now.
- Do not silently change settled requirements or governing principles. The current organization task authorizes structural repairs and maintenance instructions, not a rewrite of the design standards.
- The shopping-assistant brief is deferred. Do not expand it or merge its project folder with Styra without an owner instruction resolving that scope.
- Shopping recommendations must preserve delivery-inclusive total cost, seller reliability, return conditions, honest handling of unavailable information, and explicit customer approval before ordering or payment. Do not infer that checkout belongs in V1 from this safeguard.

## File placement

- Keep the repository root limited to entry points and repository-wide configuration or instructions.
- Store shared principles in `principles/`; keep one canonical copy of each agreement or standard and link to it.
- Store project-specific documents in `projects/<project-name>/`. Start with a project README that links to the brief, agreement, and reviews that actually exist.
- Use lowercase, hyphenated names and `.md` for Markdown. Retain meaningful existing names during moves; do not rename historical documents just to imply new status.
- If a project grows, group reviews in `reviews/` and supporting images in `assets/`; update every affected reference when moving files. Create folders when there is content to place in them.
- Keep source designs, before/after exports, and implementation artifacts distinguishable. Do not claim an asset is present until it is committed or linked to a verified source.

## Maintenance and verification

- Inspect the working tree before edits and preserve unrelated work.
- Keep changes focused. Preserve substantive content and review decisions during organizational changes. Update navigation whenever a document moves or is added.
- Verify local Markdown links, referenced repository paths, file extensions, and obsolete setup labels. Compare moved documents with their originals so substantive deletions are caught.
- For documentation-only changes, use document and diff checks; do not invent an application build or test suite.
- For authorized publication, use a reviewable branch and pull request. Do not merge or push directly to the default branch without explicit authorization. If access is unavailable, preserve concrete local changes and report the exact blocker.
- Finish with a brief report of applied changes, actual checks, unresolved questions, and publication status. Never claim remote files were updated when changes exist only locally.
