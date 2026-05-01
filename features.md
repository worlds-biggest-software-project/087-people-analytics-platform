# People Analytics Platform — Feature & Functionality Survey

> Candidate #87 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Visier People | Commercial SaaS | Proprietary; annual subscription | https://www.visier.com/ |
| Workday People Analytics | Commercial SaaS | Proprietary; add-on to Workday HCM | https://www.workday.com/en-us/products/human-capital-management/people-analytics.html |
| SAP SuccessFactors Workforce Analytics | Commercial SaaS | Proprietary; bundled with SF HCM | https://www.sap.com/products/hcm/workforce-analytics.html |
| One Model | Commercial SaaS | Proprietary; custom enterprise | https://onemodel.co/ |
| ChartHop | Commercial SaaS | Proprietary; PEPM subscription | https://www.charthop.com/ |
| OrgVue | Commercial SaaS | Proprietary; custom enterprise | https://www.orgvue.com/ |
| intelliHR | Commercial SaaS | Proprietary; PEPM subscription | https://intellihr.com/ |
| OrangeHRM | Open Source / Commercial | GPL-2.0 (OSS core); proprietary cloud | https://orangehrm.com/ |

## Feature Analysis by Solution

### Visier People

**Core features**
- Pre-built HR content library: 2,000+ pre-defined metrics, guided analyses, and benchmark comparisons covering attrition, diversity, performance, compensation, and workforce planning
- Attrition and flight-risk prediction: ML models trained on the organisation's own data patterns; continuously updated as new data arrives; prescription layer recommends specific retention interventions for high-risk individuals
- DEI analytics: representation dashboards tracking diversity across the full employee lifecycle — pipeline, hiring, promotion, compensation, and attrition; pay equity analysis with statistical significance testing
- Workforce benchmarking: anonymised comparison against peer organisations drawn from Visier's 50,000+ organisation network
- AI-powered org design: interactive org chart modeling with span-of-control analysis and cost impact modeling (2026 expansion)
- Workforce Intelligence: natural language query interface — HR leaders type a question and receive a narrative explanation with root-cause attribution

**Differentiating features**
- Fastest time-to-insight in market: pre-built HR content means organisations can answer standard people analytics questions in weeks, not months of data engineering
- Benchmarking network: proprietary anonymised peer data is a unique differentiator — no OSS or build-your-own solution can replicate this without Visier's scale
- Narrative-first UX: Visier surfaces anomalies and tells a story rather than presenting raw dashboards requiring interpretation
- People Data Platform: normalises heterogeneous HR data from 50+ HRIS sources into a unified semantic model — the heaviest data engineering work is pre-done

**UX patterns**
- Guided narrative surfacing anomalies automatically; HR leaders do not need to know what questions to ask
- Consumer-grade UX designed for HR generalists, not data scientists
- Self-service analytics: HR Business Partners can answer their own questions without submitting requests to a central analytics team
- Mobile-accessible executive dashboards

**Integration points**
- Pre-built certified connectors to Workday, SAP SuccessFactors, Oracle HCM, ADP, UKG, Ceridian, BambooHR, and 50+ HRIS systems
- Visier People Data Platform: staging and normalisation layer handling schema mapping, historical data reconciliation, and metric calculation
- REST API for custom data sources and bi-directional data push
- Workday Prism integration for Workday-native data blending

**Known gaps**
- Expensive: $25K–$200K/year; effectively priced out of sub-1,000-employee organisations
- Planning depth is secondary: attrition prediction and analytics are excellent; headcount scenario planning and financial cost modeling lag Anaplan and Orgvue
- Skills-based analytics rely on customer-provided skills data; no native skills inference
- Benchmarking network data is proprietary; customers cannot export peer comparison datasets

**Licence / IP notes**
- Fully proprietary; raised $125M Series E (2021) at $1B valuation
- People Data Platform semantic layer and benchmarking methodology are Visier's core proprietary IP
- No OSS components; customers access data via Visier-controlled interface

---

### ChartHop

**Core features**
- People data platform: unified employee record combining HRIS data, performance, compensation, equity, and custom fields in a single configurable data model
- Interactive org chart: real-time, filterable org chart enriched with people data (compensation, skills, performance, diversity attributes) for operational visibility
- Headcount and scenario planning: model org changes (new hires, departures, restructures) with real-time cost and headcount impact calculation
- DEI tracking: representation dashboards by department, level, and location with trend monitoring over time
- Compensation analytics: pay equity analysis and compensation benchmarking integrated with the headcount planning model
- Custom reporting: configurable dashboards and reports without requiring BI tool expertise

**Differentiating features**
- Best-in-class combination of operational org visualisation and people analytics in a single platform
- Real-time org chart: the living org chart updates automatically from HRIS data and shows a true picture of the organisation at any point in time
- Scenario planning UX: accessible to HR and Finance teams without data science expertise; plan changes in the org chart view and see cost impact immediately

**UX patterns**
- Org chart as the primary navigation surface: click on any person or role to see analytics
- Headcount planning mode: model changes to the org by manipulating the org chart directly
- Report builder: drag-and-drop report configuration for custom metrics

**Integration points**
- HRIS connectors: Workday, SAP SuccessFactors, ADP, BambooHR, Rippling, Gusto, and 70+ HRIS systems
- Compensation benchmarking: Radford, Mercer, Levels.fyi integrations
- HRIS write-back: update HRIS records directly from ChartHop without switching systems

**Known gaps**
- Predictive ML depth is lighter than Visier: attrition prediction is less sophisticated; flight risk scoring is not as continuously updated
- No native benchmarking network against peer organisations
- Enterprise scalability: better suited to 200–5,000 employee organisations than large enterprise

**Licence / IP notes**
- Proprietary SaaS; raised $35M Series B (2021)
- No OSS components

---

### One Model

**Core features**
- People analytics data warehouse: ingests HR data from multiple HRIS, ATS, LMS, and financial systems into a governed analytical warehouse
- Pre-built predictive models: turnover prediction, flight risk scoring, performance prediction, and diversity forecasting using ML
- Non-HR data blending: combines employee data with business outcome data (revenue, customer satisfaction, productivity) for workforce ROI analysis
- Custom model development: data science team can build custom predictive models using the One Model data layer
- Governed metrics layer: centralised metric definitions ensuring consistent calculation of headcount, attrition, and diversity metrics across all reports

**Differentiating features**
- Open data architecture: data scientists can access the underlying data layer in SQL, Python, and R — not limited to pre-built dashboards
- Non-HR signal integration: connects workforce data to business outcome signals — a capability Visier and ChartHop do not offer natively
- Best for organisations with internal data science capability who want a governed HR data foundation rather than a packaged analytics product

**UX patterns**
- Dual-audience design: pre-built dashboards for HR generalists; SQL/Python data access for data scientists
- Configurable semantic layer: centralised metric definitions customised to the organisation's HR terminology and business logic

**Integration points**
- Broad data ingestion: Workday, SAP SF, ADP, Oracle HCM, Greenhouse (ATS), Cornerstone (LMS), and financial systems
- Python and R SDK for custom model development on the One Model data layer
- Looker, Tableau, and Power BI connectors for custom dashboard delivery

**Known gaps**
- Requires data engineering investment: not self-service for HR generalists; needs data science or engineering resources
- Higher implementation complexity than ChartHop or Visier SMB
- Smaller company: fewer pre-built connectors and less partner ecosystem than Visier

**Licence / IP notes**
- Proprietary SaaS; raised $25M Series B (2022)
- No OSS components

---

### OrangeHRM (Open Source Analytics)

**Core features**
- Basic HR reporting: standard reports on headcount, leave usage, performance ratings, and recruitment pipeline from OrangeHRM's core HR modules
- Community-built analytics modules: open-source community has contributed visualisation modules; quality and maintenance are variable
- People data store: employee records, leave records, performance reviews, and time tracking data stored in an open MySQL database schema
- Custom report builder: configurable report designer for non-standard queries
- Mobile app: employee-facing mobile access to personal HR data

**Differentiating features**
- Only significant OSS HR platform with an analytics capability; others are proprietary
- Open database schema: any analytics tool (Metabase, Superset, Grafana) can connect directly to the OrangeHRM database for custom analytics
- Self-hosted: full data sovereignty with no vendor data access
- No per-user cost: unlimited employees on the self-hosted community edition

**UX patterns**
- Web-based HR admin interface; analytics via the report builder
- Employees access personal data via self-service portal or mobile app

**Integration points**
- Direct database access (MySQL) for connecting external BI tools
- REST API for integration with other HR systems
- Import/export via CSV for bulk data operations

**Known gaps**
- No predictive ML: no attrition prediction, flight risk scoring, or any ML-based analytics
- No DEI analytics module: diversity and pay equity analysis must be built externally
- No benchmarking: no peer comparison data available
- Community analytics modules have inconsistent quality and maintenance; not enterprise-grade
- Significant data engineering required to build meaningful analytics beyond basic reporting

**Licence / IP notes**
- Core: GPL-2.0 — copyleft; any modifications to OrangeHRM code that are distributed must be released under GPL-2.0
- OrangeHRM commercial (cloud and enterprise): proprietary; includes additional modules not in the GPL version
- GPL copyleft is a material consideration: building a new people analytics product on top of OrangeHRM would require GPL compliance for any HRIS-layer modifications; a better approach is to use OrangeHRM as a data source (via API/database) rather than modifying its core code

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Core HR metric library: headcount, attrition rate, time-to-hire, cost-per-hire, absenteeism, and span-of-control calculated consistently
- HRIS data integration: connect to at least one major HRIS system (Workday, BambooHR, ADP) for automated data ingestion
- Attrition and turnover reporting: voluntary vs. involuntary, by department, tenure band, and demographic group
- DEI dashboard: representation tracking by gender, ethnicity, and age across hiring, promotion, and attrition
- Role-based dashboards: CHRO board-level view and HR Business Partner unit-level view
- Data export: CSV and API access to analytical outputs for integration with financial planning tools

### Differentiating Features
- Attrition and flight risk prediction with prescription (not just prediction) — Visier, One Model
- Natural language query interface for HR leaders — Visier Workforce Intelligence
- Peer benchmarking against anonymised comparable organisations — Visier (proprietary network)
- Non-HR signal blending: connecting workforce data to business outcomes (revenue, productivity) — One Model
- Real-time org chart combined with analytics — ChartHop
- Open data architecture with Python/R data science access — One Model
- ISO 30414 automated metric calculation and reporting

### Underserved Areas / Opportunities
- **Open-source predictive analytics**: OrangeHRM provides basic reporting; no OSS platform provides attrition prediction, flight risk scoring, or any ML-based people analytics — a significant white space
- **Natural language HR data querying for mid-market**: Visier's Workforce Intelligence (NL querying) is available only at enterprise price points; the 200–2,000 employee segment has no accessible NL interface to HR data
- **ISO 30414 automated reporting**: generating the ISO 30414 human capital report is manual at most organisations; automated metric calculation and report generation is a clear OSS opportunity
- **ESG disclosure support**: GRI 401/405 workforce disclosures are increasingly required; no tool automates structured ESG workforce disclosure generation
- **Cross-system signal correlation**: connecting engagement, performance, and attrition data to identify non-obvious drivers is still primarily a data science consulting engagement at most organisations

### AI-Augmentation Candidates
- Continuous flight-risk scoring: auto-build and continuously update attrition prediction models from the organisation's own patterns without requiring a data science team
- Natural language HR querying: "Why did attrition spike in the Sales team last quarter?" — returns a narrative explanation with root-cause attribution
- Automated ISO 30414 / ESG narrative reporting: draft the human capital disclosure document directly from the analytics data
- Cross-signal correlation discovery: identify non-obvious correlations (span-of-control, manager tenure, team size) with attrition or performance outcomes without requiring pre-stated hypotheses
- Pay equity anomaly detection: continuously flag statistically significant pay gaps after controlling for legitimate factors

---

## Legal & IP Summary

- OrangeHRM is GPL-2.0 licensed; building a people analytics product as a fork of OrangeHRM requires GPL compliance for any code modifications that are distributed. The recommended approach is to use OrangeHRM as a data source via its API rather than modifying its core code — this avoids GPL copyleft obligations.
- A new OSS people analytics platform should use a permissive licence (MIT or Apache 2.0) to allow organisations to self-host without releasing their HRIS data configurations or custom analytics models.
- GDPR Article 22 restricts solely automated employment decisions derived from people analytics profiling; any flight-risk or performance prediction that informs employment action must include documented human review steps.
- IEEE P7003 (Algorithmic Bias standard) is relevant for attrition and performance prediction models; OSS tools should include bias audit tooling to detect demographic disparities in model outputs.
- ISO 30414:2018 metrics are published by ISO; implementing the metric calculations is freely permissible. ISO 30414:2025 updates add 69 standardised metrics; implementation is legally unrestricted.
- GRI 401 and GRI 405 disclosure frameworks are open standards published by GRI; freely implementable.
- Visier's benchmarking methodology and People Data Platform semantic layer are proprietary; OSS implementations should build independent semantic layer and metric calculation approaches. The specific benchmark dataset is proprietary and cannot be replicated without comparable scale.
- No known patent claims on core HR analytics metrics, dashboard features, or attrition prediction approaches; these are established data science and HR measurement patterns.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Core HR metric library: 30+ pre-built metrics covering headcount, attrition, absenteeism, time-to-hire, cost-per-hire, span-of-control, and pay equity — calculated consistently with documented formulas
- HRIS data connectors: certified integrations with Workday, BambooHR, ADP, and OrangeHRM (via API); generic REST API connector for other systems
- Attrition and turnover dashboards: voluntary vs. involuntary split; breakdown by department, manager, tenure band, location, and demographic group
- DEI representation dashboard: diversity tracking by gender, ethnicity, and age across hiring, promotion, compensation, and attrition funnel
- Role-based dashboards: CHRO board view and HRBP unit view with configurable KPI tiles
- Self-hosted deployment: full data sovereignty; all analytics computation runs within the organisation's own infrastructure

**Should-have (v1.1)**
- Attrition prediction: ML model auto-trained on the organisation's own historical data; flight risk scores with explainability (which signals drove the score)
- Natural language HR querying: plain-language question interface returning narrative explanations with data citations
- ISO 30414:2025 automated metric calculation and report generation for human capital disclosure
- Pay equity analysis: statistical significance testing for compensation gaps after controlling for role, level, and tenure
- Custom metric builder: configurable metric definitions using a formula editor for organisation-specific KPIs

**Nice-to-have (backlog)**
- ESG workforce disclosure generation: automated GRI 401/405 narrative with supporting data for sustainability reports
- Cross-signal correlation discovery: AI-identified non-obvious drivers of attrition, performance, or engagement without pre-stated hypotheses
- Non-HR signal blending: connect workforce data to business outcomes (revenue per employee, customer satisfaction, defect rates) via configurable data ingestion
- Peer benchmarking: anonymised industry benchmark data (initially via integration with public compensation and HR surveys; proprietary network as user base grows)
- Python and R data science access layer: direct SQL and API access to the analytical warehouse for organisations with internal data science capability
