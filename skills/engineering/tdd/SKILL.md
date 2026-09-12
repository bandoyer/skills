---
name: tdd
description: Build changed behaviour with a focused red-green-refactor loop. Use for test-first implementation and regression tests.
---

# Test-driven development

Use the accepted request and the project's coding standard to guide small, reviewable increments. If `clean-code` is available, load its testing reference when needed; it owns test quality and language conventions. Use a skill tool when available, otherwise read the named skill and relevant reference directly.

Choose an existing public interface that exercises the required behaviour. A specification's named interfaces are binding; when none are named, selecting a suitable existing interface is an implementation decision. Ask only if the choice changes required behaviour or architecture.

For each changed behaviour, write a meaningful test, run it and observe the relevant failure, implement enough to pass, then clean up with tests green. Expected values come from requirements or independent examples. Keep the distinguishing input and outcome visible. Do not batch speculative tests for decisions that have not been made.

Existing tests may already prove a behaviour-preserving refactor. Do not manufacture a failing test for formatting, a pure refactor, or compile-only scaffolding. Report the evidence honestly.

Use the narrowest useful check while editing and complete the project's required checks before delivery. Follow the task's scope and review allowance; this skill does not introduce a test-interface approval stage, a reviewer panel, or an additional full-suite run.

[tests.md](tests.md) and [mocking.md](mocking.md) contain TypeScript examples. Read them only when those examples help the current task.
