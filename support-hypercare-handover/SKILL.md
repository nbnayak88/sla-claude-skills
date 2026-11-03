---
name: support-hypercare-handover
description: Create a hypercare and operations handover document defining the support structure, escalation matrix, SLA commitments, handover criteria, and AMS transition timeline from project team to steady-state operations. Use at go-live and Deploy phase close. Works for any product, industry, and support model.
superlabs: AMS (Application Management Services Lab)
architecture_streams: Domain Architect, Infrastructure Architect
activate_phase: "5 - Deploy"
version: "1.0"
---

# support-hypercare-handover

Produces a **Hypercare and Operations Handover Document** for any platform go-live.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{hypercare_duration}}` | 2 weeks / 4 weeks / 8 weeks |
| `{{ams_model}}` | In-house / Managed Service / Hybrid |
| `{{go_live_date}}` | Go-live date |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Hypercare overview
- Hypercare period: `{{go_live_date}}` + `{{hypercare_duration}}`
- Purpose and objectives
- Hypercare team composition (project team + AMS team overlap)
- Operating model during hypercare

### 2. Support structure
| Support Level | Who | Scope | SLA (Response / Resolution) | Escalation To |
|---|---|---|---|---|
| Level 1 — User support | Help desk | User queries, how-to, access issues | 4h response / 1 day resolve | Level 2 |
| Level 2 — Functional support | Functional SME | Config issues, process questions | 4h response / 2 days resolve | Level 3 |
| Level 3 — Technical support | Technical lead | Integration, data, system errors | 2h response / 1 day resolve | Vendor |
| Level 4 — Vendor support | `{{product}}` vendor | Product defects | Per vendor SLA | — |

### 3. Escalation matrix
| Issue Type | L1 Owner | L2 Owner | L3 Owner | Exec Escalation | Resolution SLA |
|---|---|---|---|---|---|

### 4. Issue management during hypercare
- Daily hypercare stand-up agenda
- Issue log template
- Priority classification (Critical / High / Medium / Low)
- Communication to users for known issues

### 5. Handover criteria — project team → AMS
| Criterion | Target | Current Status | Owner |
|---|---|---|---|
| Open P1/P2 issues | 0 | ... | PM |
| Knowledge transfer sessions completed | 100% | ... | AMS Lead |
| Runbooks signed off | 100% | ... | Tech Lead |
| SLA agreement signed | Done | ... | AMS Lead |
| Monitoring dashboards handed over | Done | ... | Tech Lead |
| `{{industry}}`-specific compliance docs handed over | Done | ... | Compliance Lead |

### 6. AMS transition timeline
| Week | Activity | Owner |
|---|---|---|
| Hypercare W1 | Project team on-site / on-call full time | PM |
| Hypercare W2 | AMS team shadowing all support | AMS Lead |
| Hypercare W3–W4 | AMS team leading, project team on standby | AMS Lead |
| Post-hypercare | Full AMS ownership | AMS Lead |

### 7. Steady-state operations model
- Release management: how updates / patches are applied
- Change request process
- Periodic health check cadence
- `{{industry}}`-specific compliance review schedule

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | support-hypercare-handover | SuccessLabs Academy`
