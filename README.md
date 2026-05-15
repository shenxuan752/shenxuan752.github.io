# Portfolio Site

Personal portfolio: products I've built and analyses I've written.

Built with [Quarto](https://quarto.org). Deployed to GitHub Pages.

## Local development

```bash
# Install Quarto (one-time)
brew install --cask quarto

# Preview locally
quarto preview
```

Visit `http://localhost:3000` (or whatever port Quarto reports).

## Deploy

Pushes to `main` automatically build and deploy to GitHub Pages via the workflow in `.github/workflows/publish.yml`.

## Structure

```
portfolio/
├── _quarto.yml                    # Site config
├── index.qmd                      # Home page
├── about.qmd                      # About page
├── styles.css                     # Custom styles
├── profile.jpg                    # ADD: 400x400+ headshot
│
├── products/                      # Tools, pipelines, agents I've built
│   ├── index.qmd                  # Auto-listing of all products
│   ├── startup-screener-pipeline.qmd
│   ├── ma-trading-strategy.qmd
│   └── news-aggregator.qmd
│
└── analyses/                      # Decision write-ups
    ├── index.qmd                  # Auto-listing of all analyses
    ├── ai-startup-landscape.qmd
    ├── nyc-cannabis-market.qmd
    └── ma-trading-backtest.qmd
```

## Adding a new project

1. Decide if it's a **product** (a tool/system) or an **analysis** (a decision write-up)
2. Create `products/[name].qmd` or `analyses/[name].qmd`
3. Use the YAML front matter pattern from existing pages (title, subtitle, date, categories, image)
4. The index page for each section auto-discovers new files

## Things to fill in before launch

- [ ] Replace `YOUR-USERNAME` in `_quarto.yml`, `index.qmd`, `about.qmd`
- [ ] Replace `YOUR-LINKEDIN` everywhere
- [ ] Add `profile.jpg` (square headshot, 400x400+)
- [ ] Fill in `[REPLACE]` markers in `about.qmd`
- [ ] Fill in case-study content for each project page
- [ ] Add thumbnail images (`thumb-*.png`) for each project, or remove the `image:` field
