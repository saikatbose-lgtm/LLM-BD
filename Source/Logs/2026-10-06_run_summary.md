# Scrape run 2026-10-06 (cutoff 2026-10-01)

Method: all 355 URL rows in `URL/url_reachable.md` fetched individually with curl (HTTP-only, no JS rendering).

| Status | Count | Basis |
| --- | --- | --- |
| SUCCESS | 0 | no solicitation passed keyword + date filter |
| NO_RELEVANT_RESULTS | 288 | HTTP 200 (login/JS shells or listings without a confirmable Issue/Start Date) |
| BLOCKED | 41 | HTTP 403 (37), 503 (3), 429 (1) |
| FAILED | 26 | 404 (7), 000/timeout (2), 400 (1), 500 (1), unresolved 30x (14) |
| **Total** | **355** | |

Notes: LA County (232 open bids) and NYSIF list keyword-relevant IT items (e.g. RFP-DA-IT01 Case Management System, RFB-IS-27200231 BMC Footprints maintenance, NYSIF 2026-139-IT, 2026-121-IT) but publish no Issue/Start Date in listings, so the date filter cannot be confirmed; nothing saved. No findings, so no email sent. URL status files unchanged.
