# People Analytics Platform

> Candidate #87 · Researched: 2026-05-01

## Existing Products and Software Packages

| Tool | Description | Type | Pricing | Strengths / Weaknesses |
|---|---|---|---|---|
| **Visier People** | Cloud-native people analytics leader; workforce planning, attrition prediction, DEI dashboards | Commercial | $25,000–$120,000/year depending on employee count and modules | Strength: pre-built HR content library, fastest time-to-insight. Weakness: expensive for mid-market; data model can be rigid |
| **Workday People Analytics** | ML-powered storyteller engine embedded in Workday; surfaces anomalies automatically | Commercial | Bundled add-on to Workday HCM; ~$3–$6 PEPM additional | Strength: zero ETL for Workday customers. Weakness: only useful inside Workday; limited cross-system blending |
| **SAP SuccessFactors Workforce Analytics** | Embedded analytics in SF HCM; standard HR metrics and benchmarking | Commercial | Part of SF HCM bundle; ~$6–$10 PEPM analytics module | Strength: large pre-built metric library, global benchmarks. Weakness: poor UX, slow iteration cycles |
| **One Model** | People analytics warehouse; predictive models for turnover, diversity, performance | Commercial | Custom enterprise pricing; ~$50K–$200K/year | Strength: open data architecture, non-HR data blending. Weakness: requires data engineering resources to deploy |
| **ChartHop** | People data platform; org planning, DEI tracking, comp analytics, headcount planning | Commercial | ~$8–$16 PEPM; growth tier ~$20 PEPM | Strength: modern UI, real-time org chart + analytics. Weakness: lighter on predictive ML than Visier |
| **OrgVue** | Workforce design and org analysis tool; structural modelling, span-of-control | Commercial | Custom enterprise; typically $60K–$250K/year | Strength: best-in-class org design visualisation. Weakness: narrow focus, not a full analytics platform |
| **intelliHR** | People analytics + performance platform; attrition risk, diversity, engagement | Commercial | ~$6–$12 PEPM | Strength: engagement + analytics combined. Weakness: smaller client base, Australasia-centric |
| **OrangeHRM (Open Source)** | Open-source core HR with basic reporting; community-built analytics modules | Open Source | Free (self-hosted); commercial cloud from ~$2 PEPM | Strength: free, customizable. Weakness: basic analytics only; no predictive ML; community maintenance pace slow |

## Relevant Industry Standards or Protocols

- **ISO 30414:2018 Human Capital Reporting** — international standard defining 58 HR metrics organisations should measure and disclose; directly relevant to people analytics output.
- **GRI 401 / 405 Standards** — Global Reporting Initiative standards for workforce and diversity disclosures; increasingly required for ESG reporting.
- **GDPR Article 22 / CCPA** — regulates automated decision-making from people analytics; requires human review for employment decisions derived from profiling.
- **IEEE P7003 (Algorithmic Bias)** — standard for identifying and mitigating bias in automated systems; applies to AI-driven turnover and performance predictions.
- **XBRL (eXtensible Business Reporting Language)** — used for structured financial and HR data reporting to regulators; emerging relevance for human capital disclosures.
- **HR Open Standards** — defines canonical HR data schemas; relevant for ingesting data from multiple HRIS sources into a people analytics warehouse.

## Available Research Materials

1. Mordor Intelligence (2025). *HR Analytics Market Size, Trends & Forecast to 2031*. mordorintelligence.com. https://www.mordorintelligence.com/industry-reports/hr-analytics-market — Commercial market report.
2. Grand View Research (2025). *HR Analytics Market Size And Share, Industry Report 2033*. grandviewresearch.com. https://www.grandviewresearch.com/industry-analysis/hr-analytics-market — Commercial market sizing.
3. S&P Global Market Intelligence (2026). *HR Technology Market Forecast: People Analytics and Talent Intelligence*. spglobal.com. https://www.spglobal.com/market-intelligence/en/news-insights/research/2026/02/hr-tech-market-2025 — Peer-quality analyst report.
4. Research Nester (2025). *People Analytics Market Size & Share, Growth Analysis 2037*. researchnester.com. https://www.researchnester.com/reports/people-analytics-market/7689 — Market sizing; preprint quality.
5. Agile HR Analytics (2025). *Top People Analytics Vendors Compared: Visier, OneModel, OrgVue and More*. agile-hr-analytics.com. https://www.agile-hr-analytics.com/top-people-analytics-vendors-compared-visier-onemodel-orgvue-and-more/ — Independent practitioner comparison.
6. Visier (2025). *What Is People Analytics and How Do I Get Started?* visier.com. https://www.visier.com/blog/what-is-people-analytics-and-how-do-i-get-started/ — Vendor content; useful definitions.
7. Gartner Peer Insights (2026). *Best People Analytics Reviews*. gartner.com. https://www.gartner.com/reviews/market/people-analytics — Verified user reviews.

## Market Research

**Market Size:**
- HR Analytics market: $4.89B in 2025, projected $10.82B by 2031 (CAGR 13.64%) — Mordor Intelligence.
- People Analytics market (broader definition): $10.1B in 2025, projected $41.5B by 2037 (CAGR 12.4%) — Research Nester.
- Voluntary turnover costs U.S. employers $1 trillion annually (2025), creating strong ROI case for predictive attrition tools.

**Pricing Table:**

| Tier | Example | Price |
|---|---|---|
| Open source / free | OrangeHRM community | $0 (self-hosted) |
| SMB / growth | ChartHop Starter, intelliHR | $6–$16 PEPM |
| Mid-market | One Model, Visier SMB | $50K–$120K/year |
| Enterprise | Visier Enterprise, OrgVue | $120K–$500K+/year |

**Buyer Personas:**
- **Chief People Officer / CHRO** — requires board-ready human capital metrics; ISO 30414 compliance; ESG disclosures.
- **People Analytics Lead / HR Data Scientist** — builds predictive models; needs raw data access and Python/R integration.
- **HR Business Partner** — wants self-service dashboards for their business unit; turnover and headcount at a glance.
- **Finance / Workforce Planning team** — needs headcount forecasts and cost-per-hire data tied to budget cycles.

**Notable M&A / Funding:**
- Visier raised $125M Series E (2021, valuation ~$1B); no further public rounds since.
- ChartHop raised $35M Series B (2021).
- One Model raised $25M Series B (2022).
- Workday acquired Peakon (employee listening) for $700M (2021) and integrated analytics capabilities.

## AI-Native Opportunity

- **Continuous flight-risk scoring without manual model maintenance**: existing tools require data science teams to build and retune attrition models; an AI-native platform can auto-build and continuously update turnover prediction models by learning from the organisation's own patterns — making predictive analytics accessible to companies without a data science function.
- **Natural-language querying of HR data**: HR leaders cannot write SQL; current tools require pre-built dashboards or BI skills; an AI-native interface where a CHRO types "why did attrition spike in Sales last quarter?" and receives a narrative explanation with root-cause attribution would be genuinely transformative.
- **Automated narrative reporting for ISO 30414 / ESG disclosures**: generating the human capital report is a manual, quarterly pain point; AI can draft the structured disclosure document directly from the analytics warehouse.
- **Cross-signal correlation**: current platforms silo engagement, performance, and workforce data; AI can identify non-obvious correlations (e.g., span-of-control > 10 predicts 40% higher attrition in engineering) without a data scientist writing the hypothesis first.
- **OSS differentiation**: a permissively licensed people analytics engine with pre-built connectors to major HRIS systems, a turnover prediction model trained on synthetic HR data (avoiding cold-start), and a natural-language query layer would be the first credible open-source alternative to Visier — capturing the growing number of HR teams who want analytics without enterprise SaaS pricing.
