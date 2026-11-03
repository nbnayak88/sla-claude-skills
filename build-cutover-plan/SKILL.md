---
name: build-cutover-plan
description: Generate a detailed cutover plan with task-level checklist, go/no-go criteria, parallel run strategy, sequenced cutover activities, and post-cutover monitoring for any enterprise platform go-live. Use in Deploy phase. Works for any product, industry, and go-live complexity level.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Enterprise Architect
activate_phase: "5 - Deploy"
version: "1.0"
---

# build-cutover-plan

Produces a **Cutover Plan** for any enterprise platform go-live.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{cutover_date}}` | Go-live date and time |
| `{{cutover_window}}` | Duration (hours) |
| `{{parallel_run}}` | Yes / No |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Part A — Cutover task list
One row per task. Columns: `Task ID | Sequence | Task Name | Workstream | Owner | Duration (min) | Dependency | Planned Start | Planned End | Actual Start | Actual End | Status | Notes`

Organise tasks by workstream:
1. **Pre-cutover preparation** (T-2 weeks through T-day)
2. **System freeze and lockout** (freeze legacy, comms to users)
3. **Data migration — final load** (extract, transform, load, reconcile)
4. **Configuration promotion** (Dev → Test → Prod, per transport order)
5. **Integration activation** (enable production integrations, verify)
6. **Security and access activation** (production roles, remove test users)
7. **Smoke testing** (core process verification in production)
8. **Business sign-off** (UAT sign-off leads confirm go-live)
9. **Go-live communication** (announce go-live to users)
10. **Hypercare activation** (activate support desk, monitoring)

Generate minimum 50 tasks.

### Part B — Go / No-Go criteria
| Criterion | Owner | Status | Blocking? |
|---|---|---|---|
| All critical defects resolved | QA Lead | ... | Yes |
| Data migration reconciliation passed | Data Lead | ... | Yes |
| All integrations live and tested | Integration Lead | ... | Yes |
| Security roles verified in production | Security Architect | ... | Yes |
| Training complete for all users | OCM Lead | ... | Yes |
| Hypercare team confirmed | AMS Lead | ... | Yes |
| Executive sign-off obtained | Sponsor | ... | Yes |

### Part C — Parallel run plan (if `{{parallel_run}}` = Yes)
- Duration of parallel run
- What runs in parallel (legacy + new)
- Reconciliation frequency and method
- Decision criteria to cut legacy

### Part D — Rollback plan
- Rollback decision trigger conditions
- Rollback sequence (reverse of cutover)
- Maximum rollback window
- Communication plan for rollback

### Part E — Post go-live monitoring (first 72 hours)
| Check | Frequency | Owner | Alert Threshold |
|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | build-cutover-plan | SuccessLabs Academy`
