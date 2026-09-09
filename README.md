# Med Spa Market Intelligence — 11-Metro Project

Static market research reports for the U.S. med spa industry across 11 metros: New York (Manhattan), Charlotte, Atlanta, Miami, West Palm Beach, Orlando, Dallas, Houston, Austin, Hudson & Bergen Co., NJ (the NJ towns closest to Manhattan), and Premium Upstate NY (Hudson Valley, Westchester, and Saratoga/Finger Lakes).

No build step. No framework. Every page is a single self-contained HTML file (all CSS and JS inline), except for the Chart.js CDN script and Google Fonts, which load from public CDNs.

## Contents

- `index.html` — redirects to the hub (`Med_Spa_Multi_City_Hub.html`), so the deployed site's root URL loads the right page automatically.
- `Med_Spa_Multi_City_Hub.html` — the national hub page. Aggregates clinic supply, pricing transparency, and Google Trends search-interest data across all 11 metros, with click-to-expand clinic breakdowns, a metro comparison table, an Industry Reference section (regulation, unit economics, software, procedures, membership models), and an embedded audience-research report (YouGov + Similarweb data). Start here.
- `Manhattan_Med_Spa_Market_Report.html`, `Charlotte_Med_Spa_Market_Report.html`, `Atlanta_Med_Spa_Market_Report.html`, `Miami_Med_Spa_Market_Report.html`, `West_Palm_Beach_Med_Spa_Market_Report.html`, `Orlando_Med_Spa_Market_Report.html`, `Dallas_Med_Spa_Market_Report.html`, `Houston_Med_Spa_Market_Report.html`, `Austin_Med_Spa_Market_Report.html`, `NJ_Metro_Med_Spa_Market_Report.html`, `Upstate_NY_Med_Spa_Market_Report.html` — full standalone per-metro reports (clinic-by-clinic pricing breakdowns, procedure category stats, live Google Trends charts). The hub links directly to each of these by filename, so keep them all in the same folder/deploy as the hub page.
- `*_Med_Spa_Procedures.xlsx` — the underlying research workbooks per metro (clinic overview, all logged procedures/pricing, dashboard formulas, notes). Not needed for the deployed site — only relevant if you want the raw data.
- `Multi_City_Progress_Tracker.md` — project log describing how each metro's research was conducted and every change made along the way.
- `vercel.json` — minimal static-site config (tells Vercel there's no framework to detect).

## Deploying

### GitHub Pages

1. Push this folder's contents to a repo (see "Pushing to GitHub" below if it isn't a repo yet).
2. In the repo's Settings → Pages, set the source to the branch/root you pushed.
3. Your site will be live at `https://<user>.github.io/<repo>/` — `index.html` at the root redirects straight to the hub.

### Vercel

1. Push this folder to a GitHub repo (Vercel deploys from a git remote — see below).
2. At vercel.com, "Add New… → Project", import the repo. Leave the framework preset as "Other"/none — `vercel.json` already tells Vercel there's no build step.
3. Deploy. The root URL serves `index.html`, which redirects to the hub.

Alternatively, deploy this folder directly without GitHub using the Vercel CLI from inside it:

```
npx vercel --prod
```

### Pushing to GitHub

This folder is already a git repo with an initial commit (see below). To push it:

```
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

(Create the empty repo on GitHub first, without a README/license/gitignore, so the push doesn't conflict.)

No other configuration is required — every report is self-contained and there's nothing to build.
