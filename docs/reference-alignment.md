# Reference-workspace alignment

The owner requested the applicable organization of [claude-for-designers](https://github.com/hasinaparvin-uxdesign/claude-for-designers/tree/423b1de2aa9b4bf1050fd046987fb4f3a404ffec), inspected at revision `423b1de2aa9b4bf1050fd046987fb4f3a404ffec`. Its complete tracked tree contains 87 files. The tree, onboarding and governing documents, folder indexes, project-template fields, thirteen workflow procedures, example categories, and separate Styra drafts were inspected to understand the structure and workflow. This was a structure/workflow review, not a validation of every example's product claims or image pixels.

## Mapping

| Reference pattern | This workspace | Reason |
| --- | --- | --- |
| Root Claude instructions and existing Codex guidance | [AGENTS.md](../AGENTS.md) | One governing entry point for Codex, retaining the owner's authority |
| `.claude/skills/` and readable procedures | [.agents/skills/](../.agents/skills/) and [skills/](../skills/README.md) | Codex-native discovery with thin entry points reading one canonical procedure |
| Shared principles and root contract | [principles/](../principles/README.md) | Existing personal standards preserved; agreement remains named codex-contract.md |
| `_new-client/` | [new-client template](../projects/_new-client/README.md) | Same context/agreement/engagement/brief/critique/tokens/log/screen roles, without course answers |
| `_brief-bank/` | [optional brief bank](../projects/_brief-bank/README.md) | Links to the four source exercises instead of importing unrelated clients |
| Worked client project and extra root-level Styra folder | [projects/styra/](../projects/styra/README.md) | One canonical real project, retaining all existing distinct material |
| Six career documents and session log | [career-vault/](../career-vault/README.md) | Same role/naming pattern; clearly unfilled original templates |
| Workspace illustrations | [assets/](../assets/README.md) | Shared asset location without copying facilitator branding or inventing project evidence |
| Pick-up / work / wrap-up loop | [workflow index](../skills/README.md) and project logs | Resume from real files; save what happened, decisions, open issues, and next work |

The Codex-specific skill location and invocation follow [official OpenAI guidance](https://learn.chatgpt.com/docs/build-skills). GitHub hosting alone does not activate local skills: open the repository in Codex, or ask it to read the linked workflow directly.

## What was checked rather than copied blindly

- The reference keeps both human-readable procedures and native skill bodies. Two independently edited copies can drift. Here, native entry points load the readable source instead of duplicating it.
- Some reference guidance asks the user to paste workflow output manually, while other guidance edits files. This workspace follows the owner's request: Codex writes authorized changes directly.
- Course stages, model/subscription advice, instructor identities, sample resumes, example-client facts, hardcoded estimates, and facilitator branding are not facts about this portfolio and were not imported.
- Fixed font sizes, touch-target preferences, theme support, and sample palettes must not be advertised as universal accessibility requirements or adopted project decisions. Adapted review procedures verify the applicable standard and distinguish recommendations from requirements.
- The reference's extra root-level Styra draft mentions markets and proposed delivery scope that are not confirmed in this workspace. Those drafts remain source material in the reference, not silently imported requirements or a replacement for the deferred brief.
- Templates are legitimate empty starting points. Their presence does not mean career work, research, tokens, screen development, or approvals have happened. Existing Styra brief and report filenames remain stable so source history is discoverable.

The workflow concepts are credited to the reference workspace, whose [MIT license](https://github.com/hasinaparvin-uxdesign/claude-for-designers/blob/423b1de2aa9b4bf1050fd046987fb4f3a404ffec/LICENSE) identifies Shadman Rahman. The new instructions and blank templates here are rewritten for this owner's context rather than copied instructor content. The owner's existing substantive documents remain unchanged by this alignment.
