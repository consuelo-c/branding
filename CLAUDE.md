# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

The brand of Banquetes Consuelo C (`consuelo-c/branding`): logo, colors, font, voice and message rules. No code, no build, no tests. It knows nothing about the projects that use it: they copy values from here, never the other way around. Don't name or reference any consuming project in this repository's files.

A brand change happens here first, then gets copied into each project by hand.

## How the pieces relate

- `README.md` holds the rules, in Spanish (Colombian, «tú», no exclamation marks — the same voice it describes). It is the human-facing spec.
- `tokens.json` holds the values (colors, type family and weights, radii), each with an English `usage` note.
- The README repeats many hex values and radii inline (Color, Mensajes table, Forma). **A change to a value in `tokens.json` must be mirrored in the README, and vice versa.** Grep for the old hex before finishing.
- Layouts, components, sizes and spacing are deliberately absent: they belong to each consuming project. Don't add them here.

## Logo files

- `assets/source/` holds the originals as delivered (`fill="black"`, with a C2PA metadata block). Never edit or redraw them.
- Every other file in `assets/` is the same paths with only the fill swapped:
  - `logo.svg`, `c-logo.svg`: `fill="currentColor"`, metadata stripped
  - `*-ink.svg`: `#333333`; `*-white.svg`: `#FFFFFF` (metadata kept)
- The `fill="white"` inside the wordmark files belongs to the clip path, not the logo color; leave it.
- To regenerate a variant, copy the source file and replace only the `fill="black"` attributes.

## Checks

Markdown is linted with markdownlint (`.markdownlint.json` disables line-length and ol-prefix) and spell-checked with cspell in Spanish and English:

```sh
npx cspell README.md CLAUDE.md
```

The Spanish dictionary comes from `@cspell/dict-es-es`. Add legitimate brand or domain words to `words` in `cspell.json`.
