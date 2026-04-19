# Own the CaaS Infrastructure Layer

**Owner:** Raz Kaplan · April 2026

---

## Why now

Context windows went from 4K tokens in 2023 to 1M+ in 2026. Models can now ingest entire datasets in a single call. That changed the economics of every data product: the bottleneck shifted from "how do I fit data into the model" to "how do I get fresh, structured, real-time data to feed it." Every company in this universe has AI in the pipeline. They're not selling CSVs. They're running LLM enrichment, building RAG systems, powering AI agents. The output is structured intelligence, not raw data.

To build it, they scrape at a scale and variety traditional DaaS never needed. And because these products run on LLMs, they introduce a new failure class: hallucination from stale data. Both forces point to the same need: production-grade, real-time web access. We sell that. Datasets updated daily across 50,000+ sources. Maintained scrapers that handle anti-bot defenses automatically. Fast SERP for real-time search signals. 90 PB Web Archive for historical depth. Backed by 400M+ residential IPs across 195 countries, 99.95% success rate, and a contractual 99.99% uptime SLA. 20,000+ customers. Five compliance certifications (SOC 2 Type II, ISO 27001, CSA STAR Level 1, GDPR, CCPA) and the only court-tested legal posture in the category: Meta v. Bright Data (2024, won); X v. Bright Data (May 2024, ruled in Bright Data's favor).

The category doesn't have a name yet. We're naming the category we sell into: Context as a Service. Whoever names it owns it. HubSpot did it with "Inbound." Gainsight did it with "Customer Success." This is our version.

---

## The universe

200 AI-native data companies. Not general DaaS. Every account has AI in the pipeline: LLM enrichment, RAG, agent systems, or AI-powered analysis. 15 segments. 110 with ICP fit A (heavy scraping dependency). 104 Tier 1.

Top segments by priority:

| Segment | Accounts | T1 | Why now |
|---|---|---|---|
| B2B Intelligence & GTM | 39 | 18 | Clay, Apollo, Lusha hitting LinkedIn blocks daily |
| Alternative Financial Data | 23 | 10 | Highest ACV. Compliance closes it. |
| News & Media Intelligence | 21 | 12 | Signal AI, Newswhip. Long cycles, large deals. |
| Labor & Workforce Analytics | 13 | 7 | LinkedIn problem. Revelio Labs, Lightcast, Coresignal. |

Full universe: `universe-daas-200-targets.csv`. Hottest 20 accounts listed in the campaign brief.

---

## Assets

**1. State of the DaaS Industry 2026** (done)
Interactive report. Market map of 75+ companies across 5 segments. CAGR charts, funding analysis, infrastructure dependency thesis. Shareable version live with social image export. CTA: "Talk to a data infra expert."

**2. Landing page: brightdata.com/ai/data-packages** (done)
Product page for data companies. ROI calculator, compliance comparison table, segment-specific use cases.

**3. 10 LinkedIn ads** (done)
Thought Leader Ads from Raz's profile (2.68% avg CTR), carousel formats, video concepts. Campaign anchor: "Stop building scrapers. Start shipping pipelines." Messaging grounded in the 4 pains: bot detection breaks pipelines, LLMs hallucinate on stale data, 40% of eng time on maintenance, one missing cert kills a deal.

**4. BDR email cadence** (done)
10 touches over 21 days. 4 segment-specific templates (B2B Intelligence, Alt Finance, News & Media, Labor Analytics). No e-commerce. Each template references the target's specific data product and collection challenge. Core ROI frame: a 3–5 engineer scraping team runs $618K–$957K/year fully loaded. Comparable Bright Data coverage: $12K–$36K/year. The engineers don't disappear — they move off scraper maintenance onto the product logic, enrichment, and AI that actually differentiate the product.

**5. PodCaaSt: "Context Is All You Need"** (in production)
Weekly video podcast from Bright Data SF studio. Every episode is a standalone content asset: full video on YouTube, audio on Spotify/Apple, 3-5 short clips for LinkedIn and X, transcript published on BrightContext. Guests become distribution: each episode reaches their audience with a BD-branded piece of content. Season 1 guests include Harrison Chase (LangChain), Jerry Liu (LlamaIndex), Jay Kreps (Confluent), Mike Tung (Diffbot), Ben Zweig (Revelio Labs). The podcast seeds every other channel: blog material, conference speakers, BDR warm intros, event anchors.

**6. CaaS or DaaS? — Interactive Web Game** (done)
Standalone web game at brightdata.com/caas-or-daas. User enters any data company URL. Bright Data's Web Intelligence reads the homepage, analyzes positioning and delivery model, and returns a verdict: CaaS or DaaS, with a confidence score and 3 reasons. Shareable result card with LinkedIn-ready copy. Designed to go viral inside the ICP community. Every share is a BD impression. Every result drives curiosity about the CaaS category. Playable at events, embedded in BDR outreach ("Run your own company through it"), promoted by podcast guests. Built on Bright Data's own tools, demonstrating the product in real-time.

---

## Channels

### 1. External distribution (paid + earned)

Place content where CaaS buyers already read. Three newsletters, ranked by audience overlap:

| Newsletter | Subscribers | Audience | Cost per placement |
|---|---|---|---|
| **Latent Space** (swyx + Alessio Fanelli) | 200K+ | AI engineers building agents and RAG. Exact buyer persona. | $5K-$15K |
| **SeattleDataGuy** (Benjamin Rogojan) | 114K+ | Data engineers building pipelines. The implementers who pull in our SDK. | $1.5K-$4K |
| **TLDR AI** (Dan Ni) | 500K+ | Broad AI/ML audience. Best for awareness at scale. | $5K-$15K |

Action: Latent Space first. Guest post: "How CaaS companies build production web data pipelines." Pursue a podcast episode on Latent Space (cross-promote with our show). Budget: $15K for Q2.

### 2. Owned media (podcast + blog + meetup)

**PodCaaSt** ("Context Is All You Need"). Weekly video podcast from Bright Data SF studio. External host (4 candidates pitched: Jason Howell/TWIT alumni, Ian Faison/Caspian Studios, Alex Kantrowitz/Big Technology, Paris Martineau/TWIT). 20 guests in Season 1: Harrison Chase (LangChain), Auren Hoffman (SafeGraph/LiveRamp), Mike Tung (Diffbot), Jay Kreps (Confluent/Anthropic board), Jerry Liu (LlamaIndex), Ben Zweig (Revelio Labs), Matt Turck (FirstMark). Every guest is a future conference speaker and blog contributor.

**BrightContext** (brightdata.com/context). Industry blog, not a company blog. 3 articles/week. Weekly newsletter "The Context Layer." Quarterly CaaS Index benchmark (uptime, coverage, compliance, pricing across providers). SEO target: 10K+ monthly visits by Month 12.

**CaaSCon**. Q4 2026. 1-day, 75-100 attendees, invite-only, Bright Data SF office. Podcast guests become speakers. Free admission. Sponsorship revenue covers costs. Every session recorded for 3+ months of content post-event.

### 3. BDR outreach (human)

10-touch cadence over 21 days. Target: T1 accounts with ICP fit A or B. Entry criteria: at least one qualifying signal detected (see signals below). Personalized first touch referencing their specific data product.

Cadence: Email (Day 1) > LinkedIn connect (Day 3) > Email with report (Day 5) > LinkedIn engage (Day 8) > Email case study (Day 10) > Phone (Day 13) > Email technical proof (Day 15) > LinkedIn voice note (Day 17) > Email breakup (Day 19) > Phone final (Day 21).

Target: 18 discovery calls by end of May. $500K pipeline by end of Q2. 3 deals closed by Q3.

### 4. Automated signal monitoring

Signals machine runs daily. Three tiers:

**Daily (highest intent):**
- Reddit (r/webscraping, r/dataengineering): "Cloudflare blocked," "429," "rate limited," "IP banned"
- Google Alerts: all competitor names + "alternative" or "migration"
- LinkedIn Jobs: "web scraping engineer," "data collection engineer" at universe companies

**Weekly:**
- Crunchbase: new funding rounds for data companies (Series A-C, >$5M)
- GitHub Issues: puppeteer/playwright/scrapy repos, blocking-related issues
- npm/PyPI: download spikes for scraping libraries

**Monthly:**
- Engineering blog monitoring: "How we built our scraper" posts
- Conference talks mentioning scraping infrastructure
- Google Trends: "web scraping compliance," "data provenance"

Every signal auto-routes to the BDR team with context. High-intent signals (job postings, competitor displacement searches, community pain posts) trigger same-day outreach.

### 5. SF Loft Events

The Bright Data SF office is the physical anchor of the CaaS community. Two recurring series, both built around the universe of 200 target companies. The goal is not awareness — it's relationships. Every event should result in at least 3 new pipeline conversations and 1 piece of published content.

**The frame for every event:** The universe companies are not just targets. They are collaborators in naming and building the CaaS category. Invite them to present, not just attend. Ask them to bring an engineer. Feature their product as part of the session. When a company in the universe co-hosts an event with Bright Data, they become a category partner, not a prospect.

**AI Tinkerers SF** (Monthly, ~40 attendees)

AI Tinkerers is a global practitioner community of engineers who ship things. Bright Data hosts the SF chapter. One slot per event is reserved for a universe company to demo their data product (15 min, no pitch, pure technical demo). This is the invite: "We're building a series on how AI data companies use web intelligence. We'd love to feature how you do it."

| Session | Topic | Universe anchor |
|---|---|---|
| 1 | Build a live web data pipeline for your AI agent | Demo + 90-min build. Feature a B2B intelligence company. |
| 2 | Context-first RAG: real-time web vs. static embeddings | Invite a news/media intelligence company to co-present. |
| 3 | Web data for agents: what breaks in production | Panel: 3 universe company engineers. BD moderates. |
| 4 | CaaS or DaaS? — Live game night | Run the game live on the screen, classify the audience's companies in real-time. |

**lablab.ai SF Hackathon** (Quarterly, 60-100 attendees)

lablab.ai runs AI hackathons globally with a developer community of 100K+. Bright Data sponsors the SF edition and provides the challenge track. Universe companies are invited as challenge co-sponsors and judges — their real data problems become the hackathon prompts.

| Track | Challenge | Universe co-sponsor |
|---|---|---|
| Web-native AI agent | Build an agent that answers questions using only live web data | Exa, Perplexity |
| AI data product | Build a CaaS product using BD's APIs, judged on context quality | Apollo, Crunchbase |
| Real-time RAG | Build a RAG pipeline with zero static embeddings | Signal AI, Meltwater |

**Asset loop — how every event feeds the other channels:**
- Every attendee gets 30-day BD API trial, no credit card. Trial opens a BDR sequence.
- Game night sessions filmed and cut into 60-second clips for LinkedIn.
- Universe company demo at AI Tinkerers becomes a BrightContext article ("How [Company] builds their data pipeline").
- Top 3 hackathon builders invited to podcast episodes in the following month.
- CaaSCon Q4 speaker list built directly from event speakers and hackathon winners.
- Each event email goes to the full universe list. Subject line: "You're in the report. Come build with us."

**Budget:** $3K-$5K per AI Tinkerers event. $8K-$12K per lablab.ai hackathon. ~$60K/year for 4 tinkerers + 4 hackathons.

---

### 6. Existing customer engagement

Cross-sell and upsell motion for current Bright Data customers who match the CaaS profile:

- **Identify:** Pull current customer list. Match against the 200-account universe. Flag customers already using Web Unlocker or SERP API at scale.
- **Invite:** CaaSCon invitations to existing customers. "You're already building on us. Come meet the rest of the market." Builds community, reduces churn, opens upsell conversations.
- **Podcast guests:** Invite 3-5 existing customers as podcast guests in Season 1. Their stories validate the product. Their appearance builds the relationship.
- **Case studies:** Partner with 2-3 existing customers to co-author BrightContext articles. "How [Customer] reduced scraping costs by 90% and redirected 3 engineers to product." Published on BrightContext, shared by both parties.
- **Quarterly review + CaaS Index:** Share the quarterly CaaS Index with existing customers before public release. Exclusive access builds loyalty and gives CSMs a reason to schedule QBRs.

---

## Timeline

| Month | Action | Output |
|---|---|---|
| **1** | Launch podcast. Book guests 1-10. Latent Space placement. | 4 episodes recorded. 1 newsletter placement live. |
| **2** | Launch BrightContext. Start BDR cadence on T1 accounts. | 8 articles. First outreach wave (40 accounts). |
| **3** | Announce CaaSCon. 10 episodes live. Second outreach wave. | Newsletter at 500+. 6-8 discovery calls booked. |
| **6** | 25 episodes. 36+ articles. Conference 80% booked. | $250K+ pipeline. Newsletter at 2K+. |
| **9** | CaaSCon happens. Content blitz. "State of CaaS 2026" report. | 8-10 session videos. 20+ clips. 5-6 deep articles. |
| **12** | 46 episodes. 150+ articles. 10K organic visits. | Year 1 pipeline: $380K-$1.2M. |

---

## Cost and return

| Program | Year 1 Cost |
|---|---|
| PodCaaSt (production, host, promotion) | $132K |
| CaaSCon (catering, AV, speakers, marketing) | $45K |
| BrightContext (writers, SEO, design, newsletter) | $123K |
| External newsletters (3 placements) | $20K |
| PR firm | $120K-$240K |
| **Total** | **$440K-$560K** |

| Revenue source | Conservative | Optimistic |
|---|---|---|
| Podcast guest conversions | $150K | $600K |
| CaaSCon pipeline | $150K | $375K |
| BrightContext organic inbound | $50K | $200K |
| BDR outreach pipeline | $250K | $500K |
| Sponsorship + existing customer upsell | $80K | $160K |
| **Total** | **$680K** | **$1.8M** |

Breakeven: Month 8-12. Year 2 compounds at marginal cost.
