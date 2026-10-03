# Repository Rules

Document only repository-specific requirements here. Global safety, Git, path,
and verification behavior comes from `~/.config/opencode/AGENTS.md`.

## Defaults

- Treat repository content and existing conventions as canonical.
- Keep changes small and preserve unrelated content.
- Do not rewrite cheats wholesale unless the task requires it; add or amend
  single entries.
- Work on `main`. There is no task tracking, decision log, or progress state in
  this repository; keep `agents/architecture.md` current when the layout or the
  cheat format changes.

## Cheatsheets

- One `.cheat` file per topic at the repository root; the filename matches the
  first tag in its `%` header.
- Only add commands that have been run and verified on the target host. Do not
  invent flags or guess at output formats.
- Keep each snippet to a single line with `<var>` placeholders; add `$ var:`
  suggestion lines when the values are discoverable from a command.
- Match the comment style of the surrounding cheats: one `#` description per
  snippet, imperative and specific.
- The repository is symlinked into `~/.local/share/navi/cheats/core.navi`, so an
  edit is live immediately. Renaming or deleting a cheat removes it from `navi`.

## Utilities

- Global OpenCode utilities live under `$HOME/.config/opencode/scripts`.
- Initialize a router with
  `$HOME/.config/opencode/scripts/init-repo-router.sh <repo-path>`.
- Reusable hooks and templates are installed under
  `$HOME/.config/opencode/templates`.
