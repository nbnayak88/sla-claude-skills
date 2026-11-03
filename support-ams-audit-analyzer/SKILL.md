---
name: support-ams-audit-analyzer
description: Analyze an AMS audit checklist or health check file for any enterprise platform — reading a structured checklist (Excel or tabular data) and producing a gap summary, risk-rated findings, and a prioritised remediation plan. Use in Run phase for quarterly health checks or compliance audits. Works for any product, module, and GICS sector.
superlabs: AMS (Application Management Services Lab)
architecture_streams: Domain Architect, Industry Architect
activate_phase: "6 - Run"
version: "1.0"
---

# support-ams-audit-analyzer

Analyzes an **AMS Audit Checklist** and produces a gap summary with remediation plan.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{checklist_file}}` | Upload or paste checklist data |
| `{{audit_period}}` | Quarter or date range |
| `{{deliverable_format}}` | Google Sheet, Markdown |

## How to use
1. Provide the audit checklist — either upload a file or paste the data in tabular form
2. Specify `{{product}}`, `{{module}}`, `{{country}}`, `{{industry}}`
3. The skill reads the checklist structure and produces the outputs below

## Expected checklist input format
The checklist should contain rows with: Check ID | Category | Check Description | Status (Pass / Fail / Not Reviewed / In Progress) | Owner | Notes

Common categories: Configuration, Integration, Security & IAM, Testing / QA, Data Quality, Process Compliance, Documentation.

## What to produce

### 1. Audit summary scorecard
| Category | Total Checks | Pass | Fail | Not Reviewed | In Progress | Pass Rate % | Risk Level |
|---|---|---|---|---|---|---|---|

### 2. Gap register (Fail and Not Reviewed items)
| Gap ID | Category | Check Description | Status | Risk Level (Critical/High/Medium/Low) | Root Cause | Remediation Action | Owner | Target Date | Effort |
|---|---|---|---|---|---|---|---|---|---|

### 3. Risk-rated findings summary
| Risk Level | Count | % | Trend vs. Prior Audit |
|---|---|---|---|
| Critical | ... | ... | Improved / Same / Worse |
| High | ... | ... | ... |
| Medium | ... | ... | ... |
| Low | ... | ... | ... |

### 4. Prioritised remediation plan
| Priority | Gap ID | Remediation Action | Owner | Due Date | Effort | Status |
|---|---|---|---|---|---|---|

Order by: Critical → High → Medium → Low. Within priority, order by effort (Quick wins first).

### 5. `{{country}}` and `{{industry}}`-specific findings
- Flag any gaps with statutory or regulatory implications
- Reference relevant regulation (GDPR, SOX, HIPAA, NERC-CIP, etc.)
- Escalation recommendation if critical statutory gap found

### 6. Management summary
- Overall health score (0–100%)
- 3 key strengths
- 3 priority actions
- Recommended next audit date

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | support-ams-audit-analyzer | SuccessLabs Academy`
