---
name: grilling
description: Grill the user relentlessly about a plan, decision, or idea. Use when the user wants to stress-test their thinking, or uses any 'grill' trigger phrases.
---

Interview the user relentlessly until you reach a shared understanding. Map this as a **design tree**: every decision branches into the decisions that hang off it.

Before the first round, settle the **objective**: what this session is for, and what the user needs to have in hand when it ends (a spec, one decision, a build brief, an evaluation of a tool). Ask it as Q0 if the request does not already say. The objective is the root of the tree and the stopping rule for every round after it.

Work the tree in **rounds**. The **frontier** is every decision whose prerequisites are already settled: the questions you can ask _now_ without guessing at answers you haven't heard yet. Ask the whole frontier in one round: number each question and give your recommended answer. Then wait for the user's answers before the next round.

Format a round like so:

```
❓ **Q1** - **<question title>**: <question body, might be multiple paragraphs, including multiple choices>

➡️ <your recommended answer>

---

❓ **Q2** - **<question title>**: <question body, might be multiple paragraphs, including multiple choices>

➡️ <your recommended answer>
```

Each round the user answers reshapes the tree: settled decisions push the frontier outward and unblock questions that depended on them. Recompute the frontier and ask the next round. A question whose answer depends on another question still open in this round belongs to a _later_ round, not this one.

Finding _facts_ is your job, never the user's. When a frontier question needs a fact from the environment (filesystem, tools, etc.), dispatch a sub-agent to find it; don't ask the user for anything you could look up yourself. Don't block on it: a running exploration is an unsettled prerequisite, so only the questions downstream of it wait for the sub-agent to report; ask the rest of the frontier now. The _decisions_ are the user's: put each to them and wait.

Before asking a round, sort the frontier by the objective. A question goes to the user when its answer changes what gets built, decided, or delivered. A question with a sound default that the deliverable can carry as a stated assumption is **defaulted**: record the default and its reason in one line under the round, and do not ask it. Nothing is silently assumed; a default is written down, not skipped, and the user can overturn any of them.

The session is done when the frontier holds no question the user needs to answer: every branch of the design tree is either decided by the user or carried as a written default. When a round would consist only of defaults, do not send it as questions; present the defaults with the shared understanding instead. Do not act on it until the user confirms you have reached a shared understanding.
