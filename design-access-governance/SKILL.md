---
name: design-access-governance
description: Build an access governance document covering automated provisioning design, Segregation of Duties (SoD) controls, periodic access review processes, and privileged access management for any enterprise platform. Use in Realize phase. Works for any product, regulatory framework, and GICS industry sector.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Security Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# design-access-governance

Produces an **Access Governance Document** for any enterprise platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{regulatory_framework}}` | SOX, HIPAA, GDPR, NERC-CIP, ISO 27001, none |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{iam_tool}}` | SAP Cloud IAG, Saviynt, SailPoint, CyberArk, native, any |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Access governance framework
- Governance principles
- Roles: Access Owner, Access Approver, Access Reviewer, IAM Administrator
- Governance cadence and reporting

### 2. Automated provisioning design
- Joiner process: new user → automatic role assignment based on job/org attributes
- Mover process: role changes on transfer, promotion, country change
- Leaver process: immediate deprovisioning on termination
- Provisioning tool: `{{iam_tool}}`
- Exceptions and manual override process

### 3. SoD control matrix
| SoD Control ID | Risk | Role A | Role B | `{{regulatory_framework}}` Reference | Mitigation Control | Compensating Control |
|---|---|---|---|---|---|---|

Minimum 12 SoD controls relevant to `{{module}}` and `{{regulatory_framework}}`.

### 4. Privileged access management
| Privileged Access Type | Who Has It | Justification | Approval Required | Review Frequency | Emergency Process |
|---|---|---|---|---|---|

### 5. Periodic access review process
- Review frequency (quarterly / semi-annual / annual)
- Review owner and approver by role category
- Certification process (certify / revoke / escalate)
- Evidence and audit trail requirements for `{{regulatory_framework}}`

### 6. Access reporting
| Report | Audience | Frequency | Content |
|---|---|---|---|
| New access granted | Security | Weekly | All new permissions |
| SoD violations | Risk / Audit | Monthly | Active conflicts |
| Privileged access | CISO | Monthly | All admin access |
| Dormant accounts | IT | Quarterly | Accounts inactive >90 days |
| Access certification results | Audit | Quarterly/Annual | Certification status |

### 7. `{{industry}}`-specific governance requirements
- Specific controls required by `{{regulatory_framework}}`
- Sector-specific access risks (e.g., trading system access for Financials, clinical system access for Healthcare)

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-access-governance | SuccessLabs Academy`
