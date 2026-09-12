## What it does

`handoff` writes a concise continuation record with the current objective, decisions, approvals, evidence, remaining allowance, and next action. Historical detail stays in linked records.

## When to reach for it

Invoke `/handoff` when another agent, session, or workspace needs to continue the work. Use an existing project handoff location or a requested path; a portable handoff can use an OS temporary path.

## Common questions

**Will a handoff restart the review budget?**

No. It carries the current allowance and approved stages forward.

**Should I delete it after reading?**

No. Keep the current handoff available and update it at milestones. Archive completed history separately.

## It's working if

- The next agent can identify the original request and exact next step.
- Existing decisions and reserved checkpoints remain clear.
- Evidence is linked rather than copied into a growing history.
- No credentials are included.

## Where it fits

It supports any workflow that spans sessions. [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) maps the available tools.
