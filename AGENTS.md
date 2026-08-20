# Instructions for coding agents

This repository is Forrest Sheldon's public technical site and research notebook.

## Purpose

The site should make technical reasoning easy to follow. Its current structure distinguishes:

1. `virtual-cell/` — a featured research programme covering Virtual Cell Challenge experiments, perturbation modelling, cell-state representations, and model taxonomy.
2. `threads/` — recurring lines of inquiry that connect writing across projects and subject areas.

"Bioinformatics" is not the site's overarching identity. The broader focus is mathematical and statistical reasoning about biological systems, especially inference from noisy, finite, indirect, and high-dimensional measurements. Threads are recurring intellectual questions, not rigid disciplinary categories. Virtual Cell is currently a featured research programme and thread, but should not define the permanent identity of the site.

## Editorial principles

- Organise posts around scientific questions, not diary entries or leaderboard updates.
- Prefer the simplest adequate model and make assumptions explicit.
- State the expected outcome or hypothesis before discussing results when possible.
- Distinguish observations from interpretations.
- Failed experiments are valid results and should not be hidden.
- Preserve Forrest's distinctive technical voice. Do not turn prose into generic corporate or AI-polished writing.
- Preserve distinctive titles and framing. Do not replace memorable titles with generic SEO-style technical titles merely for polish.
- Prefer equations, derivations, figures, and concrete examples over jargon.
- Do not invent experimental results, citations, benchmarks, dates, or claims.
- Do not publish confidential, proprietary, or unpublished employer information. If provenance is unclear, leave a TODO rather than filling it in.
- Public papers, public challenge data, independently written code, and explicitly public prior work are acceptable sources when properly cited.

## Site conventions

- Quarto is the site generator.
- New posts live in a dated subdirectory with an `index.qmd`.
- New posts start with `draft: true` until Forrest explicitly decides to publish.
- Keep computational output frozen unless there is a reason to re-run it.
- Put substantial challenge modelling code in a separate challenge repository and link to it from posts; do not turn this site repository into the research codebase.
- Do not add heavy JavaScript frameworks or unnecessary build dependencies.
- Keep visual design restrained and readable.
- Let the site's taxonomy emerge as writing accumulates; do not create speculative topic hierarchies in advance.

## Private writing workflow

- `ideas/` is an intellectual notebook and writing backlog, not publication-ready prose.
- Preserve wording, uncertainty, incomplete thoughts, and distinctive titles in ideas. Do not rewrite or reorganise them merely for polish.
- Do not convert memorable titles into generic technical titles.
- Do not promote ideas into `drafts/` unless explicitly instructed.
- `drafts/` contains developing article prose. Do not promote drafts into public site sections unless explicitly instructed.
- `ideas/` and `drafts/` must remain excluded from the rendered public website.
- Research questions are first-class objects: an article should often begin with a question rather than a model name.
- Keep the writing process closely connected to actual analysis and experiments.

## Before changing the site

1. Read `_quarto.yml` and the relevant section `index.qmd`.
2. Preserve existing navigation and metadata conventions.
3. Run `quarto render` when the environment supports it.
4. Do not remove `draft: true` without an explicit publication request.
5. If a requested change could expose private research/employer material, stop and flag the exact passage or file.

## Common tasks

### Create a new Virtual Cell draft

Create `virtual-cell/posts/YYYY-MM-DD-short-slug/index.qmd` with:
- a question-led title;
- a one-sentence description;
- an absolute publication date;
- `draft: true`;
- useful categories;
- section headings that reflect the scientific argument.

### Turn an experiment into a post

Use the experiment's actual outputs. Structure the post as:
1. question;
2. model/assumptions;
3. prediction or hypothesis;
4. experiment;
5. result;
6. interpretation;
7. unresolved question.

Do not copy an entire notebook into the post. The blog explains; the research repository reproduces.
