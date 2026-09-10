---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

Call the Skill tool with "clean-code" first. Its working rules and workflow govern the implementation: state the problem, propose the change with its tests and documentation impact before editing production code, and get authorization for that stage once. A spec or ticket the user has already approved is that authorization; do not ask again for it.

Call the Skill tool with "tdd" at the seams the spec or tickets name. Tests first per increment, with each red run recorded before its code is written.

Run typechecking regularly, single test files regularly, and the full test suite once at the end. Run the repository's own gates and report their real output.

Once done, call the Skill tool with "code-review" to review the work, then hand back what changed, why it works, how it was checked, and what remains open.

Commit your work to the current branch. Open no PR, including a draft, until the user has reviewed the result and approved submission.
