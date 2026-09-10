---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

Call the Skill tool with "clean-code" first. Its working rules and workflow govern the implementation: state the problem, propose the change with its tests and documentation impact before editing production code, and get authorization for that stage once. A spec or ticket the user has already approved is that authorization; do not ask again for it.

Call the Skill tool with "tdd" at the seams the spec or tickets name. Tests first per increment, with each red run recorded before its code is written.

Run typechecking regularly, single test files regularly, and the full test suite once at the end. Run the repository's own gates and report their real output.

Commit each finished increment to the current branch with its tests, so that the diff from the fixed point to `HEAD` holds everything a reviewer must see. `code-review` reads committed changes only; an uncommitted change is invisible to it.

Once the last increment is committed, call the Skill tool with "code-review", giving it the fixed point the work started from. Fix what it confirms as a further commit with its own checks, then hand back what changed, why it works, how it was checked, and what remains open.

Open no PR, including a draft, until the user has reviewed the result and approved submission.
