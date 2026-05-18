# AI Jobs Dashboard

Interactive Next.js dashboard for the DSA 210 term project
**"AI and the Future of Entry-Level Jobs: Are Recent Graduates at Risk?"**

It reads the cleaned dataset (`../data/ai_jobs_market_cleaned.xls`, which is actually
a CSV) at build time, ships it as a static JSON asset, and renders an interactive
dashboard with filters, KPIs, and charts. The hypothesis-test numbers and ML
metrics are surfaced as cards using the values reported in the notebooks.

## Stack

- Next.js 15 (App Router) + React 18 + TypeScript
- Tailwind CSS
- Recharts (all charts re-rendered in the browser — fully interactive)

## Local development

```bash
cd web
npm install
npm run dev          # http://localhost:3000
```

`npm run dev` and `npm run build` both regenerate `public/data/jobs.json`
automatically from `../data/ai_jobs_market_cleaned.xls` via the
`predev` / `prebuild` hooks (see `scripts/build-data.mjs`).

If you re-run the notebooks and rewrite the CSV, just re-run `npm run dev`
(or `npm run data`) and the site picks up the new data.

## Deploying to Vercel

The app lives inside the `web/` subdirectory of this repo. When you import the
repository into Vercel, set:

- **Root Directory:** `web`
- **Framework Preset:** Next.js (auto-detected)
- **Build Command:** `npm run build` (default)
- **Output Directory:** (leave blank — Next.js handles this)

No environment variables are needed. The dataset is bundled as a static asset
under `/data/jobs.json`.

Alternatively, from the CLI:

```bash
npm i -g vercel
vercel --cwd web
```

## Project layout

```
web/
  scripts/build-data.mjs        # CSV -> JSON build step
  public/data/jobs.json         # generated, ~666 KB
  src/
    app/
      layout.tsx
      page.tsx                  # the dashboard
      globals.css
    components/
      FilterBar.tsx
      KPIs.tsx
      Findings.tsx              # H1 / H2 / H3 cards
      MLResults.tsx             # classification + regression tables
      charts/                   # Recharts wrappers
    lib/
      data.ts                   # useJobs() client hook
      filter.ts                 # applyFilters()
      stats.ts                  # aggregations used by the charts
      types.ts
```
