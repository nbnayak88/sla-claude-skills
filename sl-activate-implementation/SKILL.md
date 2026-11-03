---
name: sl-activate-implementation
description: Plan and run implementation of ANY solution (SAP or other) using SAP Activate across Discover, Prepare, Explore, Realize, Deploy and Run, driven by Fit-Gap results. Produces phase plan, deliverables, quality gates, workstreams, RAID, test, data migration, cutover and change plans, and a 90-day mobilization wave. Use after sl-solution-fitgap or when the user asks to implement a solution with SAP Activate.
---

# SL Activate Implementation

Applies SAP Activate to a *solution-agnostic* implementation. Phase structure mirrors the SuccessLabs payroll catalog (read-only reference; never modified). New IDs use the `SL-` prefix.

## Inputs
Fit-Gap workbook (decisions, gaps, integrations, data), CAP (constraints, stakeholders, KPIs, gates), sector profile, product, delivery model (cloud vs on-prem; SAP Activate for cloud, ERP-style, or Agile/Scrum variant), team and timeline if known.

## Phases and what each must produce
| Phase | Purpose | Core outputs | Quality gate |
|---|---|---|---|
| 1 Discover | Value and fit validated | Vision, value hypotheses, solution scope, trial/sandbox, stakeholder map, initial roadmap | Business case and scope accepted |
| 2 Prepare | Mobilize | Charter, governance, team/RACI, project plan, standards, environment plan, change strategy, data-migration strategy, security/IAM approach | Project Preparation Gate |
| 3 Explore | Fit-to-standard | Fit-to-standard workshops, REQ baseline, backlog, process model, gap resolution decisions, integration/data design, test strategy | Explore Gate (scope and backlog baselined) |
| 4 Realize | Build and test | Sprints: configuration, extensions, integrations, migration build, test cycles (unit, integration, UAT, security, performance), training build | Realize Gate (UAT passed, defects within threshold) |
| 5 Deploy | Cutover | Cutover plan and rehearsals, go-live readiness, hypercare, support handover | Go-live Gate |
| 6 Run | Operate and improve | Support model, release adoption, KPI/value tracking, continuous improvement | Value realization review |

Add **Gate 5-style benefits acceptance** in Run when the case calls for it.

## Workstreams (tailor per solution)
Project governance - Process/functional - Data migration - Integration - Security & IAM - Testing - Change, training & adoption - Technical/infrastructure/BTP - Reporting & analytics - Compliance/safety (sector) - Value realization.

## Procedure
1. **Translate Fit-Gap into delivery:** F1-F3 > configuration backlog; G1 > extension epics; G2 > procurement/integration track; G3 > exception-approved dev; P > change items; U > spike/PoC in Explore.
2. **Sequence in waves** using dependency chain: named owners and baselines > trusted identity/master data > secure connectivity and integration > data products > usable workflows > verified outcomes > replication. Start with Wave 0 (first 90 days) before building.
3. **Build the phase plan** with deliverable IDs `SL-<PHASE>-<TYPE>-<NN>`; PHASE = DISC, PREP, EXPL, REAL, DEPL, RUN; TYPE = GOV, CFG, EXT, INT, DM, TST, SEC, CHG, PM, ENB, ANL, VAL.
4. **Quality gates:** each gate has entry criteria, evidence, approvers, and stop/pivot conditions. Sector constraints (safety, regulatory) are mandatory gate evidence.
5. **Testing:** every REQ maps to at least one test scenario; include negative, permission, integration failure, reconciliation and rollback tests.
6. **Change & adoption:** role-based; frontline co-design; measure sustained task completion, not training attendance.
7. **Cutover & hypercare:** rehearsals, go/no-go criteria, rollback decision point, reconciliation checks, hypercare exit criteria.
8. **Value tracking:** benefit register with baseline, owner, attribution; Finance validates benefits.
9. **RAID:** seed risks from CAP validation backlog and sector hot spots.

## Output
- Roadmap (waves x phases), Gantt-style table, deliverable catalog (ID, phase, type, owner, acceptance), gate checklist, RAID starter, RACI, 90-day plan.
- Effort/cost only as labeled estimates with assumptions.
- Format: Docs artifact for the plan, Sheets for deliverable catalog/RAID, Slides on request.

## Guardrails
- Do not start build before Explore fit-to-standard sign-off unless running an explicit spike.
- No go-live recommendation without tested rollback and named support owner.
- If the target product is not SAP, keep the Activate phases and gates but replace SAP-specific tooling references with the vendor's equivalents and say so.

See `references/activate-deliverables.md` for the deliverable catalog template and phase checklists.
