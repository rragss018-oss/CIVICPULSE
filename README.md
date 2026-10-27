# CivicPulse — Smart Civic Hazard Reporting

## Project overview
CivicPulse is a student prototype for community reporting of waterlogging, blocked drains, and unsafe roads. It displays reports on an interactive map, offers filters, and ranks reports using a transparent demonstration heuristic.

## Requirements
- A modern web browser (Chrome, Edge, Firefox, or Safari).
- Internet access for the Leaflet JavaScript library and OpenStreetMap tiles.
- No Node.js, Python packages, API keys, or server are required for the basic static demo.

## Setup instructions
### Option A — Open directly
1. Extract the project ZIP.
2. Open `index.html` in a modern browser.
3. Allow the page to load. The map requires internet access.
4. Submit a test report and check the dashboard, filters, and priority ranking.

### Option B — Run a local HTTP server (recommended)
1. Install Python 3 if it is not already installed.
2. Open a terminal in the project folder.
3. Run:
   ```bash
   python -m http.server 8000
   ```
4. Visit `http://localhost:8000` in your browser.

## Environment variables and configuration
**No environment variables are required by this static prototype.** It does not use a backend, database server, API secret, or external application credentials. Map tiles and the Leaflet library are loaded from public CDN/OSM endpoints, so internet access is required for the interactive map.

If the project is extended with a backend in the future, store server secrets in environment variables (for example, `DATABASE_URL` or `MAP_API_KEY`) and never commit secrets to the repository. These variables are examples for a future version and are not used by this prototype.

## Main features
- Submit reports with hazard category, neighbourhood, severity, description, and optional coordinates.
- View approximate demo locations on an interactive map.
- Filter by category, priority, and neighbourhood.
- Dashboard totals and repeated-location hotspot counts.
- Tamil/English toggle for key interface text.
- Browser-local persistence using LocalStorage.
- Reset the report list to the original sample dataset.

## Repository contents
- `index.html` — application source.
- `TECHNICAL_DESIGN.md` — design, architecture diagram, data flow, and limitations.
- `sample_data.json` / `sample_data.csv` — fictional demonstration records.
- `TEST_CASES.md` — manual test plan.
- `LICENSE` — MIT licence.
- `README.md` — setup and usage guide.

## Demo data and privacy
Sample records are fictional and their coordinates are approximate. Reports entered by a user are stored in the current browser's LocalStorage only. They are not sent to authorities or shared with other users. An optional photo is not uploaded; only its filename is noted. Do not enter personal or sensitive information.

## Known limitations
- No authentication or shared backend.
- No incident verification, moderation, or abuse prevention.
- No official municipal or emergency-service integration.
- Map display requires an internet connection.
- Priority scoring is a demonstration heuristic and has not been validated for real-world safety decisions.

## AI-use disclosure
If AI tools were used to assist development, disclose the tools and assistance accurately in the competition submission. Review and test the code before describing it as your own work.

## Licence
Released under the MIT License. See `LICENSE`.
