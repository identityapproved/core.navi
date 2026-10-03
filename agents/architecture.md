# Architecture

A flat collection of navi cheatsheets. There is no build step, no code, and no
dependency graph.

## Layout

- `*.cheat` at the repository root: one file per topic (`disk`, `incus`,
  `media`, `netspeed`, `portage`, `taskwarrior`, `virsh`, `wayland`).
- `README.md`: repository purpose.
- `agents/`: this file and `rules.md`, nothing else.
- `.githooks/pre-commit`: path sanitizer.

## Install path

The repository is consumed in place through a symlink:

    ~/.local/share/navi/cheats/core.navi -> ~/github/core.navi

Edits to a `.cheat` file are live for `navi` immediately; nothing is copied or
generated.

## Cheat file format

- `% tag, tag, tag` header declares the cheatsheet tags.
- `# comment` lines describe the snippet that follows.
- A snippet is one shell line; `<var>` placeholders are resolved by `navi`.
- `$ var: <command>` lines supply value suggestions for a placeholder.

## Validation

`navi --query <tag>` or `navi fn widget::<shell>` is the only practical check;
there is no test suite or linter.
