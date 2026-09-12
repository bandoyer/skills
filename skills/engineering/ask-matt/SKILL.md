---
name: ask-matt
description: Choose a skill or workflow for the user's current task.
disable-model-invocation: true
---

# Choose the smallest useful workflow

Recommend the entry point that fits the requested outcome. Ordinary fixes and clearly specified work can proceed directly under the user's coding standard. A skill collection is not a mandatory sequence of interviews, specifications, tickets, and reviews.

| Need | Entry point |
| --- | --- |
| Implement a clear request, spec, or ticket | `/implement`; use `/tdd` for changed behaviour |
| Review committed changes | `/code-review`; direct review by default, a panel only when selected |
| Review staged or working-tree changes | A direct review of that explicit diff |
| Diagnose a bug still unclear after initial inspection | `/diagnosing-bugs` |
| Stress-test a plan through an interview | `/grill-me`; choose `/grill-with-docs` if the user wants domain documents maintained too |
| Synthesize settled decisions into a specification | `/to-spec` |
| Split an accepted plan into independently workable tickets | `/to-tickets` |
| Map a large effort whose major decisions remain unclear | `/wayfinder` |
| Process incoming external issues or PRs | `/triage` |
| Answer a design question with a bounded throwaway artifact | `/prototype` |
| Investigate a question using primary sources | `/research` |
| Survey architectural improvement opportunities | `/improve-codebase-architecture`, when that survey is the requested work |
| Clarify domain terms or record a domain decision | `/domain-modeling` |
| Design a module interface or consult deep-module vocabulary | `/codebase-design` |
| Resolve an in-progress merge or rebase conflict | `/resolving-merge-conflicts` |
| Continue in another session or workspace | `/handoff` |
| Prepare questions for someone else | `/to-questionnaire` |
| Guide steps that require human interaction | `/wizard` |
| Explain a message that did not land | `/wait-what` |
| Teach a concept over multiple sessions | `/teach` |
| Write instructions that agents will read | `/writing-for-agents` |

`/grilling` is the focused interview method used by the interview entry points and relevant planning workflows. Its stopping point is an actionable outcome, not an exhaustive list of every possible decision.

Use `/setup-matt-pocock-skills` when tracker, label, or domain-document setup is actually needed. Direct implementation, testing, diagnosis, and review do not require that setup.

## Continuity

Stay in the current session while it serves the task. Capture decisions and evidence in the appropriate artifacts so compaction can preserve them. Use a handoff when transferring work; do not clear context at every ticket or assume one fixed token threshold fits every model.

For a multi-session build, a spec and tickets can make scope and dependencies explicit. They are useful artifacts, not new approval stages. Carry existing authorization and the remaining review allowance forward. Read [PHASE-BOUNDARIES.md](PHASE-BOUNDARIES.md) only when deciding how to transfer or split the current work.
