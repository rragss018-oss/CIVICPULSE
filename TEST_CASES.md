# CivicPulse Manual Test Cases

| ID | Test | Steps | Expected result |
|---|---|---|---|
| TC-01 | Initial load | Open `index.html` | Six fictional sample reports appear in the dashboard/list. |
| TC-02 | Submit valid report | Fill category, location, severity, description; submit | New report appears and total metrics update. |
| TC-03 | Required fields | Leave location or description blank; submit | Browser prevents submission. |
| TC-04 | Coordinate pair validation | Enter latitude only and submit | Validation message asks for both coordinates or neither. |
| TC-05 | Category filter | Select Waterlogging | Only waterlogging reports appear in the list. |
| TC-06 | Priority filter | Select High | Only reports currently ranked High appear. |
| TC-07 | Location search | Search for `Tambaram` | Matching neighbourhood reports remain visible. |
| TC-08 | Hotspot count | Review locations with multiple reports | Repeated named locations contribute to hotspot metric. |
| TC-09 | Reset sample data | Click Reset demo data and confirm | Local additions are removed and six sample reports return. |
| TC-10 | Map rendering | Open with internet access | Approximate pins appear for records with coordinates. |
| TC-11 | Map unavailable | Disable internet and reload | Map may not load; report form and list remain available. |
| TC-12 | Geolocation permission | Click Use my location and grant permission | Coordinates populate the form; no report is submitted automatically. |
| TC-13 | Language toggle | Click Tamil / English | Key headings and hero copy change language. |
| TC-14 | Local-only storage | Submit a report, reload same browser | Report remains on the same browser; it is not shared with other devices. |
| TC-15 | Privacy notice | Review page notice | Demo limitations and no-official-integration disclaimer are visible. |

## Test data
Use the fictional records in `sample_data.json` or `sample_data.csv`. The application has its own built-in fictional seed data. The separate files are included for documentation and test/review purposes.
