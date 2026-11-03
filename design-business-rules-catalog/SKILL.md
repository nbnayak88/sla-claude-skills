---
name: design-business-rules-catalog
description: Build a business rules catalog for any enterprise platform and domain — covering statutory rules, computational derivation rules, workflow and approval rules, and validation rules. Use in Explore phase. Works for any product, module, country, and GICS sector.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Application Architect, Domain Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# design-business-rules-catalog

Produces a **Business Rules Catalog** for any platform, module, and domain.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Payroll, Finance GL, Procurement, ITSM, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{rule_domain}}` | Calculation, Validation, Workflow, Statutory, Security |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Business rules register — one row per rule

Columns: `Rule ID | Category | Rule Name | Description | Trigger | Input Variables | Logic / Formula | Output | `{{country}}`-specific | Statutory Reference | Priority | Owner | Status`

Categories to cover:

#### A. Statutory and regulatory rules
- Tax calculation rules for `{{country}}`
- Social insurance / benefit contribution rules
- Labour law compliance rules (overtime, leave, working hours)
- `{{industry}}`-specific regulations (NERC-CIP, HIPAA, SOX, Basel III, etc.)

Minimum 10 statutory rules.

#### B. Computational / derivation rules
- Calculation logic for key values (pay, charges, allocations, scores)
- Derivation of classification from input values
- Rounding, currency conversion, period calculation rules

Minimum 10 computation rules.

#### C. Workflow and approval rules
- When an approval is required
- Approval chain logic
- Delegation rules
- Escalation conditions

Minimum 8 workflow rules.

#### D. Validation rules
- Mandatory field checks
- Value range checks
- Cross-field consistency rules
- Duplicate detection rules

Minimum 8 validation rules.

### Rule summary dashboard
| Category | Total Rules | Statutory | Custom | Pending Confirmation |
|---|---|---|---|---|

### Conflicting rules log
| Rule A | Rule B | Conflict Description | Resolution |
|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-business-rules-catalog | SuccessLabs Academy`
