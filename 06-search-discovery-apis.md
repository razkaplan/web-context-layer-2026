# Vertical AI DaaS — Segment Brief: Search & Discovery APIs (AI-era)

**Prepared:** April 2026 | **Audience:** Raz Kaplan, AI GTM Lead, Bright Data

---

## Market Overview

- **Market size:** $280M+ AI-native search API market (2025), projected to reach $2.1B by 2029 — CAGR ~65%
- **Driver:** The rise of LLM-powered agents, RAG pipelines, and AI-native applications has created an entirely new category of web search infrastructure. AI agents need to search the live web, extract structured content, and return clean results — at scale, programmatically, without rate limits or CAPTCHA walls.
- **Web data dependency:** This segment IS the web data problem. Tavily, Exa, Perplexity's API, and competitors are essentially building structured web access layers — the same core capability as Bright Data's SERP API and Web Unlocker, but packaged for AI developer workflows.
- **Competitive dynamic:** This is Bright Data's most directly competitive AND most partnerable segment. Some of these companies are competing for the same AI developer mindshare. Others (especially Tavily, Exa) are potential technology partners or acquisition targets.

---

## Bright Data Offering

**Primary:** SERP API + Web Unlocker + Scraping Browser

| Product | Use Case |
|---|---|
| SERP API | Structured Google/Bing search results via API — the foundation of every AI search product |
| Web Unlocker | Reliable access to any public URL — feeds RAG pipelines and agent web browsing |
| Scraping Browser | Headless browser with built-in unblocking — for agents that navigate multi-step web interactions |
| Datasets | Pre-collected structured content for fine-tuning, knowledge base seeding, and offline RAG |

**Unique positioning in this segment:**
- Bright Data has 9 years of infrastructure advantage — proxy network, compliance certifications, uptime SLAs
- The "AI search" startups (Tavily, Exa) are building product layers on top of the same infrastructure problem Bright Data has already solved
- Bright Data can be positioned as the enterprise-grade backend that AI search companies either partner with or compete against

---

## Positioning

> "Every AI agent that searches the web needs an infrastructure layer that doesn't get blocked. That's Bright Data — not a search product, the reliable web access layer underneath every search product."

**Frame:** Infrastructure partner and enterprise alternative for AI search API companies and their customers.

**For AI developers building on Tavily/Exa:** "You're building on a search API. For production workloads, you need an infrastructure layer with SLAs."

**For enterprise AI teams that outgrow search API rate limits:** "When you hit Tavily's rate limits, Bright Data is the next step — same capability, enterprise scale."

**Competitive angle on Tavily:** Tavily is a wrapper around search. Bright Data is the layer that makes any URL accessible — broader scope, higher reliability, better compliance documentation.

---

## ICP

### Buyer Profile
- **Primary:** CTO, Head of AI/ML Engineering, Head of Platform at AI-native startups and enterprise AI teams
- **Secondary:** Developer Relations, VP Product at AI tool companies; Founding Engineer at LLM application startups
- **Champion:** AI engineer who has personally hit rate limits or CAPTCHA walls in a production RAG pipeline

### Company Size
- Seed–Series B AI-native application companies (5–100 engineers)
- Enterprise AI teams at Fortune 500 companies building internal AI agents (50–500 engineers)
- Developer tooling companies building on top of LLM APIs (10–200 employees)

### Tech Stack
- Python (LangChain, LlamaIndex, CrewAI, AutoGen) for agent orchestration
- OpenAI / Anthropic / Google APIs as LLM backbone
- Tavily / Exa / SerpAPI as current search layer (the incumbent to displace or complement)
- Pinecone / Weaviate / Chroma for vector storage
- FastAPI / Python async for high-throughput agent backends
- AWS / GCP / Azure for deployment

### Core Pains

1. **Rate limits at production scale** — Tavily, SerpAPI, and Google Custom Search all impose strict rate limits. AI agents running at scale hit ceilings fast and have no clean path to enterprise-grade throughput.
2. **Structured content extraction failure** — Search APIs return links. Getting clean, structured content from those links requires a second-layer scraping tool that most teams bolt together ad-hoc.
3. **CAPTCHA and bot detection in agent workflows** — When AI agents navigate the web, sites detect them and block them. Standard headless browsers (Playwright, Puppeteer) fail on major sites without specialized infrastructure.
4. **Compliance documentation for enterprise** — Enterprise customers require data provenance, SOC 2, and audit trails. Search APIs can't provide this. Teams building on Bright Data can.
5. **Cost predictability** — Per-search pricing models don't scale well for high-volume RAG pipelines. Volume-based pricing (Bright Data's model) is more predictable for production workloads.
6. **Freshness vs. cache** — Many search APIs serve cached results. AI agents operating on time-sensitive queries (market news, live events, current prices) need real-time access.

---

## Messaging

### Hook 1 — Rate limits
> "Your AI agent is production-ready. Your search API isn't."

### Hook 2 — Infrastructure vs. product
> "Tavily is a product. Bright Data is the infrastructure. There's a reason some of the most serious AI teams build on us directly."

### Hook 3 — Full-stack web access
> "Search APIs return links. Bright Data returns the page — structured, clean, unblocked."

### Hook 4 — Enterprise readiness
> "SOC 2, ISO 27001, GDPR. When your enterprise customer asks your legal team about data provenance, this is the answer."

### Hook 5 — Scale without ceiling
> "72M+ IPs. No shared pool. No rate limits we can't route around. Scale your agent fleet without a data access ceiling."

### Cold email opener
```
Subject: production web access for AI agents

Hi [Name],

When [Company]'s agents search the web at scale — what do you hit first: rate limits, CAPTCHAs, or both?

Most AI teams we talk to cobble together SerpAPI + Playwright and call it done. It works until it doesn't — usually when you're in front of a customer.

We've built the infrastructure layer that makes this a solved problem. Happy to show you how teams like [relevant customer] use it.

Raz
```

---

## LinkedIn Campaign

### Campaign 1 — Rate Limit Reality Check

**Format:** Stat card
**Headline:** "Your AI agent's biggest limitation isn't the LLM. It's the web access layer."
**Body:** Rate limits, CAPTCHAs, bot detection — the hidden blockers that stop AI agents in production. Bright Data's infrastructure is built specifically for the scale and reliability AI agents require.
**Visual:** Code snippet showing `RateLimitError: 429` in red → Bright Data API call returning clean JSON in green
**CTA:** "Build production-grade AI agent web access →"
**Targeting:** "AI Engineer", "ML Engineer", "Head of AI", "CTO", "Founding Engineer" | Companies with "AI", "LLM", "agent" in description

---

### Campaign 2 — The Full Stack

**Format:** Comparison table
**Headline:** "Search APIs return links. Bright Data returns the page."
**Body:** Tavily, Exa, SerpAPI — great for getting URLs. For getting what's on those URLs — clean, structured, unblocked — you need a second layer. Or you could use the platform that does both.
**Visual:** Comparison: Search API output (list of URLs) vs. Bright Data output (structured JSON with full content)
**CTA:** "See the difference"
**Targeting:** Same as Campaign 1 + "LangChain", "LlamaIndex", "RAG pipeline" keywords

---

### Campaign 3 — Enterprise Compliance

**Format:** Thought leadership / Document ad
**Headline:** "Your AI agent can search the web. Can it pass your customer's security review?"
**Body:** Enterprise AI deployments require data provenance, audit trails, and compliance certifications. Most search APIs can't provide these. Bright Data can — SOC 2 Type II, ISO 27001, GDPR, CCPA.
**Visual:** Trust center badge logos + enterprise-style security documentation
**CTA:** "See the compliance brief"
**Targeting:** "VP Engineering", "CISO", "Head of Enterprise Sales" at AI companies scaling to enterprise customers

---

### Campaign 4 — Direct to AI Agent Builders (Developer-focused)

**Format:** Technical tutorial / code post
**Headline:** "Stop duct-taping SerpAPI + Playwright. Here's the single-integration alternative."
**Body:** Technical walkthrough showing how to replace a fragile multi-tool scraping stack with a single Bright Data integration — one API, full web access, no blocks.
**Visual:** Before/After code comparison. Before: 4 separate tools, error handling, retry logic. After: 3 lines of Bright Data API.
**CTA:** "See the code →" (links to documentation)

---

## Events Calendar (April – October 2026)

| Event | Date | Location | Why Attend |
|---|---|---|---|
| **AI Engineer Summit** | June 2026 | San Francisco | Premier AI developer conference. LangChain, agent builders everywhere. |
| **Gartner AI Summit** | June 2026 | Austin | Enterprise AI. Decision-makers building internal agent platforms. |
| **O'Reilly AI Conference** | October 2026 | San Francisco | AI engineering + ML infra. RAG pipeline and agent track. |
| **LangChain/LlamaIndex Dev Day** | TBD 2026 | San Francisco | Developer ecosystem events for agent framework communities. |
| **a16z AI Show** | Quarterly | San Francisco | Andreessen Horowitz AI portfolio events — target emerging AI companies. |
| **Y Combinator Demo Day** | April / October 2026 | San Francisco | New AI-native companies — early adoption targets. |
| **Cerebral Valley Hackathons** | Monthly | San Francisco | Grassroots AI developer community. Agent builders. |
| **AWS re:Invent AI Track** | December 2026 | Las Vegas | Enterprise cloud + AI infra. Strong agent workload presence. |

---

## Top 20 Target Companies

| # | Company | Why | Key Title to Target |
|---|---|---|---|
| 1 | **Tavily** | AI search API; most direct competitor but also potential integration partner | Co-founder / CTO |
| 2 | **Exa (formerly Metaphor)** | Semantic web search API for AI; SERP API competitor | Co-founder / Head of Engineering |
| 3 | **Perplexity AI** | AI search product + API; massive web crawling infrastructure | Head of Infrastructure |
| 4 | **You.com** | AI search + developer API | VP Engineering |
| 5 | **Firecrawl** | Web scraping API for AI; direct Web Unlocker competitor | Co-founder / CTO |
| 6 | **Apify** | Web automation + scraping platform; enterprise automation buyers | Head of Partnerships |
| 7 | **Jina AI** | Neural search + web content extraction; vector-native | CTO |
| 8 | **Mendable (SiteGPT)** | AI search for docs and products; RAG pipeline infrastructure | CTO |
| 9 | **Browserbase** | Cloud browser infra for AI agents; Scraping Browser competitor | Co-founder / CTO |
| 10 | **Stagehand (Browserbase)** | Browser automation SDK for AI agents | Head of Engineering |
| 11 | **Crew AI** | Multi-agent framework; web access is a core agent tool need | Co-founder / CTO |
| 12 | **LangChain** | Agent framework; Bright Data MCP + tool integration opportunity | Head of Integrations |
| 13 | **Cohere** | LLM API + RAG tooling; enterprise AI; web grounding need | Head of Platform Engineering |
| 14 | **Glean** | Enterprise AI search; web data enrichment | VP Engineering |
| 15 | **Otter.ai / AssemblyAI** | AI transcription + search; content enrichment pipeline | Head of Data |
| 16 | **Kagi** | Privacy-first search; developer API focus | CTO |
| 17 | **SerpAPI** | Current search API incumbent; customers who outgrow it | — (competitive reference) |
| 18 | **Bright Data MCP users** | Companies already integrated via MCP — upsell to full platform | Head of Engineering |
| 19 | **Dust.tt** | Enterprise AI agent platform; web access core need | Co-founder / CTO |
| 20 | **Wordware** | AI workflow builder; web tool integrations needed | Head of Engineering |

---

## Competitive Notes

**Tavily:** Positioned as "AI-optimized search API." Weaker on: compliance docs, full-page content extraction, enterprise SLAs. Strong on: developer experience, LangChain/CrewAI native integrations, price for low-volume use cases.

**Firecrawl:** Web scraping API, great developer experience, simpler pricing. Weaker on: proxy network scale, compliance certs, geographic coverage, SERP structured data.

**Exa:** Semantic/neural search — different query paradigm. Strong for semantic similarity search. Weak for real-time web access and structured SERP results.

**Bright Data advantage in this segment:** The only player with 9-year enterprise track record, compliance certifications, 72M+ IP network, structured dataset products, and full-spectrum web access (proxies + headless browser + SERP + datasets in one platform).

---

*Brief prepared for Bright Data GTM. Internal use only.*
