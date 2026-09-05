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

- Quarto is the site generator, managed through Pixi. Use `pixi run` tasks rather than calling `quarto` directly.
- Every post is a subdirectory containing an `index.qmd`.
- Unpublished posts live in `draftN-short-slug/` and carry no `date:` field. Do not add dates or rename them to dated slugs while they are drafts; see "Draft lifecycle" below.
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

## Draft lifecycle

Posts are numbered while unpublished and dated only at publication.

- **Drafting.** The directory is `draftN-short-slug/` and the front matter has `draft: true` and no `date:`. With dates absent, Quarto's listings fall back to filename order, so `draft1 … draftN` is the reading order. Renumber directories to reorder the sequence.
- **Previewing.** Quarto's default `draft-mode` emits a 90-byte empty stub for any `draft: true` post, so drafts are invisible in an ordinary `pixi run preview` and are *not* readable on the deployed site. Use `pixi run drafts`, which sets `QUARTO_PROFILE=drafts` and picks up `_quarto-drafts.yml` (`draft-mode: visible`) to render and list drafts in full. CI never sets that variable.
- **Publishing.** Only on an explicit request from Forrest, and as one gesture: rename `draftN-short-slug/` to `YYYY-MM-DD-short-slug/`, add the absolute `date:`, and delete the `draft: true` line. The directory name becomes the permanent URL, so it is fixed from that point on.

Because drafts publish as empty stubs, an unfinished post in the repository is not a disclosure risk. The editorial rules about confidential material still apply to what gets written.

## Before changing the site

1. Read `_quarto.yml` and the relevant section `index.qmd`.
2. Preserve existing navigation and metadata conventions.
3. Run `pixi run validate` when the environment supports it. This is the same command CI runs.
4. Do not remove `draft: true` without an explicit publication request.
5. If a requested change could expose private research/employer material, stop and flag the exact passage or file.

## Common tasks

### Create a new Virtual Cell draft

Create `virtual-cell/posts/draftN-short-slug/index.qmd`, where `N` is the next number in the intended reading order, with:
- a question-led title;
- a one-sentence description;
- `draft: true`;
- useful categories;
- section headings that reflect the scientific argument.

Do not add a `date:` field. Author, TOC, freeze, and the `Virtual Cell` category are inherited from `virtual-cell/posts/_metadata.yml`; do not repeat them. Nothing needs registering elsewhere — `virtual-cell/index.qmd` and `posts.qmd` glob the post directories.

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

## Working together

- Come to Forrest to think problems through carefully when decisions present themselves. Always aim to understand a problem fully before proposing solutions.
- Name the options and the tradeoff rather than silently resolving a genuine editorial, modelling, or statistical choice.
