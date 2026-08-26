# Med Spa Market Intelligence — 9-Metro Project

Static market research reports for the U.S. med spa industry across 9 metros: New York (Manhattan), Charlotte, Atlanta, Miami, West Palm Beach, Orlando, Dallas, Houston, and Austin.

## Contents

- `Med_Spa_Multi_City_Hub.html` — the national hub page. Aggregates clinic supply, pricing transparency, and Google Trends search-interest data across all 9 metros, with click-to-expand clinic breakdowns, a metro comparison table, and an Industry Reference section (regulation, unit economics, software, procedures, membership models). Start here.
- `Manhattan_Med_Spa_Market_Report.html`, `Charlotte_Med_Spa_Market_Report.html`, `Atlanta_Med_Spa_Market_Report.html`, `Miami_Med_Spa_Market_Report.html`, `West_Palm_Beach_Med_Spa_Market_Report.html`, `Orlando_Med_Spa_Market_Report.html`, `Dallas_Med_Spa_Market_Report.html`, `Houston_Med_Spa_Market_Report.html`, `Austin_Med_Spa_Market_Report.html` — full standalone per-metro reports (clinic-by-clinic pricing breakdowns, procedure category stats, live Google Trends charts). The hub links directly to each of these by filename, so keep them in the same folder as the hub page.
- `*_Med_Spa_Procedures.xlsx` — the underlying research workbooks per metro (clinic overview, all logged procedures/pricing, dashboard formulas, notes).
- `Multi_City_Progress_Tracker.md` — project log describing how each metro's research was conducted and every change made along the way.

## Hosting on GitHub Pages

All HTML files are self-contained (no build step, no external assets besides the Chart.js CDN script). To publish:

1. Push this folder's contents to a repo.
2. In the repo settings, enable GitHub Pages for the branch/root you pushed to.
3. Open `Med_Spa_Multi_City_Hub.html` at your Pages URL (or rename it to `index.html` if you want it to load at the site root).

No other configuration is required.
