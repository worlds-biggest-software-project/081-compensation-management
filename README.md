# Compensation Management

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An open-source, AI-native compensation management platform delivering salary bands, merit cycles, equity tracking, and pay equity analytics with auditable methodology.

Compensation Management is a candidate project to build the first open-source platform for salary band management, comp review cycles, equity administration, and benchmarking. It targets People, Total Rewards, and Finance teams who today must choose between expensive enterprise suites such as beqom and Radford or fast-moving but proprietary SaaS tools like Pave and Carta Total Comp. The project's core problem: no open, auditable system exists for setting and defending compensation decisions under the rising weight of pay transparency regulation.

---

## Why Compensation Management?

- **No open-source option exists.** Every incumbent — Pave, beqom, PayScale, Carta Total Comp, Lattice, OpenComp, Workday Compensation, Salary.com, Pequity — is proprietary SaaS, leaving teams without a transparent alternative.
- **Enterprise pricing locks out the mid-market.** Radford surveys cost $12,000–$40,000 per year, beqom starts around $55,000 per year, and PayScale averages around $27,000 per year, making professional comp tooling inaccessible to companies under 500 employees.
- **Annual survey cadences are stale.** Traditional providers refresh data once a year, but AI skills are commanding a 56% wage premium in 2026 (up from 25% in 2023) — bands set in January are obsolete by Q2.
- **Pay transparency regulation is forcing new purchases.** The EU Pay Transparency Directive (2023/970/EU) takes effect June 2026, and U.S. state laws in Colorado, California, New York, and Illinois already require salary range disclosure — driving a wave of buying that current incumbents serve only at enterprise prices.
- **Closed methodologies fail audit obligations.** The EU Pay Transparency Directive creates new audit rights for employees and works councils; closed-source band-setting algorithms and undocumented data sources cannot meet that standard.

---

## Key Features

### Benchmarking & Salary Bands

- Compensation benchmarking with job title, geography, industry, and experience-level filters using a transparent, documented data methodology
- Salary band creation and management with configurable levels, geographic differentials, and range spreads
- Automated band generation from market data inputs for teams without dedicated compensation expertise
- Continuous band maintenance alerts when ingested market data indicates bands are drifting below market

### Merit Cycles & Offer Workflow

- Merit cycle workflow with budget allocation, manager-level inputs, and multi-level approval routing
- Offer management with band-check enforcement and documented exception approval
- Manager compensation workbench surfacing each report's current pay, band position, and recommended adjustment
- Total rewards statement portal for employee self-service compensation visibility

### Pay Equity & Compliance

- Pay equity analysis with statistical gap identification (OLS regression, Oaxaca-Blinder decomposition) by gender and other demographic attributes
- Pay equity remediation modelling with scenario simulation and budget impact projection
- EU Pay Transparency Directive compliance reporting: gender pay gap calculation, pay range publication, audit trail generation
- U.S. state pay transparency workflow for salary range generation and job posting integration

### AI-Augmented Decisions

- AI pay decision recommendations combining market benchmarks with internal equity analysis
- Dynamic offer recommendations incorporating candidate location, internal equity, competing offers, and remaining budget
- AI skills premium detection flagging roles where market rates are shifting rapidly before attrition occurs
- Natural-language compensation analytics enabling HR business partners to query pay data without SQL skills

### Equity & Total Rewards

- Equity grant benchmarking and total compensation modelling including equity value scenarios
- Executive compensation and long-term incentive (LTI) management for enterprise deployments
- HRIS integration for employee data sync and automated lifecycle updates

---

## AI-Native Advantage

AI turns compensation management from an annual project into a continuous background process. Instead of repricing bands once a year by cross-referencing multiple survey vendors, the system continuously ingests live job posting data, HRIS-submitted records, and survey feeds to auto-update midpoints and flag drift. Pay equity tooling moves beyond gap identification to model the cost of closing all statistically significant gaps, prioritise by impact, and simulate remediation budgets — work that today consumes weeks of analyst time and consultant fees. Offer generation produces personalised recommendations that account for location, competing offers, internal equity, and remaining budget, eliminating the "let me check with HR" delay.

---

## Tech Stack & Deployment

The project is expected to support self-hosted and cloud deployment, with documented data ingestion sources and an auditable band-setting algorithm to satisfy EU Pay Transparency Directive audit obligations. Job family classification will build on open occupational taxonomies — O*NET (U.S. DOL) and ESCO (EU) — both freely usable open standards. HRIS, ATS, and payroll integrations follow the patterns established by incumbents (BambooHR, Workday, Rippling, ADP, Greenhouse, Lever, Ashby, Carta). Pay equity statistical methods (OLS regression, Oaxaca-Blinder decomposition) are standard academic techniques with no patent encumbrances. EU AI Act high-risk system requirements (transparency, human oversight) and GDPR controls for sensitive compensation and demographic data are first-class concerns.

---

## Market Context

The compensation management software market was valued at approximately $3.50B in 2022 and is projected to reach $7.23B by 2030 at a 9.5% CAGR (Cognitive Market Research). Regulatory mandates are the primary demand driver: 45% of U.S. employers now operate in jurisdictions with active pay transparency laws, and the EU Pay Transparency Directive enforces from June 2026. Primary buyers are Chief People Officers, VPs of Compensation, Total Rewards Managers, and CFOs at companies in the 500–20,000-employee range, with an underserved long tail of sub-500-employee companies that cannot justify Radford ($12K+) or beqom ($55K+) spend.

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

Licence to be determined. See [discussion](#) for context.
