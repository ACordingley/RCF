# Hawthorne Live - Brisbane Bar Whyte Island

Live professional tide, weather, wind, storm & lightning dashboard - single file, no build.

**Features**
- First column: MSN weather + Open-Meteo live current (temp, feels like, humidity, pressure, wind knots, precip, UV, visibility, sunrise/sunset, moonrise/moonset, moon phase)
- Wind gauge knots visual 140px compass red needle 26px cyan
- Middle: Brisbane Bar Whyte Island Live Tide Station 046046A -27.381 153.182 QLD TMR + marine-api open-meteo direct CORS live, tidal flow, WillyWeather fancy tide 120px canvas, Storm Risk & Lightning Risk visually standout hero gradients
- Right: Windy rain radar loop only iframe sandboxed isolated no glitch, 15m separate refresh

**Live & CORS-fixed**
- Core data uses direct CORS-allowed APIs: api.open-meteo.com, marine-api.open-meteo.com (no proxy)
- MSN + QLD TMR via 3-tier proxy chain: direct -> api.allorigins.win -> corsproxy.io -> codetabs - optional, fallback to direct live
- No simulated data - all cards turn RED border 3px #ef4444 bg #fef2f2 with ⚠️ STALE if not pulling fresh (15min threshold)

**GitHub Pages deploy**
1. Create repo e.g. hawthorne-live
2. Upload all files from this folder to root (index.html must be at root)
3. Settings -> Pages -> Source: Deploy from a branch -> main / root -> Save
4. Live at https://YOURUSERNAME.github.io/hawthorne-live/ in 1-2 min

**Local test**
Just open index.html via https (not file:// for Windy iframe). Use VSCode Live Server or `npx serve .`

**Structure**
- index.html - single-file app (React bundled, no external deps except CDN tailwind/lucide)
- .nojekyll - bypass Jekyll
- README.md - this file
- CNAME optional

**Coords**
- Hawthorne weather -27.459 153.069
- Whyte Island tide gauge -27.381 153.182 Station 046046A Chart Datum LAT QLD TMR
- Radar Windy -27.459 153.069 zoom 8 overlay radar product radar

All https, no errors, 100vh no outer scroll professional fill screen.
