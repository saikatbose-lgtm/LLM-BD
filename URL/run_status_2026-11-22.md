# Run status 2026-11-22

Every URL in `URL/url_reachable.md` (385 unique) was visited individually with headless Chromium (Playwright; DOM rendered, networkidle + 2.5s wait, all frames read). Date cutoff: 2026-11-01 (Issue/Posted/Start date).

- SUCCESS = listing rendered and solicitations with an issue/posted/start date on/after 2026-11-01 were parsed and saved (or were already saved by the 2026-11-04 run).
- NO_RELEVANT_RESULTS = page rendered, but no listing with a qualifying issue/posted date was visible (includes listings that only publish due dates, e.g. Cal eProcure, Anchorage Bid Express, which cannot satisfy the date filter).
- BLOCKED = login wall, CAPTCHA/bot-check, or HTTP 403/429.
- FAILED = navigation error, HTTP 404/5xx, or CDN error page. Not moved to `url_unreachable.md` since servers responded and errors may be transient.

Counts: SUCCESS 21 + NO_RELEVANT_RESULTS 151 + BLOCKED 195 + FAILED 18 = 385 (total URLs 385)

Coverage note: for large portals only the default first page of the listing was parsed (NJ/Morris BidNet was paginated through page 5 until dates fell before the cutoff). Georgia Jaggaer (50 results), NC eVP (237 records), GA GPR, MN SWIFT, PA eMarketplace and the BidNet public aggregator may hold more November postings beyond page 1.

| # | URL | HTTP | Status | Note |
|---|---|---|---|---|
| 1 | http://newhavenhousing.cobblestonesystems.com/gateway/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 2 | http://njstart.gov/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 3 | http://norta.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 4 | http://procurement.opengov.com/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 5 | http://vendorportal.dc.gov/ | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 6 | http://www.mncppc.org/register.html | None | FAILED | page.goto: net::ERR_TOO_MANY_REDIRECTS at http://www.mncppc.org/register.html |
| 7 | http://www.morriscountybidsystem.com/ | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 8 | http://www.scsk12.org/procurement/bids | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 9 | https://a856-cityrecord.nyc.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 10 | https://access.alberta.ca/auth/realms/41898876-5358-402d-aae5-eee17a413de5/protocol/openid-connect/auth?client_id=apc-app&redirect_uri=https%3A%2F%2Fpurchasing.alberta.ca%2Fauth-callback&response_type=code&scope=openid&state=bbfd4bd389cb423a98165473274390b5&code_challenge=7gPvK1m6Ml4-FdLaOsGEF5qqfo6D4i1z5YQag7pazSY&code_challenge_method=S256&response_mode=query&apc_target=supplier | 200 | BLOCKED | login wall – listing not viewable without account |
| 11 | https://account.bonfirehub.com/login?flow=e128e6d0-9c89-447a-a993-8965998b25cf | 200 | BLOCKED | login wall – listing not viewable without account |
| 12 | https://acwd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 13 | https://alabamabuys.gov/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 14 | https://alabamabuys.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 15 | https://alamedahsg.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 16 | https://alexandriava.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 17 | https://algonquincollege.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 18 | https://alleghenycounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 19 | https://allentx.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 20 | https://alohaebuys.hawaii.gov/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 21 | https://app.az.gov/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 22 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=GIT&supplierID=1007876976&tmstmp=1763649218182 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 23 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?CustOrg=UMich&supplierID=1007876976&tmstmp=1750096171684 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 24 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1733233768378 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 25 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1757684588373 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 26 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1768591824093 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 27 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1769709497801 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 28 | https://app01.jaggaer.com/apps/Router/BrandedSupplierHome?tmstmp=1782391392219 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 29 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState | 200 | BLOCKED | login wall – listing not viewable without account |
| 30 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=CalState&AuthToken=1%3AAES2%23COeR%2B9y0uJonDteiKZ%2BEXAT%2F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%2FPIsK26ub%2FRR7PdwEzslABhuOduB5H9gT3N0M3ug%2FeRnMZKr3z3NgtkQNLRexTFFmXjo%2BndLeXxoucMxlzNwPcEg%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523COeR%252B9y0uJonDteiKZ%252BEXAT%252F0wQEtmCgTPxmtdhiaPctxEQmexjpjCV4N49d5X3drP1zeuVcth%252FPIsK26ub%252FRR7PdwEzslABhuOduB5H9gT3N0M3ug%252FeRnMZKr3z3NgtkQNLRexTFFmXjo%252BndLeXxoucMxlzNwPcEg%253D%253D%26CustOrg%3DCalState%26EventId%3D1236956%26SupplierId%3D%26tmstmp%3D1721417133691 | 200 | BLOCKED | login wall – listing not viewable without account |
| 31 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=DASIowa&AuthToken=1%3AAES2%23CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%2BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%2FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CPmLxE194MfNW61Rm11HoQxaKwxKFaW1exWmJwCj40cAzNj7b2BIxBPkLEOcvTtX%252BpJDJkJ5Cx8If85U3HHktBs0WUA2FhXYx4ylKZlWe6Dl8ZUiNC7QW2%252FpGQ9owC7ixKRB2jAVqLQgkMmXJenZQt6oet7RoJWDSA%253D%253D%26CustOrg%3DDASIowa%26EventId%3D1308705%26SupplierId%3D%26tmstmp%3D1745010830840 | 200 | BLOCKED | login wall – listing not viewable without account |
| 32 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=FSU&AuthToken=1%3AAES2%23CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%2BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%2FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%2FDqCHvRcdLpLfA%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CB2x1C8s631A6rCRGO4hHp7Pdx5kHuKL5kzpnL4rN84o8fcYVFGer%252BJObLvWJFPDMhE9q7dBcTQFe0kdKrR09eJ4wKnLUwsW8%252FUwf1ksxDTlsRHbnGqPsZBMyH3SybMT5spbptdoYIb9OLTiTlKg%252FDqCHvRcdLpLfA%253D%253D%26CustOrg%3DFSU%26EventId%3D1336325%26SupplierId%3D%26tmstmp%3D1757094185862 | 200 | BLOCKED | login wall – listing not viewable without account |
| 33 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=MDAndersonPS | 200 | BLOCKED | login wall – listing not viewable without account |
| 34 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=StateOfNewMexico | 200 | BLOCKED | login wall – listing not viewable without account |
| 35 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TAMU | 200 | BLOCKED | login wall – listing not viewable without account |
| 36 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=TriC | 200 | BLOCKED | login wall – listing not viewable without account |
| 37 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UConnFullSuite&AuthToken=1%3AAES2%23CHQBTNcjglgXPI2CtvId3j%2BfPuY04WnaPu%2BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%2FalXbKWUgJXI%2F4ESN2t3wNRSEH%2Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%3D%3D&SuccessToken=3&URL=ViewSourcingEvent%3FAuthToken%3D1%253AAES2%2523CHQBTNcjglgXPI2CtvId3j%252BfPuY04WnaPu%252BnsBcMS8bZ215VDuSfTwsRpPtX3iWiCmxfORXDKW1ZbzYtVoPOKlk1OZVSrvaXn6Zj%252FalXbKWUgJXI%252F4ESN2t3wNRSEH%252Fp3h58an4O5hfgusRc8pKjXGdlS7pAYojg2g%253D%253D%26CustOrg%3DUConnFullSuite%26EventId%3D1385650%26SupplierId%3D%26tmstmp%3D1777294149216 | 200 | BLOCKED | login wall – listing not viewable without account |
| 38 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=UIdaho | 200 | BLOCKED | login wall – listing not viewable without account |
| 39 | https://app01.jaggaer.com/apps/Router/SupplierLogin?CustOrg=URI | 200 | BLOCKED | login wall – listing not viewable without account |
| 40 | https://apps.cupertino.org/details/756 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 41 | https://apps.das.nh.gov/bidscontracts/bids.aspx | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 42 | https://apps.ideal-logic.com/uopcs | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 43 | https://arbuy.arkansas.gov/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 44 | https://arkansas.ionwave.net/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 45 | https://baltimorecity.diversitycompliance.com/FrontPage/VendorMain.asp?XID=2708 | 200 | BLOCKED | login wall – listing not viewable without account |
| 46 | https://baltimorecounty.prismcompliance.com/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 47 | https://bernco.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 48 | https://bgca.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 49 | https://bgs.vermont.gov/purchasing | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 50 | https://biddingo.com/soundtransit | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 51 | https://bidlocker.us/Home/bidlockerus | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 52 | https://bidopportunities.chugachelectric.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 53 | https://bidportal.ksu.edu/Module/Tenders/en/Vendor/Dashboard/70f4d5cf-dabf-47c6-a618-3522733a7088 | 200 | BLOCKED | login wall – listing not viewable without account |
| 54 | https://bids.sciquest.com/apps/Router/PublicEvent?CustomerOrg=GIT | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 55 | https://bids.wyomingmi.gov/Bid/SpecDownload/2236?fromLogin=1 | 200 | BLOCKED | login wall – listing not viewable without account |
| 56 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=Georgia&FromBranded=true | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 57 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=SUNY&FromBranded=true | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 58 | https://bids01.jaggaer.com/apps/Router/PublicEvent?CustomerOrg=UTSA&FromBranded=true | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 59 | https://bouldercounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 60 | https://brazosbid.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 61 | https://caleprocure.ca.gov/pages/Events-BS3/event-search.aspx | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 62 | https://camisvr.co.la.ca.us/LACoBids/BidLookUp/OpenBidList | 403 | FAILED | HTTP 403 / error page |
| 63 | https://cammnet.octa.net/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 64 | https://ccsd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 65 | https://certification-app.sbsd.virginia.gov/boLogin | 200 | BLOCKED | login wall – listing not viewable without account |
| 66 | https://ci-lubbock-tx.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 67 | https://cityofbonitasprings.procureware.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 68 | https://cityofbonitasprings.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 69 | https://claytonk12ga.bonfirehub.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 70 | https://cob.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 71 | https://comalisd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 72 | https://comet-fs.ci.minneapolis.mn.us/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=ERP.SUPPLIER.EP_COSP_PUBLIC_HOME_FL | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 73 | https://contracts-marioncountygcc.msappproxy.net/gateway/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 74 | https://cookcountyhealth.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 75 | https://cookcountyil.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 76 | https://davenport.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 77 | https://daviefl.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 78 | https://dfwairport.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 79 | https://dhr.alabama.gov/announcements/ | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 80 | https://dir.my.site.com/BidStamp/VIS_CustomLogin | 200 | BLOCKED | login wall – listing not viewable without account |
| 81 | https://dmschools.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 82 | https://dmschools.procureware.com/Companies?t=Info | 404 | FAILED | HTTP 404 / error page |
| 83 | https://douglascountypurchasing.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 84 | https://ebs.pnnl.gov/advertised.aspx | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 85 | https://ecsd.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 86 | https://ejbs.fa.us6.oraclecloud.com/supplierPortal/faces/FndOverview?fndGlobalItemNodeId=itemNode_supplier_portal_supplier_portal | 200 | BLOCKED | login wall – listing not viewable without account |
| 87 | https://emma.maryland.gov/page.aspx/en/usr/login?ReturnUrl=%2fpage.aspx%2fen%2fbuy%2fhomepage | 200 | BLOCKED | login wall – listing not viewable without account |
| 88 | https://eprocurement.esmsolutions.com/resetpassword?Token=935c91e0-3b71-4706-88a0-2cc4dc6d5da7 | 200 | BLOCKED | login wall – listing not viewable without account |
| 89 | https://esupplier.erp.delaware.gov/psc/fn92pdesup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | BLOCKED | login wall – listing not viewable without account |
| 90 | https://esupplier.sonomacounty.ca.gov/psc/FN92PRD_9/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?Page=PT_LANDINGPAGE&Action=H | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 91 | https://fairfaxcounty.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 92 | https://fayetteville-ar.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 93 | https://fayetteville-ga.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 94 | https://financials.ok.gov/psc/SOKLFP1DS/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 95 | https://flyri.com/riac/procurement/ | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 96 | https://fms-prd.ps.sc.edu/psc/FPRD/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 97 | https://fortworthtexas.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 98 | https://fscm.teamworks.georgia.gov/psc/supp/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 99 | https://garwoodnj.govoffice3.com/index.asp?SEC=2E0FA122-5AAF-4709-8370-F01AB70B1579&pri=0 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 100 | https://gccisd.ionwave.net/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 101 | https://ggbhtd.bonfirehub.com/portal/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 102 | https://goodbuy.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 103 | https://govwhitepapers.com/?utm_source=GovEvents&utm_medium=NavBar | 429 | BLOCKED | HTTP 429 bot-check/CAPTCHA/WAF |
| 104 | https://guest.supplier.systems.state.mn.us/psc/fmssupap/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 105 | https://ha.internationaleprocurement.com/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 106 | https://habc.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 107 | https://hacp.org/profile/business-developmentommincorp-com/ | 404 | FAILED | HTTP 404 / error page |
| 108 | https://hamiltoncountyohio.gob2g.com/?TN=hamiltoncountyohio | 200 | BLOCKED | login wall – listing not viewable without account |
| 109 | https://hcpss.bonfirehub.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 110 | https://health.maryland.gov/procumnt/pages/procopps.aspx?utm_source=chatgpt.com | 404 | FAILED | HTTP 404 / error page |
| 111 | https://homesa.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 112 | https://hosting.portseattle.org/sops/ | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 113 | https://hosting.portseattle.org/sops/#/Dashboard | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 114 | https://hub.edison.tn.gov/psc/fsprd/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?LP=EP_COSP_PUBLIC_HOME_FL& | 200 | BLOCKED | login wall – listing not viewable without account |
| 115 | https://idcs-9275a5d3c7c74bb390dab405c8de5456.identity.oraclecloud.com/ui/v1/signin | 200 | BLOCKED | login wall – listing not viewable without account |
| 116 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=20134&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A20134%7D&agency_name=North+County+Transit+District&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F20134%2Freset-password | 200 | BLOCKED | login wall – listing not viewable without account |
| 117 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=53010&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A53010%7D&agency_name=Long+Beach+City+College&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F53010%2Freset-password | 200 | BLOCKED | login wall – listing not viewable without account |
| 118 | https://identity.planetbids.com/identity/public/client/login.html?appCode=portal&agency_id=73214&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A73214%7D&agency_name=Sacramento+Municipal+Utility+District&agency_logo=https%3A%2F%2Ffiles-prod01.planetbids.com%2Ff73214%2F20250428114636755+SMUD_Logo_4c.png&organizationId=organization-live-4b1a8e07-9503-4b5c-8dea-4e537ec156ff&enableOtpLogin=true&showOtpPrompt=false&registerUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Fvp%2Fvp-prereg&forgotPasswordUrl=https%3A%2F%2Fvendors.planetbids.com%2Fportal%2F73214%2Freset-password | 200 | BLOCKED | login wall – listing not viewable without account |
| 119 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=39471&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A39471%7D&agency_name=San%20Diego%20Housing%20Commission | 200 | BLOCKED | login wall – listing not viewable without account |
| 120 | https://identity.planetbids.com/identity/public/oauth/login?appCode=portal&agency_id=41576&client_id=connected-app-live-a6ef820a-76d1-4cab-9e2c-26e9f246cf8f&redirect_uri=https%3A%2F%2Fvendors.planetbids.com%2Foauth%2Fcallback&state=%7B%22agency_id%22%3A41576%7D&agency_name=City%20of%20Menifee | 200 | BLOCKED | login wall – listing not viewable without account |
| 121 | https://idm-global.j1p.jaggaer.com/auth/realms/j1p-supplier-idm/login-actions/authenticate?client_id=prod-idp.app.jaggaer.com&tab_id=DvM31H7SmPk | 200 | BLOCKED | login wall – listing not viewable without account |
| 122 | https://iehp.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 123 | https://iris-vss.alaska.gov/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 124 | https://jeffersoncitymo.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 125 | https://jocogov.ionwave.net/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 126 | https://jocogov.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 127 | https://kbrsupplier.com/default.aspx | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 128 | https://knoxbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 129 | https://lacounty.gov/business/doing-business-with-la-county/lac-purchasing-and-contract-opportunities/ | 403 | FAILED | HTTP 403 / error page |
| 130 | https://lagoverpvendor.doa.louisiana.gov/irj/portal | 200 | BLOCKED | login wall – listing not viewable without account |
| 131 | https://lajoyaisd.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 132 | https://lakeworthbeachfl.bidsandtenders.net/Module/Tenders/en/Home/BidsHomepage | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 133 | https://lawa.bonfirehub.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 134 | https://lcpscm.ionwave.net/VendorRegistration/CompanyInfo.aspx | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 135 | https://leegov.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 136 | https://lexingtoncounty.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 137 | https://lexingtonky.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 138 | https://login-euxp-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?ECID-Context=1.0062xRLviAgFS8V5u30FyX0007aI0003xm%3BkXjE | 503 | FAILED | HTTP 503 / error page |
| 139 | https://login-exkk-saasfaprod1.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3D5KbKcxXM%2Fj31a5DXL88CkKQxNL8xTgjx4o0T1qvnZ%2Fm8L2PVioR3VV1mC34DycQZg0dWLUr3o1012giKiZTeLaHBd98AahIgscHY6X%2BjknHWJTGvHe2M7sMJAhATajCClH2Gx0nkCL6bzAbl%2BeHZ6uiXgB%2B2hOmd%2FQzizf5Y4YNkakpfRK5yMBTn8PZ9OsPNGrM%2B9IEZeXceK4jlLN54auwgY6%2B6KY4M7NGvbtyUVhrexBSDMkJ1OjzgiQG26s7nUNgDOOBUY1V47R2%2FWeMq%2Bd5RS64LygmWx1uZVUYM2hKWN3EGASc%2FSKuhZmDEEqqbRerUTv8simlP4wr9hR9Mpg0V0hRCebgR0PJpg4%2BHF7Ag3SZ7q9E7%2BHfRzp%2F3W%2B3GmJQk%2BTkTLecO55P653z0xHK1qj1hCGfUC%2F7kmkzXjp1zFdxcYxy0Wmms4vL3XeoVshFxno55Xarw4aCIFXtNTxZWRW7uf5m0Zw2p6WcH89Wrs2vxPwt6PMezO3rioKyymXYA0SEkvDg3C%2FapCuEENBINGbNbfVXmU9HJ3r8XnlclYMyGyIGLAznYm98%2BiO%2F0AWsh3bbiaxSI9qt8veZReDf6Rn9T76JBWjcttWwXXZET%2BU4t5KxKqJ1QJxPAEhmZzJZ2sRAm4bRXVI4ODGQRpEciLt8Lj3lB9rFv9tqgF10%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3D75ca2eec8e5ee3dbd0b2a672207ad24ecf7dc56a&ECID-Context=1.006Ivf_oUN8AxGKayTaeMG0060Ok0001FM%3BkXjE | 503 | FAILED | HTTP 503 / error page |
| 140 | https://login-ibqhjb.fa.ocs.oraclecloud.com/oam/server/obrareq.cgi?encquery%3DxS138OL6YUFqo5kXqhatUBRr5X3V1RGL4k%2Bz0kVeSsDqPlMtLQOkCPPbjyD9zFAHBZaV%2B4%2Bm1%2BC15RRXqDUzJfqgkiyvt3ZB8iYpaRVN9qApx0UAl6kxqVcVIFnLXt9LuTk4KALc3n4SIQddr6q6%2BOFzVzgiKyWa3cqoE2V12YBzK8Pi2SYryl1afztYU9JVUJP29U%2FlKJqV7biRJbQE9H2sPdqJv3kpoyqbSpybx21q5XYhaPoGc2tLTa6xi%2FRfih66LyuMO4FMp8vH5zA12aZ9ltzcyzAVFI3x7uQLcAh6pHQm7VqoYEwfyhjgh7FaYQ9cE67Q%2BeRAkhh0r5dlkA%2Fjbd93rdrtDAMuzNqFGgeGYMM%2F3wqSyRTAXhDr9kp1RGsdNmsK1lr6FA9OZ2brJTDDbjPwVNPLMB3TyYleKacbH9%2FXviCjUQ%2FHwzgt5a9ZuBGEumvbK0TxwMpgsJ0yu0jXJ6%2BfZNKN5%2FaG4Pxi2jY47gyzltsiogFvef6dIlZzVXVFjPIDgDWoc%2BR0v7%2BtJDZbAdRc3bNMWuWNuFlHz2%2BemlSYNUCtIqoSCOFJ3PMxgHpdIwsCoLnHZ1A0BPrjrnmeJlZ1BLCj1XMN8aCDPaJXMm8GUoFpBDoJcVgnroYkpEYrk4FICQDlSWQJyHDEZvAyf8mrlleFvHliIKe7iqCM0VrJPJxOx3XLM4%2FFoSIgzv34BqFfX4c4fRTLYbEEbRj5%2FXmyMe04mzMmfdsm1rdZs7boBYCvTXKmhklZQme33TFM26PGec1T0ZnFkODoiPWb3%2FSouG2DGmvCBo7uh0cfmdMNlRngKQDEg9Gi8IlTDr5a4zrqqOzUe5eYoFAwMHRnZ%2Bi9XY%2B%2FbqXxXqBVLWnW6hwImdtNFjXGJuER7GbvbnYWaahNTQQ5aBDezpKFOUdrjSKzI6ICdCnXnnpPo%2BgKo9HQXsMrFc89CE%2BnPbXiforjn%2FjUa7sPlnIN3occRYXNafpmYekQzHYI%2F5J1L1TsBHOdebeWGx20HeLYJXFOWGup58ViARCFzp0cgp8GZntiBKsdecvdg97v5k3sO5HEWS96IYcQHlDmXIdsdBsPOG1cvSJ1JixuseaaZM5OMnOTxpsV1uToblun5Vs6DfOgTv3VUQXVevMFCyC%2BTBucOnTiZCfdT92T%2Bp1XkdveKsJ2jeRebG165AKqLnEJ5eZQhBs6eWn9v%2FRow0mdfeKFavO7Fr%2FXELn9GXe13oQh0sy0RX4kW1qvKVWgI9%2FfiVQMikBsESPOFMA5dwtAFr%2BggEb7aYvdjXYs6zvmlxNxNyXwN2m3GcH7mf%2FopLRrFKVdnqD00kjja5i%2FNebYOfMTMGLVHIoL5EorazZ1hyrc2bafEjj63su3Ns2ltD0kTZvQpgdySfeQEZ21WjibhABsOHZ9SPQE91Ss5TAF6LYkOztU1VyaPmp5g%2BEwbirV3o%2FDo9a%2Fi%2By%2BFvDpPWBkpt2bIHXxWj%2F3699%2BniBsU97TRPn3nRmAmTie6HCRb0kH4k1oTrl70mjMjsI8O3bhdvhj1EnFU8r6ZSszcyTneTE%2Bma7MCYbylmnwQppds6nbIQFyzq4UMv1nLeAS3MHFZkThUexNB165wz0ycXAKMEqID%2FiVHZok2XfhRFfcA2bIk7Y%2FiBD1CplaGU%2F30%2FTC0u61H3iD5Hulp7L5f7jBTp5IjQ%3D%3D%20agentid%3DOraFusionApp_11AG%20ver%3D1%20crmethod%3D2%26cksum%3Db7d14dfa13cdabd935ca9c7841fb201bfe34a229&ECID-Context=1.006Ji0n6W6n2FSMqyKvX6G003mVL0000wW%3BkXjE | 503 | FAILED | HTTP 503 / error page |
| 141 | https://login.ehawaii.gov/lala | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 142 | https://login.neighborlysoftware.com/neighborlysoftware.onmicrosoft.com/oauth2/v2.0/authorize?p=b2c_1_signinsignup_prod&client_id=ab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4&response_type=code%20id_token%20token&scope=openid%20email%20profile%20offline_access%20https%3A%2F%2Fneighborlysoftware.onmicrosoft.com%2Fab730151-4ac5-4b8c-bdd3-4c0f1bffa3a4%2FPortal.Read&state=OpenIdConnect.AuthenticationProperties%3DRibwqB29N7HFG%2FlYtBVU9VQQ%2F47hId8udQ7Qgw4gCV5RWxEAhOVi1FNfkygg3UHLQ92Mm5nrr7PtxBGK1Ctu7VQZKAYDWo1Zw0GNewqepMxUgBtdID6wPyRuFfOCGSGsZoucI%2BKrCfxrtk7ZCE%2FsJ6Fer9k%2FkgDMMI%2Bj5ydxbYJsha6Ju%2BbwJkxl2iKxSiWbg7bz%2BzIArwJ%2BKqV8SCsJ5z%2FkyP%2BUts8TiW0nywmKbnDvMxsR8D%2B5A4UNFkxpwjbymbOFiHW9PXRCHqkEhImRWJSDNKMCqIj80loL00VhBpNteMaRXZDaK%2BHEml%2Fw1MkUBLxhoIJQTxiupyJBRNxRhG6dB%2BbWh7CUp1uHipB2lRr8sAjsfh8IPD18auSh31%2Byv71fC0%2FI2e7Kct5SLawcqg%3D%3D&response_mode=form_post&nonce=639174124887079482.NGJmZDQ0N2EtZjkwNi00ZmY4LWI4MWItNmRkMDcwMTQyNTIzMzYyNWQ4MWUtMjExYy00Yjc4LThlMDYtOWJlZDA4YzNhZDdi&tenantCode=waterlooia&portalType=contractor&nTenantId=490&ui_locales=en&machineCode=00000000-0000-0000-0000-000000000000&redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Floginredirectcomplete&post_logout_redirect_uri=https%3A%2F%2Fportal.neighborlysoftware.com%2Fwaterlooia%2Fcontractor&x-client-SKU=ID_NET472&x-client-ver=7.5.0.0 | 200 | BLOCKED | login wall – listing not viewable without account |
| 143 | https://lonestar.ionwave.net/SourcingEvents.aspx?SourceType=1 | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 144 | https://longbeachbuys.buyspeed.com/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 145 | https://lrsd.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 146 | https://madisonal.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 147 | https://marketplace.unisonglobal.com/login.do?resource_name=marketplace | 200 | BLOCKED | login wall – listing not viewable without account |
| 148 | https://mdapex.ecenterdirect.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 149 | https://mdcourts.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 150 | https://mdstad.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 151 | https://mecknc-vss.hostams.com/PRDVSS1X1/Advantage4 | 200 | BLOCKED | login wall – listing not viewable without account |
| 152 | https://menv.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 153 | https://mevss.hostams.com/PRDVSS1X1/AltSelfService | 404 | FAILED | HTTP 404 / error page |
| 154 | https://miamiu-ohiousourcing.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 155 | https://mps.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 156 | https://mtc.bonfirehub.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 157 | https://mwrd.app/Cntrctann/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 158 | https://mwrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 159 | https://my.alaska.gov/adfs/ls/?wa=wsignin1.0&wtrealm=https%3a%2f%2fmy.alaska.gov%2f&wctx=rm%3d0%26id%3dpassive%26ru%3d%252fPortal%252fPortal.aspx&wct=2023-11-24T17%3a55%3a54Z | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 160 | https://myncid.nc.gov/index.html | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 161 | https://myncid.nc.gov/index.html#/main/userProfile | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 162 | https://myok-staffing.onconcourse.com/login?type=partner | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 163 | https://nait.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 164 | https://nevada.ionwave.net/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 165 | https://nsc.bonfirehub.ca/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 166 | https://ntmwd.bonfirehub.com/registration | 200 | BLOCKED | login wall – listing not viewable without account |
| 167 | https://ny.newnycontracts.com/FrontPage/VendorMain.asp?XID=4111 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 168 | https://octa.govqa.us/WEBAPP/_rs/(S(hn5r0labmmsdycjs2dfu2bmf | 404 | FAILED | HTTP 404 / error page |
| 169 | https://oklahoma.gov/omes/divisions/central-purchasing/suppliers-and-payees/supplier-portal.html | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 170 | https://onesource.wsscwater.com//OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | login wall – listing not viewable without account |
| 171 | https://onesource.wsscwater.com/OA_HTML/RF.jsp?function_id=1016386&resp_id=-1&resp_appl_id=-1&security_group_id=0&lang_code=US&params=PhlO--YbzhGGoNoQiWelCZh8E6l6Vyf-l4j.nKjuI12HTsr8tTeQfKj07gHqCs2V0m07ZPkHnatj9d0m7aE2QQ&oas=hqMw_v58KSRcN5hDt1ZHUg | 200 | BLOCKED | login wall – listing not viewable without account |
| 172 | https://onlineservices.osc.state.ny.us/Enrollment/login?17 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 173 | https://oregonbuys.gov/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 174 | https://passport.cityofnewyork.us/page.aspx/en/buy/homepage/ven | 200 | BLOCKED | login wall – listing not viewable without account |
| 175 | https://pasupplierportal.state.pa.us/irj/portal/anonymous | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 176 | https://pbcvssp.co.palm-beach.fl.us/webapp/vssp/AltSelfService?EmailToken=02730029218941640788 | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 177 | https://pbsystem.planetbids.com/portal/13821/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 178 | https://pbsystem.planetbids.com/portal/13982/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 179 | https://pbsystem.planetbids.com/portal/13982/login# | 200 | BLOCKED | login wall – listing not viewable without account |
| 180 | https://pennbid.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 181 | https://pinalcountyaz.bonfirehub.com/portal | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 182 | https://pr-webs-vendor.des.wa.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 183 | https://pro.prismcompliance.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 184 | https://pro.prismcompliance.com/default.aspx | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 185 | https://procure.cgieva.com/page.aspx/en/sup/registration_extranet/save | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 186 | https://procure.portlandoregon.gov/bso/seller/bidAck.sdo | 200 | BLOCKED | login wall – listing not viewable without account |
| 187 | https://procurement.opengov.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 188 | https://procurement.opengov.com/portal/aurorail | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 189 | https://procurement.opengov.com/portal/baltimorecountymd | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 190 | https://procurement.opengov.com/portal/bft | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 191 | https://procurement.opengov.com/portal/bloomingtonin | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 192 | https://procurement.opengov.com/portal/brevardschools | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 193 | https://procurement.opengov.com/portal/cheyennecity | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 194 | https://procurement.opengov.com/portal/cityofbradenton | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 195 | https://procurement.opengov.com/portal/cityofedinburg | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 196 | https://procurement.opengov.com/portal/cityofhomestead | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 197 | https://procurement.opengov.com/portal/cityofnsb | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 198 | https://procurement.opengov.com/portal/cityoftampa | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 199 | https://procurement.opengov.com/portal/clevelandoh | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 200 | https://procurement.opengov.com/portal/co-hidalgo-tx | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 201 | https://procurement.opengov.com/portal/lompoc | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 202 | https://procurement.opengov.com/portal/morenovalley | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 203 | https://procurement.opengov.com/portal/oak-brook | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 204 | https://procurement.opengov.com/portal/pasadena | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 205 | https://procurement.opengov.com/portal/pinoleca | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 206 | https://procurement.opengov.com/portal/rtd-denver | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 207 | https://procurement.opengov.com/portal/saccounty | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 208 | https://procurement.opengov.com/portal/santacruzca | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 209 | https://procurement.opengov.com/portal/smcgov | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 210 | https://procurement.opengov.com/portal/stpete | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 211 | https://procurement.opengov.com/portal/tucson-az | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 212 | https://procurement.opengov.com/portal/tuolumnecountyca | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 213 | https://procurement.opengov.com/portal/wheatridgeco | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 214 | https://procurement.opengov.com/vendors/155272/proposals | 200 | BLOCKED | login wall – listing not viewable without account |
| 215 | https://proportal.sourcewell-mn.gov/Module/Tenders/en/Vendor/Dashboard/b50f7d44-0fe6-4ffe-8621-fbae66354482 | 200 | BLOCKED | login wall – listing not viewable without account |
| 216 | https://purchasing.iu.edu/resources/forms/table.html | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 217 | https://recuperacion.pr.gov/en/procurement-and-nofa/procurement/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 218 | https://sawsbid.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 219 | https://sccpss.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 220 | https://scottsdaleaz.bonfirehub.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 221 | https://sdbuynet.sandiegocounty.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 222 | https://secure.bidsandtenders.ca/Module/Tenders/en/Login/Index/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 223 | https://security.app.cpa.state.tx.us/Public/login?logout | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 224 | https://service.ariba.com/Authenticator.aw/ad/ssoIDP | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 225 | https://sigma.michigan.gov/PRDVSS1X1/Advantage4 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 226 | https://smctd.bonfirehub.com/opportunities/112297 | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 227 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=LOGINREQD&_logininst=W68E33gEyArMeQNVR!2B0pO4UAJK!2BQjvLlYP!2BnbMhYU2hA39DrCszSxwAAAYqPkSI!2F&_TKM=492813489&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER | 200 | BLOCKED | login wall – listing not viewable without account |
| 228 | https://sms-idaho-prd.tam.inforgov.com/sso/SSOServlet?_action=TIMEOUTASSERT&_ssoOrigUrl=https%3A%2F%2Fsms-idaho-prd.tam.inforgov.com%3A443%2Ffsm%2FSupplyManagementSupplier%2Fpage%2FXiSupplyManagementSupplierPage%3Fcsk.SupplierGroup%3DLUMA&_TKM=372688986&_serviceName=FSM.IEFINAPP.SUPPLYMANAGEMENTSUPPLIER&LoginId=business-development@ommincorp.com | 200 | BLOCKED | login wall – listing not viewable without account |
| 229 | https://sms-nola-prd.inforcloudsuite.com/fsm/SupplyManagementSupplier/page/XiSupplyManagementSupplierPage?csk.SupplierGroup=100 | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 230 | https://snoco.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 231 | https://solutions.sciquest.com/apps/Router/BrandedSupplierHome?CustOrg=UCOP&supplierID=1007876976&tmstmp=1738093109276 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 232 | https://solutions.sciquest.com/apps/Router/SupplierLogin | 200 | BLOCKED | login wall – listing not viewable without account |
| 233 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=BridgewaterState | 200 | BLOCKED | login wall – listing not viewable without account |
| 234 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=DASIowa | 200 | BLOCKED | login wall – listing not viewable without account |
| 235 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=Princeton&isLogout=true&tmstmp=1716220417643 | 200 | BLOCKED | login wall – listing not viewable without account |
| 236 | https://solutions.sciquest.com/apps/Router/SupplierLogin?CustOrg=StateOfUtah&isLogout=true&tmstmp=1699984786288 | 200 | BLOCKED | login wall – listing not viewable without account |
| 237 | https://solutions.sciquest.com/apps/Router/SupplierLogin?GSPSupplier_Login_Email=Business-development%40ommincorp.com&CustOrg=StateOfMontana&SuccessToken=1&tmstmp=1695233574600 | 200 | BLOCKED | login wall – listing not viewable without account |
| 238 | https://solutions.sciquest.com/apps/Router/SupplierPortalHome?tmstmp=1699981963442 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 239 | https://solutions.sciquest.com/apps/Router/SupplierWelcome?CustOrg=TriMet&supplierID=1007876976&tmstmp=1704204983800 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 240 | https://stamfordct.procureware.com/home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 241 | https://stamfordct.procureware.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 242 | https://stillwater.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 243 | https://strathcona.bonfirehub.ca/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 244 | https://supplier.esmsolutions.com/home | 200 | BLOCKED | login wall – listing not viewable without account |
| 245 | https://supplier.ionwave.net/Vendor/VendorHome.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 246 | https://supplier.ionwave.net/VendorLogin.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 247 | https://supplier.ionwave.net/VendorResponse/ResponseList.aspx?status=AVAILABLE | 200 | BLOCKED | login wall – listing not viewable without account |
| 248 | https://supplier.miamidade.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 249 | https://supplier.sok.ks.gov/psc/sokfsprdsup/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_REG_CMP_FL.GBL | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 250 | https://supplier.wmata.com/psc/supplier/SUPPLIER/ERP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL? | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 251 | https://supplierservice.sanantonio.gov/irj/portal | 200 | BLOCKED | login wall – listing not viewable without account |
| 252 | https://supplierservice.sanantonio.gov/irj/portal#12587465-vendor-info | 200 | BLOCKED | login wall – listing not viewable without account |
| 253 | https://tarrantcountytx.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 254 | https://tohowater.bonfirehub.com/login/forgot | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 255 | https://transitchicago.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 256 | https://trstexas-supplier.ivalua.app/page.aspx/en/sup/registration_manage/2594 | 200 | BLOCKED | login wall – listing not viewable without account |
| 257 | https://uiebid.ionwave.net/Login.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 258 | https://upstream.dc.gov/Sourcing/Main/ad/loginPage/SSOActions?awsso_cc=passwordadapter%3AU291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_ru%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbj9wYXNzd29yZGFkYXB0ZXI9U291cmNpbmdTdXBwbGllclVzZXI%3D%3Bawsso_lu%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRMb2dvdXQvU1NPQWN0aW9ucw%3D%3D%3Bawsso_ap%3AQUNN%3Bawsso_arid%3AMTY4ODk5MzA3NjY0NA%3D%3D%3Bawsso_ku%3AaHR0cHM6Ly91cHN0cmVhbS5kYy5nb3YvU291cmNpbmcvTWFpbi9hZC9jbGllbnRLZWVwQWxpdmUvU1NPQWN0aW9ucw%3D%3D%3Bawsso_fl%3AMQ%3D%3D&awsso_ap=ACM&awsso_hpk=true&passwordadapter=SourcingSupplierUser&awsr=true | 200 | BLOCKED | login wall – listing not viewable without account |
| 259 | https://upstream.dc.gov/Sourcing/Main?realm=System&passwordadapter=SourcingSupplierUser&awsso_tkn=24MUzqrzky68f28a69a52257ff | 200 | BLOCKED | login wall – listing not viewable without account |
| 260 | https://valenciacollege.edu/employees/procurement/solicitations.php | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 261 | https://vendor.myfloridamarketplace.com/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 262 | https://vendor.purchasingconnection.ca/default.aspx | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 263 | https://vendorportal.dc.gov/Account/Login | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 264 | https://vendors.planetbids.com/ | None | FAILED | page.goto: net::ERR_TOO_MANY_REDIRECTS at https://vendors.planetbids.com/ |
| 265 | https://vendors.planetbids.com/portal/14599/bo/bo-search | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 266 | https://vendors.planetbids.com/portal/14599/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 267 | https://vendors.planetbids.com/portal/15300/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 268 | https://vendors.planetbids.com/portal/15381/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 269 | https://vendors.planetbids.com/portal/16151/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 270 | https://vendors.planetbids.com/portal/16151/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 271 | https://vendors.planetbids.com/portal/16725/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 272 | https://vendors.planetbids.com/portal/17950/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 273 | https://vendors.planetbids.com/portal/17950/login# | 200 | BLOCKED | login wall – listing not viewable without account |
| 274 | https://vendors.planetbids.com/portal/20134/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 275 | https://vendors.planetbids.com/portal/20136/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 276 | https://vendors.planetbids.com/portal/20314/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 277 | https://vendors.planetbids.com/portal/22078/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 278 | https://vendors.planetbids.com/portal/22576/bo/bo-detail/141899 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 279 | https://vendors.planetbids.com/portal/23532/bo/bo-search | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 280 | https://vendors.planetbids.com/portal/23758/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 281 | https://vendors.planetbids.com/portal/24103/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 282 | https://vendors.planetbids.com/portal/24660/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 283 | https://vendors.planetbids.com/portal/24661/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 284 | https://vendors.planetbids.com/portal/27996/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 285 | https://vendors.planetbids.com/portal/28789/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 286 | https://vendors.planetbids.com/portal/29744/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 287 | https://vendors.planetbids.com/portal/32621/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 288 | https://vendors.planetbids.com/portal/39475/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 289 | https://vendors.planetbids.com/portal/39495/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 290 | https://vendors.planetbids.com/portal/39495/login# | 200 | BLOCKED | login wall – listing not viewable without account |
| 291 | https://vendors.planetbids.com/portal/39501/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 292 | https://vendors.planetbids.com/portal/43728/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 293 | https://vendors.planetbids.com/portal/45619/bo/bo-search | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 294 | https://vendors.planetbids.com/portal/49906/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 295 | https://vendors.planetbids.com/portal/53010/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 296 | https://vendors.planetbids.com/portal/59724/vp/vp-home | 200 | BLOCKED | login wall – listing not viewable without account |
| 297 | https://vendors.planetbids.com/portal/62287/bo/bo-search | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 298 | https://vendors.planetbids.com/portal/64863/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 299 | https://vendors.planetbids.com/portal/65292/vp/vp-prereg | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 300 | https://vendors.planetbids.com/portal/65844/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 301 | https://vendors.planetbids.com/portal/68007/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 302 | https://vendors.planetbids.com/portal/76708/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 303 | https://vendors.planetbids.com/portal/77636/portal-home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 304 | https://ventura.bonfirehub.com/registration | 200 | BLOCKED | login wall – listing not viewable without account |
| 305 | https://via.diversitycompliance.com/FrontPage/VendorMain.asp?XID=9510 | 404 | FAILED | HTTP 404 / error page |
| 306 | https://via.sbecompliance.com/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 307 | https://via.sbecompliance.com/?TN=via | 200 | BLOCKED | login wall – listing not viewable without account |
| 308 | https://vrapp.vendorregistry.com/Account/LogOn | 200 | BLOCKED | login wall – listing not viewable without account |
| 309 | https://vrapp.vendorregistry.com/Bids/View/BidsList?BuyerId=c5e9d3e7-b8e0-4e36-bcab-8db00d18d769 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 310 | https://vss.ky.gov/vssprod-ext/Advantage4 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 311 | https://vss.ky.gov/vssprod-ext/Advantage4?openDoc=openDoc&DocumentCode=RFP&DepartmentCode=415&DocumentID=2600000199&DocumentVersNo=2&targetView=ammendHistoryView&Destination=pSolication | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 312 | https://vtbuys.suppliers.vermont.gov/page.aspx/en/usr/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 313 | https://waukeshacounty.bonfirehub.com/opportunities/144594 | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 314 | https://wrd.bonfirehub.com/portal/?tab=openOpportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 315 | https://ww3.nysif.com/FooterPages/Column1/AboutNYSIF/Procurement | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 316 | https://www.ahfc.us/about-us/notices/requests-proposals | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 317 | https://www.annapolis.gov/bids.aspx | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 318 | https://www.beaconbid.com/solicitations/city-of-houston/121f4067-fb3a-4d30-85b9-ea6a6cafe989/contingent-labor-services-all-categories?token=supplier-login.ObiU4vtGsc_vRNVc-a87JReydRqhQP07ozrco4z95xclrg1KaW517ezRNB5QzTvK8dS9z_wfmREHNc6qRuGr-uHTYI229n9X2AhzK2_xmpo1LIlDsnrcN9YzPY9tkrWfy3EN_v3vttW09t3yqiaBnArwIvYLa3JnzE4G9B1giu5p7FuxEHf2iImOzrCy7TDIptzKNwKUivDO0G3DxgJ4Yz43Iz6gCzrsPGyOdGXCJV9Qg29rKw2IN4_Nw5d1czIABi6VfJW2RJtyEc02dHo1amlJHrAnTsWOtrQ8zz6lolxc5u8OanNPWUJnmTMDrOPoY-3_mtuNxCYeyzX2seLpWEfkAtq1AbX1X_Xb-492Ng&eid=bc055432-0873-482a-98b8-0490d2821dc8 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 319 | https://www.beaconbid.com/solicitations/city-of-houston/open | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 320 | https://www.bidbuy.illinois.gov/bso/external/vendor/regSummary.sdo?vendorId=NZdPl7Rvv_Oq&mode=initial&dateTime=1694627292171 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 321 | https://www.bidexpress.com/businesses/85766/home?agency=true | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 322 | https://www.bidnetdirect.com/new-jersey/lbha | 202 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 323 | https://www.bidnetdirect.com/private/supplier/solicitations/search | 200 | BLOCKED | login wall – listing not viewable without account |
| 324 | https://www.californiabids.com/bid_opportunities/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 325 | https://www.cdta.org/node/15813/register | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 326 | https://www.centralauctionhouse.com/login.php | 200 | BLOCKED | login wall – listing not viewable without account |
| 327 | https://www.cityoftulsa.org/government/departments/finance/selling-to-the-city/bid-opportunities-and-results/?t=current | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 328 | https://www.commbuys.com/bso/view/login/login.xhtml | 200 | BLOCKED | login wall – listing not viewable without account |
| 329 | https://www.cpsk12bids.com/auth/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 330 | https://www.dcwater.com/useful-links | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 331 | https://www.demandstar.com/app/suppliers/bids | 200 | BLOCKED | login wall – listing not viewable without account |
| 332 | https://www.frederickcountymd.gov/1116/Open-Bids---Current-Solicitations | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 333 | https://www.govevents.com/?signoutsucccess | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 334 | https://www.infotechexpress.com/business | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 335 | https://www.instantmarkets.com/home | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 336 | https://www.kalcounty.com/ | 403 | BLOCKED | HTTP 403 bot-check/CAPTCHA/WAF |
| 337 | https://www.kcsdschools.net/dept/finance/procurement | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 338 | https://www.laramiecountywy.gov/Request-for-Proposals | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 339 | https://www.matawanborough.com/matawan/Bid%20Notices%20and%20Requests%20for%20Proposals/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 340 | https://www.mecknc.gov/finance/procurement/Pages/default.aspx | 404 | FAILED | HTTP 404 / error page |
| 341 | https://www.mymta.info/psc/VENDOR/GUEST/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 342 | https://www.mymta.info/psc/VENDOR/SUPPLIER/SUPP/c/NUI_FRAMEWORK.PT_LANDINGPAGE.GBL?&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP&lp=SUPP.SUPPLIER.B_ESUP_SECURE_FL_HP | 200 | BLOCKED | login wall – listing not viewable without account |
| 343 | https://www.myvendorlink.com/external/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 344 | https://www.njstart.gov/bso/external/vendor/regComSrvcCodes.sdo | 500 | FAILED | HTTP 500 / error page |
| 345 | https://www.northwestmsbids.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 346 | https://www.nunavuttenders.ca/UploadBidderTC.aspx | 200 | BLOCKED | login wall – listing not viewable without account |
| 347 | https://www.nyscr.ny.gov/login.cfm | 404 | FAILED | HTTP 404 / error page |
| 348 | https://www.ptcvendorportal.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 349 | https://www.ptcvendorportal.com/#/sp/auth/signin | 200 | BLOCKED | login wall – listing not viewable without account |
| 350 | https://www.rfpmart.com/userlogin.html | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 351 | https://www.rochesterhousing.org/bid-opportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 352 | https://www.stlmsdplanroom.com/auth/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 353 | https://www.txsmartbuy.gov/esbd | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 354 | https://www.voa.va.gov/default.aspx?PageId=1 | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 355 | https://yvr.bonfirehub.ca/login | 200 | BLOCKED | login wall – listing not viewable without account |
| 356 | https://www.rfpmart.com/ | 200 | BLOCKED | HTTP 200 bot-check/CAPTCHA/WAF |
| 357 | https://bidsnexus.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 358 | https://bidranger.com/ | 429 | BLOCKED | HTTP 429 bot-check/CAPTCHA/WAF |
| 359 | https://www.bidcontract.com/ | 502 | FAILED | HTTP 502 / error page |
| 360 | https://biddingsimple.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 361 | https://publicbidtracker.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 362 | https://www.busybids.org/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 363 | https://www.contrax.company/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 364 | https://govbidwire.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 365 | https://www.bidnetdirect.com/public/solicitations/open | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 366 | https://procuralerts.com/government-bids | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 367 | https://app.rfpplanner.com/opportunity/match/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 368 | https://thebidbroker.com/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 369 | https://www.txsmartbuy.com/esbd | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 370 | https://pur.doas.ga.gov/gpr/ | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 371 | https://evp.nc.gov/solicitations/ | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 372 | https://eva.virginia.gov/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 373 | https://www.emarketplace.state.pa.us/Search.aspx | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 374 | https://www.commbuys.com/bso/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 375 | https://portal.ct.gov/das/ctsource/bidboard | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 376 | https://www.njstart.gov/bso/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 377 | https://oregonbuys.gov/bso/ | 502 | FAILED | HTTP 502 / error page |
| 378 | https://guest.supplier.systems.state.mn.us/psc/fmssupap_20/SUPPLIER/ERP/c/SCP_PUBLIC_MENU_FL.SCP_PUB_BID_CMP_FL.GBL?PAGE=SCP_PUB_BIDLIST_FL | 200 | SUCCESS | November-2026 dated solicitations parsed from listing |
| 379 | https://vss.state.co.us/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 380 | https://www.bidbuy.illinois.gov/bso/ | 200 | BLOCKED | login wall – listing not viewable without account |
| 381 | https://das.iowa.gov/vendors/bidding-opportunities | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 382 | https://caleprocure.ca.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 383 | https://vendor.myfloridamarketplace.com/search/bids | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 384 | https://vss.ky.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
| 385 | https://www.nyscr.ny.gov/ | 200 | NO_RELEVANT_RESULTS | page rendered; no listing with an issue/posted date on/after 2026-11-01 found (or listing shows only due dates) |
