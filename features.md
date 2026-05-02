# Compensation Management — Feature & Functionality Survey

> Candidate #81 · Researched: 2026-05-02

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Pave | Commercial SaaS | Proprietary; freemium (1–200 ee) + paid | https://www.pave.com |
| beqom | Commercial SaaS | Proprietary; from ~$55,000/yr | https://www.beqom.com |
| PayScale | Commercial SaaS | Proprietary; ~$27,000/yr avg | https://www.payscale.com |
| Carta Total Comp | Commercial SaaS | Proprietary; ~$21,000/yr (small teams) | https://carta.com/total-comp |
| Lattice Compensation | Commercial SaaS | Proprietary; ~$6/person/mo add-on | https://www.lattice.com |
| Radford (Aon McLagan) | Commercial data + advisory | Proprietary; $12,000–$40,000/yr per survey | https://radford.aon.com |
| OpenComp | Commercial SaaS | Proprietary; custom (Series A–D) | https://www.opencomp.com |
| Workday Compensation | Commercial SaaS | Proprietary; bundled with Workday HCM | https://www.workday.com |
| Salary.com | Commercial SaaS | Proprietary; $20,000–$100,000/yr | https://www.salary.com |
| Pequity | Commercial SaaS | Proprietary; custom | https://www.pequity.com |

## Feature Analysis by Solution

### Pave

**Core features**
- Real-time compensation benchmarking sourced via direct HRIS integrations from 8,700+ contributing companies, refreshed continuously rather than on an annual survey cycle
- Salary band (pay range) creation and management with configurable number of levels, range spreads, and geographic differentials
- Merit cycle planning with configurable budget allocation, manager-level inputs, and approval routing
- Offer management workflow enabling recruiters and HR to check candidate offers against bands in real time before extending
- Total rewards communications portal allowing employees to view their complete compensation package (salary, equity, benefits) in a personalised statement

**Differentiating features**
- Real-time data from live HRIS connections eliminates the 12–18 month lag of traditional compensation surveys
- AI-powered job matching and predictive ML algorithms that smooth data and fill coverage gaps where sample sizes are thin
- Free entry tier for companies under 200 employees with access to base benchmarks — the only major compensation benchmarking platform with a genuine free tier
- PaveOS platform combining benchmarking, pay range management, merit cycles, and total rewards communication in one end-to-end workflow

**UX patterns**
- Band visualisation showing where an employee's current pay falls relative to the band midpoint, range, and market percentile
- Merit cycle planner with budget progress bar and manager delegation of headcount subsets
- Employee total rewards statement with equity value projections at different valuation scenarios

**Integration points**
- Direct HRIS connectors to BambooHR, Workday, Rippling, ADP, and 20+ others for data contribution and import
- ATS integration to surface band data during the offer process in Greenhouse, Lever, and Ashby
- Equity data sync with Carta for startup equity compensation context

**Known gaps**
- Benchmark data skewed toward VC-backed technology startups; coverage for non-tech industries, government, and non-profit organisations is thinner
- Merit cycle automation capabilities less mature than beqom or Workday Compensation for complex multi-tier approval hierarchies
- Global multi-currency support limited compared with beqom

**Licence / IP notes**
- Proprietary SaaS; no open-source components
- AI job matching algorithm not publicly documented; methodology transparency below what EU Pay Transparency Directive audit obligations may require
- Contributor data from HRIS integrations is aggregated and anonymised; data sharing terms govern how member company data is used in benchmarks

---

### beqom

**Core features**
- Global enterprise compensation management covering merit, annual and discretionary bonuses, long-term incentives (LTI), executive compensation, and equity plan administration
- Salary band management across 100+ countries with multi-currency support and local legislative guidelines
- On-cycle and off-cycle salary review workflows with configurable approval hierarchies and budget guardrails
- Pay equity analytics (PayAnalytics module, acquired 2022) with statistical modelling to identify unexplained pay gaps by gender, ethnicity, and other protected characteristics
- EU Pay Transparency Directive compliance reporting — automated gender pay gap calculation, pay range publication, and audit trail generation

**Differentiating features**
- Strongest global compensation management in the market; the only platform that handles multi-country, multi-currency, multi-incentive compensation complexity at enterprise scale in one system
- Pay Intelligence AI module providing data-driven recommendations for individual pay decisions during merit cycles, combining market benchmarks with internal equity analysis
- PayAnalytics: dedicated pay equity modelling that simulates different remediation scenarios and projects their cost and impact before committing budget
- EU Pay Transparency Directive support built into the platform before competitors; ready for June 2026 enforcement

**UX patterns**
- Manager compensation workbench showing each direct report's current pay, band position, peer comparisons, and a recommended adjustment with AI rationale
- Pay equity dashboard with a traffic-light system showing which roles or departments have statistically significant unexplained pay gaps

**Integration points**
- Deep SAP SuccessFactors, Workday, and Oracle HCM connectors for HRIS data
- Radford, Willis Towers Watson, and Mercer survey data integrations for market benchmarking
- Payroll system connectors for downstream pay change execution

**Known gaps**
- Very expensive and implementation-heavy; minimum ~$55,000/year and 3–6 month implementation projects are typical
- Primarily designed for enterprises of 1,000+ employees; mid-market access constrained
- UX can feel complex for managers unfamiliar with compensation concepts
- Not self-service for benchmarking data; requires survey vendor subscriptions in addition to the platform

**Licence / IP notes**
- Proprietary SaaS; no open-source components
- Pay equity modelling methodology (PayAnalytics) is partially documented in academic literature; the statistical methods (OLS regression, Oaxaca-Blinder decomposition) are standard academic techniques, not proprietary
- EU Pay Transparency Directive compliance requires documented audit trails that beqom generates automatically

---

### PayScale

**Core features**
- Compensation benchmarking database combining crowdsourced salary reports and employer-submitted data covering broad job family and geography combinations
- Pay equity analytics showing median pay gaps by gender, race, and ethnicity with statistical significance indicators
- Compensation management module for managing salary bands, merit cycles, and offer decisions
- Insight Lab: data exploration environment for custom comp analysis and market positioning queries

**Differentiating features**
- Broadest SMB and mid-market coverage in benchmarking data; the most recognisable brand in this segment
- Employee-facing benchmarking: consumer PayScale.com generates candidate-side salary expectations that HR teams can reference
- Pay equity reporting with configurable groupings and pre-built regulatory report templates

**UX patterns**
- Benchmark explorer with interactive filters for job title, geography, experience, and industry
- Manager compensation guide showing recommended pay ranges for open positions
- Annual Compensation Best Practices Report: a widely-cited industry survey on pay strategy trends

**Integration points**
- HRIS integrations with BambooHR, Workday, and ADP
- ATS integration for offer benchmarking within Greenhouse and Lever

**Known gaps**
- Data quality concerns: crowdsourced methodology produces inconsistent data quality relative to HRIS-verified sources like Pave
- Slower to reflect rapid market shifts (e.g., the AI skills wage premium surge of 2024–2026)
- Compensation management module less robust than beqom for complex multi-tier approval workflows

**Licence / IP notes**
- Proprietary SaaS; no open-source components
- Crowdsourced data collection methodology described publicly; no patent claims on data collection techniques

---

### Carta Total Comp

**Core features**
- Equity and salary benchmarking drawn from Carta's private-market cap table dataset — the most accurate source of actual equity grant data for private technology companies
- Total compensation visualisation combining base salary, bonus, and equity value at different funding stages and exit scenarios
- Offer modelling showing the total compensation cost and dilution impact of a proposed offer package
- Integration with Carta's cap table management for unified equity lifecycle management from grant through exercise

**Differentiating features**
- Best-in-market private company equity data — because Carta manages cap tables for 40,000+ private companies, its equity benchmarks reflect real grant values rather than self-reported estimates
- Total compensation modelling that includes equity value projections unavailable from any other benchmarking source
- Natural home for venture-backed companies already using Carta for cap table management

**UX patterns**
- Offer builder with simultaneous base, equity, and bonus configuration and live total compensation value display
- Equity scenario modeller showing potential employee value at various exit multiples

**Integration points**
- Native Carta cap table integration
- HRIS connectors for employee data sync

**Known gaps**
- Limited coverage outside the VC-backed technology startup ecosystem
- Not suitable for public companies, non-tech industries, or companies not using Carta for cap table management
- Compensation management workflows (merit cycles, pay equity) less mature than beqom or Pave

**Licence / IP notes**
- Proprietary SaaS; no open-source components

---

### Lattice Compensation

**Core features**
- Salary band management integrated into the Lattice HR platform alongside performance and engagement data
- Merit cycle workflows where managers make compensation decisions in the same interface where they view performance ratings
- Pay equity analysis showing unexplained pay gaps segmented by gender, ethnicity, and other demographic characteristics
- Budget management tools with top-down allocation and manager-level spend visibility

**Differentiating features**
- Tightest performance-compensation integration in the market; merit recommendations are contextualised by the individual's performance rating, goal completion, and peer feedback data visible on the same screen
- Accessible entry pricing (~$6/person/month as an add-on) for organisations already using Lattice for performance management
- Compensation decisions are grounded in performance evidence, reducing the recency bias and manager subjectivity typical of spreadsheet-based merit cycles

**UX patterns**
- Manager compensation workbench embedded within the performance review flow, not a separate application
- HR admin dashboard showing budget consumption, adjustment distribution, and equity gap trends in real time

**Integration points**
- Native Lattice HRIS data; no external HRIS sync required for Lattice customers
- Carta, Pave, and Radford for external benchmarking data ingestion

**Known gaps**
- Benchmarking data is not native; relies on third-party data imports and does not provide real-time market data
- Limited global multi-country support compared with beqom
- Not a standalone compensation platform; only valuable for existing Lattice customers

**Licence / IP notes**
- Proprietary SaaS; no open-source components

---

### OpenComp

**Core features**
- Pay equity analytics identifying unexplained pay disparities by role, gender, and ethnicity
- Salary band creation with automatic band generation from market data inputs
- Offer management with band-check enforcement preventing out-of-band offers without documented exception approval
- Pay transparency tooling enabling organisations to prepare for US state pay transparency law compliance

**Differentiating features**
- Strong focus on pay equity remediation: the platform not only identifies gaps but models the cost of closing them and supports staged remediation planning
- Purpose-built for growth-stage technology companies (Series A–D) where comp infrastructure is being built for the first time
- Pay transparency workflow enabling organisations to build and publish salary ranges for job postings under Colorado, California, New York, and Illinois requirements

**UX patterns**
- Equity gap visualisation highlighting roles with statistically significant unexplained pay gaps using red/amber/green indicators
- Band builder wizard that generates initial salary bands from market data without requiring compensation expertise

**Integration points**
- HRIS connectors for BambooHR, Rippling, and ADP
- ATS integration for offer benchmarking

**Known gaps**
- Limited to tech company benchmarking data; less coverage for non-tech industries
- Not suitable for enterprises over 5,000 employees
- Global multi-country support minimal

**Licence / IP notes**
- Proprietary SaaS; no open-source components

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Compensation benchmarking with job title, geography, industry, and experience-level filters
- Salary band (pay range) creation and management with configurable levels and range spreads
- Merit cycle workflow with budget allocation, manager inputs, and approval routing
- Pay equity analysis identifying unexplained pay gaps with demographic segmentation
- Offer management with band-check validation against current pay ranges
- Total rewards statement showing employees their complete compensation package
- HRIS integration for employee data sync and automated lifecycle management

### Differentiating Features
- Real-time benchmarking from live HRIS contributions (Pave model) vs. annual survey subscriptions
- AI pay decision recommendations incorporating internal equity and market position simultaneously
- EU Pay Transparency Directive compliance reporting (gender pay gap calculation, range publication, audit trail)
- Equity grant benchmarking and total compensation modelling including equity value scenarios
- Pay equity remediation modelling simulating the cost and impact of closing identified gaps
- Multi-country, multi-currency compensation management at enterprise scale
- Performance-integrated merit cycles where compensation decisions are grounded in visible performance evidence

### Underserved Areas / Opportunities
- No open-source compensation management platform of any kind exists
- SMB access to quality benchmarking data without $12,000+ survey subscriptions
- Automated salary band generation and continuous band maintenance without manual repricing
- Real-time AI skills wage premium tracking for roles where AI competency commands a market premium
- EU Pay Transparency Directive compliance tools accessible to mid-market companies outside the beqom price tier
- Auditable, explainable AI pay recommendations suitable for regulatory scrutiny under EU Pay Transparency audit obligations

### AI-Augmentation Candidates
- Continuous salary band maintenance from ingested job posting data, HRIS submissions, and survey feeds — eliminating the annual repricing project
- Pay equity remediation modelling with scenario simulation and budget impact projection
- Dynamic offer recommendations incorporating candidate location, internal equity constraints, competing offer data, and remaining budget
- AI skills premium detection identifying roles where market rates are shifting rapidly and flagging bands that are falling below market before attrition occurs
- Natural-language compensation analytics enabling HR business partners to query pay data without SQL skills

---

## Legal & IP Summary

- No open-source compensation management platform exists; all tools are proprietary SaaS
- EU Pay Transparency Directive (2023/970/EU, effective June 2026): requires EU employers to publish pay ranges for job postings, enable pay equity audits upon employee request, report gender pay gap statistics, and maintain documented pay-setting criteria — the most significant regulatory driver of new software purchases in this category in 2026
- US State Pay Transparency Laws: Colorado, California (2023), New York (2023), Illinois (2025), and 20+ additional states requiring salary range disclosure in job postings; compliance requires systematic salary band management
- Pay equity statistical methods (OLS regression, Oaxaca-Blinder decomposition) are standard academic techniques with no patent encumbrances; freely implementable
- EU AI Act: AI systems that generate pay recommendations or inform compensation decisions affecting EU employees are likely classified as high-risk; transparency and human oversight requirements apply
- GDPR: employee compensation data combined with demographic data for pay equity analysis is sensitive personal data; requires appropriate lawful basis, data minimisation, and access controls
- Radford/Aon surveys are proprietary datasets; redistribution or use outside the subscription agreement is prohibited
- O*NET and ESCO job taxonomy frameworks are open standards maintained by US DOL and the EU respectively; freely usable for job family classification
- IFRS 2 and ASC 718 (equity compensation accounting standards) are not software-licensable; compliance requirements are informational, not technical

---

## Recommended Feature Scope

**Must-have (MVP)**
- Compensation benchmarking with job title, geography, industry, and experience-level filters using a transparent data methodology
- Salary band creation and management with configurable levels, geographic differentials, and range spread
- Merit cycle workflow with budget allocation, manager-level inputs, and multi-level approval routing
- Pay equity analysis with statistical gap identification by gender and other demographic attributes
- Offer management with band-check enforcement and documented exception approval
- HRIS integration for employee data sync and automated lifecycle updates

**Should-have (v1.1)**
- EU Pay Transparency Directive compliance reporting (gender pay gap, pay range publication, audit trail)
- US state pay transparency law compliance workflow for salary range generation and job posting integration
- AI pay decision recommendations incorporating market benchmarks and internal equity simultaneously
- Total rewards statement portal for employee self-service compensation visibility
- Pay equity remediation modelling with scenario simulation and budget impact projection

**Nice-to-have (backlog)**
- Real-time benchmarking data ingestion from HRIS contributions or live job posting sources
- Equity grant benchmarking and total compensation modelling including equity value scenarios
- Continuous salary band maintenance alerts when market data indicates band drift
- Natural-language compensation analytics for self-service HR business partner queries
- Executive compensation and long-term incentive management for enterprise deployments
