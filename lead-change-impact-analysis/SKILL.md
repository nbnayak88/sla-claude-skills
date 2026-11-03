---
name: lead-change-impact-analysis
description: Generate a change impact analysis and workshop agenda for any enterprise transformation — documenting process changes, impacted roles, training needs, resistance hotspots, and mitigation actions per workstream. Use in Realize phase. Works for any product, platform, and GICS industry sector.
superlabs: PML (Project Performance Lab)
architecture_streams: Business Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# lead-change-impact-analysis

Produces a **Change Impact Analysis** and workshop facilitation guide for any transformation.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{impacted_populations}}` | List of user groups |
| `{{go_live_date}}` | Target date |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Part A — Change impact register
| Impact ID | Process Area | Current State | Future State | Change Type | Impacted Role | Population Size | Impact Level (H/M/L) | Training Need | Comms Need | Resistance Risk | Mitigation |
|---|---|---|---|---|---|---|---|---|---|---|---|

Generate minimum 20 impacts for `{{module}}` and `{{impacted_populations}}`.

### Part B — Impact heat map (table)
Rows = Impacted roles. Columns = Process areas. Values = High / Medium / Low / None.

### Part C — Training needs summary
| Role | Process Area | Change | Training Type | Duration | Delivery Method | Owner |
|---|---|---|---|---|---|---|

### Part D — Resistance risk register
| Stakeholder Group | Resistance Driver | Risk Level | Mitigation Action | Owner | Status |
|---|---|---|---|---|---|

### Part E — Workshop agenda (change impact workshop)
1. Welcome and objectives (10 min)
2. Overview of what is changing in `{{module}}` (15 min)
3. Process walkthrough — current vs. future (30 min per process area)
4. Impact discussion by role (30 min)
5. Training needs confirmation (20 min)
6. Resistance and concerns — open forum (20 min)
7. Actions and next steps (15 min)

Total: ~2.5 hours. Adjust for `{{industry}}`-specific sensitivities.

### Part F — `{{industry}}`-specific impacts
- Union / works council implications for `{{country}}`
- Regulatory change requirements (data protection, audit trail)
- Operational continuity requirements (24/7 shift operations in Energy/Utilities)

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | lead-change-impact-analysis | SuccessLabs Academy`
