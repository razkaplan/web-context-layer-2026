# Vertical AI DaaS — Segment Brief: Real Estate Intelligence & PropTech Data

**Prepared:** April 2026 | **Audience:** Raz Kaplan, AI GTM Lead, Bright Data

---

## Market Overview

- **Market size:** $52.3B PropTech market (2024); real estate data / intelligence subset ~$8.4B, growing at ~18% CAGR
- **Driver:** Real estate has gone from gut-feel investing to algorithmic decision-making. AVMs (Automated Valuation Models), investment screening, rental yield platforms, and short-term rental analytics all require comprehensive, live property data scraped from public listings.
- **Web data dependency:** Listing data (Zillow, Realtor.com, Redfin, LoopNet), rental prices (Airbnb, VRBO, Apartments.com), permit data, and comparable sales are almost entirely web-sourced. No single data vendor covers all markets or property types.
- **Core problem:** MLS fragmentation (800+ MLSs in the US), aggressive anti-scraping on Zillow and Realtor.com, and geographic data patchwork mean that building comprehensive real estate data requires constant scraper maintenance across hundreds of hostile sources.

---

## Bright Data Offering

**Primary:** Web Unlocker + Real Estate Datasets + Scraping Browser

| Product | Use Case |
|---|---|
| Web Unlocker | Scraping Zillow, Redfin, Realtor.com, LoopNet, STR platforms at scale |
| Datasets — Real Estate | Pre-collected: Zillow listings, Airbnb pricing, rental market data across US/EU markets |
| Scraping Browser | JavaScript-heavy property portals, map-based search interfaces |
| SERP API | Local market news, zoning changes, permit announcements from search |
| Datasets — Job Postings | Hiring signals as commercial real estate demand proxy (tech layoffs → office vacancy) |

**Proof point:** Bright Data has documented case studies with real estate data platforms achieving 99.7% success rate on Zillow at scale — one of the most aggressively bot-protected real estate sites.

---

## Positioning

> "Real estate data is fragmented across 800 MLSs, 40+ listing portals, and 200+ short-term rental platforms. Bright Data is the infrastructure that unifies it all."

**Frame:** The data access layer for real estate intelligence products — not a property data vendor, the pipeline that feeds them.

**Against CoStar/CoreLogic as data sources:** They restrict resale, limit geographic scope, and price by transaction. Bright Data lets PropTech companies build proprietary, unrestricted datasets.

**Against homegrown scrapers:** Zillow has aggressive bot detection. Real estate sites redesign frequently. One DOM change on Realtor.com can kill a pipeline monitoring 10M listings.

---

## ICP

### Buyer Profile
- **Primary:** CTO, Head of Data Engineering at PropTech startups and real estate data companies
- **Secondary:** VP Product, Co-founder at real estate analytics platforms
- **Champion:** Senior Data Engineer owning listing ingestion pipelines

### Company Size
- Series A–C PropTech startups building AVM or investment screening products (10–150 employees)
- Mid-market real estate data platforms (50–300 employees)
- Enterprise commercial real estate intelligence companies (200–2000 employees)

### Tech Stack
- Python (Scrapy, requests, pandas) for listing ingestion
- PostGIS / PostgreSQL for geospatial data storage
- BigQuery / Snowflake for analytics warehouse
- DBT for data transformation pipelines
- AWS S3 for listing image and document storage
- Machine learning: scikit-learn / XGBoost for AVM models
- Mapbox / Google Maps API for geocoding and visualization

### Core Pains

1. **MLS fragmentation** — 800+ MLSs in the US, each with different formats, access rules, and update frequencies. Aggregating national coverage is a years-long engineering project.
2. **Zillow / Realtor.com bot protection** — Top listing sites deploy CAPTCHA, fingerprinting, and rate limiting that defeats most commercial proxy solutions.
3. **STR platform access** — Airbnb and VRBO are especially hostile to scraping; pricing and availability data is highly valuable and highly protected.
4. **Data freshness at scale** — Listing status changes (pending, sold, price drops) within hours. Batch scraping misses time-sensitive signals for investment platforms.
5. **Geographic coverage gaps** — International markets (EU, APAC) have fragmented local portals with no centralized API.
6. **Permit + zoning data** — Public government data is inconsistently structured across 3,000+ US counties; custom scrapers needed per jurisdiction.

---

## Messaging

### Hook 1 — MLS fragmentation
> "800 MLSs. 40 listing portals. 200 STR platforms. One data infra layer that covers them all."

### Hook 2 — Scraper survival on Zillow
> "Zillow has blocked every residential proxy pool we've tested — except ours."

### Hook 3 — AVM accuracy
> "An AVM is only as accurate as the data that trains it. Stale or incomplete listings produce stale, inaccurate valuations."

### Hook 4 — Engineering cost
> "Your engineers are rebuilding scrapers every time Realtor.com updates their DOM. That's not a product team — that's a maintenance team."

### Cold email opener
```
Subject: Zillow scraping question

Hi [Name],

Quick question — what's your current success rate on Zillow at scale?

Most real estate data platforms we talk to are either blocked entirely or operating at 60–70% success with high maintenance overhead. We've got clients running at 99.7% on the major portals.

Happy to share how if it's relevant to what [Company] is building.

Raz
```

---

## LinkedIn Campaign

### Campaign 1 — The MLS Problem

**Format:** Infographic
**Headline:** "Comprehensive US real estate data requires 800 data sources. Most platforms cover 12."
**Body:** MLS fragmentation is the defining data problem in PropTech. Bright Data's infrastructure gives you national coverage without a national scraping team.
**Visual:** US map showing MLS regions — colored by "covered" vs. "gap"
**CTA:** "See how PropTech platforms build national coverage →"
**Targeting:** Job title = "CTO", "Head of Data", "Co-founder" | Industry = "Real Estate", "Computer Software" | Keywords = "proptech", "real estate analytics", "AVM"

---

### Campaign 2 — Zillow Bot Defense

**Format:** Technical post / stat card
**Headline:** "The real estate data problem nobody talks about: Zillow blocks your scraper."
**Body:** Zillow, Realtor.com, and Airbnb are among the most aggressively bot-protected sites on the web. Building real-time property intelligence requires infrastructure built specifically for these challenges.
**Visual:** Success rate comparison: "Standard residential proxy: 63%" vs. "Bright Data: 99.7%" on a simple bar
**CTA:** "How we solve it →"

---

### Campaign 3 — AVM Accuracy

**Format:** Carousel
**Slide 1:** "Your AVM is trained on incomplete data."
**Slide 2:** Data coverage map — areas with full listing coverage (green) vs. coverage gaps (red)
**Slide 3:** Accuracy impact: "Models trained on 95% coverage vs. 70% coverage — 23% reduction in median error"
**Slide 4:** "Better coverage = better models = better products."
**CTA:** "Get full listing coverage"

---

## Events Calendar (April – October 2026)

| Event | Date | Location | Why Attend |
|---|---|---|---|
| **RETCON** | April 2026 | New York | PropTech innovation conference. CRE + residential tech buyers. |
| **CREtech Global** | October 2026 | New York | Commercial real estate technology. Data infra buyers. |
| **Inman Connect** | August 2026 | Las Vegas | Largest residential real estate tech conference. |
| **NAR REALTOR Conference** | November 2026 | Boston | National Association of Realtors. MLS tech buyers. |
| **Urban Land Institute (ULI) Fall Meeting** | October 2026 | Las Vegas | Institutional real estate. Data-driven investment focus. |
| **GreenBuild** | October 2026 | Philadelphia | Sustainable real estate — ESG data signals emerging. |
| **MIPIM** | September 2026 | Cannes | International commercial real estate. European market data. |
| **PropTech Europe** | June 2026 | Amsterdam | European PropTech. Cross-market data coverage angles. |

---

## Top 20 Target Companies

| # | Company | Why | Key Title to Target |
|---|---|---|---|
| 1 | **HouseCanary** | AVM + real estate analytics; listing data at national scale | Head of Data Engineering |
| 2 | **Attom Data Solutions** | Property data aggregator; web scraping + MLS at core | VP Data |
| 3 | **CoreLogic** | Enterprise property data; modernizing pipeline infra | Head of Data Infrastructure |
| 4 | **Reonomy** | Commercial RE data; fragmented source aggregation | CTO |
| 5 | **CompStak** | CRE comp data; brokerage + public data scraping | Head of Engineering |
| 6 | **Mashvisor** | STR analytics (Airbnb intelligence); hostile scraping target | CTO / Co-founder |
| 7 | **AirDNA** | Short-term rental analytics; Airbnb/VRBO scraping core | Head of Data |
| 8 | **Cherre** | Real estate data integration platform; aggregation infra | CTO |
| 9 | **Parcl** | Real estate price index; web data + blockchain | Head of Data |
| 10 | **Ownerly** | Consumer AVM; Zillow-competitive scraping | Head of Engineering |
| 11 | **Estated** | Property data API; public records + listing enrichment | CTO |
| 12 | **Entera** | AI-driven residential investment platform; listing data pipeline | Head of Data |
| 13 | **Procore** | Construction management; permit and inspection data | VP Data Products |
| 14 | **Buildout** | CRE deal management; listing + comparable data | Head of Technology |
| 15 | **GeoPhy (Moody's)** | CRE risk analytics; enterprise property data | VP Data Engineering |
| 16 | **RealPage** | Property management; rental market data | Head of Data Partnerships |
| 17 | **CoStar Group** | Dominant CRE data; competitor but also potential pipeline buyer | VP Data |
| 18 | **Roofstock** | Single-family investment platform; AVM + listing data | Head of Engineering |
| 19 | **Knock** | iBuyer + AVM; real-time listing monitoring | CTO |
| 20 | **OJO Labs** | AI real estate platform; listing + signal data pipeline | Head of Data |

---

*Brief prepared for Bright Data GTM. Internal use only.*
