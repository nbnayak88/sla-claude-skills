---
name: discover-ocm-briefing
description: Draft an Organizational Change Management (OCM) approach document and stakeholder briefing for any enterprise transformation. Use at Discover phase kickoff to align sponsors on change strategy. Works for any product, platform, and any GICS industry sector.
superlabs: ECL (Experts Engagement Lab)
architecture_streams: Business Architect, Domain Architect
activate_phase: "1 - Discover"
version: "1.0"
---

# discover-ocm-briefing

Produces an **OCM Approach Document and Stakeholder Briefing** for any enterprise transformation.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{industry}}` | Any GICS sector |
| `{{org_size}}` | Headcount or scope |
| `{{change_complexity}}` | Low / Medium / High / Very High |
| `{{go_live_date}}` | Target date or quarter |
| `{{deliverable_format}}` | Google Doc, Google Slides, Markdown |

## What to produce

### Part A — OCM Approach Document

#### 1. Change vision
- What is changing, for whom, and why it matters to `{{org_size}}` people in `{{industry}}`

#### 2. Change impact summary
- Impacted groups and estimated population
- Degree of change per group (Low / Medium / High)
- `{{industry}}`-specific sensitivities (e.g., union agreements in Industrials, clinical workflow disruption in Healthcare)

#### 3. OCM strategy pillars
- Sponsorship model (executive, middle management cascade)
- Communication strategy
- Training and enablement strategy
- Resistance management approach
- Measurement and adoption tracking

#### 4. OCM workstream plan
| Activity | Owner | Phase | Timing |
|---|---|---|---|
| Sponsor alignment workshop | ... | Discover | Week 1 |
| Stakeholder analysis | ... | Prepare | Week 2–3 |
| Communication plan v1 | ... | Prepare | Week 3 |
| Change impact workshops | ... | Realize | ... |
| Training delivery | ... | Deploy | ... |
| Adoption measurement | ... | Run | Ongoing |

#### 5. OCM governance
- OCM lead role and responsibilities
- Escalation path
- Reporting cadence

### Part B — Stakeholder Briefing (slide-ready outline)
1. Why we are transforming (business driver)
2. What is changing (solution summary)
3. Timeline overview
4. What it means for you (per audience)
5. How we will support you
6. Next steps and questions

## Format instructions
- Part A as `{{deliverable_format}}`; Part B as bullet outline for Slides
- Footer: `v1.0 | discover-ocm-briefing | SuccessLabs Academy`
