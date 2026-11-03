---
name: build-project-charter
description: Generate a complete project charter for any enterprise implementation or transformation programme — scope, RACI, governance model, quality gates, schedule framework, and budget structure. Use at Prepare phase kickoff. Works for any product, platform, or industry.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Enterprise Architect
activate_phase: "2 - Prepare"
version: "1.0"
---

# build-project-charter

Produces a **Project Charter** for any enterprise implementation engagement.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{project_name}}` | Any descriptive name |
| `{{product}}` | Any platform |
| `{{module}}` | Any module or workstream |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{start_date}}` | Project start |
| `{{go_live_date}}` | Target go-live |
| `{{budget_band}}` | Small (<$500k), Medium ($500k–$2M), Large (>$2M) |
| `{{delivery_model}}` | Cloud SaaS, On-Prem, Hybrid |
| `{{deliverable_format}}` | Google Doc, Word, Notion |

## What to produce

### 1. Project overview
- Project name, sponsor, project manager
- Objectives (3–5 SMART)
- Success criteria
- Alignment to business strategy

### 2. Scope statement
- In scope: modules, countries, populations, integrations
- Out of scope: explicit exclusions
- Assumptions

### 3. Governance model
- Steering committee composition and cadence
- Project leadership team
- Escalation matrix
- Decision authority matrix

### 4. RACI matrix
| Workstream | Sponsor | PM | Functional Lead | Technical Lead | Business SME | Vendor |
|---|---|---|---|---|---|---|
| Configuration | ... | ... | R | A | C | I |
| Integration | ... | ... | ... | ... | ... | ... |
| Data Migration | ... | ... | ... | ... | ... | ... |
| Testing | ... | ... | ... | ... | ... | ... |
| Change Management | ... | ... | ... | ... | ... | ... |
| Security & IAM | ... | ... | ... | ... | ... | ... |

Populate with R/A/C/I per row.

### 5. High-level schedule
| Phase | Start | End | Key Milestones |
|---|---|---|---|
| 1 Discover | ... | ... | ... |
| 2 Prepare | ... | ... | ... |
| 3 Explore | ... | ... | ... |
| 4 Realize | ... | ... | ... |
| 5 Deploy | ... | ... | ... |
| 6 Run | ... | ... | ... |

### 6. Budget framework
| Category | Indicative % | Notes |
|---|---|---|
| Software licence | ... | ... |
| Implementation services | ... | ... |
| Data migration | ... | ... |
| Testing | ... | ... |
| Training & change management | ... | ... |
| Contingency | 10–15% | ... |

### 7. Quality gates
- Gate criteria per phase (Discover → Run)
- Sign-off authority for each gate

### 8. Risks and issues log (initial)
- Top 5 risks with probability, impact, mitigation

### 9. Charter approval
- Signature block: Sponsor, PM, key stakeholders

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | build-project-charter | SuccessLabs Academy`
