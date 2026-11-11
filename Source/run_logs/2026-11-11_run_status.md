# Run Status 2026-11-11

Full sweep of all 385 unique URLs in `URL/url_reachable.md`. Fetched via curl (no JS rendering). Where a page's content/structure is unchanged from the 2026-11-04 sweep and plain curl still returns no server-rendered listing, status was carried over from that run rather than re-guessed. Pages that server-rendered real, dated solicitation rows this time were read in full and checked against the approved keyword list and the 2026-11-01 date cutoff (Issue Date, falling back to Start Date).

Totals: {'NO_RELEVANT_RESULTS': 218, 'BLOCKED': 121, 'FAILED': 30, 'SUCCESS': 16} = 385

Full per-URL table: `URL/run_status_2026-11-11.md`.

## SUCCESS pages (real listing content reviewed)

1. http://www.morriscountybidsystem.com/ — NJ Purchasing Group / BidNet Direct (Morris County) — 24 open items reviewed (page 1 of 5); 22 Unmatched + 2 Matched(unconfirmed) saved.
2. https://www.bidnetdirect.com/new-jersey/lbha — Long Branch Housing Authority — 2 Unmatched saved (1 item below cutoff, skipped).
3. https://bids.sciquest.com/apps/Router/PublicEvent?CustomerOrg=GIT — Georgia Tech — 1 Matched + 1 Unmatched saved (2 items below cutoff, skipped).
4. https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=Georgia&FromBranded=true — Georgia DOAS GA@WORK Marketplace — 9 Unmatched saved from page 1 of 3 (20 of 42 total results; pages 2–3 require JS pagination and were not reachable via curl).
5. https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=SUNY&FromBranded=true — SUNY Public Bid Site — 2 Unmatched saved (all 8 results on the single page reviewed; 6 below cutoff).
6. https://ebs.pnnl.gov/advertised.aspx — PNNL Acquisition Supplier Portal — 2 Unmatched saved (1 item below cutoff).
7. https://www.bidnetdirect.com/public/solicitations/open — BidNet Direct public national search (25,206 total open solicitations; only page 1/25 reviewed) — 2 Matched(unconfirmed, gated) saved: "Enterprise Resource Planning (ERP) Software Selection" (NV) and "DSCSA Compliance Subscription" (TX). Agency names and full scope are not visible without BidNet registration; Location is the only agency-identifying detail on the public page.
8. https://www.emarketplace.state.pa.us/Search.aspx — PA eMarketplace (DGS) — 7 Unmatched saved from the first ~10 results shown; remaining pages not paginated via curl.
9. https://bidopportunities.chugachelectric.com/ — real listing viewable, but **nothing saved**: "RFP 26-27: Data Governance and Data Lake Program" (clearly Matched on IT Services/Data Processing/Networking keywords, newly posted since the 2026-10-18 check) only shows a closing date ("Published until Dec 14, 2026"); no Issue Date or Start Date is published, so it fails the Date Filter's confirmability requirement and was not saved per rule.
10. https://www.cityoftulsa.org/.../bid-opportunities-and-results/?t=current — real listing viewable, but **nothing saved**: "TAC 1416 ClearPass Access Licenses" (Matched — Aruba ClearPass is network-access-control software) shows only a Response Deadline (11/18/2026), no Issue/Posted date; not saved per rule.
11. https://www.northwestmsbids.com/ — real listing viewable, but **nothing saved**: "RFP # 27-011-02 College Housing Management Software System" and "RFQ# 27-011-05 Technical Assistance: Grant & Data Management" look Matched (software system; data management) but the page shows only "Bids [due date]," no Issue/Start date; not saved per rule.
12. https://www.rochesterhousing.org/bid-opportunities — real listing viewable ("255 Hamilton Street Interior/Exterior Duplex Renovations," General Remodeling, Bids Due Nov 20, 2026); Unmatched on content and, separately, no Issue/Start date — not saved either way.
13. https://www.bidexpress.com/businesses/85766/home?agency=true — Municipality of Anchorage — real upcoming-solicitations list (ITB 2026B084, RFP 2026P057, CITB 2026C048) viewable without login, but only a Deadline field is shown, no Issue/Start date — not saved per rule.
14. https://www.bidcontract.com/ — third-party aggregator, public page 1 of ~49 — "79050750-Telesign Service Platform" (CA) and "IT Sourcing Event DEQ AI Permitting Pilot" (NC) look Matched, but agency names and official source links are gated behind the aggregator's own detail pages — not saved, consistent with prior sessions' handling of aggregator-only listings.
15. https://bidsnexus.com/ — third-party aggregator — "St. Vrain Valley School District ... Dell Elastic Cloud Storage" RFQ looks Matched but is gated the same way — not saved.
16. https://app.rfpplanner.com/opportunity/match/ — third-party aggregator — titles/dates visible (Waco, DART items) but all transportation/construction (Unmatched-looking) and gated for full detail — not saved.

## Saved this run

51 new records saved to `Source/Scraped/` (all dated 2026-11-11_*.md): 5 Matched, 46 Unmatched. All pass the 2026-11-01 Issue/Start Date cutoff. Breakdown by source: Georgia Tech (2), Georgia DOAS (9), SUNY (2), PNNL (2), Long Branch Housing Authority (2), Morris County/NJ Purchasing Group (24), PA eMarketplace (7), BidNet Direct national (2, gated-unconfirmed Matched), Columbus State University drone eRFQ (1, part of the Georgia DOAS set).

Matched (5): GT Smart Parking Guidance Platform & System; NJ/Morris County CCRFP Software Application Programs for LMS (unconfirmed, listing-level); NJ/Morris County Wire Transfer and Electronic Payment Security Consultant (unconfirmed, listing-level); BidNet Direct national ERP Software Selection, NV (unconfirmed, gated); BidNet Direct national DSCSA Compliance Subscription, TX (unconfirmed, gated).

Unmatched (46): construction, road/bridge maintenance, equipment, legal/professional-services appointments, waste disposal, energy, medical/clinical equipment and staffing, and similar non-IT solicitations — see individual files for each title's Relevance note.

## URL status file maintenance

- `URL/reachable/blocked.md`: removed the stale 2026-09-26 entry for `morriscountybidsystem.com` (now confirmed to server-render a real listing without login) and added it to `URL/reachable/easily_scrapable.md`, along with the Anchorage Bid Express URL and a note on the several JS-rendered portals that server-rendered full tables via plain curl this run.
- No URL changed Reachable/Unreachable/Not-Applicable category this run (all 385 returned an HTTP response). `https://www.govevents.com/?signoutsucccess` loaded (200) and is an events/conference aggregator ("Where Government Gathers"), not a procurement portal — a Not-Applicable candidate for a future pass, not reclassified this run to avoid hand-editing the large padded `url_reachable.md` table without a formatting tool.

## Not saved / observed only (no confirmable Issue or Start Date, or no official source)

- Chugach Electric RFP 26-27: Data Governance and Data Lake Program (AK) — Matched-looking, no Issue/Start date published.
- City of Tulsa TAC 1416: ClearPass Access Licenses (OK) — Matched-looking, no Issue/Start date published.
- Northwest MS Community College RFP #27-011-02 College Housing Management Software System and RFQ# 27-011-05 Technical Assistance: Grant & Data Management (MS) — Matched-looking, no Issue/Start date published.
- Municipality of Anchorage ITB 2026B084 / RFP 2026P057 / CITB 2026C048 (AK) — no Issue/Start date published.
- BidContract.com aggregator: 79050750-Telesign Service Platform (CA); IT Sourcing Event DEQ AI Permitting Pilot (NC) — gated, no official source/agency name.
- BidsNexus.com aggregator: St. Vrain Valley School District RFQ, Dell Elastic Cloud Storage (CO) — gated, no official source/agency name.
