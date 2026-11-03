---
name: move-data-migration-strategy
description: Build a complete data migration strategy document and pre-built migration template pack for any enterprise platform, data domain, and country. Use in Realize phase. Works for any product (SAP, Workday, Oracle, Salesforce, custom), any data object type, and any GICS industry sector.
superlabs: MEL (Migration Modernization Lab)
architecture_streams: Data Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# move-data-migration-strategy

Produces a **Data Migration Strategy Document and Template Pack** for any platform and domain.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any target platform |
| `{{source_system}}` | Any legacy system |
| `{{data_domain}}` | Employee, Financial, Customer, Asset, Product, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{migration_wave}}` | Wave 1, Wave 2, or All |
| `{{cutover_date}}` | Target cutover date |
| `{{deliverable_format}}` | Google Doc + Google Sheet, Markdown |

## What to produce

### Part A — Migration Strategy Document (Google Doc)

#### 1. Migration objectives and constraints
- What must be migrated by `{{cutover_date}}`
- Data retention requirements for `{{country}}` and `{{industry}}`
- Known constraints (data volume, quality, legacy system limitations)

#### 2. Migration scope
| Object | In Scope | Volume | Source | Target | Notes |
|---|---|---|---|---|---|

#### 3. Migration approach
- Extract strategy (full extract / delta / CDC)
- Transformation rules overview
- Load strategy (direct API / file / batch)
- Cutover approach (big bang / phased)

#### 4. Mock load plan
| Mock Load | Environment | Target Date | Scope | Success Criteria | Owner |
|---|---|---|---|---|---|
| Mock 1 | Dev | ... | 20% of records | Load completes, no fatal errors | Data Lead |
| Mock 2 | Test | ... | 80% of records | Field validation passes | Data Lead |
| Final load | Production | `{{cutover_date}}` | 100% | Reconciliation passed | All |

#### 5. Data quality rules and acceptance criteria
- Completeness thresholds per object
- Validation rules
- Reconciliation approach (record count, key field sums)

#### 6. `{{industry}}`-specific migration requirements
- Data archival obligations (financial records, clinical records, HR records per `{{country}}`)
- Sensitive data handling (PII, PHI, PCI)

### Part B — Migration Template Pack (Google Sheet)
One tab per migratable object. Each tab contains:
- Column headers matching `{{product}}` target fields
- Field-level validation notes (data type, mandatory, format)
- One example row of realistic data
- Error flag column

Generate templates for the top 5 objects in `{{data_domain}}`.

## Format instructions
- Output Part A as Google Doc, Part B as Google Sheet (or both as Markdown if no connector)
- Footer: `v1.0 | move-data-migration-strategy | SuccessLabs Academy`
