---
name: scale-learning-curriculum
description: Build a structured learning curriculum for enterprise technology practitioners organized by role (Consultant, Architect, PM, Functional Analyst, Developer) and implementation phase, covering any product or platform. Use for consultant onboarding, continuous upskilling, and academy programme design. Works for any product and GICS industry sector.
superlabs: SCALE (School of Career Acceleration Lab for Excellence)
architecture_streams: Domain Architect
activate_phase: "6 - Run"
version: "1.0"
---

# scale-learning-curriculum

Produces a **Learning Curriculum** organized by role and implementation phase for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module(s) |
| `{{industry}}` | Any GICS sector |
| `{{audience_roles}}` | Consultant, Architect, PM, Functional Analyst, Developer, All |
| `{{delivery_mode}}` | Self-paced, Instructor-led, Blended, Bootcamp |
| `{{duration_target}}` | Hours per role (e.g., 20h = Super Sprint 20) |
| `{{deliverable_format}}` | Google Slides, Google Doc, Markdown |

## What to produce

### 1. Curriculum architecture overview
- Product: `{{product}}` / Module: `{{module}}`
- Target audience: `{{audience_roles}}`
- Total curriculum duration per role
- Learning path structure (Foundational → Practitioner → Expert)

### 2. Learning paths by role
For each role in `{{audience_roles}}`:

#### Role: [e.g., Functional Consultant]
| Level | Module Name | Duration | Format | Prerequisites | Assessment |
|---|---|---|---|---|---|
| Foundational | Platform overview | 1h | e-Learning | None | Quiz |
| Foundational | `{{module}}` basics | 2h | e-Learning | Platform overview | Quiz |
| Practitioner | Fit-to-Standard workshop delivery | 3h | Workshop | Foundational complete | Practical |
| Practitioner | Configuration hands-on | 4h | Lab | Workshop delivery | Lab exercise |
| Expert | End-to-end implementation | 8h | Simulated project | All practitioner | Case study |

Minimum 6 modules per role. Adapt to `{{duration_target}}`.

### 3. Curriculum content map (all roles × all phases)
Rows = SAP Activate phases (Discover → Run). Columns = Roles. Value = Learning module name(s).

| Phase | `{{audience_roles[0]}}` | `{{audience_roles[1]}}` | `{{audience_roles[2]}}` | ... |
|---|---|---|---|---|
| 1 Discover | ... | ... | ... | ... |
| 2 Prepare | ... | ... | ... | ... |
| 3 Explore | ... | ... | ... | ... |
| 4 Realize | ... | ... | ... | ... |
| 5 Deploy | ... | ... | ... | ... |
| 6 Run | ... | ... | ... | ... |

### 4. `{{industry}}`-specific learning modules
| Module | Target Role | Duration | Industry Focus | Content Outline |
|---|---|---|---|---|

Minimum 4 modules covering `{{industry}}`-specific requirements, regulations, and operational patterns.

### 5. Assessment and certification framework
| Assessment | Level | Format | Pass Mark | Badge / Credential |
|---|---|---|---|---|
| Foundational quiz | Foundational | Online MCQ | 80% | SuccessLabs Foundational Badge |
| Practitioner lab | Practitioner | Hands-on lab | Task complete | SuccessLabs Practitioner Badge |
| Expert case study | Expert | Simulated project | Panel review | SuccessLabs Expert Badge |

### 6. Delivery calendar (12-month plan)
| Month | Cohort | Programme | Format | Audience | Capacity |
|---|---|---|---|---|---|

### 7. Content creation roadmap
- Modules to create vs. adapt from existing content
- Estimated effort per module
- Priority order

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | scale-learning-curriculum | SuccessLabs Academy`
