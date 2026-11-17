# Run status 2026-11-17

Automated scheduled run. Every URL in `url_reachable.md` (385 distinct URLs) was opened individually in headless Chromium (Playwright, JS rendered). Portals with readable listings were then mined (public listing/detail endpoints) for solicitations with Issue/Posted/Start date on or after the run cutoff **2026-11-01**.

Counts: SUCCESS 25, NO_RELEVANT_RESULTS 92, BLOCKED 250, FAILED 18 — total 385 (= 385 URLs).

New records saved to `Source/Scraped/`: 1177 (Matched: 64; Matched (unconfirmed, scope gated): 40; Unmatched: 1073).

Caveats:
- BidNet Direct national listing (26,000+ open items): page 1 (25 newest, all 2026-11-17) saved in full plus Matched items found via keyword searches; other Unmatched BidNet items published since 11/01 were not exhaustively enumerated.
- Bonfire portals, PennBid, BidExpress Anchorage and Houston BeaconBid: listings readable but detail pages behind Cloudflare/human-verification, so issue dates could not be confirmed and nothing was saved from them.
- Minnesota SWIFT detail pages hit a Radware CAPTCHA after the listing was read; MN records are listing-level only.

| # | URL | HTTP | Status | New items | Note |
|---|---|---|---|---|---|
| 1 | http://newhavenhousing.cobblestonesystems.com/gateway/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 2 | http://njstart.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2951 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 3 | http://norta.procureware.com/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 4 | http://procurement.opengov.com/ | 200 | BLOCKED | 0 | Login wall |
| 5 | http://vendorportal.dc.gov/ | 200 | BLOCKED | 0 | Redirects to https://vendorportal.dc.gov/Account/Login - invoicing portal login; no solicitations (eSourcing in PASS). |
| 6 | http://www.mncppc.org/register.html | - | FAILED | 0 | Navigation error: page.goto: net::ERR_TOO_MANY_REDIRECTS at http://www.mncppc.org/register.html |
| 7 | http://www.morriscountybidsystem.com/ | 200 | SUCCESS | 54 | Redirects to BidNet Direct New Jersey Purchasing Group open list (109 open, 5 pages, all read). 71 items published on/after 11/01; 17 already saved in earlier runs (11/02-11/04) were skipped; 54 new items added (5 Matched). Detail pages gated to registered members - listing-level data only. |
| 8 | http://www.scsk12.org/procurement/bids | 200 | FAILED | 0 | Page returns PHP parse error instead of bid list |
| 9 | https://a856-cityrecord.nyc.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2462 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 10 | https://access.alberta.ca/auth/realms/41898876-5358-402d-aae5-eee17a413de5/protocol/openid-connect/auth?client_id=apc-app&redirect_uri=https%3A%2F%2Fpurchasing.alberta.ca%2Fauth-callback&response_type=code&scope=openid&state=bbfd4bd389cb423a98165473274390b5&code_challenge=7gPvK1m6Ml4-FdLaOsGEF5qqfo6D4i1z5YQag7pazSY&code_challenge_method=S256&response_mode=query&apc_target=supplier | 200 | BLOCKED | 0 | Login wall |
| 11 | https://account.bonfirehub.com/login?flow=e128e6d0-9c89-447a-a993-8965998b25cf | 200 | BLOCKED | 0 | Login wall |
| 12 | https://acwd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 13 | https://alabamabuys.gov/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | 0 | HTTP 200; bot-check/WAF/access denied |
| 14 | https://alabamabuys.gov/page.aspx/en/usr/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 15 | https://alamedahsg.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 16 | https://alexandriava.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 17 | https://algonquincollege.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 18 | https://alleghenycounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 19 | https://allentx.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | 0 | Login wall |
| 20 | https://alohaebuys.hawaii.gov/bso/view/login/login.xhtml | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2879 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 21 | https://app.az.gov/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 22 | https://app.rfpplanner.com/opportunity/match/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (5691 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 23 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=GIT&supplierID=1007876976&tmstmp=1763649218182 | 200 | BLOCKED | 0 | Login wall |
| 24 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=UMich&supplierID=1007876976&tmstmp=1750096171684 | 200 | BLOCKED | 0 | Login wall |
| 25 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1733233768378 | 200 | BLOCKED | 0 | Login wall |
| 26 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1757684588373 | 200 | BLOCKED | 0 | Login wall |
| 27 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1768591824093 | 200 | BLOCKED | 0 | Login wall |
| 28 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1769709497801 | 200 | BLOCKED | 0 | Login wall |
| 29 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1782391392219 | 200 | BLOCKED | 0 | Login wall |
| 30 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 31 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState&AuthToken=1%3AAES2%23COeR%2B9y0uJonDteiKZ%2BEXAT%2F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%2FPIsK26ub%2FRR7PdwEzslABhuOduB5H9gT3N0M3ug%2FeRnMZKr3z3NgtkQNLRexTFFmXjo%2BndLeXxoucMxlzNwPcEg%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523COeR%252B9y0uJonDteiKZ%252BEXAT%252F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%252FPIsK26ub%252FRR7PdwEzslABhuOduB5H9gT3N0M3ug%252FeRnMZKr3z3NgtkQNLRexTFFmXjo%252BndLeXxoucMxlzNwPcEg%253D%253D%26CustOrg%3DCalState%26EventId%3D1236956%26SupplierId%3D%26tmstmp%3D1721417133691 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 32 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=DASIowa&AuthToken=1%3AAES2%23CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%2BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%2FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%252BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%252FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%253D%253D%26CustOrg%3DDASIowa%26EventId%3D1308705%26SupplierId%3D%26tmstmp%3D1745010830840 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 33 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=FSU&AuthToken=1%3AAES2%23CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%2BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%2FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%2FDqCHvRcdLpLfA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%252BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%252FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%252FDqCHvRcdLpLfA%253D%253D%26CustOrg%3DFSU%26EventId%3D1336325%26SupplierId%3D%26tmstmp%3D1757094185862 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 34 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=MDAndersonPS | 200 | BLOCKED | 0 | Login wall |
| 35 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=StateOfNewMexico | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 36 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TAMU | 200 | BLOCKED | 0 | Login required to view solicitations |
| 37 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TriC | 200 | BLOCKED | 0 | Login required to view solicitations |
| 38 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UConnFullSuite&AuthToken=1%3AAES2%23CHQBTNcjglgXPI2CtvId3j%2BfPuY04WnaPu%2BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%2FalXbKWUgJXI%2F4ESN2t3wNRSEH%2Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CHQBTNcjglgXPI2CtvId3j%252BfPuY04WnaPu%252BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%252FalXbKWUgJXI%252F4ESN2t3wNRSEH%252Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%253D%253D%26CustOrg%3DUConnFullSuite%26EventId%3D1385650%26SupplierId%3D%26tmstmp%3D1777294149216 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 39 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UIdaho | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 40 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=URI | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 41 | https://apps.cupertino.org/details/756 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1766 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 42 | https://apps.das.nh.gov/bidscontracts/bids.aspx | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 43 | https://apps.ideal-logic.com/uopcs | 200 | BLOCKED | 0 | Login wall |
| 44 | https://arbuy.arkansas.gov/bso/view/login/login.xhtml | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 45 | https://arkansas.ionwave.net/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 46 | https://baltimorecity.diversitycompliance.com/FrontPage/VendorMain.asp?XID=2708 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 47 | https://baltimorecounty.prismcompliance.com/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 48 | https://bernco.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable (2 open items: RFSQ 15-27-NH Development Partner Round 2, RFP 16-27-SS Economic Growth and Prosperity Consulting Services, closes 2026-11-24); detail pages behind Cloudflare challenge so issue dates not confirmable; nothing saved. |
| 49 | https://bgca.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable after longer wait: "There are no open projects at this time." |
| 50 | https://bgs.vermont.gov/purchasing | 200 | NO_RELEVANT_RESULTS | 0 | Public procurement page readable; no solicitation with issue/posted date on/after 2026-11-01 shown |
| 51 | https://biddingo.com/soundtransit | 200 | SUCCESS | 4 | Public listing with Date Posted; 4 open RPs posted on/after 11-01 (all Unmatched). Detail pages redirect/require Biddingo registration, listing-level data used. |
| 52 | https://biddingsimple.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (5115 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 53 | https://bidlocker.us/Home/bidlockerus | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2760 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 54 | https://bidopportunities.chugachelectric.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (812 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 55 | https://bidportal.ksu.edu/Module/Tenders/en/Vendor/Dashboard/70f4d5cf-dabf-47c6-a618-3522733a7088 | 200 | BLOCKED | 0 | Login wall |
| 56 | https://bidranger.com/ | 429 | BLOCKED | 0 | HTTP 429; bot-check/WAF/access denied |
| 57 | https://bids.sciquest.com/apps/Router/PublicEvent?CustomerOrg=GIT | 200 | SUCCESS | 4 | Public listing readable (6 open events); 4 opened on/after 2026-11-01. Contract Intelligence Solution (2027-IFB-INTECH-0036) Matched; other 3 Unmatched. Descriptions/NIGP codes from GPR cross-posts PE-50300-*. |
| 58 | https://bids.wyomingmi.gov/Bid/SpecDownload/2236?fromLogin=1 | 200 | BLOCKED | 0 | Login wall |
| 59 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=Georgia&FromBranded=true | 200 | SUCCESS | 26 | Public listing readable (48 open events across 3 pages); 26 opened on/after 2026-11-01. Details taken from the matching public GPR event pages (same event numbers). |
| 60 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=SUNY&FromBranded=true | 200 | SUCCESS | 2 | Public listing readable (7 open events); 2 opened on/after 2026-11-01 (26AXB0036, 26/27-030MC), both Unmatched. |
| 61 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=UTSA&FromBranded=true | 200 | SUCCESS | 0 | Public listing readable (2 open events); both opened on/after 2026-11-01 (743-2027-RFQ-1586, 743-2026-RFQ-1540), both Unmatched. |
| 62 | https://bidsnexus.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (6040 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 63 | https://bouldercounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 64 | https://brazosbid.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 65 | https://caleprocure.ca.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1495 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 66 | https://caleprocure.ca.gov/pages/Events-BS3/event-search.aspx | 200 | SUCCESS | 184 | 380 posted events listed (end date only); every event detail page was opened (popup /event/<BU>/<ID>) to read Published Date. 186 published on/after 2026-11-01; 2 already saved (27-002, 27-003 22nd DAA) skipped; 184 recorded (18 Matched). Published Date for events with version >1 may reflect the latest version. |
| 67 | https://camisvr.co.la.ca.us/LACoBids/BidLookUp/OpenBidList | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2489 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 68 | https://cammnet.octa.net/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (811 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 69 | https://ccsd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 70 | https://certification-app.sbsd.virginia.gov/boLogin | 200 | BLOCKED | 0 | Login wall |
| 71 | https://ci-lubbock-tx.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable (15 open items, close dates only); detail pages Cloudflare-challenged so open dates not confirmable on Bonfire. Two of its items are cross-posted on ESBD with posting dates and are included in A.json via ESBD: RFP27-20022-KM Police Department Promotional Assessment Center Services (posted 2026-11-02) and RFP27-20062-KM Armored Car Services (posted 2026-11-06), both Unmatched. |
| 72 | https://cityofbonitasprings.procureware.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Public Bids grid readable; only 2 records (RFB 26-11, RFB 26-12), both available in September and Closed to Bidding. |
| 73 | https://cityofbonitasprings.procureware.com/login | 200 | BLOCKED | 0 | Login wall |
| 74 | https://claytonk12ga.bonfirehub.com/login | 200 | BLOCKED | 0 | Login wall |
| 75 | https://cob.procureware.com/login | 200 | BLOCKED | 0 | Login wall |
| 76 | https://comalisd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 77 | https://comet-fs.ci.minneapolis.mn.us/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=ERP.SUPPLIER.EP_COSP_PUBLIC_HOME_FL | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 78 | https://contracts-marioncountygcc.msappproxy.net/gateway/Login.aspx | 200 | BLOCKED | 0 | CobbleStone Contract Insight login page; solicitations not visible without login. |
| 79 | https://cookcountyhealth.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 80 | https://cookcountyil.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 81 | https://das.iowa.gov/vendors/bidding-opportunities | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2772 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 82 | https://davenport.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 83 | https://daviefl.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable after longer wait: "There are no open projects at this time." |
| 84 | https://dfwairport.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable (18 open items, close dates only); detail pages behind Cloudflare challenge, so issue dates could not be confirmed and nothing saved. Possibly relevant items for manual check: PA2288 AI Field Assistants and Real-Time Emergency Platforms (closes 2026-11-24), DFW12345 Ignition Edge and MQTT Integration with DeltaV (closes 2026-11-18), PA2270 Investment Consulting Services (closes 2026-12-01). |
| 85 | https://dhr.alabama.gov/announcements/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1593 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 86 | https://dir.my.site.com/BidStamp/VIS_CustomLogin | 200 | BLOCKED | 0 | Login wall |
| 87 | https://dmschools.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 88 | https://dmschools.procureware.com/Companies?t=Info | 404 | FAILED | 0 | HTTP 404 |
| 89 | https://douglascountypurchasing.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 90 | https://ebs.pnnl.gov/advertised.aspx | 200 | SUCCESS | 5 | 6 advertised solicitations; 5 with Issue Date on/after 2026-11-01 (detail pages via View button read: NAICS, contracts specialist, synopsis). All Unmatched (goods/construction/quantum-computer lease RFI). U-10Mo Fabrication (issued 2026-09-17) excluded. |
| 91 | https://ecsd.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 92 | https://ejbs.fa.us6.oraclecloud.com/supplierPortal/faces/FndOverview?fndGlobalItemNodeId=itemNode_supplier_portal_supplier_portal | 200 | BLOCKED | 0 | Login wall |
| 93 | https://emma.maryland.gov/page.aspx/en/usr/login?ReturnUrl=%2fpage.aspx%2fen%2fbuy%2fhomepage | 200 | BLOCKED | 0 | Login required to view solicitations |
| 94 | https://eprocurement.esmsolutions.com/resetpassword?Token=935c91e0-3b71-4706-88a0-2cc4dc6d5da7 | 200 | BLOCKED | 0 | Login wall |
| 95 | https://esupplier.erp.delaware.gov/psc/fn92pdesup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | BLOCKED | 0 | Login wall |
| 96 | https://esupplier.sonomacounty.ca.gov/psc/FN92PRD_9/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?Page=PT_LANDINGPAGE&Action=H | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 97 | https://eva.virginia.gov/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 98 | https://evp.nc.gov/solicitations/ | 200 | SUCCESS | 139 | eVP open solicitations (258) sorted by Posted Date; paged until posted < 2026-11-01; 139 posted 2026-11-02..2026-11-17, all detail pages read (description, commodity code, owner). 9 Matched. None in existing IDs. |
| 99 | https://fairfaxcounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 100 | https://fayetteville-ar.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 101 | https://fayetteville-ga.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 102 | https://financials.ok.gov/psc/SOKLFP1DS/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 103 | https://flyri.com/riac/procurement/ | 200 | NO_RELEVANT_RESULTS | 0 | Only new solicitation RFP 37399 (CUPPS/GMS/IDS) issued July 17, 2026; 'ERP Migration Implementation Consultant' listed as Coming Soon (not issued). |
| 104 | https://fms-prd.ps.sc.edu/psc/FPRD/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | 0 | Login wall |
| 105 | https://fortworthtexas.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 106 | https://fscm.teamworks.georgia.gov/psc/supp/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 107 | https://garwoodnj.govoffice3.com/index.asp?SEC=2E0FA122-5AAF-4709-8370-F01AB70B1579&pri=0 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2215 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 108 | https://gccisd.ionwave.net/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 109 | https://ggbhtd.bonfirehub.com/portal/ | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 110 | https://goodbuy.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 111 | https://govbidwire.com/ | 200 | SUCCESS | 4 | Aggregator homepage (secondary source); 5 bids shown published 2026-11-17 captured from public detail pages (1 Matched: UTSA132 RESNET). Full search/official postings gated behind paid plan. CMAR Carteret County item 'Releases Dec 3, 2026' skipped (not yet issued). |
| 112 | https://govwhitepapers.com/?utm_source=GovEvents&utm_medium=NavBar | 429 | BLOCKED | 0 | HTTP 429; bot-check/WAF/access denied |
| 113 | https://guest.supplier.systems.state.mn.us/psc/fmssupap/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | BLOCKED | 0 | Redirects to validate.perfdrive.com Radware Captcha Page (bot manager) - no content viewable. Same Minnesota supplier portal's public bid list is covered via the fmssupap_20 bid-list URL. |
| 114 | https://guest.supplier.systems.state.mn.us/psc/fmssupap_20/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_BID_CMP_FL.GBL?PAGE=SCP_PUB_BIDLIST_FL | 200 | SUCCESS | 42 | Public SWIFT bid list (60 rows) readable; 42 events with Start Date on/after 2026-11-01 extracted at listing level (incl. 3 Law Enforcement Liaison events re-posted under new IDs 2000018895-97, prior same-titled events already saved). Event detail pages could not be opened: follow-up automated access to the same domain now returns a Radware CAPTCHA, so description/codes/POC are listing-level only. 1 item (2000018863 ADM/RFP Accessibility Services Enterprise Program) tagged Matched (unconfirmed). |
| 115 | https://ha.internationaleprocurement.com/ | 200 | BLOCKED | 0 | Login wall |
| 116 | https://habc.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 117 | https://hacp.org/profile/business-developmentommincorp-com/ | 404 | FAILED | 0 | HTTP 404 |
| 118 | https://hamiltoncountyohio.gob2g.com/?TN=hamiltoncountyohio | 200 | BLOCKED | 0 | Login required to view solicitations |
| 119 | https://hcpss.bonfirehub.com/login | 200 | BLOCKED | 0 | Login wall |
| 120 | https://health.maryland.gov/procumnt/pages/procopps.aspx?utm_source=chatgpt.com | 404 | FAILED | 0 | HTTP 404 |
| 121 | https://homesa.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable (10 open items) but it shows only close dates; every /opportunities/<id> detail page returns a Cloudflare 'Performing security verification' challenge, so issue/open dates could not be confirmed and nothing was saved (not guessed). Items include 2610-5721 Website Redesign, Hosting and Maintenance (closes 2026-12-04) and 2610-5719 Multi-site Alarm System - worth a manual check. |
| 122 | https://hosting.portseattle.org/sops/ | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 123 | https://hosting.portseattle.org/sops/#/Dashboard | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 124 | https://hub.edison.tn.gov/psc/fsprd/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?LP=EP_COSP_PUBLIC_HOME_FL& | 200 | BLOCKED | 0 | Login required to view solicitations |
| 125 | https://idcs-9275a5d3c7c74bb390dab405c8de5456.identity.oraclecloud.com/ui/v1/signin | 200 | BLOCKED | 0 | Login wall |
| 126 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=20134&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A20134%7D&agency_name=North+County+Transit+District&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Freset-password | 200 | BLOCKED | 0 | Login wall |
| 127 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=53010&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A53010%7D&agency_name=Long+Beach+City+College&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Freset-password | 200 | BLOCKED | 0 | Login wall |
| 128 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=73214&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A73214%7D&agency_name=Sacramento+Municipal+Utility+District&agency_logo=https%3A%2F%2Ffiles-prod01.planetbids.com%2Ff73214%2F20250428114636755+SMUD_Logo_4c.png&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Freset-password | 200 | BLOCKED | 0 | Login wall |
| 129 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=39471&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A39471%7D&agency_name=San%20Diego%20Housing%20Commission | 200 | BLOCKED | 0 | Login wall |
| 130 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=41576&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A41576%7D&agency_name=City%20of%20Menifee | 200 | BLOCKED | 0 | Login wall |
| 131 | https://idm-global.j1p.jaggaer.com/auth/realms/j1p-supplier-idm/login-actions/authenticate?client_id=prod-idp.app.jaggaer.com&tab_id=DvM31H7SmPk | 200 | BLOCKED | 0 | Login wall |
| 132 | https://iehp.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable after longer wait: "There are no open projects at this time." |
| 133 | https://iris-vss.alaska.gov/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 134 | https://jeffersoncitymo.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 135 | https://jocogov.ionwave.net/ | 200 | BLOCKED | 0 | Login wall |
| 136 | https://jocogov.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 137 | https://kbrsupplier.com/default.aspx | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 138 | https://knoxbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 139 | https://lacounty.gov/business/doing-business-with-la-county/lac-purchasing-and-contract-opportunities/ | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 140 | https://lagoverpvendor.doa.louisiana.gov/irj/portal | 200 | BLOCKED | 0 | Login wall |
| 141 | https://lajoyaisd.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 142 | https://lakeworthbeachfl.bidsandtenders.net/Module/Tenders/en/Home/BidsHomepage | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 143 | https://lawa.bonfirehub.com/login | 200 | BLOCKED | 0 | Login wall |
| 144 | https://lcpscm.ionwave.net/VendorRegistration/CompanyInfo.aspx | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 145 | https://leegov.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 146 | https://lexingtoncounty.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | 0 | Login wall |
| 147 | https://lexingtonky.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 148 | https://login-euxp-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?ECID-Context=1.0062xRLviAgFS8V5u30FyX0007aI0003xm%3BkXjE | 503 | FAILED | 0 | HTTP 503 |
| 149 | https://login-exkk-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3D5KbKcxXM%2Fj31a5DXL88CkKQxNL8xTgjx4o0T1qvnZ%2Fm8L2PVioR3VV1mC34DycQZg0dWLUr3o1012giKiZTeLaHBd98AahIgscHY6X%2BjknHWJTGvHe2M7sMJAhATajCClH2Gx0nkCL6bzAbl%2BeHZ6uiXgB%2B2hOmd%2FQzizf5Y4YNkakpfRK5yMBTn8PZ9OsPNGrM%2B9IEZeXceK4jlLN54auwgY6%2B6KY4M7NGvbtyUVhrexBSDMkJ1OjzgiQG26s7nUNgDOOBUY1V47R2%2FWeMq%2Bd5RS64LygmWx1uZVUYM2hKWN3EGASc%2FSKuhZmDEEqqbRerUTv8simlP4wr9hR9Mpg0V0hRCebgR0PJpg4%2BHF7Ag3SZ7q9E7%2BHfRzp%2F3W%2B3GmJQk%2BTkTLecO55P653z0xHK1qj1hCGfUC%2F7kmkzXjp1zFdxcYxy0Wmms4vL3XeoVshFxno55Xarw4aCIFXtNTxZWRW7uf5m0Zw2p6WcH89Wrs2vxPwt6PMezO3rioKyymXYA0SEkvDg3C%2FapCuEENBINGbNbfVXmU9HJ3r8XnlclYMyGyIGLAznYm98%2BiO%2F0AWsh3bbiaxSI9qt8veZReDf6Rn9T76JBWjcttWwXXZET%2BU4t5KxKqJ1QJxPAEhmZzJZ2sRAm4bRXVI4ODGQRpEciLt8Lj3lB9rFv9tqgF10%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3D75ca2eec8e5ee3dbd0b2a672207ad24ecf7dc56a&ECID-Context=1.006Ivf_oUN8AxGKayTaeMG0060Ok0001FM%3BkXjE | 503 | FAILED | 0 | HTTP 503 |
| 150 | https://login-ibqhjb.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3DxS138OL6YUFqo5kXqhatUBRr5X3V1RGL4k%2Bz0kVeSsDqPlMtLQOkCPPbjyD9zFAHBZaV%2B4%2Bm1%2BC15RRXqDUzJfqgkiyvt3ZB8iYpaRVN9qApx0UAl6kxqVcVIFnLXt9LuTk4KALc3n4SIQddr6q6%2BOFzVzgiKyWa3cqoE2V12YBzK8Pi2SYryl1afztYU9JVUJP29U%2FlKJqV7biRJbQE9H2sPdqJv3kpoyqbSpybx21q5XYhaPoGc2tLTa6xi%2FRfih66LyuMO4FMp8vH5zA12aZ9ltzcyzAVFI3x7uQLcAh6pHQm7VqoYEwfyhjgh7FaYQ9cE67Q%2BeRAkhh0r5dlkA%2Fjbd93rdrtDAMuzNqFGgeGYMM%2F3wqSyRTAXhDr9kp1RGsdNmsK1lr6FA9OZ2brJTDDbjPwVNPLMB3TyYleKacbH9%2FXviCjUQ%2FHwzgt5a9ZuBGEumvbK0TxwMpgsJ0yu0jXJ6%2BfZNKN5%2FaG4Pxi2jY47gyzltsiogFvef6dIlZzVXVFjPIDgDWoc%2BR0v7%2BtJDZbAdRc3bNMWuWNuFlHz2%2BemlSYNUCtIqoSCOFJ3PMxgHpdIwsCoLnHZ1A0BPrjrnmeJlZ1BLCj1XMN8aCDPaJXMm8GUoFpBDoJcVgnroYkpEYrk4FICQDlSWQJyHDEZvAyf8mrlleFvHliIKe7iqCM0VrJPJxOx3XLM4%2FFoSIgzv34BqFfX4c4fRTLYbEEbRj5%2FXmyMe04mzMmfdsm1rdZs7boBYCvTXKmhklZQme33TFM26PGec1T0ZnFkODoiPWb3%2FSouG2DGmvCBo7uh0cfmdMNlRngKQDEg9Gi8IlTDr5a4zrqqOzUe5eYoFAwMHRnZ%2Bi9XY%2B%2FbqXxXqBVLWnW6hwImdtNFjXGJuER7GbvbnYWaahNTQQ5aBDezpKFOUdrjSKzI6ICdCnXnnpPo%2BgKo9HQXsMrFc89CE%2BnPbXiforjn%2FjUa7sPlnIN3occRYXNafpmYekQzHYI%2F5J1L1TsBHOdebeWGx20HeLYJXFOWGup58ViARCFzp0cgp8GZntiBKsdecvdg97v5k3sO5HEWS96IYcQHlDmXIdsdBsPOG1cvSJ1JixuseaaZM5OMnOTxpsV1uToblun5Vs6DfOgTv3VUQXVevMFCyC%2BTBucOnTiZCfdT92T%2Bp1XkdveKsJ2jeRebG165AKqLnEJ5eZQhBs6eWn9v%2FRow0mdfeKFavO7Fr%2FXELn9GXe13oQh0sy0RX4kW1qvKVWgI9%2FfiVQMikBsESPOFMA5dwtAFr%2BggEb7aYvdjXYs6zvmlxNxNyXwN2m3GcH7mf%2FopLRrFKVdnqD00kjja5i%2FNebYOfMTMGLVHIoL5EorazZ1hyrc2bafEjj63su3Ns2ltD0kTZvQpgdySfeQEZ21WjibhABsOHZ9SPQE91Ss5TAF6LYkOztU1VyaPmp5g%2BEwbirV3o%2FDo9a%2Fi%2By%2BFvDpPWBkpt2bIHXxWj%2F3699%2BniBsU97TRPn3nRmAmTie6HCRb0kH4k1oTrl70mjMjsI8O3bhdvhj1EnFU8r6ZSszcyTneTE%2Bma7MCYbylmnwQppds6nbIQFyzq4UMv1nLeAS3MHFZkThUexNB165wz0ycXAKMEqID%2FiVHZok2XfhRFfcA2bIk7Y%2FiBD1CplaGU%2F30%2FTC0u61H3iD5Hulp7L5f7jBTp5IjQ%3D%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3Db7d14dfa13cdabd935ca9c7841fb201bfe34a229&ECID-Context=1.006Ji0n6W6n2FSMqyKvX6G003mVL0000wW%3BkXjE | 503 | FAILED | 0 | HTTP 503 |
| 151 | https://login.ehawaii.gov/lala | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 152 | https://login.neighborlysoftware.com/neighborlysoftware.onmicrosoft.com/oauth2/v2.0/authorize?p=b2c_1_signinsignup_prod&client_id=ab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4&response_type=code%20id_token%20token&scope=openid%20email%20profile%20offline_access%20https%3A%2F%2Fneighborlysoftware.onmicrosoft.com%2Fab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4%2FPortal.Read&state=OpenIdConnect.AuthenticationProperties%3DRibwqB29N7HFG%2FlYtBVU9VQQ%2F47hId8udQ7Qgw4gCV5RWxEAhOVi1FNfkygg3UHLQ92Mm5nrr7PtxBGK1Ctu7VQZKAYDWo1Zw0GNewqepMxUgBtdID6wPyRuFfOCGSGsZoucI%2BKrCfxrtk7ZCE%2FsJ6Fer9k%2FkgDMMI%2Bj5ydxbYJsha6Ju%2BbwJkxl2iKxSiWbg7bz%2BzIArwJ%2BKqV8SCsJ5z%2FkyP%2BUts8TiW0nywmKbnDvMxsR8D%2B5A4UNFkxpwjbymbOFiHW9PXRCHqkEhImRWJSDNKMCqIj80loL00VhBpNteMaRXZDaK%2BHEml%2Fw1MkUBLxhoIJQTxiupyJBRNxRhG6dB%2BbWh7CUp1uHipB2lRr8sAjsfh8IPD18auSh31%2Byv71fC0%2FI2e7Kct5SLawcqg%3D%3D&response_mode=form_post&nonce=639174124887079482.NGJmZDQ0N2EtZjkwNi00ZmY4LWI4MWItNmRkMDcwMTQyNTIzMzYyNWQ4MWUtMjExYy00Yjc4LThlMDYtOWJlZDA4YzNhZDdi&tenantCode=waterlooia&portalType=contractor&nTenantId=490&ui_locales=en&machineCode=00000000-0000-0000-0000-000000000000&redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Floginredirectcomplete&post_logout_redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Fwaterlooia%2Fcontractor&x-client-SKU=ID_NET472&x-client-ver=7.5.0.0 | 200 | BLOCKED | 0 | Login wall |
| 153 | https://lonestar.ionwave.net/SourcingEvents.aspx?SourceType=1 | 200 | SUCCESS | 1 | Public IonWave listing (3 items, with Bid Issue Date). Only 26-10-05 Insurance Broker Services (issued 2026-11-17) qualifies; 26-10-01 (issued 10/27) and RFP 26-09-03 Addendum 2 (issued 9/18) are before cutoff. Listing-level data only (details require supplier login). Unmatched. |
| 154 | https://longbeachbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 155 | https://lrsd.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login wall |
| 156 | https://madisonal.procureware.com/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 157 | https://marketplace.unisonglobal.com/login.do?resource_name=marketplace | 200 | BLOCKED | 0 | Login wall |
| 158 | https://mdapex.ecenterdirect.com/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 159 | https://mdcourts.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 160 | https://mdstad.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 161 | https://mecknc-vss.hostams.com/PRDVSS1X1/Advantage4 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 162 | https://menv.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 163 | https://mevss.hostams.com/PRDVSS1X1/AltSelfService | 404 | FAILED | 0 | HTTP 404 |
| 164 | https://miamiu-ohiousourcing.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 165 | https://mps.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable after longer wait: "There are no open projects at this time." |
| 166 | https://mtc.bonfirehub.com/login | 200 | BLOCKED | 0 | Login wall |
| 167 | https://mwrd.app/Cntrctann/ | 200 | NO_RELEVANT_RESULTS | 0 | Public procurement page readable; no solicitation with issue/posted date on/after 2026-11-01 shown |
| 168 | https://mwrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 169 | https://my.alaska.gov/adfs/ls/?wa=wsignin1.0&wtrealm=https%3a%2f%2fmy.alaska.gov%2f&wctx=rm%3d0%26id%3dpassive%26ru%3d%252fPortal%252fPortal.aspx&wct=2023-11-24T17%3a55%3a54Z | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 170 | https://myncid.nc.gov/index.html | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 171 | https://myncid.nc.gov/index.html#/main/userProfile | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 172 | https://myok-staffing.onconcourse.com/login?type=partner | 200 | BLOCKED | 0 | Login wall |
| 173 | https://nait.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 174 | https://nevada.ionwave.net/ | 200 | BLOCKED | 0 | Login wall |
| 175 | https://nsc.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable after longer wait: "There are no open projects at this time." |
| 176 | https://ntmwd.bonfirehub.com/registration | 200 | BLOCKED | 0 | Login wall |
| 177 | https://ny.newnycontracts.com/FrontPage/VendorMain.asp?XID=4111 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 178 | https://octa.govqa.us/WEBAPP/_rs/(S(hn5r0labmmsdycjs2dfu2bmf | 404 | FAILED | 0 | HTTP 404 |
| 179 | https://oklahoma.gov/omes/divisions/central-purchasing/suppliers-and-payees/supplier-portal.html | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 180 | https://onesource.wsscwater.com//OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | 0 | Login wall |
| 181 | https://onesource.wsscwater.com/OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | 0 | Login wall |
| 182 | https://onlineservices.osc.state.ny.us/Enrollment/login?17 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 183 | https://oregonbuys.gov/bso/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (3611 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 184 | https://oregonbuys.gov/bso/view/login/login.xhtml | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 185 | https://passport.cityofnewyork.us/page.aspx/en/buy/homepage/ven | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 186 | https://pasupplierportal.state.pa.us/irj/portal/anonymous | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 187 | https://pbcvssp.co.palm-beach.fl.us/webapp/vssp/AltSelfService?EmailToken=02730029218941640788 | 200 | FAILED | 0 | VSS URL (with and without EmailToken) redirects to the Palm Beach County home page discover.pbc.gov; no solicitation listing is reachable at this URL. |
| 188 | https://pbsystem.planetbids.com/portal/13821/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 189 | https://pbsystem.planetbids.com/portal/13982/login | 200 | BLOCKED | 0 | Login wall |
| 190 | https://pbsystem.planetbids.com/portal/13982/login# | 200 | BLOCKED | 0 | Login wall |
| 191 | https://pennbid.bonfirehub.com/portal/?tab=openOpportunities | 200 | BLOCKED | 0 | Open-opportunities list (143 projects) readable, but it shows only close dates; no open/issue date in the list or in the public JSON feed, and every opportunity detail page returns a Cloudflare 'Performing security verification' 403 challenge. Issue dates could not be confirmed, so nothing saved. |
| 192 | https://pinalcountyaz.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 193 | https://portal.ct.gov/das/ctsource/bidboard | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (3202 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 194 | https://pr-webs-vendor.des.wa.gov/ | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 195 | https://pro.prismcompliance.com/ | 200 | BLOCKED | 0 | Login wall |
| 196 | https://pro.prismcompliance.com/default.aspx | 200 | BLOCKED | 0 | Login wall |
| 197 | https://procuralerts.com/government-bids | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1966 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 198 | https://procure.cgieva.com/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | 0 | HTTP 200; bot-check/WAF/access denied |
| 199 | https://procure.portlandoregon.gov/bso/seller/bidAck.sdo | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 200 | https://procurement.opengov.com/login | 200 | BLOCKED | 0 | Login wall |
| 201 | https://procurement.opengov.com/portal/aurorail | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 202 | https://procurement.opengov.com/portal/baltimorecountymd | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 203 | https://procurement.opengov.com/portal/bft | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 204 | https://procurement.opengov.com/portal/bloomingtonin | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 205 | https://procurement.opengov.com/portal/brevardschools | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 206 | https://procurement.opengov.com/portal/cheyennecity | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 207 | https://procurement.opengov.com/portal/cityofbradenton | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 208 | https://procurement.opengov.com/portal/cityofedinburg | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 209 | https://procurement.opengov.com/portal/cityofhomestead | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 210 | https://procurement.opengov.com/portal/cityofnsb | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 211 | https://procurement.opengov.com/portal/cityoftampa | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 212 | https://procurement.opengov.com/portal/clevelandoh | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 213 | https://procurement.opengov.com/portal/co-hidalgo-tx | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 214 | https://procurement.opengov.com/portal/lompoc | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 215 | https://procurement.opengov.com/portal/morenovalley | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 216 | https://procurement.opengov.com/portal/oak-brook | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 217 | https://procurement.opengov.com/portal/pasadena | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 218 | https://procurement.opengov.com/portal/pinoleca | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 219 | https://procurement.opengov.com/portal/rtd-denver | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 220 | https://procurement.opengov.com/portal/saccounty | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 221 | https://procurement.opengov.com/portal/santacruzca | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 222 | https://procurement.opengov.com/portal/smcgov | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 223 | https://procurement.opengov.com/portal/stpete | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 224 | https://procurement.opengov.com/portal/tucson-az | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 225 | https://procurement.opengov.com/portal/tuolumnecountyca | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 226 | https://procurement.opengov.com/portal/wheatridgeco | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 227 | https://procurement.opengov.com/vendors/155272/proposals | 200 | BLOCKED | 0 | Login wall |
| 228 | https://proportal.sourcewell-mn.gov/Module/Tenders/en/Vendor/Dashboard/b50f7d44-0fe6-4ffe-8621-fbae66354482 | 200 | BLOCKED | 0 | Login wall |
| 229 | https://publicbidtracker.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Readable aggregator, but neither homepage nor state pages publish posted/issue dates (deadlines only); cannot confirm date filter. |
| 230 | https://pur.doas.ga.gov/gpr/ | 200 | SUCCESS | 256 | Public GPR search (eventSearch JSON) readable without login; 549 open events, 288 posted on/after 2026-11-01. 256 attributed here (26 GA@WORK/Jaggaer state events attributed to the Georgia Jaggaer portal, 4 Georgia Tech cross-posts kept under the GIT portal, 2 sole-source/intent-to-award notices excluded). Public detail pages give description, buyer contact and NIGP codes. |
| 231 | https://purchasing.iu.edu/resources/forms/table.html | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (4160 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 232 | https://recuperacion.pr.gov/en/procurement-and-nofa/procurement/ | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable; the 3 active items were posted Oct 26, Oct 23 and Sep 17, 2026 (before cutoff). |
| 233 | https://sawsbid.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 234 | https://sccpss.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 235 | https://scottsdaleaz.bonfirehub.com/login | 200 | BLOCKED | 0 | Login wall |
| 236 | https://sdbuynet.sandiegocounty.gov/page.aspx/en/usr/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 237 | https://secure.bidsandtenders.ca/Module/Tenders/en/Login/Index/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 238 | https://security.app.cpa.state.tx.us/Public/login?logout | 200 | BLOCKED | 0 | Login required to view solicitations |
| 239 | https://service.ariba.com/Authenticator.aw/ad/ssoIDP | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 240 | https://sigma.michigan.gov/PRDVSS1X1/Advantage4 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 241 | https://smctd.bonfirehub.com/opportunities/112297 | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 242 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=LOGINREQD&_logininst=W68E33gEyArMeQNVR!2B0pO4UAJK!2BQjvLlYP!2BnbMhYU2hA39DrCszSxwAAAYqPkSI!2F&_TKM=492813489&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER | 200 | BLOCKED | 0 | Login wall |
| 243 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=TIMEOUTASSERT&_ssoOrigUrl=https%3A%2F%2Fsms-idaho-prd.tam.inforgov.com%3A443%2Ffsm%2FSupplyManagementSupplier%2Fpage%2FXiSupplyManagementSupplierPage%3Fcsk.SupplierGroup%3DLUMA&_TKM=372688986&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER&LoginId=business-development@ommincorp.com | 200 | BLOCKED | 0 | Login wall |
| 244 | https://sms-nola-prd.inforcloudsuite.com/fsm/SupplyManagementSupplier/page/XiSupplyManagementSupplierPage?csk.SupplierGroup=100 | 200 | SUCCESS | 4 | Open Events list is public (10 events); 4 opened on/after 2026-11-01 (events 4737, 4808, 4848, 4849), all Unmatched. Event details/documents require supplier sign-in, so listing-level data only. |
| 245 | https://snoco.procureware.com/login | 200 | BLOCKED | 0 | Login wall |
| 246 | https://solutions.sciquest.com/apps/Router/BrandedSupplierHome?CustOrg=UCOP&supplierID=1007876976&tmstmp=1738093109276 | 200 | BLOCKED | 0 | Login wall |
| 247 | https://solutions.sciquest.com/apps/Router/SupplierLogin | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 248 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=BridgewaterState | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 249 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=DASIowa | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 250 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=Princeton&isLogout=true&tmstmp=1716220417643 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 251 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=StateOfUtah&isLogout=true&tmstmp=1699984786288 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 252 | https://solutions.sciquest.com/apps/Router/SupplierLogin?GSPSupplier_Login_Email=Business-development%40ommincorp.com&CustOrg=StateOfMontana&SuccessToken=1&tmstmp=1695233574600 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 253 | https://solutions.sciquest.com/apps/Router/SupplierPortalHome?tmstmp=1699981963442 | 200 | BLOCKED | 0 | Login wall |
| 254 | https://solutions.sciquest.com/apps/Router/SupplierWelcome?CustOrg=TriMet&supplierID=1007876976&tmstmp=1704204983800 | 200 | BLOCKED | 0 | Login wall |
| 255 | https://stamfordct.procureware.com/home | 200 | SUCCESS | 9 | Public Bids grid readable at /Bids without login. 9 open solicitations with Available Date on/after 11/01 added (1 Matched: 2027.0166 SIP Trunking Services). The individual bid detail page could not be opened. |
| 256 | https://stamfordct.procureware.com/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 257 | https://stillwater.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 258 | https://strathcona.bonfirehub.ca/login | 200 | BLOCKED | 0 | Login wall |
| 259 | https://supplier.esmsolutions.com/home | 200 | BLOCKED | 0 | Login wall |
| 260 | https://supplier.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | 0 | Login wall |
| 261 | https://supplier.ionwave.net/VendorLogin.aspx | 200 | BLOCKED | 0 | Login wall |
| 262 | https://supplier.ionwave.net/VendorResponse/ResponseList.aspx?status=AVAILABLE | 200 | BLOCKED | 0 | Login wall |
| 263 | https://supplier.miamidade.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1456 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 264 | https://supplier.sok.ks.gov/psc/sokfsprdsup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 265 | https://supplier.wmata.com/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | 0 | Login wall |
| 266 | https://supplierservice.sanantonio.gov/irj/portal | 200 | BLOCKED | 0 | Login wall |
| 267 | https://supplierservice.sanantonio.gov/irj/portal#12587465-vendor-info | 200 | BLOCKED | 0 | Login wall |
| 268 | https://tarrantcountytx.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 269 | https://thebidbroker.com/ | 200 | NO_RELEVANT_RESULTS | 0 | Construction-bid aggregator marketing homepage; single example (McHOST Road Imprv, East Baton Rouge) shows due date only, no posted/issue date; full listings need account. |
| 270 | https://tohowater.bonfirehub.com/login/forgot | 200 | BLOCKED | 0 | Login wall |
| 271 | https://transitchicago.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 272 | https://trstexas-supplier.ivalua.app/page.aspx/en/sup/registration_manage/2594 | 200 | BLOCKED | 0 | Login required to view solicitations |
| 273 | https://uiebid.ionwave.net/Login.aspx | 200 | BLOCKED | 0 | Login required to view solicitations |
| 274 | https://upstream.dc.gov/Sourcing/Main/ad/loginPage/SSOActions?awsso_cc=passwordadapter%3AU291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_ru%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbj9wYXNzd29yZGFkYXB0ZXI9U291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_lu%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRMb2dvdXQvU1NPQWN0aW9ucw%3D%3D%3Bawsso_ap%3AQUNN%3Bawsso_arid%3AMTY4ODk5MzA3NjY0NA%3D%3D%3Bawsso_ku%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRLZWVwQWxpdmUvU1NPQWN0aW9ucw%3D%3D%3Bawsso_fl%3AMQ%3D%3D&awsso_ap=ACM&awsso_hpk=true&passwordadapter=SourcingSupplierUser&awsr=true | 200 | BLOCKED | 0 | Login wall |
| 275 | https://upstream.dc.gov/Sourcing/Main?realm=System&passwordadapter=SourcingSupplierUser&awsso_tkn=24MUzqrzky68f28a69a52257ff | 200 | BLOCKED | 0 | Login wall |
| 276 | https://valenciacollege.edu/employees/procurement/solicitations.php | 200 | NO_RELEVANT_RESULTS | 0 | Public procurement page readable; no solicitation with issue/posted date on/after 2026-11-01 shown |
| 277 | https://vendor.myfloridamarketplace.com/login | 200 | BLOCKED | 0 | Login wall |
| 278 | https://vendor.myfloridamarketplace.com/search/bids | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1141 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 279 | https://vendor.purchasingconnection.ca/default.aspx | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1875 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 280 | https://vendorportal.dc.gov/Account/Login | 200 | BLOCKED | 0 | DC invoicing vendor portal login page; no solicitation listing (eSourcing is in PASS). Arguably not applicable. |
| 281 | https://vendors.planetbids.com/ | - | FAILED | 0 | Navigation error: page.goto: net::ERR_TOO_MANY_REDIRECTS at https://vendors.planetbids.com/ |
| 282 | https://vendors.planetbids.com/portal/14599/bo/bo-search | 200 | SUCCESS | 3 | County of Stanislaus: 3 posted on/after 11/01 (Homeless Assistance 26-28-JNS 11/02, Scour Countermeasure RFP 2026-003 11/13, Refugee Social Services Employment Services 26-30-JNS 11/16), all Unmatched. Detail pages public. |
| 283 | https://vendors.planetbids.com/portal/14599/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 284 | https://vendors.planetbids.com/portal/15300/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 285 | https://vendors.planetbids.com/portal/15381/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 286 | https://vendors.planetbids.com/portal/16151/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 287 | https://vendors.planetbids.com/portal/16151/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 288 | https://vendors.planetbids.com/portal/16725/login | 200 | BLOCKED | 0 | Login wall |
| 289 | https://vendors.planetbids.com/portal/17950/login | 200 | BLOCKED | 0 | Login wall |
| 290 | https://vendors.planetbids.com/portal/17950/login# | 200 | BLOCKED | 0 | Login wall |
| 291 | https://vendors.planetbids.com/portal/20134/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 292 | https://vendors.planetbids.com/portal/20136/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 293 | https://vendors.planetbids.com/portal/20314/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 294 | https://vendors.planetbids.com/portal/22078/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 295 | https://vendors.planetbids.com/portal/22576/bo/bo-detail/141899 | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 296 | https://vendors.planetbids.com/portal/23532/bo/bo-search | 200 | SUCCESS | 4 | City of Palmdale: 4 bids posted on/after 11/01 (Rigging, Lighting, AV production RFPs posted 11/03; SAVES civil engineering RFP posted 11/10), all Unmatched. Detail pages public. |
| 297 | https://vendors.planetbids.com/portal/23758/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 298 | https://vendors.planetbids.com/portal/24103/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 299 | https://vendors.planetbids.com/portal/24660/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 300 | https://vendors.planetbids.com/portal/24661/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 301 | https://vendors.planetbids.com/portal/27996/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 302 | https://vendors.planetbids.com/portal/28789/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 303 | https://vendors.planetbids.com/portal/29744/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 304 | https://vendors.planetbids.com/portal/32621/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 305 | https://vendors.planetbids.com/portal/39475/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 306 | https://vendors.planetbids.com/portal/39495/login | 200 | BLOCKED | 0 | Login wall |
| 307 | https://vendors.planetbids.com/portal/39495/login# | 200 | BLOCKED | 0 | Login wall |
| 308 | https://vendors.planetbids.com/portal/39501/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 309 | https://vendors.planetbids.com/portal/43728/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 310 | https://vendors.planetbids.com/portal/45619/bo/bo-search | 200 | SUCCESS | 1 | City of Inglewood: 1 posted on/after 11/01 (CB-27-02 Gate Valve Replacement, posted 11/09), Unmatched. |
| 311 | https://vendors.planetbids.com/portal/49906/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 312 | https://vendors.planetbids.com/portal/53010/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 313 | https://vendors.planetbids.com/portal/59724/vp/vp-home | 200 | BLOCKED | 0 | Login wall |
| 314 | https://vendors.planetbids.com/portal/62287/bo/bo-search | 200 | NO_RELEVANT_RESULTS | 0 | City of Adelanto: listing readable; newest posting 10/06/2026 (closed). Nothing posted on/after 11/01. |
| 315 | https://vendors.planetbids.com/portal/64863/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 316 | https://vendors.planetbids.com/portal/65292/vp/vp-prereg | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 317 | https://vendors.planetbids.com/portal/65844/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 318 | https://vendors.planetbids.com/portal/68007/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 319 | https://vendors.planetbids.com/portal/76708/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 320 | https://vendors.planetbids.com/portal/77636/portal-home | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 321 | https://ventura.bonfirehub.com/registration | 200 | BLOCKED | 0 | Login wall |
| 322 | https://via.diversitycompliance.com/FrontPage/VendorMain.asp?XID=9510 | 404 | FAILED | 0 | HTTP 404 |
| 323 | https://via.sbecompliance.com/ | 200 | BLOCKED | 0 | Login required to view solicitations |
| 324 | https://via.sbecompliance.com/?TN=via | 200 | BLOCKED | 0 | Login required to view solicitations |
| 325 | https://vrapp.vendorregistry.com/Account/LogOn | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 326 | https://vrapp.vendorregistry.com/Bids/View/BidsList?BuyerId=c5e9d3e7-b8e0-4e36-bcab-8db00d18d769 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (729 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 327 | https://vss.ky.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2807 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 328 | https://vss.ky.gov/vssprod-ext/Advantage4 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2807 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 329 | https://vss.ky.gov/vssprod-ext/Advantage4?openDoc=openDoc&DocumentCode=RFP&DepartmentCode=415&DocumentID=2600000199&DocumentVersNo=2&targetView=ammendHistoryView&Destination=pSolication | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2807 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 330 | https://vss.state.co.us/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2181 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 331 | https://vtbuys.suppliers.vermont.gov/page.aspx/en/usr/login | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 332 | https://waukeshacounty.bonfirehub.com/opportunities/144594 | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 333 | https://wrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | 0 | Bonfire public listing readable (close dates only); detail pages behind Cloudflare check, so issue dates cannot be confirmed — nothing saved |
| 334 | https://ww3.nysif.com/FooterPages/Column1/AboutNYSIF/Procurement | 200 | SUCCESS | 4 | Listing shows due dates only; issue dates taken from solicitation PDFs. 4 qualifying (2 Matched: 2026-136-IT, 2026-140-INS). 2026-147-ADM Event Management Platform RFI dated Nov 3, 2026 skipped (due 11/13/2026, already closed). 2026-143-ADM (Oct 26) and 2026-45-INV (Oct 23) predate cutoff. |
| 335 | https://www.ahfc.us/about-us/notices/requests-proposals | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1505 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 336 | https://www.annapolis.gov/bids.aspx | 502 | FAILED | 0 | HTTP 502 |
| 337 | https://www.beaconbid.com/solicitations/city-of-houston/121f4067-fb3a-4d30-85b9-ea6a6cafe989/contingent-labor-services-all-categories?token=supplier-login.ObiU4vtGsc_vRNVc-a87JReydRqhQP07ozrco4z95xclrg1KaW517ezRNB5QzTvK8dS9z_wfmREHNc6qRuGr-uHTYI229n9X2AhzK2_xmpo1LIlDsnrcN9YzPY9tkrWfy3EN_v3vttW09t3yqiaBnArwIvYLa3JnzE4G9B1giu5p7FuxEHf2iImOzrCy7TDIptzKNwKUivDO0G3DxgJ4Yz43Iz6gCzrsPGyOdGXCJV9Qg29rKw2IN4_Nw5d1czIABi6VfJW2RJtyEc02dHo1amlJHrAnTsWOtrQ8zz6lolxc5u8OanNPWUJnmTMDrOPoY-3_mtuNxCYeyzX2seLpWEfkAtq1AbX1X_Xb-492Ng&eid=bc055432-0873-482a-98b8-0490d2821dc8 | 200 | NO_RELEVANT_RESULTS | 0 | Single solicitation detail page (RFP-2025-0011 Contingent Labor, released 2025-02-08, Pending Award) — not new |
| 338 | https://www.beaconbid.com/solicitations/city-of-houston/open | 200 | NO_RELEVANT_RESULTS | 0 | BeaconBid public open list readable (30 items, due dates only); solicitation detail pages now show a human-verification challenge, so release dates cannot be confirmed — nothing saved. Titles worth manual review: Integrated Library System (ILS) HPL; Citywide Network Cabling |
| 339 | https://www.bidbuy.illinois.gov/bso/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (3103 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 340 | https://www.bidbuy.illinois.gov/bso/external/vendor/regSummary.sdo?vendorId=NZdPl7Rvv_Oq&mode=initial&dateTime=1694627292171 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (270 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 341 | https://www.bidcontract.com/ | 502 | FAILED | 0 | HTTP 502 |
| 342 | https://www.bidexpress.com/businesses/85766/home?agency=true | 200 | NO_RELEVANT_RESULTS | 0 | Municipality of Anchorage listing readable without login (13 upcoming solicitations, e.g. RFP 2026P059 AWWU Billing Software, ITB 2026B090 Cisco Spine and Leaf Network Refresh), but the public listing shows only deadlines, no issue/posted dates, and every solicitation detail page redirects to an Info Tech Express login. Issue dates could not be confirmed, so nothing saved. |
| 343 | https://www.bidnetdirect.com/new-jersey/lbha | 200 | NO_RELEVANT_RESULTS | 0 | Listing readable; 3 open solicitations - the two published 11/02 (On Call Roofing IFB-20261201a, Cyclical Painting IFB-20261201b) were already saved 2026-11-02; Snow Removal published 10/20 (before cutoff). |
| 344 | https://www.bidnetdirect.com/private/supplier/solicitations/search | 200 | BLOCKED | 0 | Login wall |
| 345 | https://www.bidnetdirect.com/public/solicitations/open | 200 | SUCCESS | 58 | National BidNet Direct aggregator (26,000+ open, ~thousands published since 11/01) - cannot be enumerated in full. Captured all 25 page-1 items (published 11/17) plus 37 Matched IT/staffing/data/cyber items found via keyword searches (information technology, IT services, staffing, software, consulting services, network, data processing, cybersecurity, temporary staff) published 11/02-11/17. Detail pages (agency, number, scope, contact) locked to registered members; listing-level data only. |
| 346 | https://www.busybids.org/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (6717 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 347 | https://www.californiabids.com/bid_opportunities/ | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 348 | https://www.cdta.org/node/15813/register | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 349 | https://www.centralauctionhouse.com/login.php | 200 | BLOCKED | 0 | Login page only (Central Bidding sign-in); no listing visible. |
| 350 | https://www.cityoftulsa.org/government/departments/finance/selling-to-the-city/bid-opportunities-and-results/?t=current | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (4159 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 351 | https://www.commbuys.com/bso/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2331 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 352 | https://www.commbuys.com/bso/view/login/login.xhtml | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2331 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 353 | https://www.contrax.company/ | 200 | SUCCESS | 4 | Aggregator homepage; 4 example bids with posted dates on public detail pages (all Unmatched). Full notices gated ($9). |
| 354 | https://www.cpsk12bids.com/auth/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 355 | https://www.dcwater.com/useful-links | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (1876 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 356 | https://www.demandstar.com/app/suppliers/bids | 200 | BLOCKED | 0 | Login wall |
| 357 | https://www.emarketplace.state.pa.us/Search.aspx | 200 | SUCCESS | 68 | Searched with Posted Since 11/01/2026 (97 rows, amended-date based); 75 had Solicitation Start Date on/after 11/01; 7 already saved earlier (6100066854, 6100066981, 6100066903, DOT-RFP006720, 6100066848, 6100066994, SCI Camp Hill Sewer Upgrade) were skipped; 68 new added (4 Matched). |
| 358 | https://www.frederickcountymd.gov/1116/Open-Bids---Current-Solicitations | 200 | NO_RELEVANT_RESULTS | 0 | Public procurement page readable; no solicitation with issue/posted date on/after 2026-11-01 shown |
| 359 | https://www.govevents.com/?signoutsucccess | 200 | NO_RELEVANT_RESULTS | 0 | Events/webinars calendar only; no solicitations. Effectively not applicable. |
| 360 | https://www.infotechexpress.com/business | 200 | BLOCKED | 0 | Login wall |
| 361 | https://www.instantmarkets.com/home | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2652 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 362 | https://www.kalcounty.com/ | 403 | BLOCKED | 0 | HTTP 403; bot-check/WAF/access denied |
| 363 | https://www.kcsdschools.net/dept/finance/procurement | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (6498 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 364 | https://www.laramiecountywy.gov/Request-for-Proposals | 200 | NO_RELEVANT_RESULTS | 0 | Public procurement page readable; no solicitation with issue/posted date on/after 2026-11-01 shown |
| 365 | https://www.matawanborough.com/matawan/Bid%20Notices%20and%20Requests%20for%20Proposals/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (7094 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 366 | https://www.mecknc.gov/finance/procurement/Pages/default.aspx | 404 | FAILED | 0 | HTTP 404 |
| 367 | https://www.mymta.info/psc/VENDOR/GUEST/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 368 | https://www.mymta.info/psc/VENDOR/SUPPLIER/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP | 200 | BLOCKED | 0 | Login wall |
| 369 | https://www.myvendorlink.com/external/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 370 | https://www.njstart.gov/bso/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (2951 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 371 | https://www.njstart.gov/bso/external/vendor/regComSrvcCodes.sdo | 500 | FAILED | 0 | HTTP 500 |
| 372 | https://www.northwestmsbids.com/ | 200 | SUCCESS | 1 | 2 projects accepting bids. RFP #27-012-06 Technical Coordinator (ad run Nov 3 & Nov 10) added as Matched. 63663 NWCC Agriculture Technology Facility (REBID) ad ran 10/23 and 10/30 (before cutoff). Project files are login-gated; detail text is public. |
| 373 | https://www.nunavuttenders.ca/UploadBidderTC.aspx | 200 | BLOCKED | 0 | Login wall |
| 374 | https://www.nyscr.ny.gov/ | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (3362 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 375 | https://www.nyscr.ny.gov/login.cfm | 404 | FAILED | 0 | HTTP 404 |
| 376 | https://www.ptcvendorportal.com/ | 200 | BLOCKED | 0 | Login/registration/supplier-portal landing page; no public solicitation listing visible at this URL (rendered with Chromium) |
| 377 | https://www.ptcvendorportal.com/#/sp/auth/signin | 200 | BLOCKED | 0 | Login wall |
| 378 | https://www.rfpmart.com/ | 200 | BLOCKED | 0 | HTTP 200; bot-check/WAF/access denied |
| 379 | https://www.rfpmart.com/userlogin.html | 200 | BLOCKED | 0 | HTTP 200; bot-check/WAF/access denied |
| 380 | https://www.rochesterhousing.org/bid-opportunities | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (4266 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 381 | https://www.stlmsdplanroom.com/auth/login | 200 | BLOCKED | 0 | Login required to view solicitations |
| 382 | https://www.txsmartbuy.com/esbd | 200 | SUCCESS | 0 | Redirects to https://www.txsmartbuy.gov/esbd (same ESBD listing as the .gov URL). Public, no login. Paged the ESBD service by last-modified until before 2026-11-01: 309 postings with Posting Date >= 2026-11-01; 300 are Posted/Addendum Posted (7 Posting Cancelled, 2 Closed excluded). All 300 recorded in A.json under the .gov portal_url (17 Matched). Detail JSON gave NIGP codes, contact name/email, descriptions. |
| 383 | https://www.txsmartbuy.gov/esbd | 200 | SUCCESS | 300 | Public ESBD listing + detail pages readable without login. 300 qualifying postings (posted 2026-11-01..2026-11-17), 17 Matched, 283 Unmatched (113 are TxDOT highway maintenance/construction lettings). |
| 384 | https://www.voa.va.gov/default.aspx?PageId=1 | 200 | NO_RELEVANT_RESULTS | 0 | Page loaded (998 chars); no solicitation with issue/posted date on/after 2026-11-01 found in rendered content |
| 385 | https://yvr.bonfirehub.ca/login | 200 | BLOCKED | 0 | Login wall |
