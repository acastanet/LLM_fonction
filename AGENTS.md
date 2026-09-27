# Repository Guidelines

## Project Structure & Content

This repository contains a French editorial series about how large language models work; it has no application source code. The first four reference manuscripts and their topic materials live in `1 _Matrice/`, `2_Traitement/`, `3_Qui parle/`, and `4_Alignement/`. Identically named article copies also exist at the repository root; keep each pair synchronized when editing. The new `5_Grokking/` folder contains `grokking_generalisation_modifie.md` and PNG illustrations about grokking and generalization. Series decisions, the roadmap, progress, source checks, and writing guidance are in the root-level Markdown files. `planches/` and `Présentation/` hold visual and presentation assets. Preserve accents and spaces in existing paths.

## Editorial and Writing Conventions

**Mandatory:** Read and apply `styleCVGZ.md` before drafting or revising any article text, including openings, transitions, and conclusions. Check every edit against its voice, rhythm, structure, and vocabulary guidance.

`AnSu/` contains PDF references: a project overview, a theoretical paper, and practical MVP guidance. Use them to ground educational examples. Distinguish AnSu from its Agent naïf use case, and proposed benefits from measured outcomes. The theoretical paper describes prompt v7; the September practical guide discusses v7.5.

Write article content in French for readers without specialist technical knowledge. Follow `GUIDE_REDACTION_SERIE_RECHERCHES_LLM.md` to finalize the five existing manuscripts: retain their titles, examples, and main content; prioritize order, transitions, and limited edits. The intended reading order is article 1, article 2, grokking, article 3, article 4. `DECISIONS_EDITORIALES_SERIE.md` remains useful where compatible with this extension. Consult `styleCVGZ.md` for voice. Distinguish metaphor from mechanism and cite checkable sources. Use descriptive lowercase filenames with underscores for articles (for example, `article_02_un_modele_continue.md`); keep related figures beside their article and use relative links. Update references when renaming assets.

## Development and Validation

There is no build system or automated test suite. Before submitting edits, inspect `git diff --check`, confirm Markdown image and source links resolve, and preview changed Markdown or SVGs. If Pandoc is installed, a Markdown syntax/render check can use:

```powershell
pandoc .\article_01_comment_le_texte_arrive.md -f markdown -t html | Out-Null
```

For diagrams, preserve the series’ shared visual style and verify the rendered output after editing; do not rely on XML validity alone.

## Commits and Pull Requests

The available history contains only `Initial commit`, so no established commit convention can be inferred. Use a short imperative subject that names the change, such as `Clarify article 2 transition`. A pull request should summarize editorial or visual changes, list affected manuscripts and assets, explain factual/source updates, and include before/after images for substantial visual revisions. Link a related issue when one exists.
