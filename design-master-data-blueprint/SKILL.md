---
name: design-master-data-blueprint
description: Generate an organisational and master data foundation blueprint for any enterprise platform — mapping org structures, master data objects, hierarchies, and their relationships. Use in Explore phase. Replaces product-specific "foundation object" terminology with a universal framework. Works for SAP, Workday, Oracle, Salesforce, or any platform.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Data Architect, Enterprise Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# design-master-data-blueprint

Produces an **Organisational and Master Data Foundation Blueprint** for any enterprise platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | SAP SF, Workday, Oracle Fusion, Salesforce, any |
| `{{module}}` | HCM, Finance, CRM, Supply Chain, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{org_complexity}}` | Simple (1 company) / Medium (multi-entity) / Complex (multi-country, matrix) |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Master data architecture overview
- Master data domains in scope
- Ownership and stewardship model
- Relationship to `{{product}}` data model

### 2. Organisational structure blueprint
| Level | Object Type | Platform Name (in `{{product}}`) | Cardinality | Parent Object | Example Value |
|---|---|---|---|---|---|
| 1 | Legal entity / Company | ... | 1..n | Root | Acme Corp Ltd |
| 2 | Business unit | ... | 1..n | Legal entity | Operations Division |
| 3 | Department | ... | 1..n | Business unit | IT Infrastructure |
| 4 | Cost centre | ... | 1..n | Department | IT-INFRA-001 |
| 5 | Location | ... | 1..n | Legal entity | London HQ |

Adapt levels to `{{org_complexity}}` and `{{industry}}` (e.g., project hierarchy for Real Estate, asset hierarchy for Energy, clinical unit for Healthcare).

### 3. Job and classification structure
| Object | Description | Link to Org | Country-specific? |
|---|---|---|---|
| Job family | ... | ... | No |
| Job function | ... | ... | No |
| Job / position | ... | ... | `{{country}}` |
| Grade / band | ... | ... | `{{country}}` |

### 4. Master data governance design
- Data ownership per object (HR, Finance, IT)
- Creation and maintenance process
- Approval workflow
- Audit trail requirements

### 5. Data model relationship diagram (described in table form)
- Entity: object name, platform object type, key field, cardinality to parent
- Minimum 10 entities for `{{module}}`

### 6. Country and regulatory mapping
- Objects that vary by `{{country}}` (e.g., statutory registration numbers, tax codes, social insurance schemes)
- `{{industry}}`-specific master data objects (e.g., licence records for Healthcare, equipment IDs for Industrials)

### 7. Master data load sequence
- Recommended load order to respect parent-child dependencies
- Interdependencies with data migration plan

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-master-data-blueprint | SuccessLabs Academy`
