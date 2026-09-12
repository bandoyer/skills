## What it does

`to-spec` turns settled conversation and codebase knowledge into a concise specification for the configured tracker. It captures accepted outcomes and important failure behaviour without restarting the interview.

## When to reach for it

Invoke `/to-spec` when you want a durable specification from decisions already made. Tracker and label setup is required only for publishing to that configured destination.

## Common questions

**Do I need to approve every test interface?**

No. The spec records binding interface decisions already made and describes observable acceptance. Routine placement at existing interfaces can be chosen during implementation.

**Will it invent a long list of future stories?**

No. Stories cover the accepted scope. New product decisions and material architectural questions remain explicit, rather than being silently filled in.

## It's working if

- The specification preserves the decisions and scope you already established.
- Outcomes and meaningful failure behaviour are testable.
- Routine internal choices remain available to implementation.
- Publishing follows the configured destination and existing authorization.

## Where it fits

Use it when a durable contract helps. [implement](https://github.com/bandoyer/skills/blob/main/docs/engineering/implement.md) can also work from a clear request without a formal spec. [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) maps other entry points.
