---
name: lead-stakeholder-plan
description: Build a stakeholder map and communication plan for any enterprise transformation. Identifies key influencers, impacted groups, and communication channels, then generates a phased communications calendar. Use in Prepare phase. Works for any product and any GICS industry sector.
superlabs: PML (Project Performance Lab)
architecture_streams: Business Architect
activate_phase: "2 - Prepare"
version: "1.0"
---

# lead-stakeholder-plan

Produces a **Stakeholder Map and Communication Plan** for any enterprise transformation.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{go_live_date}}` | Target date |
| `{{org_size}}` | Headcount |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Part A — Stakeholder Map (table)
| Stakeholder Group | Role | Interest Level | Influence Level | Impact of Change | Current Sentiment | Desired Sentiment | Owner |
|---|---|---|---|---|---|---|---|
| Executive Sponsor | Champion | High | High | Low | Supportive | Champion | PM |
| HR Leadership | Key User | High | High | High | Neutral | Supportive | OCM Lead |
| Finance Leadership | ... | ... | ... | ... | ... | ... | ... |
| IT / Platform Team | ... | ... | ... | ... | ... | ... | ... |
| End Users | ... | ... | ... | ... | ... | ... | ... |
| Works Council / Union | ... | ... | ... | ... | ... | ... | ... |
| Regulatory Body | ... | ... | ... | ... | ... | ... | ... |

Add `{{industry}}`-specific stakeholders (e.g., NERC auditors for Utilities, clinical governance for Healthcare).

### Part B — Communication Plan
| # | Communication | Audience | Channel | Frequency | Owner | Phase | Content Summary |
|---|---|---|---|---|---|---|---|
| 1 | Project Launch Announcement | All staff | Email + Intranet | Once | Sponsor | Prepare | ... |
| 2 | Steering Committee Update | Execs | Slides | Monthly | PM | All | ... |
| 3 | Project Newsletter | All impacted | Email | Bi-weekly | OCM Lead | Realize–Deploy | ... |
| 4 | Go-live Countdown | All users | Email + Teams | Weekly (T-4 weeks) | OCM Lead | Deploy | ... |
| 5 | Post Go-live Adoption | All users | Email + Portal | Weekly (T+4 weeks) | OCM Lead | Run | ... |

Add rows for `{{industry}}`-specific channels (e.g., floor briefings for Manufacturing, shift handover notes for Energy).

### Part C — Communication calendar
- Month-by-month grid from Prepare through Run
- Colour-coded by audience segment

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | lead-stakeholder-plan | SuccessLabs Academy`
