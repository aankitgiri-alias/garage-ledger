# Garage OS v2.1

Static GitHub Pages-ready garage showroom + maintenance console.

## New in v2.1

- WhatsApp chat export ingestion (`.txt`, export without media)
- Local in-browser parsing; chat content is not uploaded by the site
- Heuristic detection of:
  - rides / trips
  - fuel / CNG / diesel / petrol entries
  - service activity
  - repair / issue notes
  - compliance notes such as PUC / insurance
  - care / cleaning notes
- Vehicle auto-detection for known garage vehicles
- Optional sender filter and default vehicle mapping
- Preview before applying
- Local browser journal storage using `localStorage`
- CSV export for later import into Google Sheets / the master ledger

## Important limitation

Because GitHub Pages is a static host, the page cannot securely write directly into a private Google Sheet by itself. v2.1 therefore parses locally and exports structured CSV. A later version can add a small authenticated Google Apps Script endpoint so approved imports can update the live sheet with one click.

## Deploy

Upload `index.html` and the `assets/` folder to the GitHub Pages repository root, commit, and push.
