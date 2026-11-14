# Run status 2026-11-14

Date-filter cutoff: 2026-11-01 (1st of the run month). Method: every URL in `url_reachable.md` was opened individually in a headless Chromium browser (JS rendered); for portal families with a known public listing path (PlanetBids `bo-search`, IonWave `SourcingEvents`, ProcureWare `/Bids`, Periscope BSO open-bids search, Bonfire open-opportunities tab) that public listing on the same portal was opened as well. Detail pages were read for Georgia GPR, NC eVP, PA eMarketplace, BSO and most IonWave items.

Counts: SUCCESS 77 + NO_RELEVANT_RESULTS 151 + BLOCKED 108 + FAILED 49 = 385 (URLs extracted from `url_reachable.md`: 385; the file header says 387 but 385 distinct URL rows exist).

New records saved to `Source/Scraped/`: 801 (51 Matched / Matched-unconfirmed, 750 Unmatched). 36 further November items seen were already on file from earlier runs and were not duplicated.

## Limits of this run (read before relying on a NO_RELEVANT_RESULTS row)

- **OpenGov (26 portal URLs):** every `procurement.opengov.com/portal/...` page returned a Cloudflare "Just a moment" check — BLOCKED. No workaround was attempted.
- **Bonfire (≈45 URLs):** the public open-opportunities list loads, but it shows closing dates only and each opportunity detail page is behind a Cloudflare check, so no issue date could be confirmed and nothing was saved (date rule 5).
- **Jaggaer / SciQuest (32 URLs):** all redirected to Jaggaer's US maintenance notice (a later retry returned 403) — FAILED this run; retry on a weekday.
- **Minnesota supplier portal:** bid list replaced by a Radware/hCaptcha bot check — BLOCKED.
- **PlanetBids:** listing pages loaded (first ~30 rows per agency, which covers all rows in "Bidding" stage); the portal stopped returning content after ~50 page loads, so detail pages could not be opened — PlanetBids matches are tagged "unconfirmed".
- **High-volume state portals:** Texas ESBD (2,526 pages) was read for its first 6 pages (150 most recently updated rows); BidNet public open list (25,771 rows) for its first 3 pages; Illinois BidBuy for the first 25 open bids; Georgia GPR, NC eVP (8 pages), PA eMarketplace (14 pages), Nevada and the Morris County list were paged through. Cal eProcure's event list shows end dates only (no posting date) and was not saved from.
- **Aggregators (RFPMart, BidNet public):** dates are the aggregator's own posted/published dates and agency names are often hidden; those records say so.
- No URL was moved between `url_reachable.md` / `url_unreachable.md` / `url_not_applicable.md` this run: a single failed fetch (e.g. the Jaggaer maintenance window) is not enough to reclassify.

| # | URL | HTTP | Status | Note |
|---|---|---|---|---|
| 001 | http://newhavenhousing.cobblestonesystems.com/gateway/Login.aspx | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 002 | http://njstart.gov/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 003 | http://norta.procureware.com/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 004 | http://procurement.opengov.com/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 005 | http://vendorportal.dc.gov/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 006 | http://www.mncppc.org/register.html | None | FAILED | Error: page.goto: net::ERR_TOO_MANY_REDIRECTS at https://www.mncppc.org/register |
| 007 | http://www.morriscountybidsystem.com/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 008 | http://www.scsk12.org/procurement/bids | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 009 | https://a856-cityrecord.nyc.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 010 | https://access.alberta.ca/auth/realms/41898876-5358-402d-aae5-eee17a413de5/protocol/openid-connect/auth?client_id=apc-app&redirect_uri=https%3A%2F%2Fpurchasing.alberta.ca%2Fauth-callback&response_type=code&scope=openid&state=bbfd4bd389cb423a98165473274390b5&code_challenge=7gPvK1m6Ml4-FdLaOsGEF5qqfo6D4i1z5YQag7pazSY&code_challenge_method=S256&response_mode=query&apc_target=supplier | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 011 | https://account.bonfirehub.com/login?flow=e128e6d0-9c89-447a-a993-8965998b25cf | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 012 | https://acwd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (2 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 013 | https://alabamabuys.gov/page.aspx/en/sup/registration_extranet/save | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 014 | https://alabamabuys.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 015 | https://alamedahsg.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 016 | https://alexandriava.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 017 | https://algonquincollege.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 018 | https://alleghenycounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 019 | https://allentx.ionwave.net/Vendor/VendorHome.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 020 | https://alohaebuys.hawaii.gov/bso/view/login/login.xhtml | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 021 | https://app.az.gov/page.aspx/en/sup/registration_extranet/save | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 022 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=GIT&supplierID=1007876976&tmstmp=1763649218182 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 023 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=UMich&supplierID=1007876976&tmstmp=1750096171684 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 024 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1733233768378 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 025 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1757684588373 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 026 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1768591824093 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 027 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1769709497801 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 028 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1782391392219 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 029 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 030 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState&AuthToken=1%3AAES2%23COeR%2B9y0uJonDteiKZ%2BEXAT%2F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%2FPIsK26ub%2FRR7PdwEzslABhuOduB5H9gT3N0M3ug%2FeRnMZKr3z3NgtkQNLRexTFFmXjo%2BndLeXxoucMxlzNwPcEg%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523COeR%252B9y0uJonDteiKZ%252BEXAT%252F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%252FPIsK26ub%252FRR7PdwEzslABhuOduB5H9gT3N0M3ug%252FeRnMZKr3z3NgtkQNLRexTFFmXjo%252BndLeXxoucMxlzNwPcEg%253D%253D%26CustOrg%3DCalState%26EventId%3D1236956%26SupplierId%3D%26tmstmp%3D1721417133691 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 031 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=DASIowa&AuthToken=1%3AAES2%23CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%2BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%2FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%252BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%252FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%253D%253D%26CustOrg%3DDASIowa%26EventId%3D1308705%26SupplierId%3D%26tmstmp%3D1745010830840 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 032 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=FSU&AuthToken=1%3AAES2%23CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%2BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%2FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%2FDqCHvRcdLpLfA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%252BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%252FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%252FDqCHvRcdLpLfA%253D%253D%26CustOrg%3DFSU%26EventId%3D1336325%26SupplierId%3D%26tmstmp%3D1757094185862 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 033 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=MDAndersonPS | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 034 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=StateOfNewMexico | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 035 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TAMU | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 036 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TriC | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 037 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UConnFullSuite&AuthToken=1%3AAES2%23CHQBTNcjglgXPI2CtvId3j%2BfPuY04WnaPu%2BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%2FalXbKWUgJXI%2F4ESN2t3wNRSEH%2Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CHQBTNcjglgXPI2CtvId3j%252BfPuY04WnaPu%252BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%252FalXbKWUgJXI%252F4ESN2t3wNRSEH%252Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%253D%253D%26CustOrg%3DUConnFullSuite%26EventId%3D1385650%26SupplierId%3D%26tmstmp%3D1777294149216 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 038 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UIdaho | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 039 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=URI | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 040 | https://apps.cupertino.org/details/756 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 041 | https://apps.das.nh.gov/bidscontracts/bids.aspx | 403 | BLOCKED | HTTP 403 bot-check/WAF (Access Denied) |
| 042 | https://apps.ideal-logic.com/uopcs | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 043 | https://arbuy.arkansas.gov/bso/view/login/login.xhtml | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 044 | https://arkansas.ionwave.net/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 045 | https://baltimorecity.diversitycompliance.com/FrontPage/VendorMain.asp?XID=2708 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 046 | https://baltimorecounty.prismcompliance.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 047 | https://bernco.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (2 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 048 | https://bgca.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 049 | https://bgs.vermont.gov/purchasing | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 050 | https://biddingo.com/soundtransit | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 051 | https://bidlocker.us/Home/bidlockerus | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 052 | https://bidopportunities.chugachelectric.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 053 | https://bidportal.ksu.edu/Module/Tenders/en/Vendor/Dashboard/70f4d5cf-dabf-47c6-a618-3522733a7088 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 054 | https://bids.sciquest.com/apps/Router/PublicEvent?CustomerOrg=GIT | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 055 | https://bids.wyomingmi.gov/Bid/SpecDownload/2236?fromLogin=1 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 056 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=Georgia&FromBranded=true | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 057 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=SUNY&FromBranded=true | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 058 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=UTSA&FromBranded=true | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 059 | https://bouldercounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (12 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 060 | https://brazosbid.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 061 | https://caleprocure.ca.gov/pages/Events-BS3/event-search.aspx | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 062 | https://camisvr.co.la.ca.us/LACoBids/BidLookUp/OpenBidList | 403 | BLOCKED | HTTP 403 bot-check/WAF () |
| 063 | https://cammnet.octa.net/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 064 | https://ccsd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 065 | https://certification-app.sbsd.virginia.gov/boLogin | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 066 | https://ci-lubbock-tx.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (11 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 067 | https://cityofbonitasprings.procureware.com/ | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 068 | https://cityofbonitasprings.procureware.com/login | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 069 | https://claytonk12ga.bonfirehub.com/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 070 | https://cob.procureware.com/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 071 | https://comalisd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 072 | https://comet-fs.ci.minneapolis.mn.us/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=ERP.SUPPLIER.EP_COSP_PUBLIC_HOME_FL | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 073 | https://contracts-marioncountygcc.msappproxy.net/gateway/Login.aspx | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 074 | https://cookcountyhealth.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 075 | https://cookcountyil.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 076 | https://davenport.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 077 | https://daviefl.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 078 | https://dfwairport.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (16 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 079 | https://dhr.alabama.gov/announcements/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 080 | https://dir.my.site.com/BidStamp/VIS_CustomLogin | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 081 | https://dmschools.ionwave.net/Vendor/VendorHome.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 082 | https://dmschools.procureware.com/Companies?t=Info | 404 | FAILED | landing page loaded but the public open-bids page returned HTTP 404 |
| 083 | https://douglascountypurchasing.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 084 | https://ebs.pnnl.gov/advertised.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 085 | https://ecsd.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (8 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 086 | https://ejbs.fa.us6.oraclecloud.com/supplierPortal/faces/FndOverview?fndGlobalItemNodeId=itemNode_supplier_portal_supplier_portal | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 087 | https://emma.maryland.gov/page.aspx/en/usr/login?ReturnUrl=%2fpage.aspx%2fen%2fbuy%2fhomepage | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 088 | https://eprocurement.esmsolutions.com/resetpassword?Token=935c91e0-3b71-4706-88a0-2cc4dc6d5da7 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 089 | https://esupplier.erp.delaware.gov/psc/fn92pdesup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 090 | https://esupplier.sonomacounty.ca.gov/psc/FN92PRD_9/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?Page=PT_LANDINGPAGE&Action=H | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 091 | https://fairfaxcounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 092 | https://fayetteville-ar.ionwave.net/Login.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 093 | https://fayetteville-ga.ionwave.net/Login.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 094 | https://financials.ok.gov/psc/SOKLFP1DS/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 095 | https://flyri.com/riac/procurement/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 096 | https://fms-prd.ps.sc.edu/psc/FPRD/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 097 | https://fortworthtexas.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (17 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 098 | https://fscm.teamworks.georgia.gov/psc/supp/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 099 | https://garwoodnj.govoffice3.com/index.asp?SEC=2E0FA122-5AAF-4709-8370-F01AB70B1579&pri=0 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 100 | https://gccisd.ionwave.net/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 101 | https://ggbhtd.bonfirehub.com/portal/ | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 102 | https://goodbuy.ionwave.net/Login.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 103 | https://govwhitepapers.com/?utm_source=GovEvents&utm_medium=NavBar | 429 | BLOCKED | HTTP 429 bot-check/WAF (Vercel Security Checkpoint) |
| 104 | https://guest.supplier.systems.state.mn.us/psc/fmssupap/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | BLOCKED | MN portal: bidding-opportunities pagelet replaced by hCaptcha bot check |
| 105 | https://ha.internationaleprocurement.com/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 106 | https://habc.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (4 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 107 | https://hacp.org/profile/business-developmentommincorp-com/ | 404 | FAILED | HTTP 404 |
| 108 | https://hamiltoncountyohio.gob2g.com/?TN=hamiltoncountyohio | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 109 | https://hcpss.bonfirehub.com/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 110 | https://health.maryland.gov/procumnt/pages/procopps.aspx?utm_source=chatgpt.com | 404 | FAILED | HTTP 404 |
| 111 | https://homesa.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 112 | https://hosting.portseattle.org/sops/ | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 113 | https://hosting.portseattle.org/sops/#/Dashboard | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 114 | https://hub.edison.tn.gov/psc/fsprd/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?LP=EP_COSP_PUBLIC_HOME_FL& | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 115 | https://idcs-9275a5d3c7c74bb390dab405c8de5456.identity.oraclecloud.com/ui/v1/signin | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 116 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=20134&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A20134%7D&agency_name=North+County+Transit+District&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Freset-password | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 117 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=53010&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A53010%7D&agency_name=Long+Beach+City+College&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Freset-password | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 118 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=73214&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A73214%7D&agency_name=Sacramento+Municipal+Utility+District&agency_logo=https%3A%2F%2Ffiles-prod01.planetbids.com%2Ff73214%2F20250428114636755+SMUD_Logo_4c.png&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Freset-password | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 119 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=39471&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A39471%7D&agency_name=San%20Diego%20Housing%20Commission | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 120 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=41576&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A41576%7D&agency_name=City%20of%20Menifee | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 121 | https://idm-global.j1p.jaggaer.com/auth/realms/j1p-supplier-idm/login-actions/authenticate?client_id=prod-idp.app.jaggaer.com&tab_id=DvM31H7SmPk | 400 | BLOCKED | login wall — no public listing reachable from this URL |
| 122 | https://iehp.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 123 | https://iris-vss.alaska.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 124 | https://jeffersoncitymo.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 125 | https://jocogov.ionwave.net/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 126 | https://jocogov.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 127 | https://kbrsupplier.com/default.aspx | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 128 | https://knoxbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 129 | https://lacounty.gov/business/doing-business-with-la-county/lac-purchasing-and-contract-opportunities/ | 403 | BLOCKED | HTTP 403 bot-check/WAF () |
| 130 | https://lagoverpvendor.doa.louisiana.gov/irj/portal | 502 | FAILED | HTTP 502 |
| 131 | https://lajoyaisd.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 132 | https://lakeworthbeachfl.bidsandtenders.net/Module/Tenders/en/Home/BidsHomepage | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 133 | https://lawa.bonfirehub.com/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (5 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 134 | https://lcpscm.ionwave.net/VendorRegistration/CompanyInfo.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 135 | https://leegov.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 136 | https://lexingtoncounty.ionwave.net/Vendor/VendorHome.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 137 | https://lexingtonky.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 138 | https://login-euxp-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?ECID-Context=1.0062xRLviAgFS8V5u30FyX0007aI0003xm%3BkXjE | 503 | FAILED | HTTP 503 |
| 139 | https://login-exkk-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3D5KbKcxXM%2Fj31a5DXL88CkKQxNL8xTgjx4o0T1qvnZ%2Fm8L2PVioR3VV1mC34DycQZg0dWLUr3o1012giKiZTeLaHBd98AahIgscHY6X%2BjknHWJTGvHe2M7sMJAhATajCClH2Gx0nkCL6bzAbl%2BeHZ6uiXgB%2B2hOmd%2FQzizf5Y4YNkakpfRK5yMBTn8PZ9OsPNGrM%2B9IEZeXceK4jlLN54auwgY6%2B6KY4M7NGvbtyUVhrexBSDMkJ1OjzgiQG26s7nUNgDOOBUY1V47R2%2FWeMq%2Bd5RS64LygmWx1uZVUYM2hKWN3EGASc%2FSKuhZmDEEqqbRerUTv8simlP4wr9hR9Mpg0V0hRCebgR0PJpg4%2BHF7Ag3SZ7q9E7%2BHfRzp%2F3W%2B3GmJQk%2BTkTLecO55P653z0xHK1qj1hCGfUC%2F7kmkzXjp1zFdxcYxy0Wmms4vL3XeoVshFxno55Xarw4aCIFXtNTxZWRW7uf5m0Zw2p6WcH89Wrs2vxPwt6PMezO3rioKyymXYA0SEkvDg3C%2FapCuEENBINGbNbfVXmU9HJ3r8XnlclYMyGyIGLAznYm98%2BiO%2F0AWsh3bbiaxSI9qt8veZReDf6Rn9T76JBWjcttWwXXZET%2BU4t5KxKqJ1QJxPAEhmZzJZ2sRAm4bRXVI4ODGQRpEciLt8Lj3lB9rFv9tqgF10%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3D75ca2eec8e5ee3dbd0b2a672207ad24ecf7dc56a&ECID-Context=1.006Ivf_oUN8AxGKayTaeMG0060Ok0001FM%3BkXjE | 503 | FAILED | HTTP 503 |
| 140 | https://login-ibqhjb.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3DxS138OL6YUFqo5kXqhatUBRr5X3V1RGL4k%2Bz0kVeSsDqPlMtLQOkCPPbjyD9zFAHBZaV%2B4%2Bm1%2BC15RRXqDUzJfqgkiyvt3ZB8iYpaRVN9qApx0UAl6kxqVcVIFnLXt9LuTk4KALc3n4SIQddr6q6%2BOFzVzgiKyWa3cqoE2V12YBzK8Pi2SYryl1afztYU9JVUJP29U%2FlKJqV7biRJbQE9H2sPdqJv3kpoyqbSpybx21q5XYhaPoGc2tLTa6xi%2FRfih66LyuMO4FMp8vH5zA12aZ9ltzcyzAVFI3x7uQLcAh6pHQm7VqoYEwfyhjgh7FaYQ9cE67Q%2BeRAkhh0r5dlkA%2Fjbd93rdrtDAMuzNqFGgeGYMM%2F3wqSyRTAXhDr9kp1RGsdNmsK1lr6FA9OZ2brJTDDbjPwVNPLMB3TyYleKacbH9%2FXviCjUQ%2FHwzgt5a9ZuBGEumvbK0TxwMpgsJ0yu0jXJ6%2BfZNKN5%2FaG4Pxi2jY47gyzltsiogFvef6dIlZzVXVFjPIDgDWoc%2BR0v7%2BtJDZbAdRc3bNMWuWNuFlHz2%2BemlSYNUCtIqoSCOFJ3PMxgHpdIwsCoLnHZ1A0BPrjrnmeJlZ1BLCj1XMN8aCDPaJXMm8GUoFpBDoJcVgnroYkpEYrk4FICQDlSWQJyHDEZvAyf8mrlleFvHliIKe7iqCM0VrJPJxOx3XLM4%2FFoSIgzv34BqFfX4c4fRTLYbEEbRj5%2FXmyMe04mzMmfdsm1rdZs7boBYCvTXKmhklZQme33TFM26PGec1T0ZnFkODoiPWb3%2FSouG2DGmvCBo7uh0cfmdMNlRngKQDEg9Gi8IlTDr5a4zrqqOzUe5eYoFAwMHRnZ%2Bi9XY%2B%2FbqXxXqBVLWnW6hwImdtNFjXGJuER7GbvbnYWaahNTQQ5aBDezpKFOUdrjSKzI6ICdCnXnnpPo%2BgKo9HQXsMrFc89CE%2BnPbXiforjn%2FjUa7sPlnIN3occRYXNafpmYekQzHYI%2F5J1L1TsBHOdebeWGx20HeLYJXFOWGup58ViARCFzp0cgp8GZntiBKsdecvdg97v5k3sO5HEWS96IYcQHlDmXIdsdBsPOG1cvSJ1JixuseaaZM5OMnOTxpsV1uToblun5Vs6DfOgTv3VUQXVevMFCyC%2BTBucOnTiZCfdT92T%2Bp1XkdveKsJ2jeRebG165AKqLnEJ5eZQhBs6eWn9v%2FRow0mdfeKFavO7Fr%2FXELn9GXe13oQh0sy0RX4kW1qvKVWgI9%2FfiVQMikBsESPOFMA5dwtAFr%2BggEb7aYvdjXYs6zvmlxNxNyXwN2m3GcH7mf%2FopLRrFKVdnqD00kjja5i%2FNebYOfMTMGLVHIoL5EorazZ1hyrc2bafEjj63su3Ns2ltD0kTZvQpgdySfeQEZ21WjibhABsOHZ9SPQE91Ss5TAF6LYkOztU1VyaPmp5g%2BEwbirV3o%2FDo9a%2Fi%2By%2BFvDpPWBkpt2bIHXxWj%2F3699%2BniBsU97TRPn3nRmAmTie6HCRb0kH4k1oTrl70mjMjsI8O3bhdvhj1EnFU8r6ZSszcyTneTE%2Bma7MCYbylmnwQppds6nbIQFyzq4UMv1nLeAS3MHFZkThUexNB165wz0ycXAKMEqID%2FiVHZok2XfhRFfcA2bIk7Y%2FiBD1CplaGU%2F30%2FTC0u61H3iD5Hulp7L5f7jBTp5IjQ%3D%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3Db7d14dfa13cdabd935ca9c7841fb201bfe34a229&ECID-Context=1.006Ji0n6W6n2FSMqyKvX6G003mVL0000wW%3BkXjE | 503 | FAILED | HTTP 503 |
| 141 | https://login.ehawaii.gov/lala | 403 | BLOCKED | HTTP 403 bot-check/WAF (403 Forbidden) |
| 142 | https://login.neighborlysoftware.com/neighborlysoftware.onmicrosoft.com/oauth2/v2.0/authorize?p=b2c_1_signinsignup_prod&client_id=ab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4&response_type=code%20id_token%20token&scope=openid%20email%20profile%20offline_access%20https%3A%2F%2Fneighborlysoftware.onmicrosoft.com%2Fab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4%2FPortal.Read&state=OpenIdConnect.AuthenticationProperties%3DRibwqB29N7HFG%2FlYtBVU9VQQ%2F47hId8udQ7Qgw4gCV5RWxEAhOVi1FNfkygg3UHLQ92Mm5nrr7PtxBGK1Ctu7VQZKAYDWo1Zw0GNewqepMxUgBtdID6wPyRuFfOCGSGsZoucI%2BKrCfxrtk7ZCE%2FsJ6Fer9k%2FkgDMMI%2Bj5ydxbYJsha6Ju%2BbwJkxl2iKxSiWbg7bz%2BzIArwJ%2BKqV8SCsJ5z%2FkyP%2BUts8TiW0nywmKbnDvMxsR8D%2B5A4UNFkxpwjbymbOFiHW9PXRCHqkEhImRWJSDNKMCqIj80loL00VhBpNteMaRXZDaK%2BHEml%2Fw1MkUBLxhoIJQTxiupyJBRNxRhG6dB%2BbWh7CUp1uHipB2lRr8sAjsfh8IPD18auSh31%2Byv71fC0%2FI2e7Kct5SLawcqg%3D%3D&response_mode=form_post&nonce=639174124887079482.NGJmZDQ0N2EtZjkwNi00ZmY4LWI4MWItNmRkMDcwMTQyNTIzMzYyNWQ4MWUtMjExYy00Yjc4LThlMDYtOWJlZDA4YzNhZDdi&tenantCode=waterlooia&portalType=contractor&nTenantId=490&ui_locales=en&machineCode=00000000-0000-0000-0000-000000000000&redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Floginredirectcomplete&post_logout_redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Fwaterlooia%2Fcontractor&x-client-SKU=ID_NET472&x-client-ver=7.5.0.0 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 143 | https://lonestar.ionwave.net/SourcingEvents.aspx?SourceType=1 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 144 | https://longbeachbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 145 | https://lrsd.ionwave.net/Login.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 146 | https://madisonal.procureware.com/login | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 147 | https://marketplace.unisonglobal.com/login.do?resource_name=marketplace | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 148 | https://mdapex.ecenterdirect.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 149 | https://mdcourts.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (5 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 150 | https://mdstad.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (2 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 151 | https://mecknc-vss.hostams.com/PRDVSS1X1/Advantage4 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 152 | https://menv.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (3 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 153 | https://mevss.hostams.com/PRDVSS1X1/AltSelfService | 404 | FAILED | HTTP 404 |
| 154 | https://miamiu-ohiousourcing.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 155 | https://mps.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 156 | https://mtc.bonfirehub.com/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (6 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 157 | https://mwrd.app/Cntrctann/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 158 | https://mwrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 159 | https://my.alaska.gov/adfs/ls/?wa=wsignin1.0&wtrealm=https%3a%2f%2fmy.alaska.gov%2f&wctx=rm%3d0%26id%3dpassive%26ru%3d%252fPortal%252fPortal.aspx&wct=2023-11-24T17%3a55%3a54Z | 403 | BLOCKED | HTTP 403 bot-check/WAF (alaska.gov) |
| 160 | https://myncid.nc.gov/index.html | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 161 | https://myncid.nc.gov/index.html#/main/userProfile | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 162 | https://myok-staffing.onconcourse.com/login?type=partner | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 163 | https://nait.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (6 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 164 | https://nevada.ionwave.net/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 165 | https://nsc.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 166 | https://ntmwd.bonfirehub.com/registration | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (6 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 167 | https://ny.newnycontracts.com/FrontPage/VendorMain.asp?XID=4111 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 168 | https://octa.govqa.us/WEBAPP/_rs/(S(hn5r0labmmsdycjs2dfu2bmf))/SupportHome.aspx?sSessionID=136023057:64058TERBOPBL%5BFZ%5BSWSTLWXOUBTSH | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 169 | https://oklahoma.gov/omes/divisions/central-purchasing/suppliers-and-payees/supplier-portal.html | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 170 | https://onesource.wsscwater.com//OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 171 | https://onesource.wsscwater.com/OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 172 | https://onlineservices.osc.state.ny.us/Enrollment/login?17 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 173 | https://oregonbuys.gov/bso/view/login/login.xhtml | 200 | FAILED | landing page loaded but the public open-bids page returned HTTP 502 |
| 174 | https://passport.cityofnewyork.us/page.aspx/en/buy/homepage/ven | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 175 | https://pasupplierportal.state.pa.us/irj/portal/anonymous | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 176 | https://pbcvssp.co.palm-beach.fl.us/webapp/vssp/AltSelfService?EmailToken=02730029218941640788 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 177 | https://pbsystem.planetbids.com/portal/13821/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 178 | https://pbsystem.planetbids.com/portal/13982/login | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 179 | https://pbsystem.planetbids.com/portal/13982/login# | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 180 | https://pennbid.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (139 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 181 | https://pinalcountyaz.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (5 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 182 | https://pr-webs-vendor.des.wa.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 183 | https://pro.prismcompliance.com/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 184 | https://pro.prismcompliance.com/default.aspx | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 185 | https://procure.cgieva.com/page.aspx/en/sup/registration_extranet/save | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 186 | https://procure.portlandoregon.gov/bso/seller/bidAck.sdo | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 187 | https://procurement.opengov.com/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 188 | https://procurement.opengov.com/portal/aurorail | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 189 | https://procurement.opengov.com/portal/baltimorecountymd | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 190 | https://procurement.opengov.com/portal/bft | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 191 | https://procurement.opengov.com/portal/bloomingtonin | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 192 | https://procurement.opengov.com/portal/brevardschools | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 193 | https://procurement.opengov.com/portal/cheyennecity | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 194 | https://procurement.opengov.com/portal/cityofbradenton | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 195 | https://procurement.opengov.com/portal/cityofedinburg | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 196 | https://procurement.opengov.com/portal/cityofhomestead | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 197 | https://procurement.opengov.com/portal/cityofnsb | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 198 | https://procurement.opengov.com/portal/cityoftampa | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 199 | https://procurement.opengov.com/portal/clevelandoh | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 200 | https://procurement.opengov.com/portal/co-hidalgo-tx | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 201 | https://procurement.opengov.com/portal/lompoc | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 202 | https://procurement.opengov.com/portal/morenovalley | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 203 | https://procurement.opengov.com/portal/oak-brook | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 204 | https://procurement.opengov.com/portal/pasadena | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 205 | https://procurement.opengov.com/portal/pinoleca | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 206 | https://procurement.opengov.com/portal/rtd-denver | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 207 | https://procurement.opengov.com/portal/saccounty | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 208 | https://procurement.opengov.com/portal/santacruzca | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 209 | https://procurement.opengov.com/portal/smcgov | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 210 | https://procurement.opengov.com/portal/stpete | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 211 | https://procurement.opengov.com/portal/tucson-az | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 212 | https://procurement.opengov.com/portal/tuolumnecountyca | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 213 | https://procurement.opengov.com/portal/wheatridgeco | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 214 | https://procurement.opengov.com/vendors/155272/proposals | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 215 | https://proportal.sourcewell-mn.gov/Module/Tenders/en/Vendor/Dashboard/b50f7d44-0fe6-4ffe-8621-fbae66354482 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 216 | https://purchasing.iu.edu/resources/forms/table.html | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 217 | https://recuperacion.pr.gov/en/procurement-and-nofa/procurement/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 218 | https://sawsbid.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 219 | https://sccpss.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 220 | https://scottsdaleaz.bonfirehub.com/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 221 | https://sdbuynet.sandiegocounty.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 222 | https://secure.bidsandtenders.ca/Module/Tenders/en/Login/Index/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 223 | https://security.app.cpa.state.tx.us/Public/login?logout | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 224 | https://service.ariba.com/Authenticator.aw/ad/ssoIDP | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 225 | https://sigma.michigan.gov/PRDVSS1X1/Advantage4 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 226 | https://smctd.bonfirehub.com/opportunities/112297 | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 227 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=LOGINREQD&_logininst=W68E33gEyArMeQNVR!2B0pO4UAJK!2BQjvLlYP!2BnbMhYU2hA39DrCszSxwAAAYqPkSI!2F&_TKM=492813489&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 228 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=TIMEOUTASSERT&_ssoOrigUrl=https%3A%2F%2Fsms-idaho-prd.tam.inforgov.com%3A443%2Ffsm%2FSupplyManagementSupplier%2Fpage%2FXiSupplyManagementSupplierPage%3Fcsk.SupplierGroup%3DLUMA&_TKM=372688986&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER&LoginId=business-development@ommincorp.com | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 229 | https://sms-nola-prd.inforcloudsuite.com/fsm/SupplyManagementSupplier/page/XiSupplyManagementSupplierPage?csk.SupplierGroup=100 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 230 | https://snoco.procureware.com/login | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 231 | https://solutions.sciquest.com/apps/Router/BrandedSupplierHome?CustOrg=UCOP&supplierID=1007876976&tmstmp=1738093109276 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 232 | https://solutions.sciquest.com/apps/Router/SupplierLogin | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 233 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=BridgewaterState | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 234 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=DASIowa | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 235 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=Princeton&isLogout=true&tmstmp=1716220417643 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 236 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=StateOfUtah&isLogout=true&tmstmp=1699984786288 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 237 | https://solutions.sciquest.com/apps/Router/SupplierLogin?GSPSupplier_Login_Email=Business-development%40ommincorp.com&CustOrg=StateOfMontana&SuccessToken=1&tmstmp=1695233574600 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 238 | https://solutions.sciquest.com/apps/Router/SupplierPortalHome?tmstmp=1699981963442 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 239 | https://solutions.sciquest.com/apps/Router/SupplierWelcome?CustOrg=TriMet&supplierID=1007876976&tmstmp=1704204983800 | 200 | FAILED | Jaggaer platform maintenance notice (retry also returned 403) |
| 240 | https://stamfordct.procureware.com/home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 241 | https://stamfordct.procureware.com/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 242 | https://stillwater.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 243 | https://strathcona.bonfirehub.ca/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (8 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 244 | https://supplier.esmsolutions.com/home | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 245 | https://supplier.ionwave.net/Vendor/VendorHome.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 246 | https://supplier.ionwave.net/VendorLogin.aspx | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 247 | https://supplier.ionwave.net/VendorResponse/ResponseList.aspx?status=AVAILABLE | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 248 | https://supplier.miamidade.gov/ | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 249 | https://supplier.sok.ks.gov/psc/sokfsprdsup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 250 | https://supplier.wmata.com/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 251 | https://supplierservice.sanantonio.gov/irj/portal | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 252 | https://supplierservice.sanantonio.gov/irj/portal#12587465-vendor-info | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 253 | https://tarrantcountytx.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 254 | https://tohowater.bonfirehub.com/login/forgot | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (7 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 255 | https://transitchicago.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (8 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 256 | https://trstexas-supplier.ivalua.app/page.aspx/en/sup/registration_manage/2594 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 257 | https://uiebid.ionwave.net/Login.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 258 | https://upstream.dc.gov/Sourcing/Main/ad/loginPage/SSOActions?awsso_cc=passwordadapter%3AU291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_ru%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbj9wYXNzd29yZGFkYXB0ZXI9U291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_lu%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRMb2dvdXQvU1NPQWN0aW9ucw%3D%3D%3Bawsso_ap%3AQUNN%3Bawsso_arid%3AMTY4ODk5MzA3NjY0NA%3D%3D%3Bawsso_ku%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRLZWVwQWxpdmUvU1NPQWN0aW9ucw%3D%3D%3Bawsso_fl%3AMQ%3D%3D&awsso_ap=ACM&awsso_hpk=true&passwordadapter=SourcingSupplierUser&awsr=true | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 259 | https://upstream.dc.gov/Sourcing/Main?realm=System&passwordadapter=SourcingSupplierUser&awsso_tkn=24MUzqrzky68f28a69a52257ff | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 260 | https://valenciacollege.edu/employees/procurement/solicitations.php | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 261 | https://vendor.myfloridamarketplace.com/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 262 | https://vendor.purchasingconnection.ca/default.aspx | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 263 | https://vendorportal.dc.gov/Account/Login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 264 | https://vendors.planetbids.com/ | None | FAILED | Error: page.goto: net::ERR_TOO_MANY_REDIRECTS at https://vendors.planetbids.com/ |
| 265 | https://vendors.planetbids.com/portal/14599/bo/bo-search | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 266 | https://vendors.planetbids.com/portal/14599/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 267 | https://vendors.planetbids.com/portal/15300/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 268 | https://vendors.planetbids.com/portal/15381/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 269 | https://vendors.planetbids.com/portal/16151/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 270 | https://vendors.planetbids.com/portal/16151/vp/vp-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 271 | https://vendors.planetbids.com/portal/16725/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 272 | https://vendors.planetbids.com/portal/17950/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 273 | https://vendors.planetbids.com/portal/17950/login# | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 274 | https://vendors.planetbids.com/portal/20134/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 275 | https://vendors.planetbids.com/portal/20136/vp/vp-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 276 | https://vendors.planetbids.com/portal/20314/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 277 | https://vendors.planetbids.com/portal/22078/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 278 | https://vendors.planetbids.com/portal/22576/bo/bo-detail/141899 | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 279 | https://vendors.planetbids.com/portal/23532/bo/bo-search | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 280 | https://vendors.planetbids.com/portal/23758/portal-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 281 | https://vendors.planetbids.com/portal/24103/portal-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 282 | https://vendors.planetbids.com/portal/24660/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 283 | https://vendors.planetbids.com/portal/24661/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 284 | https://vendors.planetbids.com/portal/27996/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 285 | https://vendors.planetbids.com/portal/28789/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 286 | https://vendors.planetbids.com/portal/29744/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 287 | https://vendors.planetbids.com/portal/32621/vp/vp-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 288 | https://vendors.planetbids.com/portal/39475/vp/vp-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 289 | https://vendors.planetbids.com/portal/39495/login | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 290 | https://vendors.planetbids.com/portal/39495/login# | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 291 | https://vendors.planetbids.com/portal/39501/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 292 | https://vendors.planetbids.com/portal/43728/vp/vp-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 293 | https://vendors.planetbids.com/portal/45619/bo/bo-search | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 294 | https://vendors.planetbids.com/portal/49906/vp/vp-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 295 | https://vendors.planetbids.com/portal/53010/portal-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 296 | https://vendors.planetbids.com/portal/59724/vp/vp-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 297 | https://vendors.planetbids.com/portal/62287/bo/bo-search | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 298 | https://vendors.planetbids.com/portal/64863/portal-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 299 | https://vendors.planetbids.com/portal/65292/vp/vp-prereg | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 300 | https://vendors.planetbids.com/portal/65844/portal-home | 200 | NO_RELEVANT_RESULTS | public listing read via portal's open-bids page; no solicitation issued on/after 2026-11-01 |
| 301 | https://vendors.planetbids.com/portal/68007/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 302 | https://vendors.planetbids.com/portal/76708/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 303 | https://vendors.planetbids.com/portal/77636/portal-home | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 304 | https://ventura.bonfirehub.com/registration | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (6 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 305 | https://via.diversitycompliance.com/FrontPage/VendorMain.asp?XID=9510 | 404 | FAILED | HTTP 404 |
| 306 | https://via.sbecompliance.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 307 | https://via.sbecompliance.com/?TN=via | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 308 | https://vrapp.vendorregistry.com/Account/LogOn | 429 | BLOCKED | HTTP 429 bot-check/WAF () |
| 309 | https://vrapp.vendorregistry.com/Bids/View/BidsList?BuyerId=c5e9d3e7-b8e0-4e36-bcab-8db00d18d769 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 310 | https://vss.ky.gov/vssprod-ext/Advantage4 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 311 | https://vss.ky.gov/vssprod-ext/Advantage4?openDoc=openDoc&DocumentCode=RFP&DepartmentCode=415&DocumentID=2600000199&DocumentVersNo=2&targetView=ammendHistoryView&Destination=pSolication | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 312 | https://vtbuys.suppliers.vermont.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 313 | https://waukeshacounty.bonfirehub.com/opportunities/144594 | 403 | BLOCKED | HTTP 403 bot-check/WAF (Just a moment...) |
| 314 | https://wrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (0 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 315 | https://ww3.nysif.com/FooterPages/Column1/AboutNYSIF/Procurement | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 316 | https://www.ahfc.us/about-us/notices/requests-proposals | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 317 | https://www.annapolis.gov/bids.aspx | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 318 | https://www.beaconbid.com/solicitations/city-of-houston/121f4067-fb3a-4d30-85b9-ea6a6cafe989/contingent-labor-services-all-categories?token=supplier-login.ObiU4vtGsc_vRNVc-a87JReydRqhQP07ozrco4z95xclrg1KaW517ezRNB5QzTvK8dS9z_wfmREHNc6qRuGr-uHTYI229n9X2AhzK2_xmpo1LIlDsnrcN9YzPY9tkrWfy3EN_v3vttW09t3yqiaBnArwIvYLa3JnzE4G9B1giu5p7FuxEHf2iImOzrCy7TDIptzKNwKUivDO0G3DxgJ4Yz43Iz6gCzrsPGyOdGXCJV9Qg29rKw2IN4_Nw5d1czIABi6VfJW2RJtyEc02dHo1amlJHrAnTsWOtrQ8zz6lolxc5u8OanNPWUJnmTMDrOPoY-3_mtuNxCYeyzX2seLpWEfkAtq1AbX1X_Xb-492Ng&eid=bc055432-0873-482a-98b8-0490d2821dc8 | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 319 | https://www.beaconbid.com/solicitations/city-of-houston/open | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 320 | https://www.bidbuy.illinois.gov/bso/external/vendor/regSummary.sdo?vendorId=NZdPl7Rvv_Oq&mode=initial&dateTime=1694627292171 | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 321 | https://www.bidexpress.com/businesses/85766/home?agency=true | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 322 | https://www.bidnetdirect.com/new-jersey/lbha | 202 | SUCCESS | 2 November IFBs visible (already recorded 2026-11-02; no new record needed) |
| 323 | https://www.bidnetdirect.com/private/supplier/solicitations/search | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 324 | https://www.californiabids.com/bid_opportunities/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 325 | https://www.cdta.org/node/15813/register | 403 | BLOCKED | HTTP 403 bot-check/WAF (Access denied / www.cdta.org) |
| 326 | https://www.centralauctionhouse.com/login.php | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 327 | https://www.cityoftulsa.org/government/departments/finance/selling-to-the-city/bid-opportunities-and-results/?t=current | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 328 | https://www.commbuys.com/bso/view/login/login.xhtml | 200 | FAILED | landing page loaded but the public open-bids page returned HTTP 502 |
| 329 | https://www.cpsk12bids.com/auth/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 330 | https://www.dcwater.com/useful-links | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 331 | https://www.demandstar.com/app/suppliers/bids | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 332 | https://www.frederickcountymd.gov/1116/Open-Bids---Current-Solicitations | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 333 | https://www.govevents.com/?signoutsucccess | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 334 | https://www.infotechexpress.com/business | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 335 | https://www.instantmarkets.com/home | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 336 | https://www.kalcounty.com/ | 403 | BLOCKED | HTTP 403 bot-check/WAF (Attention Required! / Cloudfla) |
| 337 | https://www.kcsdschools.net/dept/finance/procurement | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 338 | https://www.laramiecountywy.gov/Request-for-Proposals | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 339 | https://www.matawanborough.com/matawan/Bid%20Notices%20and%20Requests%20for%20Proposals/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 340 | https://www.mecknc.gov/finance/procurement/Pages/default.aspx | 404 | FAILED | HTTP 404 |
| 341 | https://www.mymta.info/psc/VENDOR/GUEST/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 342 | https://www.mymta.info/psc/VENDOR/SUPPLIER/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 343 | https://www.myvendorlink.com/external/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 344 | https://www.njstart.gov/bso/external/vendor/regComSrvcCodes.sdo | 500 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 345 | https://www.northwestmsbids.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 346 | https://www.nunavuttenders.ca/UploadBidderTC.aspx | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 347 | https://www.nyscr.ny.gov/login.cfm | 404 | FAILED | HTTP 404 |
| 348 | https://www.ptcvendorportal.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 349 | https://www.ptcvendorportal.com/#/sp/auth/signin | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 350 | https://www.rfpmart.com/userlogin.html | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 351 | https://www.rochesterhousing.org/bid-opportunities | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 352 | https://www.stlmsdplanroom.com/auth/login | 200 | BLOCKED | login wall — no public listing reachable from this URL |
| 353 | https://www.txsmartbuy.gov/esbd | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 354 | https://www.voa.va.gov/default.aspx?PageId=1 | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 355 | https://yvr.bonfirehub.ca/login | 200 | NO_RELEVANT_RESULTS | public Bonfire list read (1 open); list shows closing dates only and opportunity detail pages are behind a Cloudflare check, so no issue/start date could be confirmed |
| 356 | https://www.rfpmart.com/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 357 | https://bidsnexus.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 358 | https://bidranger.com/ | 429 | BLOCKED | HTTP 429 bot-check/WAF (Vercel Security Checkpoint) |
| 359 | https://www.bidcontract.com/ | 502 | FAILED | HTTP 502 |
| 360 | https://biddingsimple.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 361 | https://publicbidtracker.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 362 | https://www.busybids.org/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 363 | https://www.contrax.company/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 364 | https://govbidwire.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 365 | https://www.bidnetdirect.com/public/solicitations/open | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 366 | https://procuralerts.com/government-bids | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 367 | https://app.rfpplanner.com/opportunity/match/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 368 | https://thebidbroker.com/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 369 | https://www.txsmartbuy.com/esbd | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 370 | https://pur.doas.ga.gov/gpr/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 371 | https://evp.nc.gov/solicitations/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 372 | https://eva.virginia.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 373 | https://www.emarketplace.state.pa.us/Search.aspx | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 374 | https://www.commbuys.com/bso/ | 200 | FAILED | landing page loaded but the public open-bids page returned HTTP 502 |
| 375 | https://portal.ct.gov/das/ctsource/bidboard | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 376 | https://www.njstart.gov/bso/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 377 | https://oregonbuys.gov/bso/ | 200 | FAILED | landing page loaded but the public open-bids page returned HTTP 502 |
| 378 | https://guest.supplier.systems.state.mn.us/psc/fmssupap_20/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_BID_CMP_FL.GBL?PAGE=SCP_PUB_BIDLIST_FL | 200 | BLOCKED | HTTP 200 bot-check/WAF (Radware Captcha Page) |
| 379 | https://vss.state.co.us/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 380 | https://www.bidbuy.illinois.gov/bso/ | 200 | SUCCESS | November-dated solicitations found on this portal's public listing |
| 381 | https://das.iowa.gov/vendors/bidding-opportunities | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 382 | https://caleprocure.ca.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 383 | https://vendor.myfloridamarketplace.com/search/bids | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 384 | https://vss.ky.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
| 385 | https://www.nyscr.ny.gov/ | 200 | NO_RELEVANT_RESULTS | page loaded; no solicitation with a confirmable issue/start date on/after 2026-11-01 |
