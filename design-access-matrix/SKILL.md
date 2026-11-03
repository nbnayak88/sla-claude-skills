---
name: design-access-matrix
description: Generate a role-based access or permission design matrix for any enterprise platform — defining roles, permission groups, data access scopes, and sensitive access controls. Use in Explore phase. Works for SAP, Workday, Oracle, Salesforce, ServiceNow, or any platform across all GICS sectors.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Security Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# design-access-matrix

Produces a **Role-Based Access / Permission Design Matrix** for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{access_model}}` | RBAC, ABAC, RBP, Profile-based, any |
| `{{regulatory_framework}}` | SOX, HIPAA, GDPR, NERC-CIP, none |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Part A — Role catalogue
| Role ID | Role Name | Role Type | Description | User Population | Modules / Objects | Data Scope | Sensitive Access? |
|---|---|---|---|---|---|---|---|
| R-001 | System Administrator | Technical | Full admin access | IT team only | All | All entities | Yes — restricted |
| R-002 | HR Manager | Business | HR data management | HR Managers | HR module | Own department | No |
| R-003 | Finance Approver | Business | Approve financial transactions | Finance managers | Finance module | Own cost centre | No |
| ... | ... | ... | ... | ... | ... | ... | ... |

Generate minimum 15 roles for `{{module}}` and `{{industry}}`.

### Part B — Permission matrix
Rows = Roles. Columns = Key functions / objects. Values = Full / Read / No Access.

| Role | Create | Read | Update | Delete | Approve | Report | Admin |
|---|---|---|---|---|---|---|---|
| System Admin | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| HR Manager | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ | ❌ |
| ... | ... | ... | ... | ... | ... | ... | ... |

### Part C — Segregation of Duties (SoD) matrix
| Conflict ID | Role A | Role B | Conflict Risk | `{{regulatory_framework}}` Reference | Mitigation |
|---|---|---|---|---|---|

Minimum 8 SoD conflicts relevant to `{{module}}` and `{{regulatory_framework}}`.

### Part D — Sensitive access register
| Access Item | Risk Level | Justification Required | Approval Authority | Review Frequency |
|---|---|---|---|---|

### Part E — Data access scope design
- Row-level security / data scoping rules
- Multi-country / multi-entity access design for `{{country}}`
- `{{industry}}`-specific data isolation requirements (e.g., clinical data for Healthcare, trading desk data for Financials)

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-access-matrix | SuccessLabs Academy`
