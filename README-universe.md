# DaaS Universe — 200 Target Companies

**File:** `universe-daas-200-targets.csv`  
**Created:** 2026-04-13  
**Total Companies:** 200

## Overview
Expanded DaaS universe for Bright Data's outreach campaign. Combines existing 162-company baseline with 38 new high-value targets across 15 vertical segments.

## Structure

### Columns
- **Company** — Legal company name
- **Website** — Primary domain
- **Segment** — Vertical market classification (15 segments)
- **Type** — AI-Native or Traditional
- **What_They_Sell** — Core value proposition
- **HQ_Country** — Headquarters location
- **Employee_Range** — Size tier (10-50, 50-100, 100-500, 500-1000, 1000-5000, 5000+)
- **Funding_Status** — Bootstrap, Series A-E, Public, Acquired, Private
- **ICP_Fit** — Scraping use-case fit
  - **A** = Heavy web scraping dependency
  - **B** = Partial / secondary dependency
  - **C** = Minimal dependency
  - **X** = Not applicable
- **Priority_Tier** — Outreach priority
  - **T1** = Top target (104 companies)
  - **T2** = Secondary (86 companies)
  - **T3** = Awareness / low fit (10 companies)
- **Scraping_Dependency** — High/Medium/Low

## Segment Breakdown

| Segment | Count | Focus |
|---------|-------|-------|
| B2B Intelligence & GTM | 39 | Sales intel, enrichment, discovery |
| E-commerce & Price Intelligence | 32 | Dynamic pricing, market analytics |
| Alternative Financial Data | 23 | Market data, alternative datasets |
| News & Media Intelligence | 21 | Social listening, brand monitoring |
| AI Training & Infrastructure | 13 | Data extraction, ML pipelines |
| Labor & Workforce Analytics | 13 | Job market, talent intel |
| Real Estate & PropTech | 11 | Property data, valuation, location |
| Cybersecurity Data | 11 | Threat intel, asset discovery |
| Search & Discovery APIs | 10 | Web search, content APIs, scraping |
| Social Media & Influencer Data | 9 | Creator databases, social analytics |
| Supply Chain & Trade Data | 7 | Trade intelligence, supply chain |
| Healthcare & Pharma Data | 4 | Clinical, pharma intelligence |
| Podcast & Audio Data | 4 | Podcast search, audio analytics |
| Travel & Hospitality Data | 2 | Price intelligence, hotel data |
| Government & Regulatory Data | 1 | SEC filings, regulatory tracking |

## Key Metrics

### By Type
- **AI-Native:** 172 companies (86%)
- **Traditional:** 28 companies (14%)

### By ICP Fit
- **A (Heavy scraping):** 110 companies (55%)
- **B (Partial):** 68 companies (34%)
- **C (Minimal):** 11 companies (6%)
- **X (Not applicable):** 11 companies (6%)

### By Scraping Dependency
- **High:** 102 companies (51%)
- **Medium:** 75 companies (38%)
- **Low:** 23 companies (11%)

### By Priority
- **T1 (Top):** 104 companies (52%)
- **T2 (Secondary):** 86 companies (43%)
- **T3 (Awareness):** 10 companies (5%)

## Geographic Distribution
- **USA:** 134 companies (67%)
- **Europe:** 36 companies (18%)
- **Asia:** 24 companies (12%)
- **Other:** 6 companies (3%)

## Key Insights

1. **High-value segment:** B2B Intelligence & GTM has largest count (39) due to broad sub-verticals
2. **Strong AI-Native ratio:** 86% AI-Native indicates market has shifted toward LLM/AI-first companies
3. **High scraping dependency:** 55% rated "A" (heavy) — strong product-market fit with Bright Data value prop
4. **Geographic concentration:** 67% USA-based; 18% Europe; strong in UK, Israel, Germany
5. **Funding profile:** Mix of bootstrapped (Listen Notes, Shodan), Series A-B (high growth), and Public (Numerator, Dataminr)

## Usage

### For Outreach
- Filter by **Priority_Tier** = T1 for initial push (104 targets)
- Filter by **ICP_Fit** = A for highest scraping dependency (110 targets)
- Combine: **T1 + ICP_Fit=A** = ~60 top targets

### For Research
- Segment by **Type** to compare AI-Native vs Traditional approaches
- Use **Employee_Range** to calibrate engagement (50-100 = founders, 500+ = enterprise sales)
- Cross-reference **Funding_Status** with deal size expectations

### For Competitive Analysis
- Identify overlapping segments with Bright Data competitors
- Map Segment + Type combinations to understand market dynamics
- Track which segments have highest AI-Native concentration

## Notes
- All data reflects public information + reasonable estimates (Q1 2026)
- Funding status reflects most recent known round; verify before outreach
- ICP_Fit assessed based on product architecture + known use cases
- Scraping_Dependency estimated from product documentation + community signals

---

**Build script:** `/sessions/zealous-magical-lamport/mnt/build_daas_universe.py`
