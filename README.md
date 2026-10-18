# Codex Hasina’s Workspace
UI/UX and user-centered product design portfolio focused on solving real-world problems by combining user research, business needs, interaction design, prototyping, design systems, and thoughtful visual design.

## Start here

- [Working agreement with Codex](principles/codex-contract.md): how we collaborate and who makes decisions.
- [Design taste](principles/design-taste.md): the design standards applied across projects.
- [Anti-AI-slop rules](principles/anti-ai-slop.md): checks for specific, useful design and clear copy.
- [Project index](projects/README.md): project documents and their current status.
- [Codex instructions](AGENTS.md): reading order, file placement, and maintenance workflow.
- [Design workflows](skills/README.md): the reference's thirteen workflow categories, adapted for Codex.
- [Career vault](career-vault/README.md): clearly unfilled career and portfolio templates.
- [Reference alignment](docs/reference-alignment.md): what was adopted, adapted, or intentionally excluded.

## Where things belong

```text
AGENTS.md                      Instructions Codex reads when working here
README.md                      Portfolio introduction and navigation
.agents/skills/                Codex entry points for the reusable workflows
principles/                    Shared design standards and working agreement
skills/                        Canonical readable workflow instructions
projects/
  README.md                    Project index
  _new-client/                 Empty project template to copy when asked
  _brief-bank/                 Optional practice-brief reference index
  styra/                       AI Shopping Assistant agreement, brief, and reviews
career-vault/                  Unfilled positioning, story, resume, and proposal templates
assets/                       Shared asset guidance; project images stay with their project
docs/                         Reference mapping and maintenance rationale
```

Put a rule that applies across projects in `principles/`. Put a brief, review, decision, or design asset for one project inside its folder under `projects/`. Use lowercase names with hyphens and `.md` for Markdown documents. Folder names are literal names such as `principles`, without arrows or setup instructions.

The `codex-contract.md` files serve the same shared/project agreement roles as the reference's Claude contracts. The names and skill discovery are adapted for Codex; your existing principles and project material remain your own.

## Everyday use

Ask “pick up Styra” to resume from its [log](projects/styra/log.md), then name the task you want done. Ask “save my progress” to leave a truthful handoff. Ask “I'm stuck” for an evidence-based diagnosis. Codex edits authorized files directly; no manual copy-and-paste is required.

For a new project, ask Codex to copy the [new-client template](projects/_new-client/README.md) into a named sibling folder. For career work, use the [career vault](career-vault/README.md). Templates and linked exercises are not completed work or verified personal facts.

## Current focus

The repository structure and shared principles are ready for ongoing maintenance. Developing the shopping-assistant brief is deferred. Existing project documents retain their original draft, pending-decision, and verification status.

The owner confirmed that **Styra** is the product name of the AI Shopping Assistant. Its agreement, existing draft brief, and reviews now live together in [one project folder](projects/styra/README.md). That project index records the latest confirmed direction and the scope questions that remain open.

Codex should edit the relevant files directly for authorized work, verify the changes, and report what was applied. The owner retains final product and design direction. Proposed changes to settled requirements or governing principles require approval. Published changes should be reviewed through a pull request before merging.
