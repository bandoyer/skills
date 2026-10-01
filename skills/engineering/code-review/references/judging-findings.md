# Judging findings you did not produce

Panel reviewers and relayed reviews see a slice of the code and a short statement of intent. They don't know what was already tried and rejected, which constraints sit outside the code, which parts are temporary, or what the next change will address. You do. Filter, put each finding in context, and decide. Don't aggregate.

## Reasons to dismiss or downgrade

- **Nitpick gravity.** Reviewers fill their review. When nothing serious turns up, nits get inflated to fill the space. If every finding is a nit or a style preference, the candidate is probably fine. Say so.
- **Hypothetical, not actual.** "What if this is null?" is a finding only if a caller can pass null. Trace the call site. If upstream validation or the type system rules it out, dismiss it.
- **Premature abstraction.** A suggestion to extract a function, add an interface, or generalize is advice unless the code needs to change in a second way now.
- **A different approach.** "I would have done it differently" is not a defect unless the reviewer shows a concrete problem with the current approach.
- **Missing context.** The reviewer flags code the change didn't touch, a pattern consistent with the rest of the codebase, or a fix that conflicts with a constraint you know about.

## Reasons to take a finding seriously

- Two reviewers raised it independently.
- It names a concrete execution path, not a hypothetical.
- It shows a gap in your own understanding of the code.
- It is a security or correctness finding. These deserve scrutiny even from a single reviewer.

Don't dismiss a finding because it is uncomfortable.

## The verdict

The user should be able to fix the **Act on** items and ship with confidence. The **Dismissed** list is a trust mechanism, not busywork: showing what you rejected and why lets the user overrule you.

Adapted from the interrogate lead-judgment framework in pstack, Copyright (c) 2026 Lauren Tan, MIT License (`judging-findings.LICENSE`).
