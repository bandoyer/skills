---
name: tdd
description: Test-driven development. Use when the user wants to build features or fix bugs test-first, mentions "red-green-refactor", or wants integration tests.
---

# Test-Driven Development

TDD is the red → green loop. This skill is the reference that makes that loop produce tests worth keeping: what a good test is, where tests go, the anti-patterns, and the rules of the loop. Every section applies on every cycle: consult them before and during the loop, not after.

When exploring the codebase, read `CONTEXT.md` (if it exists) so test names and interface vocabulary match the project's domain language, and respect ADRs in the area you're touching.

## What a good test is

The standard lives in the `clean-code` skill. Call the Skill tool with "clean-code" and read its `references/testing.md`, plus the language file for the code under test. That file holds what a good test is, where expected values come from, the anti-patterns to catch before handing back, and where substitutes stand. In one line: tests verify behavior through public interfaces, read like a specification, and survive refactors because they never reach inside.

[tests.md](tests.md) and [mocking.md](mocking.md) illustrate the same rules in TypeScript.

## Seams: where tests go

A **seam** is the public boundary you test at: the interface where you observe behavior without reaching inside. Tests live at seams, never against internals.

**Test only at pre-agreed seams.** When a spec, contract, or ticket the user approved names the seams, those are the agreed seams: test there without another round. Otherwise, before writing any test, write down the seams under test and confirm them with the user. No test is written at an unconfirmed seam. You can't test everything, so agreeing the seams up front is how testing effort lands on the critical paths and complex logic instead of every edge case.

When no seams are named, ask: "What's the public interface, and which seams should we test?"

When the shape of that interface is itself in question (how deep the module is, where the seam belongs, what the interface should expose), call the Skill tool with "codebase-design" for the vocabulary. It is the shared source of the module, interface, depth, seam, adapter, leverage and locality terms, and it is a reference to consult, not a session to run.

## Anti-patterns

The implementation-coupled and tautological tests are defined in `clean-code`'s `references/testing.md`; catch them there. One anti-pattern is specific to the loop's shape:

- **Horizontal slicing**: writing all tests first, then all implementation. Bulk tests verify _imagined_ behavior: you test the _shape_ of things rather than user-facing behavior, the tests go insensitive to real changes, and you commit to test structure before understanding the implementation. Work in **vertical slices** instead: one test → one implementation → repeat, each test a **tracer bullet** that responds to what the last cycle taught you.

## Rules of the loop

- **Red before green.** Write the failing test first, then only enough code to pass it. Don't anticipate future tests or add speculative features.
- **Paste the red.** Run the new test and record its failing output before writing the code. A test that passes before the code exists is not testing the rule; rewrite it until it is red, or say why it cannot be.
- **One slice at a time.** One seam, one test, one minimal implementation per cycle.
- **Clean with the tests green.** After each green, improve names, structure, and duplication under the tests, following the cleaning cycle in `clean-code`'s `references/code.md`. Each cleaning step preserves behavior; when one breaks a test, back out that step. Review (the `code-review` skill) checks the result; cleaning does not wait for it.
