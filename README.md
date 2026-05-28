# Mav-Tracker (JMCR Travel Checklist)

A collaborative packing and trip preparation web app for Ryan Nguyen's travel team — Jon, Mary, Cordelia, and Maverick.

---

## What It Does

A shared checklist app designed around Ryan's medical needs during travel. Multiple family members can pack simultaneously, each checking off items under their own color-coded stamp. Items sink to the bottom when checked, keeping the active list clean and focused.

---

## Users

| Name | Color | Role |
|---|---|---|
| Jon | Teal | |
| Mary | Blue | |
| Cordelia (Cordy) | Pink/Rose | |
| Maverick (Mav) | Coral | |
| Ryan | Amber | |

Each user selects themselves from the toolbar before checking items. Their initial stamps automatically on every item they pack.

---

## Categories / Tabs

| Tab | Description |
|---|---|
| 🎒 Ryan's Backpack | Carry-on items always with Ryan: Valtoco, O2 monitor, emergency meds, suction |
| 💊 Medications | All Rx and OTC medications |
| 🏥 Medical Equipment | Ventilator, nebulizer, iStat, formula pump, oxygen generator, etc. |
| 👤 Personal Items | Clothing, toiletries, accessories — one sub-list per person |

---

## Key Features

- **Collaborative** — multiple users pack simultaneously; each item shows who checked it
- **Check / Skip** — checked items sink to the bottom with user stamp; skipped items are visually distinct (not just unchecked)
- **Drag & drop** — reorder items within a category
- **Bidirectional arrows** — move items up/down within their category
- **Edit categories and items** — rename, add, remove
- **Progress bar** — tracks Ryan's pack progress (Backpack + Meds + Equipment + Personal Items only; ignores other users' personal lists)
- **"New Trip" reset** — clears all checks and skips; items return to original order; nothing is deleted

---

## Design Theme

Ocean / beach / vacation — sandy tones, teal and coral accents, wave-inspired dividers.

---

## Technical Stack

| Component | Details |
|---|---|
| Frontend | Single-file HTML/CSS/JS (no framework) |
| Backend | Google Apps Script + Google Sheets |
| Hosting | Google Apps Script Web App |
| Data | Google Sheets (items, checks, user stamps, settings) |
| Icons | Tabler Icons |

### Google Sheets Structure
- **Items** — all checklist items with category, order, text, checked status, skip status, user stamp
- **Settings** — user names, active user, current trip metadata

---

## How to Use

1. Open the app link in Safari (or any browser)
2. Select your name from the toolbar ("As: Jon / Mary / Cordy / Mav")
3. Tap the tab for your assigned category
4. Check items as you pack — your initial stamps automatically
5. Use **Skip** for items intentionally left out this trip
6. When the trip is done, tap **New Trip** to reset all checks for the next trip

---

## How to Update / Redeploy

1. Open the Google Apps Script editor for the project
2. Edit `Code.gs` or `Index.html`
3. Click **Deploy** → **Manage deployments** → pencil icon → **New version** → **Deploy**
4. Hard refresh the app URL

---

## Notes

- The progress bar counts only Ryan's four core categories — not Jon/Mary/Cordy/Mav personal lists
- Checked items physically move to the bottom of their category; unchecking restores them to their original position
- "New Trip" restores original item order across all categories
- User names are editable in-app via the pencil icon on the toolbar

---

*Built for Ryan Nguyen's travel team — Jon, Mary, Cordy & Mav*
