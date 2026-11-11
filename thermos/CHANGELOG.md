# Changelog

## 2.0.0

- **Breaking:** Thermos is now a Claude Code plugin only. The Cursor manifest (`.cursor-plugin/plugin.json`) and the Cursor marketplace entry are removed; the plugin is defined by `.claude-plugin/plugin.json` and listed in `.claude-plugin/marketplace.json`.
- **Breaking:** `thermo-nuclear-review` and `thermo-nuclear-code-quality-review` are no longer slash commands (`user-invocable: false`). They drop `disable-model-invocation`, so the subagents can preload them through their `skills:` frontmatter, and Claude can use them directly.
- Skills and agents use Claude Code names: `thermos:`-scoped agent and skill names, the Agent tool (was `Task`), and the `Explore` subagent instead of Cursor's `shell`/`explore` types. `run_in_background` is gone; subagents launched together already run in parallel in the background.
- PR-discussion checks cover any review bot (for example Claude Code Review, BugBot, CodeRabbit) or human reviewer, not only BugBot.
- README rewritten for Claude Code installation and usage.

## 1.0.0

- Initial Thermos plugin release.
- Skills: `thermo-nuclear-review`, `thermo-nuclear-code-quality-review`, `thermos`.
- Agents: `thermo-nuclear-review-subagent`, `thermo-nuclear-code-quality-review-subagent`.
- Architecture diagram embedded as a mermaid block in README.
