# People Analytics Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source people analytics platform for turnover prediction, diversity analytics, and span-of-control analysis — without enterprise SaaS pricing.

People Analytics Platform is a self-hosted analytics engine for HR and workforce data. It is built for CHROs, people analytics leads, and HR business partners who need predictive workforce insights, ISO 30414 reporting, and DEI analytics, but who are priced out of incumbent tools or need full data sovereignty over sensitive employee data.

---

## Why People Analytics Platform?

- Visier, OrgVue, and One Model are effectively priced out of sub-1,000-employee organisations, with enterprise contracts ranging from $50K to $500K+ per year.
- Workday People Analytics and SAP SuccessFactors Workforce Analytics are only useful inside their own HCM stacks, with limited cross-system data blending and slow iteration cycles.
- The only significant open-source HR option, OrangeHRM, provides basic reporting only — no predictive ML, no DEI analytics, no benchmarking, and is GPL-2.0 copyleft.
- Natural-language querying of HR data (e.g. Visier Workforce Intelligence) is gated behind enterprise pricing; the 200–2,000 employee segment has no accessible NL interface to HR data.
- ISO 30414 human capital reports and GRI 401/405 ESG workforce disclosures are still drafted manually at most organisations, despite the underlying metrics being well-defined.

---

## Key Features

### Core HR Metrics & Reporting

- Pre-built metric library covering headcount, attrition rate, time-to-hire, cost-per-hire, absenteeism, span-of-control, and pay equity, with documented formulas
- Voluntary vs. involuntary turnover dashboards broken down by department, manager, tenure band, location, and demographic group
- Role-based dashboards with a CHRO board-level view and HR Business Partner unit-level view
- Custom metric builder using a formula editor for organisation-specific KPIs
- CSV and API export of analytical outputs for integration with financial planning tools

### Predictive Workforce Analytics

- Attrition and flight-risk prediction using ML models auto-trained on the organisation's own historical data
- Continuously updated turnover models that do not require an in-house data science team to maintain
- Flight-risk scoring with explainability — surfacing which signals drove each individual score
- Cross-signal correlation discovery to identify non-obvious drivers of attrition (e.g. span-of-control, manager tenure, team size) without pre-stated hypotheses
- Pay equity anomaly detection with statistical significance testing after controlling for role, level, and tenure

### Diversity, Equity & Inclusion

- Representation dashboards tracking gender, ethnicity, and age across the full employee lifecycle — hiring, promotion, compensation, and attrition
- Pay equity analysis with statistical significance testing
- Trend monitoring of representation over time by department, level, and location
- Bias audit tooling for attrition and performance prediction models, aligned with IEEE P7003

### Compliance & Disclosure Reporting

- Automated ISO 30414:2025 human capital metric calculation and report generation
- Automated GRI 401 and GRI 405 workforce and diversity disclosure drafts for ESG reporting
- Documented human-review steps in workflows that influence employment decisions, supporting GDPR Article 22 and CCPA obligations
- Structured disclosure outputs suitable for board reporting and regulator submission

### Natural Language Interface

- Plain-language question interface — HR leaders ask "why did attrition spike in Sales last quarter?" and receive a narrative explanation with root-cause attribution
- Data citations attached to narrative answers so insights are auditable
- Self-service analytics for HR Business Partners without requiring SQL or BI tooling

---

## AI-Native Advantage

Unlike incumbent platforms that require data science teams to build and retune attrition models, the platform auto-builds and continuously updates turnover prediction models from each organisation's own patterns — making predictive analytics accessible to companies without a dedicated data science function. A natural-language query layer lets non-technical HR leaders interrogate workforce data directly, while AI-drafted ISO 30414 and GRI 401/405 narratives turn quarterly disclosure work from a manual exercise into a generated artefact. AI is also used to surface non-obvious cross-signal correlations between span-of-control, manager tenure, engagement, and attrition that would otherwise require a consulting engagement to discover.

---

## Tech Stack & Deployment

- Self-hosted deployment with full data sovereignty: all analytics computation runs within the organisation's own infrastructure
- HRIS connectors for Workday, BambooHR, ADP, and OrangeHRM (via API), plus a generic REST API connector for other systems
- Python and R data science access layer providing direct SQL and API access to the analytical warehouse for organisations with internal data science capability
- Aligned with HR Open Standards canonical schemas for HRIS data ingestion, ISO 30414:2018/2025 for human capital metrics, and GRI 401/405 for ESG disclosure output
- Recommended permissive licensing (MIT or Apache 2.0) so organisations can self-host without releasing HRIS data configurations or custom analytics models

---

## Market Context

The HR Analytics market is estimated at $4.89B in 2025, projected to reach $10.82B by 2031 (CAGR 13.64%, Mordor Intelligence), with the broader people analytics market estimated at $10.1B in 2025 (Research Nester). Incumbent pricing ranges from ~$6–$20 PEPM for SMB tools (ChartHop, intelliHR) to $50K–$500K+/year for enterprise platforms (Visier, OrgVue, One Model), while voluntary turnover is estimated to cost U.S. employers $1 trillion annually — a strong ROI case for accessible predictive attrition tooling. Primary buyers are CHROs and Chief People Officers, people analytics leads and HR data scientists, HR business partners, and finance/workforce planning teams.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. A permissive licence (MIT or Apache 2.0) is recommended so that organisations can self-host without copyleft obligations on their HRIS configurations or custom analytics models. See [discussion](#) for context.
