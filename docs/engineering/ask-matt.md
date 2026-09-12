## What it does

`ask-matt` recommends the smallest useful entry point for the requested outcome. The collection is a set of optional tools, not a required pipeline.

## When to reach for it

Invoke `/ask-matt` when you are unsure which skill fits. A clear implementation request can proceed directly without an interview, formal spec, or tracker setup.

## Common questions

**Must every task go through grilling, specs, tickets, and review?**

No. Planning artifacts help when the task needs unresolved decisions, coordination, or a durable contract. Ordinary work can proceed under the user's coding standard.

**Which skills belong globally?**

Reusable methods can be available globally if their descriptions are narrow. Project facts, commands, domain vocabulary, and operational restrictions belong with that project. Install only the workflows you use; copying the collection into every prompt wastes context.

**Should I clear context between tickets?**

Only when that is useful. Preserve scope, decisions, evidence, and the remaining allowance so a new session or compaction does not restart the task.

## It's working if

- The recommendation matches the task instead of enlarging it.
- Direct work stays direct.
- Optional workflows preserve existing authorization and stopping limits.

## Where it fits

It is the human-facing router across [the maintained skills](https://github.com/bandoyer/skills/blob/main/README.md). It recommends explicit-only workflows without executing them.
