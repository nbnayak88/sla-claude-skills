---
name: design-data-model
description: Produce a data model design document for any enterprise platform — defining objects, fields, data types, classification schemes, and regulatory mapping. Use in Explore phase. Works for any product, data domain, country, and GICS industry sector.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Data Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# design-data-model

Produces a **Data Model Design Document** for any platform and domain.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{data_domain}}` | Employee, Financial, Customer, Product, Asset, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Data model scope
- Entities in scope for `{{module}}` and `{{data_domain}}`
- Entities out of scope
- Related models (integration data model, analytics model)

### 2. Entity catalogue
| Entity | Platform Object | Description | Key Field | Data Type | Mandatory | Source |
|---|---|---|---|---|---|---|

Minimum 15 entities for `{{data_domain}}`. Include standard entities (person, organisation, transaction, classification) and `{{industry}}`-specific entities.

### 3. Field-level data dictionary (for top 5 entities)
| Field Name | Data Type | Length | Mandatory | Allowed Values | Validation Rule | Regulatory Reference |
|---|---|---|---|---|---|---|

### 4. Classification and code list design
| Classification | Values | Governance Owner | Country-specific |
|---|---|---|---|

### 5. Regulatory and statutory field mapping
| Regulatory Requirement | Field | Entity | `{{country}}` | Authority |
|---|---|---|---|---|

Add `{{industry}}`-specific requirements (e.g., NPI for US Healthcare, LEI for Financials, EAN/GLN for Consumer Staples).

### 6. Data quality rules
| Rule ID | Entity | Field | Rule Type | Condition | Error Action |
|---|---|---|---|---|---|

### 7. Data model decisions
| # | Decision | Options | Chosen | Rationale |
|---|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-data-model | SuccessLabs Academy`
