# Project Agent Instructions

These instructions refine the global OpenCode policy for this repository.

## Workflow

- Inspect the repository, current branch, worktree, and existing instructions before editing.
- Preserve unrelated work and prefer minimal, targeted changes.
- Discover and run the repository's documented validation commands before declaring work complete.
- Do not create, switch, merge, or push branches unless the user requests it.
- Work happens on `main`; there are no topic branches.

## Project Context

- Architecture and cheat file format: `agents/architecture.md`
- Repository-specific rules: `agents/rules.md`

Read the relevant supporting file before changing behavior it describes. When
the user says `update memory`, update whichever of `AGENTS.md`,
`agents/architecture.md`, and `agents/rules.md` the change affects, then stage
or commit only when requested.

## Path Hygiene

- Use relative paths when practical and `~` or `$HOME` for home paths.
- Data stores live under `$HOME`. Write their paths as `~` or `$HOME`.
- Check changed files for username-bearing paths and secrets before sharing or staging.
