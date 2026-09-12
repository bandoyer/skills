## What it does

`implement` completes a request, specification, or ticket through local implementation, appropriate checks, and bounded review. It preserves the requested scope and existing approvals.

## When to reach for it

Invoke `/implement` when you want this explicit implementation workflow. Ordinary requests can also be handled directly without a preceding interview or ticket-creation sequence.

## Common questions

**Does it pause for another implementation approval?**

A direct implementation request or approved specification authorizes local work. It preserves an expressly reserved checkpoint and asks about material ambiguity, not routine choices.

**Does review include the work just written?**

When commits are authorized, it records the starting reference and candidate before using the committed-diff review skill. If work stays uncommitted, it reviews the actual local diff directly instead.

**Can review run indefinitely?**

No. The task's declared review allowance governs. Confirmed in-scope blockers get an authorized repair and a focused delta check; optional advice does not start another cycle.

## It's working if

- The requested behaviour runs and the required checks complete.
- Pre-existing user work remains intact.
- The review covers the actual candidate.
- The final report states the result and real limits without publishing it automatically.

## Where it fits

It uses [tdd](https://github.com/bandoyer/skills/blob/main/docs/engineering/tdd.md) for changed behaviour and [code-review](https://github.com/bandoyer/skills/blob/main/docs/engineering/code-review.md) when reviewing committed work. [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) maps optional planning and preparation tools.
