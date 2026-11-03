---
name: build-project-plan
description: Build a detailed implementation project plan across all 6 SAP Activate phases (or equivalent) for any enterprise platform. Produces a structured task list with phases, workstreams, owners, durations, dependencies, and milestones. Use in Prepare phase. Works for any product or industry.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Enterprise Architect
activate_phase: "2 - Prepare"
version: "1.0"
---

# build-project-plan

Produces a **Full Implementation Project Plan** across all 6 phases for any enterprise platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module(s) |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{start_date}}` | Project start date |
| `{{go_live_date}}` | Target go-live |
| `{{team_size}}` | Number of project team members |
| `{{waves}}` | Number of deployment waves |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Master task list — one row per task
Columns: `Task ID | Phase | Workstream | Task Name | Owner | Duration (days) | Start | End | Dependencies | Status | Priority | Notes`

Generate tasks for ALL of the following workstreams across ALL 6 phases:

**Workstreams to cover:**
1. Project Management & Governance
2. Configuration & Development
3. Integration
4. Data Migration
5. Testing (Unit, Integration, UAT, Performance, Security)
6. Change Management & Enablement
7. Security & IAM
8. Analytics & Reporting
9. Infrastructure & Environment
10. Cutover & Go-live

**Phases:**
- Phase 1 Discover: Scope, business case, solution vision, stakeholder kickoff
- Phase 2 Prepare: Charter, governance, environment setup, workshop scheduling, strategies
- Phase 3 Explore: Fit-to-standard workshops, design documents, backlog, test strategy
- Phase 4 Realize: Configuration sprints, integration build, data migration dev/test, test execution, enablement build
- Phase 5 Deploy: Cutover rehearsal, go-live, hypercare
- Phase 6 Run: Steady-state operations, release management, adoption tracking

### Milestone summary table
| # | Milestone | Phase | Target Date | Owner | Gate Criteria |
|---|---|---|---|---|---|
| M1 | Business case accepted | Discover | ... | Sponsor | Signed scope doc |
| M2 | Project preparation gate | Prepare | ... | PM | Charter approved |
| M3 | Explore gate | Explore | ... | PM | Backlog baselined |
| M4 | Realize gate | Realize | ... | PM | UAT passed |
| M5 | Go-live | Deploy | `{{go_live_date}}` | PM | Readiness checklist green |
| M6 | Steady-state handover | Run | ... | AMS Lead | Support plan signed |

### Resource plan summary
- Roles required per phase
- Estimated FTE days per workstream

## Format instructions
- Output as `{{deliverable_format}}` with one row per task
- Minimum 60 tasks across all phases and workstreams
- Footer: `v1.0 | build-project-plan | SuccessLabs Academy`
