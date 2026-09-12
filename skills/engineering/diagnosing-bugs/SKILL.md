---
name: diagnosing-bugs
description: Diagnose difficult or intermittent bugs and performance regressions when the cause remains unclear after initial inspection.
---

# Diagnose difficult bugs

Establish an evidence-supported cause or the precise remaining uncertainty. Stay within the task's scope and observation budget. A request to diagnose alone does not authorize a fix; an implementation request can include investigation, repair, and verification without another routine checkpoint.

Start with the reported trigger, expected and actual behaviour, logs, and relevant code. Reading code may reveal how to construct a reproduction. Distinguish observations from hypotheses and do not expose secrets in commands, logs, or saved artifacts.

Prefer a small repeatable check that exercises the actual symptom: an existing test, a CLI or HTTP request, a captured trace, or a targeted harness. Improve its speed or determinism only as far as needed to answer the question. Reuse a useful reproduction rather than requiring exhaustive minimization.

When the cause is unclear, state the plausible explanation and the observation that would distinguish it from alternatives. Use as many hypotheses as the evidence warrants, without a fixed count. Run the smallest bounded experiment that can settle the uncertainty. A repeated failure without new evidence is a reason to change the experiment or report the limit, not repeat the same work.

For intermittent failures, bound repetition or stress by time and resources. For performance, measure a baseline and compare under equivalent conditions. Production instrumentation, new paid calls, and live-system mutations retain their authorization requirements.

If reproduction is unavailable, continue useful read-only analysis of existing evidence. Report what is established, what is inferred, and what additional observation would settle the question. Do not claim a verified cause or fix without supporting evidence.

When a fix is authorized, add a meaningful regression test before changing behaviour where feasible, apply the smallest repair, and verify the original scenario plus relevant required checks. Follow the user's coding standard. Remove only your temporary instrumentation and artifacts; preserve useful captured evidence and pre-existing work. Report the cause, result, checks, and remaining limitations, then stop.
