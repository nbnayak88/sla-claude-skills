---
name: discover-fit-gap-analysis
description: Produce a Fit-to-Standard or Fit-Gap analysis for any enterprise product or module — documenting standard solution coverage versus business requirements, configuration gaps, extension needs, and a prioritised backlog. Use in Explore phase. Works for any platform, module, and GICS sector.
superlabs: PIL (Product Innovation Lab)
architecture_streams: Application Architect, Domain Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# discover-fit-gap-analysis

Produces a **Fit-to-Standard / Fit-Gap Analysis** for any product or module.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module or process area |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{process_area}}` | HR, Finance, Procurement, Sales, ITSM, any |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Fit-Gap register — one row per requirement

Columns: `Req ID | Process Area | Requirement Description | Standard Fit (Yes/Partial/No) | Gap Description | Resolution (Config/Extension/Process Change/Out of Scope) | Priority (Critical/High/Medium/Low) | Effort (S/M/L) | Owner | Sprint | Status`

Populate with minimum 30 representative requirements for `{{module}}` and `{{process_area}}`. Group by process area.

### Gap summary by resolution type
| Resolution Type | Count | % of Total | Notes |
|---|---|---|---|
| Configuration only | ... | ... | Fits standard |
| Minor configuration | ... | ... | Small adjustment |
| Process change required | ... | ... | Business to adapt |
| Extension / custom development | ... | ... | Needs build |
| Out of scope | ... | ... | Deferred |

### Backlog (priority-ordered)
| Priority | Req ID | Description | Resolution | Owner | Sprint |
|---|---|---|---|---|---|
| Critical | ... | ... | ... | ... | ... |
| High | ... | ... | ... | ... | ... |

### `{{industry}}`-specific gap analysis
- Identify requirements unique to `{{industry}}` sector (e.g., shift scheduling for Manufacturing, clinical workflow for Healthcare, NERC-CIP for Utilities)
- Flag if standard product covers them or requires industry-specific extension

### Decision log
| Decision # | Description | Options Considered | Decision Made | Date | Owner |
|---|---|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | discover-fit-gap-analysis | SuccessLabs Academy`
