# CLAUDE.md

Conventions for any Claude Code session working in this repository.

## What this repo is

A LaTeX guide describing a workflow that combines Overleaf, GitHub, and Claude
Code for writing academic papers. The repository is deliberately structured as
a worked example of that workflow, so patterns here (modular `\input`,
`.gitignore`, this very file) should be kept representative.

## File layout

- `main.tex` — preamble and `\input{sections/...}` of each section. Do not put
  prose here; keep it a thin shell.
- `sections/*.tex` — one file per section of the guide.
- `references.bib` — bibliography (small; used for a citation example).
- `README.md` — one-paragraph pointer to `main.tex`.

## Style

- British English ("colour", "organise", "centre").
- Second person for instructions to the reader ("you", not "we" or "one").
- Present tense for descriptions; imperative for steps.
- Oxford comma; en-dash for ranges; em-dash for asides without surrounding
  spaces.
- Defined terms italicised on first use, roman afterwards.
- Keep sentences short. Prefer concrete verbs over abstract nouns.

## LaTeX conventions

- `\citet{}` when the author is a grammatical subject ("Smith et al. (2023)
  showed…"); `\citep{}` when parenthetical. Every `\cite` key must exist in
  `references.bib`; never invent keys.
- Use the existing `tipbox` and `pitfallbox` environments for callouts rather
  than inventing new ones.
- Use the existing `shell`, `prompt`, and `tex` listings styles rather than
  ad-hoc formatting.
- Use `booktabs` rules (`\toprule`, `\midrule`, `\bottomrule`); no vertical
  rules.
- Prefer `\texttt{}` for inline code in prose and `lstlisting` for blocks.

## Do not commit

Build artefacts: `*.aux`, `*.log`, `*.out`, `*.toc`, `*.bbl`, `*.blg`, `*.fls`,
`*.fdb_latexmk`, `*.synctex.gz`, and compiled PDFs. These are covered by
`.gitignore`; keep them there.

## Commit style

- Imperative mood, ≤ 72 characters for the subject line.
- Describe the *why*, not the *what* (the diff shows the what).
- Example: `Tighten intro to fit 400-word limit requested by R1`.
- One logical change per commit.

## When editing

- Make the smallest diff that achieves the request. Do not reflow entire
  paragraphs unless asked.
- If asked to do something global, produce a plan or a report first; wait for
  approval before writing.
- When adding a new section, add it both as a `sections/<name>.tex` file and as
  an `\input{sections/<name>}` in `main.tex`, in the intended reading order.
