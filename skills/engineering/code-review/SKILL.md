---
name: code-review
description: Review committed branch, PR, or commit-range changes against the requested behaviour and project standards.
---

# Review committed changes

Produce an actionable review of a fixed candidate. Review directly by default. A reviewer panel is used only when selected and authorized for the task. If you are already an assigned reviewer, do not invoke this skill recursively or delegate your review.

## Establish the scope

Resolve and record the candidate commit requested by the user; use `HEAD` only when reviewing the current checkout. For a branch or PR, use its established target when unambiguous; otherwise ask which comparison is intended. Validate both references and inspect the commit list. Use `git diff <base>...<candidate>` for a branch comparison from the merge-base, or `git diff <base> <candidate>` for explicitly requested endpoints. State the actual comparison. Both exclude staged, working-tree, and untracked changes. If the request concerns those changes, review them directly with an appropriate explicit scope instead of claiming a committed comparison includes them.

Use the request, supplied spec, or linked issue as the behavioural source. Consult tracker configuration only when needed to retrieve a referenced issue. No tracker setup or formal spec is required to review an otherwise clear request. If intent cannot be established, report that limitation and still review what the evidence supports.

Load the applicable project standards and `clean-code` references when available and relevant. Use a skill tool or read the files directly. Read surrounding code where necessary to understand consequences; do not turn a diff review into a whole-repository audit.

## Assess and report

Check both required behaviour and documented standards. Find missing behaviour, defects, scope expansion, and tests that cannot detect plausible mistakes. Do not derive expected behaviour from the implementation alone. Treat design smells as hypotheses, not automatic violations or instructions to refactor.

Each blocker needs a triggering case, consequence, file/line evidence, and the smallest needed repair. Tie it to an accepted criterion or a material correctness, data-loss, security, or compatibility risk. Separate optional advice. Prioritize verified findings and give an overall recommendation; keep their behavioural or standards origin identifiable without duplicating the report.

Reuse valid check results for the same candidate; run additional checks only to resolve a concrete uncertainty or satisfy a required gate. Follow the declared review allowance. This skill reports findings and does not itself authorize repairs, publication, or another review round.

## When a panel was selected

Give the fixed roster the same candidate, scope, behavioural source, relevant standards, and remaining allowance. Each reviewer works read-only, without further delegation or access to the other reviews. Preserve their reports, verify and deduplicate findings, then recommend a disposition. A delta review covers unresolved blockers and regressions caused by the repair, keeping settled findings closed.
