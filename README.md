# Forrest Sheldon — research site

Quarto source for a public research notebook focused on mathematical and statistical reasoning about biological systems, including virtual cells, perturbation modelling, and inference from noisy, high-dimensional measurements.

The site separates published writing from recurring threads of inquiry. Virtual Cell remains a featured research programme without defining the site's permanent scope.

## Local preview

Install [Pixi](https://pixi.prefix.dev/), then from the repository root:

```bash
pixi run preview
```

To render the production site:

```bash
pixi run render
```

To validate the complete build using the locked environment:

```bash
pixi run validate
```

Pixi installs the pinned Quarto toolchain from `pixi.lock`. The local environment lives in `.pixi/`; rendered output goes to `_site/`. Both directories are ignored by git.

## Publishing

`.github/workflows/pages.yml` renders the site and deploys `_site/` to GitHub Pages on pushes to `main`.

After creating the GitHub repository:

1. Push this project to `main`.
2. In **Settings → Pages**, set the publishing source to **GitHub Actions**.
3. Run the `Deploy Quarto site to Pages` workflow, or push a commit to `main`.
4. Add a custom domain later in **Settings → Pages** if desired.

## Draft workflow

Posts begin with:

```yaml
draft: true
```

They remain visible during `quarto preview` but are excluded from the published listings/site. Remove `draft: true` only when the article is ready to publish.

## Recommended repository split

Keep this repository focused on communication. The Virtual Cell Challenge analysis belongs in a separate repository with its own scientific environment. This site should consume figures, tables, and results from research projects rather than depending on their full software stacks.
