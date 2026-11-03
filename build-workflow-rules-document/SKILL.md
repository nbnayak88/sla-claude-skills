---
name: build-workflow-rules-document
description: Produce a workflow and rules configuration document for any enterprise platform — covering approval flows, delegation rules, notification rules, automation triggers, and dynamic conditions. Use in Realize phase. Works for any product, module, and industry.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Application Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# build-workflow-rules-document

Produces a **Workflow and Rules Configuration Document** for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{workflow_engine}}` | Built-in / BPM / ServiceNow Flow / Power Automate / any |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Workflow architecture overview
- Workflow engine used (`{{workflow_engine}}`)
- Workflow types in scope (approval, notification, automation, escalation)
- Integration with role/permission model

### 2. Workflow register — one row per workflow
| Workflow ID | Name | Trigger | Process Area | Approver Logic | Steps | SLA | Delegation Allowed | Escalation | `{{country}}`-specific |
|---|---|---|---|---|---|---|---|---|---|

Generate minimum 15 workflows for `{{module}}`.

### 3. Workflow design detail (for top 5 workflows)
Per workflow:
- Trigger condition
- Step-by-step approval chain (with roles from access matrix)
- Delegation rules
- SLA and reminder schedule
- Escalation path
- Completion notification

### 4. Delegation rules
| Rule ID | Delegator Role | Delegate Role | Scope | Condition | Duration | Auto-Approve? |
|---|---|---|---|---|---|---|

### 5. Automation and trigger rules
| Rule ID | Trigger Event | Condition | Action | Target Object | Timing |
|---|---|---|---|---|---|

### 6. Notification configuration
| Notification ID | Event | Recipients | Channel (Email/In-App/SMS) | Template | Frequency |
|---|---|---|---|---|---|

### 7. `{{industry}}`-specific workflow requirements
- Regulatory approval requirements (e.g., dual-control for Financials, clinical sign-off for Healthcare)
- Union or works council notification rules for `{{country}}`

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | build-workflow-rules-document | SuccessLabs Academy`
