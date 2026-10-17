# Pokemon Crystal News Maker — REON fork

RGBDS source and tools for assembling Pokemon News editions for Crystal.
The original assembly sources, localized game text and directory layout are
preserved. This fork corrects malformed Italian text literals and Spanish
personality-quiz page text that otherwise prevent or corrupt assembly.

## Source and build entry points

- Monthly `2002_*_issue.asm` sources and `minigame/` define editions and games.
- `pokecrystal/`, `macros/` and `ranking_types.asm` supply shared assembly data.
- `Makefile` has regional targets `j`, `e`, `d`, `f`, `i`, `s`; it uses RGBDS,
  Python 3 and `newschecksum.py`, writing generated editions under `bin/2002/`.
- `note/` retains original minigame reference material, not a second changelog.

Review toolchain assumptions in the Makefile before building. REON's web editor
and scheduling integration live in the server repository, not in this tool.
Do not infer emulator or hardware validation from source-level assembly fixes.

The fork uses `master` as its baseline (no `main` exists). The
[integrated changelog](https://github.com/zenaror/reon/blob/feature/full_server/docs/CHANGELOG.md#pokemon-news-maker)
records its final changes. Workspace contributor instructions apply; preserve
original game-language strings and human/upstream credits.
