# trade-tools-site (public)

The storefront and SEO surface, served by GitHub Pages.

**This repo is public on purpose** — GitHub Pages requires it on a free account,
and it means the agent can read the live site with no credential at all. Nothing
sensitive belongs here: no ledger, no product source, no keys.

## Layout

```
index.html                     landing page, one card per live calculator
assets/style.css               shared styles, light + dark
calculators/<slug>/index.html  one self-contained calculator per folder
```

## Conventions

- Each calculator is a single self-contained HTML file. No build step, no framework, no dependencies.
- **No tracking scripts and no third-party requests.** The footer promises nothing leaves the browser; that promise has to stay true.
- Every page states it is a planning tool, not financial advice.
- The paid workbook is one clearly-marked link at the bottom, after the math has already been given away. The calculator is not a teaser.

## Adding a calculator

1. Copy an existing folder under `calculators/`, rename it to the new slug
2. Replace the inputs, the calculation, and the "How this is calculated" section
3. Verify the math independently before publishing — a wrong calculator is worse than no calculator
4. Add a card to `index.html`

## Deploy

Push to `main`. Pages redeploys in about a minute.
