---
name: validate-golive-readiness
description: Generate a go-live readiness checklist with RAG (Red / Amber / Green) status tracking across all workstreams — system, data, integration, security, training, support, and governance — for any enterprise platform go-live. Use in Deploy phase. Works for any product, industry, and country.
superlabs: QAL (Quality Assurance Lab)
architecture_streams: Enterprise Architect
activate_phase: "5 - Deploy"
version: "1.0"
---

# validate-golive-readiness

Produces a **Go-Live Readiness Checklist** with RAG status for any enterprise go-live.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{go_live_date}}` | Target go-live |
| `{{deliverable_format}}` | Google Sheet, Excel, Checklist Markdown |

## What to produce

### Readiness checklist — one row per item

Columns: `Check ID | Category | Check Description | Owner | RAG Status (🟢/🟡/🔴) | Evidence / Comment | Blocking? | Resolved By`

#### Category 1 — System readiness
- All environments provisioned and stable
- No P1/P2 open defects
- Performance test passed (within SLA)
- Security vulnerability scan passed
- Backup and recovery tested

#### Category 2 — Data readiness
- Final data migration load completed
- Reconciliation report approved by business
- Data quality checks passed (completeness, accuracy)
- Opening balances / carry-forward data confirmed

#### Category 3 — Integration readiness
- All interfaces live in production
- End-to-end integration test passed
- Monitoring and alerting configured
- Runbooks for each interface completed

#### Category 4 — Security readiness
- All production users provisioned with correct roles
- Test/project team access removed from production
- SoD conflicts resolved or mitigated
- Privileged access reviewed and approved

#### Category 5 — Training and OCM readiness
- Training completion rate ≥ target %
- Support desk activated and staffed
- FAQ and knowledge base live
- Go-live communication sent to all users

#### Category 6 — Governance readiness
- Business sign-off on UAT obtained
- Executive sponsor approval for go-live
- Hypercare plan activated
- AMS / support handover plan confirmed
- `{{industry}}`-specific compliance sign-off obtained (e.g., SOX controls documentation, HIPAA BAA in place)

### RAG summary dashboard
| Category | Total Checks | 🟢 Green | 🟡 Amber | 🔴 Red | Blocking Reds |
|---|---|---|---|---|---|

### Go / No-Go recommendation
Based on RAG summary: [GO / NO-GO / CONDITIONAL GO]
- Conditions (if conditional): list unresolved ambers and reds with owner and resolution date

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | validate-golive-readiness | SuccessLabs Academy`
