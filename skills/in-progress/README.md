# In Progress

Beta. These skills are public on purpose: try them and tell me what breaks. They're excluded from the plugin and the top-level README until they graduate to a stable bucket, they get no docs pages, and they can change or disappear without warning.

The plugin won't give you these. Install one directly:

```bash
npx skills@latest add mattpocock/skills --skill=<name>
```

- **[loop-me](./loop-me/SKILL.md)**: Grill yourself into implementable workflow specs over multiple sessions, using the current directory as a stateful workspace. User-invoked.
- **[writing-beats](./writing-beats/SKILL.md)**: Shape an article as a journey of beats, choose-your-own-adventure style. Pick a starting beat, write only that beat, then pivot to the next, until the article reaches a natural end.
- **[writing-fragments](./writing-fragments/SKILL.md)**: Grilling session that mines you for fragments (heterogeneous nuggets of writing) and appends them to a single document as raw material for a future article.
- **[writing-shape](./writing-shape/SKILL.md)**: Take a markdown file of raw material and shape it into an article paragraph by paragraph, arguing format choices at each step.
- **[claude-handoff](./claude-handoff/SKILL.md)**: Hand the current conversation off to a fresh background agent that picks up the work immediately, seeded with a handoff summary via `claude --bg`. User-invoked.
- **[setup-ts-deep-modules](./setup-ts-deep-modules/SKILL.md)**: Wire dependency-cruiser into a TypeScript repo so each package is a deep module: implementation hidden in subfolders, reachable only through its entry-point files, tests exercising it through those. User-invoked.
- **[implement-spec](./implement-spec/SKILL.md)**: Implement a whole spec on one branch. Works the tickets as a task graph rather than a list, running implementer subagents across the ready frontier for maximum concurrency, and lands the result as a single PR. User-invoked.
- **[retro](./retro/SKILL.md)**: Suggest improvements to the coding agent's environment (steering files, coding standards, automated checks, tooling) after a session. STUB: design notes only, not functional yet. User-invoked.

Adapted from [pstack](https://github.com/cursor/plugins/tree/main/pstack) by Lauren Tan (MIT; each directory keeps her `LICENSE`):

- **[unslop](./unslop/SKILL.md)**: Remove AI writing patterns from a draft a person will read. Other skills route their prose through it.
- **[technical-writing](./technical-writing/SKILL.md)**: Writing standard for documentation, READMEs, ADRs, PR descriptions, and commit messages. Runs its output through unslop.
- **[blast-radius](./blast-radius/SKILL.md)**: Find what a change could break outside its diff, and prove the one fact it is safe because of by running real code. User-invoked.
- **[create-verification-skill](./create-verification-skill/SKILL.md)**: Generate a project-local `verify-<app>` skill that launches, drives, and captures evidence from the real app, with a feature map. User-invoked.
- **[maintain-verification-skill](./maintain-verification-skill/SKILL.md)**: Keep a verification skill's feature map true to the app: a source pass and a live pass, then at most one PR of proven corrections. User-invoked.
