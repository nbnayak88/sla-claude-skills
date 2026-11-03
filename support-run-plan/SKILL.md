---
name: support-run-plan
description: Generate a run-phase support plan for any enterprise platform covering steady-state operations model, release and upgrade management cadence, user adoption KPI tracking, and AMS governance rhythm. Use at end of Deploy phase and into Run. Works for any product, industry, and AMS model.
superlabs: AMS (Application Management Services Lab)
architecture_streams: Infrastructure Architect, Domain Architect
activate_phase: "6 - Run"
version: "1.0"
---

# support-run-plan

Produces a **Run-Phase Support Plan** for any enterprise platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{ams_model}}` | In-house / Managed Service / Hybrid |
| `{{release_cadence}}` | Bi-annual (H1/H2), Quarterly, Monthly, Continuous |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Steady-state operations model
- Support team structure and roles
- Coverage hours (business hours / 24×7 / follow-the-sun)
- Tooling: ticketing system, monitoring platform, knowledge base
- SLA framework (by priority tier)

### 2. Incident and problem management
| Process | Owner | Tool | SLA | Escalation |
|---|---|---|---|---|
| Incident logging | Help desk | ... | P1: 1h response | L2 → L3 → Vendor |
| Problem root cause analysis | Tech lead | ... | Within 5 days of P1 | CISO / CTO |
| Known error documentation | Tech lead | ... | Ongoing | — |

### 3. Release and upgrade management
- Release cadence: `{{release_cadence}}`
- Release calendar for next 12 months
- Release testing approach (regression scope, owners)
- Change Advisory Board (CAB) process
- `{{product}}` vendor release tracking

### 4. Change request management
| CR Type | Initiator | Approval Required | SLA | Priority |
|---|---|---|---|---|
| Configuration change | Business | L2 + IT Manager | 5 days | Normal |
| Security change | Security Architect | CISO | 3 days | High |
| Integration change | Tech Lead | IT Manager + Business | 5 days | Normal |
| Emergency change | Any | Sponsor + IT Manager | Same day | Critical |

### 5. User adoption tracking
| KPI | Baseline | T+30 | T+60 | T+90 | T+6M | Owner | Data Source |
|---|---|---|---|---|---|---|---|
| Active user rate | ... | ... | ... | ... | ... | OCM Lead | System logs |
| Process completion rate | ... | ... | ... | ... | ... | Functional Lead | Transactions |
| Self-service rate | ... | ... | ... | ... | ... | OCM Lead | Ticket types |
| Support ticket volume | ... | Declining | Declining | Stable | Stable | AMS Lead | Helpdesk |

### 6. AMS governance rhythm
| Forum | Frequency | Attendees | Agenda |
|---|---|---|---|
| Operational stand-up | Daily (hypercare) / Weekly | AMS team | Incidents, open items |
| Service review | Monthly | AMS Lead + Client | SLA performance, backlog |
| Strategic review | Quarterly | Sponsor + AMS Lead | Roadmap, enhancements |
| Compliance review | Per `{{industry}}` schedule | Compliance + AMS | Audit readiness |

### 7. Continuous improvement backlog
- Process for capturing enhancement requests
- Backlog prioritisation criteria
- Release pipeline for enhancements

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | support-run-plan | SuccessLabs Academy`
