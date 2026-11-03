---
name: lead-training-plan
description: Build a go-live OCM and end-user training plan for any enterprise platform implementation — covering training needs analysis, curriculum design, delivery schedule, training materials index, and support desk readiness. Use in Deploy phase. Works for any product, industry, and user population.
superlabs: PML (Project Performance Lab)
architecture_streams: Business Architect, UI/UX Architect
activate_phase: "5 - Deploy"
version: "1.0"
---

# lead-training-plan

Produces a **Go-Live OCM and End-User Training Plan** for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{user_population}}` | Total users and role breakdown |
| `{{go_live_date}}` | Target go-live |
| `{{training_delivery}}` | Classroom, Virtual, e-Learning, Hybrid |
| `{{deliverable_format}}` | Google Slides, Google Doc, Markdown |

## What to produce

### Part A — Training needs analysis
| Role | Process Area | Current Proficiency | Required Proficiency | Training Gap | Training Type | Duration | Priority |
|---|---|---|---|---|---|---|---|

### Part B — Curriculum design
| Course ID | Course Name | Target Role | Learning Objectives (3–5) | Duration | Format | Prerequisites | Delivery Tool |
|---|---|---|---|---|---|---|---|

Generate minimum 8 courses for `{{module}}` and `{{user_population}}`.

### Part C — Training delivery schedule
| Week | Audience | Course | Format | Trainer | Venue / Platform | Capacity | Completion Target |
|---|---|---|---|---|---|---|---|

Map to T-4 weeks through T-0 relative to `{{go_live_date}}`.

### Part D — Training materials index
| Material ID | Title | Format | Course | Owner | Status | Location |
|---|---|---|---|---|---|---|
| TM-001 | System overview e-learning | SCORM | All | ... | Draft | ... |
| TM-002 | Quick reference guide | PDF | Managers | ... | Draft | ... |
| TM-003 | Process walk-through video | MP4 | End users | ... | Draft | ... |

### Part E — Support desk readiness
- Support model: Level 1 / Level 2 / Level 3
- FAQ document (top 20 anticipated questions)
- Escalation path
- Knowledge base articles required
- Support desk go-live date (should precede go-live by 1 week)

### Part F — Post go-live adoption tracking
| KPI | Baseline | Target (T+30) | Target (T+60) | Target (T+90) | Measure Method |
|---|---|---|---|---|---|
| Login rate | 0% | 80% | 90% | 95% | System login logs |
| Process completion rate | 0% | 75% | 85% | 90% | Transaction counts |
| Support ticket volume | Baseline TBD | <X per week | Declining | Stable | Helpdesk system |

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | lead-training-plan | SuccessLabs Academy`
