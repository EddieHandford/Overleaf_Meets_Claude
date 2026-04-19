# Overleaf Meets Claude Code

A practical guide to writing LaTeX documents using **Overleaf** for drafting,
**GitHub** for version control, and **Claude Code** for bulk, structural, and
cross-cutting edits.

The guide itself is a LaTeX document. The repository is structured as a worked
example of the workflow it describes: modular sections under `sections/`, a
`CLAUDE.md` of conventions, and a `.gitignore` for build artefacts.

## Read the guide

- Open `main.tex` in Overleaf (import via **New Project → Import from GitHub**).
- Or build locally:

  ```sh
  latexmk -pdf main.tex
  ```

## Repository layout

```
main.tex              # preamble and \input{} of each section
sections/             # one file per section
  introduction.tex
  why.tex
  setup.tex
  workflow.tex
  strengths.tex
  tips.tex
  pitfalls.tex
  conclusion.tex
references.bib        # bibliography
CLAUDE.md             # conventions for Claude Code sessions
.gitignore            # LaTeX build artefacts
.gitattributes        # better diffs for .tex and .bib
```

## Using this repo as a template

1. Fork or copy the structure.
2. Replace the guide content in `sections/` with your own paper.
3. Edit `CLAUDE.md` to describe your paper's conventions.
4. Link the repo to Overleaf (**Overleaf → Menu → GitHub**, requires Overleaf
   Premium).
5. Clone locally and run `claude` in the project directory.

The full workflow — including setup, the daily loop, and a catalogue of edits
Claude Code is especially good at on a LaTeX project — is in the guide itself.
