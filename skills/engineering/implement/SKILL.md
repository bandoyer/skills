---
name: implement
description: Implement the work described by a request, specification, or ticket.
disable-model-invocation: true
---

# Implement

Complete the requested work within its accepted scope, using the project instructions and the user's coding standard. A direct implementation request or an approved specification authorizes the local work; preserve any expressly reserved checkpoints. Do not require a preceding interview, ticket breakdown, or another approval of routine implementation choices.

Before editing, identify the requested outcome, relevant existing code, starting Git reference, pre-existing work, and required checks. Explain the approach briefly and continue. Load `clean-code` when available and `tdd` for changed behaviour; use a skill tool when available or read the named skill directly.

Implement reviewable increments. Reuse existing tests for pure refactors. Finish relevant checks and fix failures caused by the change within the authorized scope. Do not broaden work to unrelated failures or optional cleanup.

Follow the project's commit policy. If local commits are authorized, commit only task-owned changes and record the candidate and starting reference before using the committed-diff `code-review` skill. If work remains uncommitted, review that actual diff directly instead. Do not commit unrelated user changes to make a review command convenient.

Review once using the task's declared allowance. Repair confirmed in-scope blockers when authorized, then check only closure and repair regressions. Do not invoke review recursively or keep polishing until no advice remains. Report the result, meaningful evidence, and unresolved limitations.

Follow the user's publication boundaries. A finished local result does not itself authorize a PR, push, merge, or deployment.
