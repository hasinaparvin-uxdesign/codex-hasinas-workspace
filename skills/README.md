# Design workflows

These are the reference workspace's thirteen workflow categories, adapted for this portfolio and Codex. The instructions here are the canonical readable versions; small entry points under [.agents/skills](../.agents/skills/) load these same files without maintaining a second copy.

## Choose the work you need

| Work | Workflow | Output |
| --- | --- | --- |
| Resume a session | [pick-up](pick-up.md) | Read the newest project log and current files |
| Save progress | [wrap-up](wrap-up.md) | Update the selected project's log |
| Diagnose a blocker | [stuck](stuck.md) | Inspect evidence and fix or explain the blocker |
| Challenge assumptions | [grill-me](grill-me.md) | Clarifications or a requirements handshake in the selected target |
| Consolidate a brief | [design-brief](design-brief.md) | Approved target brief; preserve source versions |
| Map the journey | [information-architecture](information-architecture.md) | Project IA document and its visual companion |
| Document a design system | [design-tokens](design-tokens.md) | Project tokens and actual source/binding status |
| Plan implementation | [brief-to-tasks](brief-to-tasks.md) | Project tasks with dependencies and completion criteria |
| Build an approved screen | [frontend-design](frontend-design.md) | Implementation in the existing project stack |
| Review design quality | [design-review](design-review.md) | Evidence and proposed decisions in critique notes |
| Review usability heuristics | [heuristic-evaluation](heuristic-evaluation.md) | Ten-heuristic assessment with evidence limits |
| Stress-test perspectives | [persona-acid-test](persona-acid-test.md) | Scenario-based critique, explicitly distinct from user research |
| Prepare a job application | [application-pack](application-pack.md) | Evidence-based drafts in the career vault |

For new design work, the usual sequence is clarify the problem, settle a brief, map the journey, define or reuse tokens, plan tasks, build, then review. Reuse adequate existing work. A repository-organization request does not require designing a product or running all thirteen workflows.

## How to use them

Ask in ordinary language, such as “pick up Styra” or “review this screen against my principles.” Codex can choose a matching repository skill. In Codex CLI or the IDE, use a named skill such as `$pick-up`; see the [official skills documentation](https://learn.chatgpt.com/docs/build-skills). Availability depends on the repository being opened in the local Codex workspace, not merely viewed on GitHub. If a skill is not listed, ask Codex to read its linked workflow directly.

Codex writes authorized outputs into the relevant files and verifies them. You do not need to copy text between chat and GitHub. A skill is a procedure, not permission to publish, send messages, pay, or change product scope. Styra's brief remains deferred until the owner resumes it.
