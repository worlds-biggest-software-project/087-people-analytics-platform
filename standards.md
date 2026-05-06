# Standards & API Reference

> Project: People Analytics Platform · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 30414:2025 — Human Resource Management: Requirements and Recommendations for Human Capital Reporting and Disclosure**
- URL: https://www.iso.org/standard/30414
- The second edition of the world's first global standard for human capital reporting, published August 2025. Defines 69 standardised metrics across 11 core areas (compliance and ethics, costs, diversity, leadership, culture, health and safety, productivity, recruitment and turnover, skills development, succession planning, and workforce availability). Unlike the 2018 edition, the 2025 revision introduces mandatory requirements alongside recommendations and aligns with global sustainability reporting frameworks. Implementing ISO 30414:2025 metric calculations is legally unrestricted; a people analytics platform should automate calculation and structured reporting of all 69 metrics.

**ISO/TS 30407–30438 — Human Capital Measurement Technical Specifications**
- URL: https://www.iso.org/committee/671949.html
- A suite of 17+ technical specifications that support ISO 30414 by providing detailed measurement practices across the 11 core human capital reporting areas. These define calculation methodologies for individual metrics (e.g., turnover rate, time-to-fill, cost-per-hire) and are directly implementable in a people analytics metric library.

**ISO/IEC 42001:2023 — Artificial Intelligence Management System**
- URL: https://www.iso.org/standard/81230.html
- Specifies requirements for establishing, implementing, maintaining, and continually improving an AI management system within organisations. Relevant to the governance of attrition prediction and flight-risk scoring models embedded in a people analytics platform; addresses risk management, transparency, and auditability of AI decisions.

### W3C & IETF Standards

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- The foundational standard for delegated authorisation. All major HRIS systems (Workday, SAP SuccessFactors, BambooHR, ADP) use OAuth 2.0 as their primary API authentication mechanism. A people analytics platform must implement OAuth 2.0 to connect to source HRIS systems and to expose its own API to downstream consumers.

**RFC 9700 — Best Current Practice for OAuth 2.0 Security (January 2025)**
- URL: https://datatracker.ietf.org/doc/rfc9700/
- Published January 2025, this BCP updates the OAuth 2.0 threat model and security guidance to incorporate practical experience from widespread deployment. Supersedes RFC 6819 and RFC 8252 in key areas. Any new people analytics platform should implement RFC 9700 guidance (PKCE for all clients, exact redirect URI matching, sender-constrained tokens) rather than the older OAuth 2.0 baseline.

**RFC 7519 — JSON Web Tokens (JWT)**
- URL: https://datatracker.ietf.org/doc/html/rfc7519
- Defines the compact, URL-safe means of representing claims for use in OAuth 2.0 bearer tokens and OpenID Connect ID tokens. HRIS APIs routinely issue signed JWTs; a people analytics platform must validate JWTs when receiving calls from connected systems and may issue its own JWTs for its API consumers.

**RFC 7396 — JSON Merge Patch**
- URL: https://datatracker.ietf.org/doc/html/rfc7396
- Defines a partial update format for JSON documents, commonly used by HRIS REST APIs for partial employee record updates. Relevant for HRIS write-back features (e.g., updating a field in Workday or BambooHR without replacing the full record).

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- An identity layer on top of OAuth 2.0 enabling single sign-on. Workday, SAP SuccessFactors, and major HRIS systems support OIDC for user authentication; a people analytics platform should support OIDC for SSO so enterprise customers can authenticate with their existing identity provider (Okta, Azure AD, Google).

### Data Model & API Specifications

**HR Open Standards — JSON/XML HR Data Schemas (v4.5, 2026)**
- URL: https://www.hropenstandards.org/standards
- Downloads: https://www.hropenstandards.org/standards-downloads
- The only independent non-profit standard suite for HR data exchange, maintained by the HR Open Standards Consortium since 1999. Defines canonical JSON and XML schemas for employee records, job postings, candidate data, and compensation. The February 2026 release (v4.5) introduces the Trusted Career Profile (TCP) and an Open API for HRIS vendors. A people analytics platform should align its internal employee data model with HR Open Standards schemas to maximise interoperability with HRIS source systems and downstream consumers.

**OpenAPI Specification 3.1**
- URL: https://spec.openapis.org/oas/v3.1.0
- The de facto standard for documenting REST APIs. All major HRIS APIs (Workday REST, SAP SuccessFactors OData alongside OpenAPI, BambooHR) publish or generate OpenAPI 3.1 specifications. A people analytics platform should expose its own API under an OpenAPI 3.1 spec to enable client SDK generation, Postman collections, and automated testing.

**OData 4.0 / OData 4.01**
- URL: https://www.odata.org/documentation/
- An OASIS standard protocol for building and consuming RESTful APIs with rich query capabilities. SAP SuccessFactors exposes its primary API surface as OData V2 and OData V4; any integration with SAP SF must implement OData query conventions ($filter, $expand, $select, $orderby). A people analytics platform connecting to SAP SF must handle OData semantics in its SAP connector.

**JSON Schema Draft 2020-12**
- URL: https://json-schema.org/specification
- Defines the structure and validation rules for JSON data. Used for validating incoming HRIS data payloads, documenting data intake API schemas, and ensuring that transformed analytics datasets conform to expected shapes before persisting to the analytics warehouse.

### Security & Authentication Standards

**OWASP API Security Top 10 (2023 edition, current as of 2026)**
- URL: https://owasp.org/API-Security/editions/2023/en/0x00-header/
- Documents the top 10 API security risks including broken object-level authorisation (BOLA), authentication failures, and unrestricted resource consumption. Directly applicable to a people analytics platform's public API, which handles sensitive employee PII; platform design should address all OWASP API Security Top 10 risks.

**NIST Privacy Framework 1.1 (final expected Q4 2025)**
- URL: https://www.nist.gov/privacy-framework
- Provides a risk-based approach for managing privacy risk. The April 2025 draft update specifically addresses AI tools and their relationship to privacy risks, including data reconstruction, prompt injection, and membership inference — all relevant to ML-based attrition prediction models that train on employee data. A people analytics platform should align its data governance model with NIST PF 1.1 Govern and Protect functions.

**NIST AI Risk Management Framework 1.0 (AI RMF)**
- URL: https://www.nist.gov/system/files/documents/2023/01/26/AI%20RMF%201.0.pdf
- Defines seven characteristics of trustworthy AI: validity, safety, security, accountability, explainability, privacy enhancement, and fairness. The fairness characteristic directly addresses harmful bias in ML models — a critical requirement for attrition prediction and flight-risk scoring in a people analytics platform, where biased models can trigger discriminatory employment actions.

**IEEE 7003-2024 — Standard for Algorithmic Bias Considerations (published January 2025)**
- URL: https://standards.ieee.org/ieee/7003/11357/
- Establishes processes to define, measure, and mitigate algorithmic bias throughout the AI system lifecycle. Provides criteria for validation datasets, application boundary documentation, and user expectation management. A people analytics platform should implement IEEE 7003-2024 bias audit processes for its attrition and performance prediction models to detect demographic disparities in model outputs.

**TLS 1.3 (RFC 8446)**
- URL: https://datatracker.ietf.org/doc/html/rfc8446
- The current transport security standard. All HRIS API connections and all people analytics platform API endpoints must use TLS 1.3 (minimum TLS 1.2 for legacy compatibility). Employee data transmission in plain text is a critical security failure and GDPR violation.

### Regulatory Frameworks

**EU General Data Protection Regulation (GDPR) — Article 22**
- URL: https://gdpr-info.eu/art-22-gdpr/
- Provides data subjects the right not to be subject to solely automated decisions that produce legal or similarly significant effects. The 2023 SCHUFA ruling by the European Court of Justice expanded Article 22 scope: AI-generated flight-risk scores or performance rankings that effectively determine employment actions may be treated as automated decisions even if a human nominally approves the output. A people analytics platform must support documented human review workflows for any prediction output that informs employment action.

**EU Artificial Intelligence Act — Annex III, Category 4 (HR High-Risk Systems)**
- URL: https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai
- All AI used in recruitment, promotion, performance evaluation, and worker monitoring is classified as high-risk. Full enforcement of high-risk obligations is scheduled for August 2, 2026 (with a proposed deferral to December 2, 2027 under the November 2025 Digital Omnibus proposal, not yet adopted as of May 2026). High-risk obligations include: worker notification, human oversight with ability to override, monitoring for discrimination, logging, and data protection compliance. A people analytics platform that deploys predictive ML must provide conformity documentation under the EU AI Act.

**UK Data (Use and Access) Act 2025 (DUAA)**
- URL: https://www.legislation.gov.uk/ukpga/2025
- The UK's first major post-Brexit reform of automated decision-making rules, enacted in 2025 and expected to take effect in 2026. Updates and partially diverges from EU GDPR Article 22 rules. A people analytics platform serving UK organisations must track DUAA implementation regulations as they are published.

**SEC Regulation S-K Item 101(c) — Human Capital Disclosures**
- URL: https://www.sec.gov/rules/final/2020/33-10825.pdf
- Requires US public company registrants to describe human capital resources and any human capital measures or objectives material to managing the business in their annual Form 10-K. Effective since November 2020; fiscal year 2025 Form 10-K is the sixth year of mandatory disclosure. Inline XBRL tagging of human capital narrative disclosures is required. A people analytics platform should be capable of exporting ISO 30414-aligned metric data in formats suitable for SEC human capital disclosure drafting.

**GRI 401: Employment (2016) and GRI 405: Diversity and Equal Opportunity (2016, under revision)**
- URL: https://www.globalreporting.org/how-to-use-the-gri-standards/gri-standards-english-language/
- GRI 401 requires disclosure of new employee hires, turnover, and benefits by age, gender, and region. GRI 405 requires disclosure of diversity in governance bodies and employees by gender, age, and minority group membership. A global public consultation on a revised GRI 405 (Diversity and Inclusion) standard is underway, with the exposure draft open until September 2025. A people analytics platform should automate GRI 401 and 405 disclosure calculations and support export of structured data for sustainability reports.

**EU Corporate Sustainability Reporting Directive (CSRD) — ESRS S1 (Own Workforce)**
- URL: https://www.efrag.org/standards/esrs
- Requires approximately 50,000 European companies to provide detailed human capital reporting under the European Sustainability Reporting Standards (ESRS S1: Own Workforce). ESRS S1 aligns with ISO 30414 and GRI 401/405 metrics but adds third-party assurance requirements and more granular disclosure obligations (e.g., workforce composition by contract type, country, collective bargaining coverage, and gender pay gap). A people analytics platform targeting European enterprise customers must support ESRS S1 metric calculation and structured disclosure export.

**XBRL (eXtensible Business Reporting Language) — 2026 SEC Taxonomy**
- URL: https://www.sec.gov/newsroom/whats-new/2603-2026-xbrl-taxonomies-update
- XBRL US: https://xbrl.us/xbrl-taxonomy/2025-us-gaap/
- SEC filers must use Inline XBRL (iXBRL) to tag human capital narrative disclosures and quantitative amounts in Form 10-K filings. The 2026 XBRL taxonomy (applicable from March 16, 2026) is the current active taxonomy. A people analytics platform that generates human capital disclosure outputs for US public companies should export metric data in XBRL-compatible formats.

---

## Similar Products — Developer Documentation & APIs

### Visier People

- **Description:** The market-leading cloud-native people analytics SaaS platform, covering attrition prediction, DEI analytics, workforce benchmarking, and natural-language HR querying (Vee AI assistant). Serves 50,000+ organisations.
- **API Documentation:** https://docs.visier.com/developer/apis/apis.htm
- **SDKs/Libraries:** No published SDKs; REST API access via API key + OAuth 2.0 token
- **Developer Guide (Getting Started):** https://docs.visier.com/developer/apis/apis-get-started-home.htm
- **Key API Surfaces:**
  - Data Query API — query people analytics metrics and dimensions: https://docs.visier.com/developer/apis/data-out/data-query/data-query-api.htm
  - Data Model API — discover objects and metrics in the solution: https://docs.visier.com/developer/apis/data-model-query/data-model-query-api.htm
  - Vee API — natural language HR queries returning narrative + data: https://docs.visier.com/developer/apis/data-out/vee/vee-api.htm
  - Direct Data Intake API and Data Upload API — ingesting HR data from source systems
  - Users and Administration API — user and permission management
- **Standards:** REST/JSON; OAuth 2.0 + API key authentication
- **Authentication:** API key + OAuth 2.0 bearer token

### Workday People Analytics

- **Description:** ML-powered people analytics storyteller engine embedded in Workday HCM. Surfaces workforce anomalies automatically; tightly coupled to the Workday data model. Also relevant as a primary HRIS data source for any people analytics platform.
- **API Documentation:** https://developer.workday.com/
- **SDKs/Libraries:** No official SDK; community libraries available via Workday developer portal
- **Developer Guide:** https://samaintegrations.com/mastering-workday-rest-api-integration-the-complete-2025-guide-for-businesses/ (community guide); https://assistnow.com/blog/workday-rest-api-guide (2026 guide)
- **Key API Surfaces:**
  - SOAP Web Services — broadest coverage of Workday data; legacy but comprehensive
  - REST API — modern, growing coverage of HR, payroll, benefits, and time data; requires OAuth 2.0
  - Reports-as-a-Service (RaaS) — custom report extraction via URL-based API; most common for analytics data extraction
  - Workday Prism Analytics — data blending layer accepting external data for analysis within Workday
- **Standards:** SOAP (legacy), REST/JSON (modern), OAuth 2.0 Authorization Code grant
- **Authentication:** OAuth 2.0 with Integration System User (ISU); client ID/secret registered in Workday tenant

### SAP SuccessFactors HCM Suite

- **Description:** SAP's cloud HCM suite including Workforce Analytics module; embedded analytics with standard HR metrics, global benchmarking, and DEI dashboards. A major HRIS data source for enterprise people analytics platforms.
- **API Documentation:** https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM (OData V2); https://help.sap.com/docs/successfactors-platform/sap-successfactors-api-reference-guide-odata-v4 (OData V4)
- **API Explorer:** https://api.sap.com/products/SAPSuccessFactors/apis/ODATA
- **SDKs/Libraries:** SAP Cloud SDK (Java, JavaScript/Node.js): https://sap.github.io/cloud-sdk/
- **Developer Guide:** https://help.sap.com/docs/successfactors-platform (SAP Help Portal)
- **Standards:** OData V2 (primary, broadest entity coverage), OData V4 (newer, expanding coverage); REST/JSON
- **Authentication:** OAuth 2.0 with SAML2 bearer assertion or client credentials; API key for non-OAuth legacy endpoints

### ChartHop

- **Description:** People data platform combining real-time org chart, headcount and scenario planning, DEI tracking, and compensation analytics. Particularly relevant for org design and headcount planning feature patterns.
- **API Documentation:** https://docs.charthop.com/charthop-for-developers
- **Developer Basics:** https://docs.charthop.com/developer-basics
- **SDKs/Libraries:** No official SDK; REST API access; Merge.dev provides a ChartHop connector within its unified HRIS API
- **Developer Guide:** https://docs.charthop.com/ (documentation hub)
- **Key API Capabilities:** Pull/push people data (current org roster via findJobs API call); event notifications (webhooks); syncing data to/from ChartHop for HRIS write-back
- **Standards:** REST/JSON; webhooks for event-driven integration
- **Authentication:** API key; OAuth 2.0 for marketplace app integrations

### BambooHR

- **Description:** A widely-used HRIS for SMB and mid-market organisations (10–2,000 employees). The most common data source for a people analytics platform targeting the underserved mid-market segment.
- **API Documentation:** https://documentation.bamboohr.com/docs
- **Developer Portal:** https://developers.bamboohr.com
- **SDKs/Libraries:** Official PHP SDK and Python SDK, both supporting OAuth 2.0; community SDKs in JavaScript and Ruby
- **Developer Guide:** https://documentation.bamboohr.com/docs/api-details (Technical Overview); https://truto.one/blog/how-to-integrate-with-the-bamboohr-api-2026-engineering-guide/ (2026 engineering guide)
- **Key API Capabilities:** Employee data CRUD; custom fields; time-off and leave records; performance reviews; payroll information; webhooks for real-time change events; cursor-based pagination (GET /api/v1/employees endpoint, added October 2025)
- **Standards:** REST/JSON; webhooks; OAuth 2.0 (required for new marketplace integrations as of April 2025), API key via HTTP Basic Auth (existing integrations)
- **Authentication:** OAuth 2.0 Authorization Code (required for new integrations); API key + HTTP Basic Auth (legacy)

### ADP Workforce Now

- **Description:** ADP's flagship HCM platform for mid-market and enterprise. A key HRIS data source, particularly for organisations in North America where ADP has dominant market share in payroll and HR.
- **API Documentation:** https://developers.adp.com/
- **Marketplace API Catalog:** https://developers.adp.com/articles/guides/adp-workforce-now-api-catalog
- **API Inventory:** https://developers.adp.com/articles/guides/workforce-now-api-inventory
- **Developer Guide:** https://developers.adp.com/ (requires developer agreement with ADP)
- **Key API Capabilities:** Employee demographics, earnings, deductions, payroll results, benefits and insurance administration; HR events; time and labour
- **Standards:** REST/JSON; OAuth 2.0
- **Authentication:** OAuth 2.0; requires formal developer agreement and approval from ADP before sandbox or production access is granted

### OrangeHRM (Open Source)

- **Description:** The primary open-source HRIS with basic analytics reporting. GPL-2.0 licensed core. Relevant both as a data source connector and as a reference for the open-source HR data model.
- **API Documentation:** https://orangehrm.github.io/orangehrm-api-doc/ (community edition REST API)
- **Help Centre:** https://help.orangehrm.com/hc/en-us/categories/900000147946-API-Documentation
- **Starter API:** https://api-starter.orangehrm.com/ (OrangeHRM Starter v5.5+)
- **GitHub:** https://github.com/orangehrm/orangehrm
- **SDKs/Libraries:** No official SDKs; REST API access; direct MySQL database access is also a practical integration path
- **Developer Guide:** https://github.com/orangehrm/orangehrm/wiki/REST-API
- **Standards:** REST/JSON; direct database (MySQL) access also supported
- **Authentication:** OAuth 2.0 (Starter edition); basic auth (community edition)

### Merge.dev — Unified HRIS API

- **Description:** A unified API platform that normalises 50+ HRIS, ATS, payroll, and directory integrations into a single API surface. Building against Merge significantly reduces the HRIS connector maintenance burden for a people analytics platform — instead of building and maintaining individual connectors for Workday, SAP SF, BambooHR, ADP, and 40+ others, a single Merge integration provides access to all.
- **API Documentation:** https://docs.merge.dev/hris/
- **Developer Portal:** https://merge.dev/
- **SDKs/Libraries:** Python, Node.js, Ruby, Go, Java SDKs available
- **Key API Capabilities:** Normalised employee records, employment types, locations, departments, groups, pay groups, time-off, documents, and benefits across all connected HRIS systems; field mapping; webhook events for change detection
- **Standards:** REST/JSON; OpenAPI 3.0 specification published; webhooks
- **Authentication:** API key for Merge API; Merge handles OAuth 2.0 flows with underlying HRIS systems on behalf of the integrating application

### People Data Labs

- **Description:** External workforce intelligence data provider offering enrichment of employee records with market data — job titles, skills, seniority, career history, and compensation benchmarks. Relevant for a people analytics platform's skills inference and benchmarking features.
- **API Documentation:** https://docs.peopledatalabs.com/
- **OpenAPI Specification:** https://github.com/peopledatalabs/openAPI-specifications
- **SDKs/Libraries:** JavaScript, Python, Go, Java, Ruby SDKs available
- **Standards:** REST/JSON; OpenAPI 3.1 specification published
- **Authentication:** API key

---

## Notes

**Emerging Standards Under Development**

- **GRI Diversity and Inclusion Exposure Draft**: GRI's global public consultation on a revised GRI 405 standard closed September 2025. The revised standard is expected to be published in 2026 and will replace GRI 405:2016. Platform implementations should track the final publication as it will update mandatory DEI disclosure requirements.

- **EU AI Act High-Risk Obligations Deferral**: The European Commission's Digital Omnibus (November 2025) proposes to defer high-risk AI compliance from August 2, 2026 to December 2, 2027. As of May 2026, the Digital Omnibus has not been formally adopted; the original August 2026 deadline remains legally operative.

- **HR Open Standards v4.5 Open API for HRIS Vendors**: The February 2026 release of HR Open Standards introduces a new Open API specification for HRIS vendors and wallet holders alongside the Trusted Career Profile (TCP). This is an emerging standard worth monitoring for alignment as it could become a canonical interoperability layer for employee credential and career data exchange.

**Data Sovereignty and Self-Hosting Considerations**

- A self-hosted people analytics platform that does not transmit employee data to third-party cloud services avoids most GDPR data transfer obligations (Chapter V) that affect SaaS analytics tools. This is a significant architectural advantage for an open-source, self-hosted alternative. However, if the platform integrates with cloud-based unified APIs (e.g., Merge.dev), data residency and sub-processor obligations must be assessed.

- CSRD requires third-party assurance for human capital disclosures from in-scope European companies. A people analytics platform should maintain audit logs and data lineage documentation to support assurance processes.
