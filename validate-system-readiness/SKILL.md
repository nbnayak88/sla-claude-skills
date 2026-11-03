---
name: validate-system-readiness
description: Generate a system readiness checklist covering environment provisioning, tenant or instance access, IAM pre-checks, ALM tooling, and integration prerequisites for any enterprise platform before implementation begins. Use at end of Prepare phase. Works for any cloud or on-premise product.
superlabs: QAL (Quality Assurance Lab)
architecture_streams: Infrastructure Architect, Security Architect
activate_phase: "2 - Prepare"
version: "1.0"
---

# validate-system-readiness

Produces a **System Readiness Checklist** ensuring all environments and access prerequisites are in place.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{environments}}` | Dev, Test, UAT, Prod (default all) |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{deployment_model}}` | Cloud SaaS, On-Prem, Hybrid, BTP/PaaS |
| `{{alm_tool}}` | SAP Cloud ALM, Jira, Azure DevOps, ServiceNow, any |
| `{{deliverable_format}}` | Google Sheet, Excel, Checklist Markdown |

## What to produce

### Checklist structure — one row per check

Columns: `Check ID | Category | Check Description | Owner | Status (✅/⚠️/❌) | Due Date | Notes`

**Categories to cover:**

#### A. Environment provisioning
- Dev / sandbox environment live and accessible
- Test environment live and accessible
- UAT environment live and accessible
- Production environment provisioned (access restricted)
- Non-production to production promotion path confirmed

#### B. User access and IAM
- Admin accounts created for project team
- Role-based access configured per team function
- MFA / SSO configured
- Service accounts for integrations created
- Access review and approval process established

#### C. ALM tooling (`{{alm_tool}}`)
- ALM tenant/instance live
- Project created in ALM tool
- Test management module configured
- Transport/deployment pipeline configured (if applicable)
- Integration between ALM and source control confirmed

#### D. Integration prerequisites
- API endpoints documented
- Middleware / integration platform accessible
- Certificates / OAuth tokens provisioned
- Firewall / network rules confirmed
- Test integration connection successful

#### E. Data migration prerequisites
- Source system data extract tested
- Data migration tooling installed and configured
- Target migration templates downloaded
- Data staging area set up

#### F. `{{industry}}`-specific checks
- Add sector-specific items (e.g., NERC-CIP network isolation for Utilities, HIPAA audit logging for Healthcare, SOX change controls for Financials)

### Summary dashboard
| Category | Total Checks | Complete | Pending | Blocked | % Ready |
|---|---|---|---|---|---|
| Environment | ... | ... | ... | ... | ... |
| IAM | ... | ... | ... | ... | ... |
| ALM | ... | ... | ... | ... | ... |
| Integration | ... | ... | ... | ... | ... |
| Data Migration | ... | ... | ... | ... | ... |
| Sector-specific | ... | ... | ... | ... | ... |
| **TOTAL** | ... | ... | ... | ... | **=FORMULA** |

## Format instructions
- Output as `{{deliverable_format}}`
- RAG status per category
- Footer: `v1.0 | validate-system-readiness | SuccessLabs Academy`
