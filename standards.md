# Standards & API Reference

> Project: Compensation Management · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 30400:2016 — Human Resource Management: Vocabulary**
- URL: https://www.iso.org/standard/64064.html
- Defines the foundational vocabulary for all ISO human resource management standards. Relevant as the definitional baseline for compensation-related concepts such as remuneration, benefits, and total rewards in any standards-compliant HR data model.

**ISO 30405:2016 — Human Resource Management: Guidelines on Recruitment**
- URL: https://www.iso.org/standard/64066.html
- Covers the HR lifecycle including offer management and onboarding workflows. Relevant to the offer management and candidate compensation benchmarking features of a compensation management platform.

**ISO/TR 30406:2017 — Sustainable Employability Management for Organisations**
- URL: https://www.iso.org/standard/65828.html
- Provides guidance on fair compensation practices as part of sustainable workforce management. Referenced in research as a framework for equitable pay strategy and compensation governance.

**ISO 30415:2021 — Human Resource Management: Diversity and Inclusion**
- URL: https://www.iso.org/standard/71164.html
- Establishes principles for integrating diversity and inclusion across the HR lifecycle, including pay equity. Directly relevant to pay equity analytics features (statistical gap identification by gender, ethnicity, and other protected characteristics) and compliant with the data categories required by the EU Pay Transparency Directive.

**ISO/IEC 27001:2022 — Information Security Management Systems**
- URL: https://www.iso.org/standard/27001
- The globally recognised certification for information security management. Highly relevant given that compensation and pay equity data is sensitive personal data under GDPR; major SaaS vendors in this category (Paycom, Leapsome) hold ISO 27001 certification. Any open-source platform should be designed to support ISO 27001 compliance in its data handling architecture.

**ISO/IEC 29101:2018 — Privacy Architecture Framework**
- URL: https://www.iso.org/standard/45124.html
- Provides a privacy architecture framework aligned with ISO 27001 and GDPR principles. Relevant for designing the data access control, audit logging, and data minimisation features required by EU Pay Transparency audit obligations.

---

### W3C & IETF Standards

**RFC 9110 — HTTP Semantics (2022)**
- URL: https://www.rfc-editor.org/rfc/rfc9110
- The foundational HTTP standard underpinning all REST API interactions. Any compensation management platform exposing a REST API must comply with HTTP semantics for status codes, headers, content negotiation, and request methods.

**RFC 6749 — The OAuth 2.0 Authorization Framework**
- URL: https://www.rfc-editor.org/rfc/rfc6749
- The standard authorization framework used by all major HRIS platforms (Workday, BambooHR, ADP, Rippling) for secure API access. A compensation management platform must implement OAuth 2.0 to integrate with existing HRIS infrastructure and to expose its own API securely.

**RFC 7519 — JSON Web Token (JWT)**
- URL: https://www.rfc-editor.org/rfc/rfc7519
- JWT is the standard token format used with OAuth 2.0 and OpenID Connect for carrying identity claims between services. Relevant for session management and API authorization in the compensation platform's API layer.

**OpenID Connect Core 1.0 (OIDC)**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- The identity layer on top of OAuth 2.0; the standard for SSO and identity federation used across enterprise HRIS integrations. BambooHR requires OAuth 2.0 / OIDC for all new marketplace integrations as of April 2025.

**RFC 8288 — Web Linking**
- URL: https://www.rfc-editor.org/rfc/rfc8288
- Standard for hypermedia linking in REST APIs. Relevant for pagination and resource linking in compensation data API responses.

---

### Data Model & API Specifications

**HR Open Standards (HR-JSON) — Compensation Module v4.2**
- URL: https://www.hropenstandards.org/standards
- Downloads: https://www.hropenstandards.org/standards-downloads
- GitHub: https://github.com/HROpen
- The only independent, non-profit, vendor-neutral specification suite for HR data exchange. The 4.2 release (February 2026) includes JSON Schema, XML Schema, samples, and documentation for Compensation, Benefits, Assessments, Interviewing, Recruiting, and Payroll. The Compensation module defines a canonical data model for salary, bonus, incentive pay, and benefits data exchange between HR systems. The Payroll module's `PayrollMasterData` specification covers pay rates, deductions, garnishments, and tax structures. Freely downloadable and implementable; the most relevant formal data standard for this project's API and data model design.

**OpenAPI Specification v3.2.0**
- URL: https://spec.openapis.org/oas/v3.2.0.html
- GitHub: https://github.com/OAI/OpenAPI-Specification
- The standard format for describing REST APIs in a machine-readable, language-agnostic format. Version 3.2.0 (September 2025) adds structured tag nesting, streaming media type support, native QUERY method, and OAuth 2.0 Device Authorization Flow. The compensation management platform's API should be documented and published using OpenAPI 3.2.0 to enable automated SDK generation, interactive documentation, and integration partner onboarding.

**O*NET Standard Occupational Classification (SOC) System**
- Web Services URL: https://services.onetcenter.org/
- API Reference (v2.0): https://services.onetcenter.org/reference/
- Maintained by the U.S. Department of Labor, O*NET provides a comprehensive taxonomy of occupations, skills, tasks, and competencies used as the foundation for job family classification in compensation benchmarking. The v2.0 REST API (launched November 2025) provides read access to the full O*NET database with endpoints for occupation search, detailed job profiles, and skills data. Access is free for registered developers. Directly usable for job-to-benchmark matching and compensation band assignment.

**ESCO Classification — European Skills, Competences, Qualifications and Occupations**
- API URL: https://esco.ec.europa.eu/en/use-esco/use-esco-services-api
- Web Service API: https://esco.ec.europa.eu/en/use-esco/use-esco-services-api/esco-web-service-api
- The EU equivalent of O*NET: a multilingual classification of occupations, skills, and qualifications maintained by the European Commission. ESCO v1.2.0 was released in May 2024. The REST API is available for free use under the EUPL 1.2 licence and provides programmatic access to all ESCO occupation and skill classifications in multiple EU languages. Directly relevant for EU-market compensation band assignment and EU Pay Transparency Directive job evaluation compliance.

**JSON Schema (Draft 2020-12)**
- URL: https://json-schema.org/draft/2020-12
- The standard for describing the structure, validation, and documentation of JSON data. Relevant for defining the canonical data model for compensation objects (salary bands, pay ranges, offers, equity grants) that will be exchanged via the platform's API and stored internally.

---

### Regulatory & Compliance Frameworks

**EU Pay Transparency Directive — Directive (EU) 2023/970**
- Official text: https://eur-lex.europa.eu/eli/dir/2023/970/oj/eng
- EU Council overview: https://www.consilium.europa.eu/en/policies/pay-transparency/
- The most significant regulatory driver of software purchases in this category. Member states had until 7 June 2026 to implement the Directive into national law. Key technical requirements for software:
  - Calculation and reporting of the gender pay gap (unadjusted and adjusted), broken down by worker category, age, employment type, and economic sector
  - Publication of pay ranges for all job postings accessible to job applicants before interview
  - On-request provision of information about individual pay and the average pay for workers performing the same or equivalent work, broken down by gender
  - Joint pay assessment and action plan when an unexplained gender pay gap of 5% or more is detected in any worker category
  - Audit trail documentation for pay-setting criteria
  - Employers with 250+ employees must publish their first reports by June 2027; employers with 100–249 employees report every three years

**EU AI Act — Regulation (EU) 2024/1689**
- URL: https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai
- Annex III (high-risk systems): https://artificialintelligenceact.eu/annex/3/
- Fully applicable from 2 August 2026. AI systems used in HR for screening, selection, performance evaluation, or other employment-related decisions are classified as high-risk under Annex III. AI-generated pay recommendations in a compensation management platform fall within this classification. High-risk AI obligations include: human oversight mechanisms, transparency and explainability of AI decisions, risk management documentation, technical robustness, and accuracy standards. Employers must inform and consult employee representative bodies before deploying high-risk AI systems.

**GDPR — General Data Protection Regulation (EU) 2016/679**
- URL: https://gdpr-info.eu/
- Compensation data combined with demographic data (gender, ethnicity) for pay equity analysis is sensitive personal data requiring a lawful basis, explicit consent or legitimate interest documentation, data minimisation, purpose limitation, and robust access controls. GDPR requires audit logs of who accessed pay equity data and when, data retention policies, and the ability to fulfil data subject access and deletion requests. Privacy-by-design architecture is required.

**U.S. State Pay Transparency Laws**
- Colorado Equal Pay for Equal Work Act (2021): https://cdle.colorado.gov/equal-pay-for-equal-work
- California SB 1162 (2023): https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202120220SB1162
- New York Pay Transparency Law (2023): https://dol.ny.gov/pay-transparency
- Collectively require salary range disclosure in job postings and, in some states, pay data reporting to state agencies. Software must generate compliant salary range text and integrate with ATS job posting workflows.

**FLSA — Fair Labor Standards Act (U.S.)**
- URL: https://www.dol.gov/agencies/whd/flsa
- Federal framework governing exempt/non-exempt employee classification, minimum wage, and overtime. Compensation management software must correctly handle FLSA classification when managing hourly vs. salaried compensation structures and ensure overtime calculations comply with current DOL thresholds.

**IFRS 2 — Share-Based Payment**
- URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-2-share-based-payment/
- International accounting standard for recognising the cost of equity compensation (stock options, RSUs) in financial statements. Relevant for any equity grant benchmarking and total compensation modelling features; the platform should produce outputs compatible with IFRS 2 expense recognition requirements.

**ASC 718 — Compensation—Stock Compensation (U.S. GAAP)**
- URL: https://asc.fasb.org/718
- U.S. equivalent of IFRS 2. Governs how stock-based compensation is valued and expensed for U.S. companies. Relevant for equity grant modelling and total compensation features serving U.S.-based companies.

**IRS Section 409A — Nonqualified Deferred Compensation**
- URL: https://www.irs.gov/retirement-plans/409a-nonqualified-deferred-compensation
- U.S. tax regulation governing equity compensation valuation for private companies. Drives demand for 409A valuation integration in compensation management platforms, particularly for startup equity benchmarking features.

---

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749) + PKCE (RFC 7636)**
- OAuth 2.0 URL: https://www.rfc-editor.org/rfc/rfc6749
- PKCE URL: https://www.rfc-editor.org/rfc/rfc7636
- The mandatory authentication standard for HRIS API integrations. BambooHR requires OAuth 2.0 for all new marketplace integrations (as of April 2025); ADP and Workday use OAuth 2.0 for their REST APIs. PKCE (Proof Key for Code Exchange) is required for public clients to prevent authorization code interception attacks.

**OWASP API Security Top 10 (2023)**
- URL: https://owasp.org/API-Security/editions/2023/en/0x00-header/
- The authoritative checklist for API security vulnerabilities. Directly applicable to the compensation platform's API design, particularly given that compensation and pay equity data is sensitive personal data. Key risks: Broken Object Level Authorization (ensuring users can only access their own employees' data), Broken Function Level Authorization (preventing managers from accessing other managers' pay bands), and Excessive Data Exposure (minimising what pay data is returned by default).

**NIST SP 800-63B — Digital Identity Guidelines**
- URL: https://pages.nist.gov/800-63-3/sp800-63b.html
- U.S. federal guidance on authentication assurance levels. Relevant for enterprise deployments requiring multi-factor authentication and authenticator assurance levels for access to sensitive pay data.

**SOC 2 Type II**
- AICPA URL: https://www.aicpa-cima.com/resources/article/soc-2
- The de facto audit standard for SaaS platforms handling sensitive enterprise data. All major compensation management vendors (Pave, beqom, PayScale) maintain SOC 2 Type II certification. An open-source platform aiming for enterprise adoption should be designed to support SOC 2 audit requirements (security, availability, confidentiality, processing integrity).

---

### MCP Server Specifications

No published MCP server specifications exist specifically for compensation management as of May 2026. The Model Context Protocol (MCP) is relevant for enabling AI agents to query compensation benchmarks, retrieve salary band data, and generate pay recommendations in conversational AI contexts. The platform should expose an MCP server implementation that wraps its REST API, providing tools for: salary band lookup by job family and geography, pay equity gap retrieval by demographic segment, offer recommendation generation, and merit cycle status queries. The MCP specification is available at https://modelcontextprotocol.io/specification.

---

## Similar Products — Developer Documentation & APIs

### Pave
- **Description:** Real-time compensation benchmarking platform drawing from live HRIS integrations across 8,700+ contributing companies; covers 200+ job families across 50+ countries.
- **API Documentation:** https://www.pave.com/products/api
- **SDKs/Libraries:** No public SDK listed; REST/JSON API; common destinations include Workday, AWS, Snowflake, Looker, Tableau, SAP, Oracle via the Analytics API.
- **Developer Guide:** https://www.pave.com/blog-posts/build-a-more-connected-compensation-stack-ways-to-use-the-pave-api
- **Standards:** REST/JSON; OpenAPI not publicly documented.
- **Authentication:** API key-based authentication; OAuth 2.0 for HRIS data contributor connections.
- **Notes:** API enables running compensation data queries, custom reports, and merit cycle integrations. Morgan Stanley at Work announced an API integration with Pave in 2025 for real-time compensation benchmarking embedded in wealth management workflows.

### PayScale (Jobalyzer API)
- **Description:** Compensation benchmarking data combining crowdsourced salary reports and employer-submitted data; SMB and mid-market focus across broad industry and geography coverage.
- **API Documentation:** https://developers.payscale.com/
- **Jobalyzer API Reference:** https://developers.payscale.com/jobalyzer/api.html
- **SDKs/Libraries:** No official SDK listed; HTTP REST with JSON inputs/outputs.
- **Developer Guide:** https://developers.payscale.com/jobalyzer/index.html
- **Standards:** REST/JSON; inputs and outputs are JSON; compensable factors include job title, city, state, country, skills.
- **Authentication:** API key; partner registration required.
- **Key Endpoints:**
  - Pay Report: Base pay, total pay, bonus, commission, and profit-sharing with percentile distributions (10th–90th)
  - Years of Experience Report: Base pay percentiles across career stages
  - Skill Impact: How specific skills shift compensation for a job title
- **HRIS Integrations (2025):** Oracle, SAP SuccessFactors, Gusto, Humi, Paylocity, ADP, BambooHR, UKG, Remote, Namely, Dayforce.

### Workday Compensation API
- **Description:** Compensation management natively integrated into Workday HCM; covers salary bands, merit cycles, equity tracking, and multi-country pay management for enterprise customers.
- **API Documentation:** https://community.workday.com/sites/default/files/file-hosting/restapi/
- **SOAP WSDL Directory (v46.1):** https://community.workday.com/sites/default/files/file-hosting/productionapi/index.html
- **Developer Guide:** https://www.apideck.com/blog/create-a-workday-rest-api-integration
- **Standards:** REST and SOAP (WSDL/XML); REST API currently at v44.2 for SOAP equivalents; JSON and XML supported.
- **Authentication:** OAuth 2.0; requires Integration System Security Group (ISSG) and Integration System User (ISU) setup.
- **Key Objects:** Worker API (employee records, compensation data, job profiles, organisational relationships); Compensation API (pay grades, bands, merit plans).
- **Notes:** Workday's REST API is the primary integration target for any compensation platform aiming to sync with enterprise HRIS deployments, as Workday is the dominant HCM platform in the 1,000+ employee segment.

### Carta Developer Platform (Equity & Cap Table API)
- **Description:** Equity and cap table management platform for private companies; Issuer API provides access to full cap table data, equity grant records, and holdings data for downstream integration.
- **API Documentation:** https://docs.carta.com/api-platform/docs/introduction
- **API Overview:** https://carta.com/api/
- **SDKs/Libraries:** Not publicly listed; REST/JSON.
- **Developer Guide:** https://docs.carta.com/carta/docs/introduction
- **Standards:** REST/JSON; OpenAPI 3.x likely (based on interactive documentation structure).
- **Authentication:** OAuth 2.0.
- **Key APIs:**
  - Issuer API: Cap table data, equity grants, holdings — for HRIS provider integration and financial services
  - Investor API: Portfolio company data for VC monitoring
  - Launch API: Automated new account creation (used by Stripe Atlas)
- **Notes:** The Issuer API is the key integration point for any compensation platform wanting to incorporate actual equity grant data (option grants, RSU schedules, vesting) into total compensation modelling.

### BambooHR API
- **Description:** HRIS platform for SMBs; REST API provides access to employee records, compensation tables, time-off, benefits, and payroll data for 30,000+ companies.
- **API Documentation:** https://documentation.bamboohr.com/reference
- **Technical Overview:** https://documentation.bamboohr.com/docs/api-details
- **SDKs/Libraries:** Official SDKs listed at https://documentation.bamboohr.com/docs/sdks; R package `bambooHR` available on CRAN.
- **Developer Guide:** https://documentation.bamboohr.com/docs/getting-started
- **Standards:** REST/JSON; API requests to `https://{companyDomain}.bamboohr.com/api/`.
- **Authentication:** API key via HTTP Basic Auth (legacy); OAuth 2.0 required for new marketplace integrations as of April 2025.
- **Key Endpoints:**
  - GET /api/v1/employees: Retrieve employee data with filtering, sorting, pagination (added October 2025)
  - GET /api/v1/employees/{id}: Employee record including current compensation values from historical tables
  - Compensation table: Read/write pay rate, paidPer, effective date
- **Notes:** BambooHR is the most common HRIS integration target for SMB-focused compensation tools; its compensation table API directly maps to the salary band and pay rate data model needed by a compensation management platform.

### ADP Workforce Now API
- **Description:** Enterprise payroll and HR platform; REST APIs cover employee data, payroll inputs, earnings, deductions, tax withholdings, and pay statement retrieval for US-based enterprise and mid-market companies.
- **API Documentation:** https://developers.adp.com/
- **API Catalog:** https://developers.adp.com/articles/guides/adp-workforce-now-api-catalog
- **Developer Guide:** https://developers.adp.com/ (ticketed support + code samples for registered partners)
- **Standards:** REST/JSON; OpenAPI specifications available for registered developer partners.
- **Authentication:** OAuth 2.0 for all REST API access.
- **Key APIs:**
  - Workers v2 API: Employee records, job and compensation data
  - Pay Data Input v1 API: Earnings, deductions, tax withholdings
  - Payroll Results API: Pay statements and payroll processing results
- **Notes:** ADP Workforce Now processes payroll for 1M+ businesses; integration with its Worker and Pay Data APIs is essential for any compensation platform aiming to downstream actual pay changes from merit cycles into payroll processing.

### Rippling API
- **Description:** All-in-one workforce platform combining HR, IT, and finance; REST API provides access to employee data, compensation, payroll, and benefits with effective dating support.
- **API Documentation:** https://developer.rippling.com/documentation/developer-portal/rest-api/api
- **API Reference:** https://developer.rippling.com/docs/rippling-api/a310f900b0f84-api-reference
- **SDKs/Libraries:** OpenAPI specification generated from Data Transfer Objects; SDK generation supported via OpenAPI tooling.
- **Standards:** REST/JSON; OpenAPI specification published at developer.rippling.com; resource endpoints use plural nouns (`/workers`, `/users`).
- **Authentication:** API key or OAuth 2.0 access token, each scoped to a single Rippling company.
- **Key Features:** Compensation changes with effective dating; base compensation field history; payroll data sync.
- **Notes:** Rippling's API design is notable for being generated directly from DTO class definitions with versioning annotations, making it consistently aligned with the platform data model. Growing HRIS market share in the 50–500 employee segment makes it a priority integration target.

### Merge HRIS Unified API
- **Description:** Unified API layer normalising 50+ HRIS integrations (Workday, BambooHR, ADP, Rippling, UKG, HiBob, and more) into a single standardised API; enables a compensation platform to integrate with multiple HRIS systems through one integration.
- **API Documentation:** https://docs.merge.dev/hris/
- **Unified API Overview:** https://docs.merge.dev/merge-unified/use-cases
- **SDKs/Libraries:** Java SDK: https://github.com/merge-api/merge-hris-java; SDKs available for Python, Node.js, Go, Java, and Ruby.
- **Developer Guide:** https://docs.merge.dev/get-started/unified-api/
- **Standards:** REST/JSON; OpenAPI 3.0.
- **Authentication:** API key (X-Account-Token + Authorization header for each linked account).
- **Key Objects:** Employee, Employment, Location, Company, PayGroup, TimeOff, Benefit — including compensation fields: pay rate, pay period, pay frequency, pay currency, effective date.
- **Notes:** Using Merge (or a similar unified API such as Finch, Unified.to, or Truto) dramatically reduces the engineering cost of achieving broad HRIS compatibility. A compensation platform integrating via Merge gains access to employee compensation data from 50+ HRIS systems without building each integration individually.

### Lattice API
- **Description:** People management platform combining performance, engagement, and compensation; REST API provides access to employee data, compensation bands, merit cycles, and performance ratings for Lattice-managed workforces.
- **API Documentation:** https://lattice.com/api
- **Help Center (Public API):** https://help.lattice.com/hc/en-us/articles/360059449534-Lattice-s-Public-API
- **Standards:** REST/JSON.
- **Authentication:** API key generated from Admin > Platform > API keys.
- **Key Features (August 2025):** Pull weighted performance scores into HRIS (Workday, UKG) to drive pay and promotion decisions; compensation planning integration.
- **Notes:** Lattice's API is relevant as an integration source for performance-rating data that compensation platforms can ingest to provide performance-contextualised pay recommendations.

---

## Notes

**Unified HRIS Integration Middleware**
Several third-party unified API providers (Merge, Finch, Unified.to, Truto, Bindbee) offer normalised access to 50–200+ HRIS platforms via a single REST integration. For an open-source compensation management platform with limited engineering resources, adopting a unified API middleware for HRIS connectivity is strongly recommended over building individual integrations. This is the standard integration strategy for new entrants in the HR software market as of 2026.

**No Open HR Compensation Data Standard Exists**
While HR Open Standards provides a JSON schema for compensation data exchange, there is no open, widely-adopted REST API standard specifically for compensation benchmarking data. The market relies entirely on proprietary vendor APIs (Pave, Radford/Aon, Mercer). An open-source compensation platform that publishes an OpenAPI specification for its benchmarking data model could seed a de-facto open standard, particularly valuable given EU Pay Transparency audit requirements for explainable, auditable pay-setting methodology.

**EU Pay Transparency Reporting Format Not Yet Standardised**
As of May 2026, the EU Commission (Eurostat) has not published a technical specification for the data format in which employers must submit gender pay gap reports. The Directive specifies the required data fields (unadjusted pay gap, pay gap by worker category, by age, by employment type) but leaves the submission format to member state implementations. This represents an early-mover opportunity for an open-source platform to publish a reference reporting schema and methodology that could influence how member states implement their technical reporting systems.

**O*NET v2.0 API — Occupational Taxonomy for Job Matching**
The November 2025 O*NET API v2.0 release adds features particularly valuable for compensation platforms: technology skills search (enabling AI skills premium detection), registered apprenticeship reports, and improved occupation data with fewer nesting levels and more consistent property names. Integration with O*NET v2.0 provides a free, authoritative source of occupation classification that can underpin salary band assignment without dependence on proprietary job family taxonomies.
