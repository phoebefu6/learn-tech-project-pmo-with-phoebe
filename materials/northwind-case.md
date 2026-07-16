# Northwind - the running case bible

Every session runs the PMO tools on ONE fictional project: the **Northwind Data Platform Initiative**.
All numbers below are made up and rounded - dummy data for teaching only, no real company.
Numbers here are canon: all pages and presenter notes must stay consistent with this file.
Update here first if anything changes.

## The company

**Northwind** is a fictional mid-size omni-channel retailer (physical stores + e-commerce + a
loyalty app). It has grown for 15 years and its data now sits scattered across five source
systems that never shared a warehouse. The CEO has set a clear mandate: get the business onto
one governed data platform that can serve BI, analytics, data science, and AI - fast.

- 15 years old, ~$1.2B annual revenue
- 380 stores + an e-commerce site + a loyalty mobile app
- ~6M loyalty members
- Data estate: ~120 source tables across 5 source systems, ~80 TB of historical archive
- Five source systems: POS (Oracle), e-commerce (Postgres), loyalty app (MySQL),
  finance ERP (SAP export), marketing (SaaS API)
- Target cloud: AWS (S3 landing, Redshift lake + warehouse, Glue ETL, QuickSight BI)

## The situation (why the mandate is urgent)

- Years of deferred data ownership: no shared dictionary, no lineage, inconsistent keys
- The CEO wants "100% of source and app data into the warehouse" - and has given 90 days
- To honour the deadline, the team will do a pragmatic **raw dump (~80 TB) into a staging
  data lake** first. This is an interim step, not a governed warehouse - it is not queryable
  as-is without schema harmonisation, consolidation, and quality assurance.
- The real deliverable is the governed platform built on top, in stages
- Critical technical roles are not yet hired - this is the hardest dependency in the plan

## The lifecycle this project must deliver (DW -> BI -> AI/ML)

1. **Ingest** - raw archive + daily incremental into the lake
2. **Warehouse (DW) construction** - harmonise schemas, build bronze/silver/gold layers,
   migrate the legacy warehouse, certify core datasets
3. **BI** - governed dashboards and self-service on certified data
4. **Data science / AI / ML** - a prioritised pool of data products, first model only on
   certified, traceable data

## Cast (recurring roles in examples - generic names, no real people)

- **The CEO** - sets the 90-day mandate ("all data in the warehouse"), the escalation ceiling
- **Priya** - Head of Data & Analytics; owns technical acceptance criteria and PMO planning.
  This is the seat the learner sits in - each session hands you the pen.
- **Marcus** - PMO Execution; tracks milestones, action items, the risk register, cadence
- **The Executive Sponsor** - cross-org alignment, senior-hire panel lead, blocker escalation
- **Source dev teams** (external) - own the data dictionary, ERDs, keys, table clarifications
- **Cloud/Infra partner** (external) - landing zone, VPC, IAM, security baseline
- **Governance office** (CIO / Data Governance) - data classification, PII policy, retention,
  quality accountability, lineage ownership

## The priorities the charter names (P1-P4 pattern)

- **P1 - Source data & knowledge transfer:** schema docs for all tables/versions; a formal KT
  programme; expect a low-quality rushed dictionary, so plan an independent profiling pass.
- **P2 - Cloud & infrastructure:** AWS primary; isolated environment; landing zone (VPC, IAM,
  secrets, network security, compliance baseline) BEFORE any data is ingested.
- **P3 - Governance & data dictionary:** classification, PII tagging, retention, access tiers
  defined BEFORE architecture is finalised; ERDs, PKs, column-level business definitions.
- **P4 - Hiring (hard dependency):** no technical milestone is committed until the critical
  hires are in place; hiring runs as a parallel track from day one.

## The milestone spine (canon - Session 2 builds this, later sessions reference it)

| ID | Milestone | Lifecycle stage |
|----|-----------|-----------------|
| M1 | Raw archive load into the data lake | Ingest |
| M1.1 | Daily incremental (D+1) pipeline | Ingest |
| M1.2 | SIT/UAT environment for the data team | Enabler |
| M2 | Cloud & data infrastructure setup | Infra |
| M2.1 | Critical roles hired & onboarded | Enabler (hard gate) |
| M3 | Legacy warehouse migration into the platform | DW |
| M4 | Governed warehouse build (silver/gold, certified) | DW |
| M5 | Raw exploration & data dictionary study | Discovery |
| M5.2 | Data product idea pool (prioritised backlog) | Discovery |
| M6 | One-stop platform in production (BI + DS + AI/ML) | Production |

Milestone table columns (the reusable skeleton): **ID · Milestone · Success Criteria ·
Key Success Metrics · Primary Dependency**.

## Canon decisions (so sessions do not contradict each other)

- The "100%" mandate is reframed: the raw dump is the interim honesty step; the governed
  **curated** layer is the real deliverable. Scope is sized by peer benchmark (a curated
  working set), not by treating all 120 tables as equally important.
- **Hiring is the hard dependency:** no technical milestone is committed until the Data
  Architect and Data Engineering Lead are onboarded. Hiring is a parallel track from day one.
- **Governance before architecture:** classification, PII, retention, and access tiers are
  signed off before the warehouse design is finalised (M2 is gated by governance).
- **Data products are prioritised** by business value x feasibility x data readiness. The
  first AI/ML product ships only on certified, traceable data (M6).

## The risk register spine (canon - Session 4 builds this)

| ID | Risk | Severity |
|----|------|----------|
| R1 | Low-quality / incomplete data dictionary | HIGH |
| R2 | Archive completeness & reconciliation gaps | HIGH |
| R3 | Critical hiring delayed - blocks all tech milestones | HIGH |
| R4 | Governance not defined before architecture | HIGH |
| R5 | Scope creep - "100% of everything" vs a curated set | MEDIUM |
| R6 | Cloud cost blowout on 80 TB raw + reprocessing | MEDIUM |
| R7 | Over-reliance on a single infra/vendor dependency | MEDIUM |
| R8 | Network security & data residency not formalised | MEDIUM |
