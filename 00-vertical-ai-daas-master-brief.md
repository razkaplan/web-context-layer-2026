# Vertical AI DaaS — GTM Master Brief

**Owner:** Raz Kaplan, AI GTM Lead
**Date:** April 2026
**Status:** Active — campaign build phase

---

## What this is

This is the GTM brief for the **Vertical AI DaaS** segment — companies that sell structured data as a product to downstream AI pipelines, research teams, or enterprise buyers. Not retailers. Not e-commerce scrapers. Companies building defensible data businesses on top of web data infrastructure.

Six segment briefs live in this folder. Each is researched, complete, and ready to build a LinkedIn campaign from. This document is the frame that ties them together — who this audience is, why now, what we're selling, how we're prioritizing, and what success looks like.

---

## Why this segment, why now

### 1. AI made web access a mass-market infrastructure requirement

By March 2026, **57% of organizations have AI agents running in production** (Master of Code). **58% of AI agent use cases involve research and summarizing real-world information** — making live web access the #1 functional requirement across the entire category (LangChain State of AI Agents Report). LangChain alone has 50,000+ production apps. CrewAI is the fastest-growing agent framework in 2025–2026.

The consequence: every company building a data product that feeds these agents — alt data platforms, B2B intelligence tools, media monitors, workforce analytics — has the same underlying infrastructure problem. **Data products feeding AI agents need to solve the same web access problem at scale that the agents themselves face.** That problem is Bright Data's core product.

Sources: [Grand View Research](https://www.grandviewresearch.com/industry-analysis/ai-agents-market-report) · [Master of Code](https://masterofcode.com/blog/ai-agent-statistics) · [LangChain State of AI Agents](https://www.langchain.com/stateofaiagents)

---

### 2. Microsoft killed Bing API — 50,000+ pipelines are mid-migration

On **August 11, 2025**, Microsoft retired the Bing Search API without a drop-in replacement. API creation was silently disabled in March 2025, weeks before the announcement (Windows Central). The recommended migration path — Azure AI Foundry — is a full platform commitment, not an API swap.

Every data company that used Bing for SERP data, news monitoring, or search-based enrichment is actively replacing it now. This is a live trigger event, not a trend.

Sources: [Windows Central](https://www.windowscentral.com/software-apps/browsing/bing-search-apis-to-be-decommissioned-completely) · [SerpAPI migration guide](https://serpapi.com/blog/bing-search-api-replacement-web-search/)

---

### 3. Compliance requirements have eliminated most of this market — except Bright Data

Enterprise procurement now treats **SOC 2 Type II as a minimum requirement** in US vendor reviews — "most security review processes assume vendors have a SOC 2 Type II report" and many refuse to proceed without one (Hyperproof). ISO 27001 is increasingly mandatory in EU procurement.

Here is the specific competitive gap: **Tavily has SOC 2. Exa has SOC 2 Type II. Firecrawl's certification status is unverified.** None of them have ISO 27001. None have GDPR documentation, CCPA, or CSA STAR. Bright Data has all five.

This matters in two directions: (1) Bright Data can win enterprise deals that competitors cannot close due to security review failure; (2) Vertical AI DaaS companies building on Bright Data's infrastructure inherit a compliance story they can present to their own enterprise buyers — a downstream selling point none of their alternatives can offer.

Sources: [Hyperproof SOC 2 Guide](https://hyperproof.io/soc2/) · [Tavily Trust Center](https://trust.tavily.com/) · [Exa Security (SOC 2)](https://docs.exa.ai/reference/security-soc-2) · [Scytale 2026](https://scytale.ai/center/soc-2/the-soc-2-compliance-checklist/)

---

## What we're selling

We are not selling proxy access. We are selling the infrastructure layer that makes their data product possible.

**Primary products:**
- **Web Unlocker** — production-grade access to any public URL through rate limits, CAPTCHAs, and bot detection middleware. Core product for every segment.
- **SERP API** — structured search results via API. Direct Bing replacement. Feeds financial signal, media monitoring, B2B intelligence pipelines.
- **Scraping Browser** — headless browser with built-in unblocking. For JS-heavy portals, map-based search, ATS career pages.
- **Datasets** — pre-collected, structured, updated daily. LinkedIn, job postings, real estate listings, news. For teams that want to skip pipeline build entirely.

**The frame in every conversation:**

> "You build the intelligence layer. We build the access layer. If your data product depends on reading the public web, Bright Data is the infrastructure underneath it."

---

## The six segments

| # | Segment | Market size (2024) | CAGR | Brief |
|---|---|---|---|---|
| 1 | Alternative Financial Data | $21.6B | ~24% | [01-alternative-financial-data.md](./01-alternative-financial-data.md) |
| 2 | B2B Intelligence & GTM Data | $2.6B | ~28% | [02-b2b-intelligence-gtm-data.md](./02-b2b-intelligence-gtm-data.md) |
| 3 | News & Media Intelligence | $15.5B | ~31% | [03-news-media-intelligence.md](./03-news-media-intelligence.md) |
| 4 | Real Estate Intelligence & PropTech | $52.3B (PropTech) | ~18% | [04-real-estate-proptech.md](./04-real-estate-proptech.md) |
| 5 | Labor Market & Workforce Analytics | $280M+ | ~22% | [05-labor-workforce-analytics.md](./05-labor-workforce-analytics.md) |
| 6 | Search & Discovery APIs | $280M | ~65% | [06-search-discovery-apis.md](./06-search-discovery-apis.md) |

---

## The common pains — with evidence

### Pain 1 — Bot detection and rate limiting at scale break production pipelines

LinkedIn deploys rate limiting, IP blocking, CAPTCHA challenges, and advanced anti-automation algorithms. The documented result: "popular scraping tools shutting down or breaking overnight" and "fragile workflows that stop working when LinkedIn tweaks its code" (SociaVault, 2025; Generect, 2026). LinkedIn has pursued legal action against scrapers — hiQ Labs v. LinkedIn established precedent that is still being litigated. Zillow, major news outlets, and financial data sites deploy Cloudflare, browser fingerprinting, and dynamic JS rendering that defeats standard residential proxies within days of scaling.

The shared mechanism: residential proxy pools are flagged by behavioral analysis because they're shared across users. Volume triggers detection. Detection triggers blocks. Blocks trigger pipeline failures.

**A company building a LinkedIn-dependent data product cannot maintain a homegrown scraper at production scale. This is not a cost problem — it is an architectural constraint. The only solution is dedicated infrastructure that separates your traffic fingerprint from every other customer on the network. That is Bright Data's 72M+ IP network, 9 years of anti-detection R&D, and 99.7% documented success rate on the sites that block everyone else.** → This is a campaign.

Sources: [SociaVault 2025](https://sociavault.com/blog/linkedin-scraping-guide-2025) · [Generect 2026](https://generect.com/blog/linkedin-scraping/)

---

### Pain 2 — Scraper maintenance consumes engineering capacity that should go to product

The benchmark: **engineers spend 40% of their time fighting broken feeds and reprocessing stale data** — two full working days per week on maintenance, not product (Monte Carlo Data, via Estuary.dev).

The important clarification for 2026: this is not a "hire better engineers" problem. AI coding tools have made writing a scraper trivial. The problem is not building the scraper — it is the fact that **every time a target site changes its DOM, deploys new anti-bot middleware, or updates its JavaScript rendering, the scraper breaks at runtime regardless of how well it was written**. Cursor doesn't fix a 429. Copilot doesn't rotate your IPs. The maintenance loop is structural, not a skill gap.

For companies in this segment — alt data vendors, media monitors, PropTech platforms — scraper maintenance is direct opportunity cost: every hour on a broken pipeline is an hour not improving model accuracy, data coverage, or product differentiation.

Sources: [Estuary: Pipeline Maintenance](https://estuary.dev/blog/reducing-data-engineering-technical-debt) · [Crawlbase: Enterprise Web Scraping](https://crawlbase.com/blog/web-scraping-api-for-enterprise/)

---

### Pain 3 — LLM-powered data products hallucinate on stale or missing web data

This is the emerging pain specific to the new generation of AI-native data companies. Companies building data products on top of LLMs — AI-generated market intelligence, automated research briefs, AI-enriched lead data — face a structural reliability problem: **LLMs trained on static data produce outdated, fabricated, or generically plausible outputs when the underlying facts have changed** (K2View, NVIDIA Technical Blog, 2025).

Research identifies the specific failure modes in production RAG systems: fabricated statistics (the LLM generates plausible-sounding numbers from retrieved text chunks instead of computing them from real data), incomplete retrieval (vector search returns top-k similar documents but misses relevant scattered data), and out-of-domain fabrication (when no relevant data exists, the model returns similar-looking results and invents an answer) (MDPI Mathematics, 2025).

The only structural fix is real-time web grounding — retrieving live data at query time rather than relying on indexed or cached content. **A data product built on stale retrieval will hallucinate. A data product built on live web access will not.** This is why companies like Tavily, Exa, and Perplexity API exist — and why they all need reliable infrastructure underneath them. Bright Data is that infrastructure.

For the Vertical AI DaaS segment specifically: companies selling AI-enriched alt data, AI-generated media intelligence, or AI-summarized workforce analytics are delivering a product whose accuracy is directly dependent on the freshness of the web data feeding it. Stale data in → hallucinated insight out → customer complaint → churn.

Sources: [K2View: RAG Hallucination](https://www.k2view.com/blog/rag-hallucination/) · [NVIDIA: Agentic RAG](https://developer.nvidia.com/blog/traditional-rag-vs-agentic-rag-why-ai-agents-need-dynamic-knowledge-to-get-smarter/) · [CX Today: AI Hallucinations Start With Dirty Data](https://www.cxtoday.com/customer-analytics-intelligence/ai-hallucinations-start-with-dirty-data-governing-knowledge-for-rag-agents/)

---

### Pain 4 — Compliance gap blocks enterprise deals

**SOC 2 Type II is now standard in US enterprise vendor reviews. ISO 27001 is becoming mandatory in EU procurement.** Tavily has SOC 2. Exa has SOC 2 Type II. Firecrawl's certification is unverified. None have ISO 27001, GDPR documentation, CCPA, or CSA STAR.

For a Series A–C data company trying to sell to a Fortune 500 financial firm, hedge fund, or global enterprise: their data vendor's compliance stack is their compliance stack. Bright Data's full certification suite — SOC 2 Type II, ISO 27001, GDPR, CCPA, CSA STAR — is a pass-through competitive advantage.

Sources: [Hyperproof](https://hyperproof.io/soc2/) · [Tavily Trust Center](https://trust.tavily.com/) · [Exa Security](https://docs.exa.ai/reference/security-soc-2)

---

## Prioritization

**Go now — high urgency:**
- **Search & Discovery APIs** — 65% CAGR. Bing migration is live. Tavily, Firecrawl, Exa are conversations to have today.
- **B2B Intelligence & GTM** — Clay, Apollo, Lusha are scaling into LinkedIn rate limit walls right now.

**Go now — high deal size:**
- **Alternative Financial Data** — highest average deal size. Compliance documentation closes deals here.
- **Real Estate Intelligence** — PropTech infrastructure buyers. Attom, HouseCanary, Reonomy are well-capitalized.

**Go next — longer cycle:**
- **News & Media Intelligence** — Large accounts (Meltwater, Cision) but long enterprise sales cycles. Lead with Signal AI, Newswhip for faster motion.
- **Labor & Workforce Analytics** — Lead with the LinkedIn rate limit problem. Revelio Labs, Lightcast are the right first targets.

---

## What we are NOT doing

- **Retail / e-commerce** — separate GTM motion, different buyers, different competitive dynamics
- **Solo developers** — covered by the [/agents page](https://brightdata.com/agents); not this segment

---

## Content and influencer program

The top two priorities — Search & Discovery APIs and B2B Intelligence — have a specific buyer: **CTO and Head of AI/Product at AI-native startups and scaling B2B SaaS companies**. Not data engineers. The content and influencer program needs to reflect this.

---

### Blog posts — targeting AI product builders and GTM leaders

| Title | Audience | Angle |
|---|---|---|
| **"Your AI data product is only as good as your last web request"** | CTO at AI-native data companies | Hallucination = stale data = infrastructure problem. Live web grounding is the fix. |
| **"After Bing: what the best AI teams replaced it with"** | CTO / Head of AI mid-migration | Concrete migration guide. Bright Data SERP API as the answer. |
| **"The compliance test your AI data vendor will fail"** | CPO / Head of Partnerships at scaling data companies | Walk through the SOC 2 + ISO 27001 procurement gauntlet. Name who passes and who doesn't. |
| **"LinkedIn rate limits are not a bug in your scraper. They're the product."** | CTO at B2B intelligence companies | LinkedIn's anti-automation measures are intentional and permanent. Infrastructure is the only path. |
| **"The real cost of scraper maintenance in 2026 (hint: it's not your engineers)"** | CTO / VP Engineering at data startups | 40% stat + opportunity cost framing. Coding agents don't fix runtime IP blocks. |
| **"Why RAG-based data products hallucinate — and what actually fixes it"** | Head of AI, ML engineers at data companies | Technical depth on stale-retrieval hallucination. Real-time web grounding as the solution. |

---

### Short-form posts (Raz's LinkedIn — plain voice, no AI jargon)

1. **"The 3 sites that will break your data product at scale"** — LinkedIn, Zillow, major news outlets. Each with one specific technical reason.
2. **"Microsoft retired Bing API in August 2025. Here's what happened to the pipelines."** — Hot take on who moved where.
3. **"Your AI data product is hallucinating. Not because of the LLM. Because of the data feeding it."** — Stale retrieval → fabricated output → customer churn.
4. **"Tavily has SOC 2. Exa has SOC 2. Neither has ISO 27001. Here's why that matters when you sell to a bank."** — Compliance gap made specific.
5. **"AI coding tools made writing scrapers easy. They did nothing for the runtime."** — Cursor + Copilot don't rotate IPs.
6. **"Vertical AI DaaS: the $50B+ opportunity nobody is calling by name."** — Framing post for the category.

---

### Influencer and brand partnerships — aligned to actual ICP

**Tier 1 — AI product builders and startup CTOs**

| Partner | Platform | Audience | Activation |
|---|---|---|---|
| **Swyx / Alessio** (Latent Space Podcast) | Podcast + Substack | AI engineers, startup CTOs, agent builders | Episode on "live web access for AI agents" — natural fit with Bright Data MCP and agent infrastructure |
| **Greg Kamradt** (@GregKamradt) | Twitter/X + YouTube | 100K+ LLM practitioners, AI product builders | Tutorial: building a RAG pipeline with live web data via Bright Data. His audience builds exactly what we sell to. |
| **Ben Tossell** (Ben's Bites) | Newsletter | 100K+ AI founders and operators | Sponsored slot in Ben's Bites with specific angle: "the web access layer your AI product is missing" |
| **Lenny Rachitsky** (Lenny's Newsletter) | Substack | 700K+ product managers and founders | Guest post or ad on AI product infrastructure — framed as a product decision, not an engineering one |

**Tier 2 — B2B GTM and RevOps audience (for B2B Intelligence segment)**

| Partner | Platform | Audience | Activation |
|---|---|---|---|
| **Kyle Poyar** (Growth Unhinged) | Substack | 60K+ GTM leaders, SaaS operators | Co-authored piece: "The live data gap in AI-powered GTM" — positions Bright Data as infrastructure for Clay/Apollo users |
| **Sangram Vajre** (GTM Partners) | LinkedIn + Podcast | Enterprise GTM leaders | Thought leadership on AI signal quality in revenue operations |
| **The SaaStr community** | Newsletter + events | B2B SaaS founders and executives | Sponsored content at SaaStr Annual (May 2026) — "what your AI SDR tool is scraping and why it matters" |

**Tier 3 — Technical community integrations**

| Community | Tactic |
|---|---|
| **LangChain ecosystem** | Official Bright Data MCP integration tutorial — featured in LangChain docs and newsletter |
| **Hugging Face** | Publish live Bright Data datasets on HF Hub. "The live data" partner positioning. |
| **Y Combinator AI batch** | Direct outreach to AI/data companies in current batch — early adopter program |

---

## Success metrics

| Metric | Target | Timeline |
|---|---|---|
| LinkedIn campaigns live | 6 (one per segment) | End of April 2026 |
| Target accounts contacted | 120 (20 per segment) | End of May 2026 |
| Blog posts published | 6 | End of May 2026 |
| Influencer activations | 3 (Tier 1) | End of June 2026 |
| Discovery calls booked | 18 (15% response rate) | End of May 2026 |
| Pipeline created | $500K+ | End of Q2 2026 |
| Deals closed | 3 | End of Q3 2026 |

---

## How to use these briefs

1. **Pick the segment.** Start with Search & Discovery APIs and B2B Intelligence.
2. **Pull the ICP.** Title, company size, tech stack are specified. Use for LinkedIn targeting.
3. **Use the cold email hook.** First-touch ready in each brief. No links, <150 words, specific pain reference.
4. **Run the LinkedIn campaigns.** Three ad concepts per segment. One stat/comparison, one technical proof, one compliance angle.
5. **Work the target list.** 20 named companies × 6 segments = 120 accounts. All scraping-dependent, well-funded, actively scaling.

Being specific is the only message that works here. "We help data companies scale" is not a message. "You're hitting LinkedIn's rate limits at scale and there is no homegrown fix for it — here's why and here's ours" is.

---

*All six segment briefs are in this folder. Questions or updates: Raz Kaplan.*
