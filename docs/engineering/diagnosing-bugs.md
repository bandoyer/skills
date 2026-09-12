## What it does

`diagnosing-bugs` investigates difficult bugs and performance regressions using targeted evidence and bounded experiments. Reading relevant code is allowed before a runnable reproduction exists.

## When to reach for it

Type `/diagnosing-bugs`, or the agent can select it when the cause remains unclear after initial inspection. Ordinary fixes with an evident cause do not need the full diagnostic workflow.

## Common questions

**What if the failure cannot be reproduced locally?**

The agent can inspect existing logs, traces, and code, distinguishing evidence from hypotheses. It reports the smallest additional observation needed without claiming the cause or repair was verified.

**Will it require several theories for an obvious defect?**

No. The number of hypotheses and amount of minimization follow the uncertainty. A useful reproduction does not need to become an exhaustive minimization exercise.

**Will diagnosis change production or launch paid experiments?**

Those actions keep their authorization requirements. A diagnosis-only request stays diagnostic; a fix request can include the necessary local investigation and repair.

## It's working if

- Each experiment answers a concrete unresolved question.
- Repetition and performance measurements have explicit bounds.
- The original symptom is checked after an authorized fix.
- Temporary instrumentation is cleaned up and useful evidence is retained.
- The final explanation separates observations, inferences, and limitations.

## Where it fits

This is a standalone investigation tool. An authorized repair follows the user's coding standard and may use [tdd](https://github.com/bandoyer/skills/blob/main/docs/engineering/tdd.md). [ask-matt](https://github.com/bandoyer/skills/blob/main/docs/engineering/ask-matt.md) maps the other entry points.
