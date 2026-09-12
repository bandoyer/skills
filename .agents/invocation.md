# Invocation and dependencies

Preserve each skill's existing invocation policy unless changing it is part of the user's request.

- User-invoked skills have `disable-model-invocation: true` for Claude Code and `policy.allow_implicit_invocation: false` in `agents/openai.yaml` for Codex.
- Model-invoked skills omit those restrictions. Their descriptions should state the narrow capability and when it applies, without long trigger lists.
- Keep `interface.display_name`, `interface.short_description`, and the two harness policies consistent. The README lists distinguish the two groups.

An explicit-only workflow is chosen by the user, not silently invoked by another skill. Router prose can recommend it without executing it. Do not treat a dependency reference as permission to expand task scope or start a paid session.

For a needed model-invoked dependency, use the available skill tool, one skill per call. If no such tool exists, read its `SKILL.md` and the relevant reference directly. A harness-specific tool name is not a prerequisite for reading Markdown. Do not reload material already available.

Reading a glossary for vocabulary does not require an active `domain-modeling` workflow. Use that skill when the task includes developing terminology or recording domain decisions.
