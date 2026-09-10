---
"mattpocock-skills": patch
---

implement: commit each finished increment before calling `code-review`, and give the review the fixed point the work started from. `code-review` diffs committed changes from a fixed point to `HEAD`, so reviewing before committing left the reviewers blind to the work. Fixes from the review land as a further commit with their own checks.
