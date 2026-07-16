# Course map - learn-tech-project-pmo-with-phoebe

Six 45-minute sessions. One running case (Northwind, see `northwind-case.md`). Learners leave
with a full PMO pack: charter, milestone map, dependency graph, risk register, RACI, tracker.

The course teaches the working ~80% of established project-management practice as applied to a
data-platform build. Certifications (PMP, PRINCE2, etc.) and full standards stay official -
this teaches the practitioner core and cites the canon.

## Source canon (frameworks this course leans on)

| Source | What we take from it |
|--------|----------------------|
| PMBOK Guide / PMI (project charter, scope, stakeholder, risk) | charter anatomy, milestone & success-criteria discipline, risk process |
| RACI / responsibility assignment matrix | ownership model (Responsible/Accountable/Consulted/Informed) |
| RAID log practice (Risks, Assumptions, Issues, Dependencies) | risk register + dependency register |
| Critical Path Method (CPM) & dependency types | hard vs soft dependencies, gates, parallel tracks |
| Stage-gate / phase-gate governance | milestone gates, go/no-go criteria |
| Probability x impact risk scoring | severity tagging (HIGH/MED/LOW), mitigation-owner-trigger |
| Data-migration & data-warehouse delivery practice | bronze/silver/gold, reconciliation, certified datasets, DW->BI->AI/ML lifecycle |
| Benchmarking for scope sizing | peer-evidence working-set sizing (curated vs raw estate) |

Re-verify: PM standards evolve (PMBOK editions shift emphasis). Facts here are practitioner-stable;
confirm edition-specific wording before formal delivery.

## Per-session coverage (✓ live · ◐ self-study)

### Session 1 - Frame the Initiative & the Charter (🟢 foundation)
| Topic | Depth |
|-------|-------|
| Project charter anatomy (context, position, objectives) | ✓ |
| Priorities model P1-P4 (data, infra, governance, hiring) | ✓ |
| "Interim vs final" honesty (raw dump vs governed platform) | ✓ |
| Stakeholder framing & the mandate | ◐ |
| Scope statement & assumptions | ◐ |
Build: 1-page Northwind charter (context + 4 priorities).

### Session 2 - Milestone Architecture (🟡 core)
| Topic | Depth |
|-------|-------|
| Milestone table: ID · Milestone · Success Criteria · Key Metrics · Primary Dependency | ✓ |
| Laddering M1->M6 + sub-milestones | ✓ |
| SMART success criteria & measurable metrics | ✓ |
| DW->BI->AI/ML lifecycle mapped to milestones | ✓ |
| Stage-gate go/no-go criteria | ◐ |
Build: Northwind milestone map.

### Session 3 - Dependencies & Hard Gates (🟠 advanced)
| Topic | Depth |
|-------|-------|
| Dependency types (finish-to-start etc.), hard vs soft | ✓ |
| The hard gate: hiring blocks technical milestones | ✓ |
| Critical path & parallel tracks | ✓ |
| Governance-before-architecture gate | ✓ |
| Dependency register (RAID D) | ◐ |
Build: dependency graph + hard-gate list.

### Session 4 - The Risk Register (🟡 core)
| Topic | Depth |
|-------|-------|
| Risk register anatomy (R1-R8), probability x impact | ✓ |
| Severity tagging HIGH/MED/LOW | ✓ |
| Mitigation -> owner -> trigger -> escalation | ✓ |
| RAID log (risks/assumptions/issues/dependencies) | ◐ |
| Risk burn-down & review cadence | ◐ |
Build: 8-row Northwind risk register.

### Session 5 - Ownership & RACI (🟡 core)
| Topic | Depth |
|-------|-------|
| RACI matrix (Responsible/Accountable/Consulted/Informed) | ✓ |
| Internal PIC vs external cross-functional ownership | ✓ |
| Governance sign-offs & escalation points | ✓ |
| One-accountable rule & over-Consulted anti-pattern | ◐ |
Build: Northwind RACI matrix.

### Session 6 - Sizing, Benchmarking & Tracking (🟠 advanced)
| Topic | Depth |
|-------|-------|
| Peer-benchmark scope sizing (curated working set) | ✓ |
| Migration/inventory tracker (source->silver->gold, coverage %, quality flags) | ✓ |
| Status cadence, RAG reporting, action-item closure | ✓ |
| Path to production: certified BI + DS sandbox + AI/ML on traceable data | ✓ |
| KPI/health dashboard for the PMO | ◐ |
Build: benchmark + tracking dashboard; wrap the Northwind initiative.

## Not covered by design (honest list)

- Certification prep (PMP, PRINCE2, CAPM) - this is practitioner practice, not exam cramming
- Detailed cost estimation / earned-value management (EVM) - named, not drilled
- Agile ceremonies (sprints, standups) - this course is initiative/milestone PMO, not scrum
- Vendor contracting & legal - referenced in risk/governance, not taught
- Hands-on AWS/Redshift/Glue build - the DATA build is the context; this course teaches the PMO
