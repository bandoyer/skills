## What it does

`tdd` builds changed behaviour in small red-green-refactor increments. Expected values come from the request or independent examples, and tests exercise useful existing interfaces.

## When to reach for it

Type `/tdd`, or the agent can select it for test-first implementation or regression tests. A pure refactor normally uses existing tests unchanged.

## Common questions

**Do I have to choose the test interfaces?**

No. The agent selects suitable existing interfaces and asks only if the choice changes required behaviour or architecture. An accepted specification can name a binding interface.

**Will every small edit need a new failing test?**

No. Existing tests can prove a behaviour-preserving refactor; formatting and compile-only scaffolding need appropriate evidence, without an invented behavioural red.

**Does this start another review cycle?**

No. Testing stays within the task's scope and existing check/review allowance.

## It's working if

- A new behavioural test fails for the relevant reason before the fix.
- The test observes the requested outcome and permits internal refactoring.
- Routine test-placement choices do not return to you for approval.
- Required checks finish without unrelated test or metric work.

## Where it fits

Use it directly or within [implement](https://github.com/bandoyer/skills/blob/main/docs/engineering/implement.md). The user's coding standard owns test quality. [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) helps choose an entry point.
