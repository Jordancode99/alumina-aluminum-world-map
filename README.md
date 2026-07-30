# Global Alumina & Aluminum Asset Map — updateable version

## What changed

- Current facility status is grouped into **Operational**, **Not operating yet**, **Offline / shut down**, and **Needs review**.
- The original detailed status remains visible for restart, ramp-up, expansion, idle, closure, and construction cases.
- Current status is dated **30 July 2026** and is kept separate from the selected annual production/capacity year.
- The website includes a browser-based data update manager, CSV import/export, and an exportable `assets-data.js` publication file.
- Facility selection is organized by country: choose a country first, then select from the facilities available in that country.

## Files

- `index.html` — public map interface.
- `assets-data.js` — all facility data and the status as-of date. This is the only file that normally needs replacement when publishing routine updates.
- `facility-update-template-2026.csv` — editable update sheet with one row per facility for 2026.

## Updating production or operating status without coding

1. Open `index.html` through the hosted public site or a local web server.
2. Click **Data updates**.
3. Either edit one facility directly or download the selected-year update CSV.
4. Edit `production_kt`, `capacity_kt`, `operating_capacity_kt`, `current_operating_state`, `detailed_status`, `status_note`, and `status_as_of` as needed.
5. Import the CSV. The map updates immediately in that browser.
6. Click **Export assets-data.js**.
7. Replace the existing `assets-data.js` on GitHub Pages, Netlify, Cloudflare Pages, Vercel, or another static host. The public map updates after redeployment.

Browser edits are local drafts only. They do not change what other visitors see until the exported `assets-data.js` is uploaded to the public host.

## Operating-state rules used for the initial classification

- **Operational:** Operating; Restarting / restarted; Expansion; Included in parent site; ramp-up (`爬产中`).
- **Not operating yet:** Planned; Planned / under construction.
- **Offline / shut down:** Shut down; No active capacity; Idle / no production.
- **Needs review:** Unknown or unclear source status.

These classifications follow the uploaded workbooks. They are not an independent real-time verification of every facility.
