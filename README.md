# Tronics Field Assist

Videojet service management app for Tronics field technicians and customer service.

## Setup

1. Edit `config.js` — paste your Anthropic API key
2. Push to GitHub
3. Enable GitHub Pages: Settings → Pages → Branch: main → / (root)
4. Access at `https://YOUR-USERNAME.github.io/REPO-NAME`

## Files

| File | Purpose | Update frequency |
|------|---------|-----------------|
| `index.html` | App code | When features change |
| `data.js` | SAP data (customers, equipment, inventory, techs) | Periodically refresh from SAP |
| `config.js` | API key + app settings | Rarely |

## Updating data

Export fresh CSVs from SAP B1, run the Python script (ask Anthony), replace `data.js`, push to GitHub — Pages redeploys automatically.

## Logins

All users: PIN `1234` (change in `config.js` per user before go-live)

## Architecture

Phase 1 (current): Static files on GitHub Pages, tickets in-memory (reset on refresh)  
Phase 2: Supabase for ticket persistence  
Phase 3: HubSpot integration  
Phase 4: SAP B1 Service Layer live data  
