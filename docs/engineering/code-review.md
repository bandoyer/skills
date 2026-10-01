## What it does

`code-review` checks a committed candidate against the requested behaviour and applicable project standards. It reviews directly by default and prioritizes verified blockers separately from advice. A report written for a person sorts findings into Act on, Consider, Noted, and Dismissed, each with a reason. An output contract supplied by the caller, such as a verifier schema, takes precedence over those groups.

## When to reach for it

Type `/code-review`, or the agent can select it for a committed branch, PR, or commit-range review, or to judge findings another reviewer produced.

| Situation | Review scope |
| --- | --- |
| Committed branch or PR | Compare the captured candidate against its supplied or unambiguous target |
| Explicit commit endpoints | Resolve both commits and compare those endpoints; the candidate need not be the checkout's `HEAD` |
| Staged, working-tree, or untracked changes | Request a direct review of those changes; the committed comparison excludes them |
| An explicitly selected reviewer panel | Give the fixed roster one frozen candidate and a bounded brief |
| Findings relayed from another reviewer | Judge each finding against the candidate and the accepted request |

## Common questions

**Do I need an issue tracker and a formal specification?**

No. A clear task request can establish intended behaviour. The reviewer reports limits when intent is missing and still checks what available evidence supports.

**Will it launch two reviewers every time?**

No. A panel is an explicit workflow choice. Assigned reviewers work directly and do not spawn further reviewers.

**Why does review keep finding more things?**

Design advice can vary between passes. This workflow separates advice from blockers, follows the declared review allowance, and limits delta review to unresolved blockers and repair regressions.

**Can I trust a reported finding without checking it?**

A finding must include the triggering case, consequence, source evidence, and smallest repair. The host verifies and prioritizes panel findings; a confident opinion alone is not a blocker.

**Another model reviewed this. Which of its findings matter?**

Relay the findings and ask for a judgment. Each one is checked against the code and sorted into the four groups. Dismissed findings stay in the report with the reason, so you can overrule the call.

## It's working if

- The report identifies the exact candidate and comparison.
- Every blocker has a concrete consequence and supporting evidence.
- No verified blocker is moved to advice to keep the Act on list short.
- Tests that would pass with every called function returning an empty value are reported.
- Missing intent is reported rather than invented.
- Settled findings stay closed and reviewer recursion does not occur.
- The report gives an overall recommendation.

## Where it fits

Use it independently or after committed increments from [implement](https://github.com/bandoyer/skills/blob/main/docs/engineering/implement.md). [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) routes other requests.
