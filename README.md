# Kurdish Businessman — Shipping & Logistics Management (UI prototype)

Trilingual (Kurdish Sorani · Arabic · English) dashboard for managing shipments from China to Iraq/Kurdistan (sea · air · land): shipments, merchants, debts, received warehouse stock, sales, profit reports, operating expenses, fixed assets, salaries, team permissions and PDF reports.

> **Status:** UI test version. All data is sample data kept in the browser (`localStorage`), and the login is simulated. A real database and authentication come in the next phase. **Do not enter real data or real passwords.**

## Languages / stack
| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox, dark mode) |
| Logic | Vanilla JavaScript (no framework, no build step) |
| Libraries (loaded from CDN when exporting PDF) | html2canvas, jsPDF |
| Fonts (Google Fonts) | Source Sans 3, Libre Franklin, IBM Plex Mono, Noto Sans Arabic, Noto Kufi Arabic |

## Structure (flat, all files in the repository root)
```
index.html   page shell, loads the scripts in order
style.css    all styles
i18n.js      translation store
ku.js        Kurdish (Sorani, RTL)
en.js        English (LTR)
ar.js        Arabic (RTL)
data.js      sample reference lists
icons.js     SVG icons
app.js       state, rendering, events, PDF export
logo.png, banner.jpg, login-bg.jpg
```
Script order matters: `i18n → ku/en/ar → data → icons → app`.

## Run locally
Open through a local server (browsers block some features on `file://`):
```
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publish on GitHub Pages
1. Create a repository and upload all these files (keep the folders).
2. Settings → Pages → Source: **Deploy from a branch** → `main` / `(root)` → Save.
3. After a minute the site is live at `https://<user>.github.io/<repo>/`.

## Demo accounts
Use the buttons on the login page (manager and admins). Password for all: `demo1234`.
Data is stored in the browser under the key `kb-logistics-v1`; clear site data to reset.
