---
name: move-data-migration-approach
description: Generate a data migration approach document and Fit-to-Standard (or discovery) workshop schedule for any enterprise platform migration. Covers migration strategy, object inventory, tooling, and quality gates. Use in Prepare phase. Works for any product, data domain, or industry.
superlabs: MEL (Migration Modernization Lab)
architecture_streams: Data Architect
activate_phase: "2 - Prepare"
version: "1.0"
---

# move-data-migration-approach

Produces a **Data Migration Approach Document** and **Workshop Schedule** for any platform migration.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any target platform |
| `{{source_system}}` | Legacy ERP, flat files, custom DB, any |
| `{{data_domain}}` | Employee master, financial data, customer records, assets, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{migration_complexity}}` | Low / Medium / High |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Migration strategy
- Approach: Big Bang vs. Phased vs. Parallel Run
- Rationale based on `{{migration_complexity}}` and `{{industry}}` constraints
- Cutover implications

### 2. Data object inventory
| Object | Source System | Target System | Volume | Complexity | Migration Tool | Owner |
|---|---|---|---|---|---|---|
| ... | `{{source_system}}` | `{{product}}` | ... | ... | ... | ... |

Populate with common objects for `{{data_domain}}` (e.g., employees, org units, positions, pay data for HR; GL accounts, cost centres for Finance).

### 3. Migration tooling
- Recommended migration tool(s) for `{{product}}`
- Extract, Transform, Load (ETL) pattern
- Validation and reconciliation approach

### 4. Data quality framework
- Data profiling approach
- Cleansing rules and ownership
- Acceptance criteria (record count, field-level completeness thresholds)

### 5. Migration runbook overview
| Milestone | Description | Owner | Phase |
|---|---|---|---|
| Data assessment | Profile source data | Data Lead | Prepare |
| Template download | Get target templates | Tech Lead | Prepare |
| Mock load 1 | Development tenant | Data Lead | Realize |
| Mock load 2 | Test tenant | Data Lead | Realize |
| Final cutover load | Production | Data Lead | Deploy |
| Reconciliation | Validate counts and values | Business SME | Deploy |

### 6. Fit-to-Standard / Discovery workshop schedule
| Workshop # | Topic | Audience | Duration | Phase | Pre-reads |
|---|---|---|---|---|---|
| W-01 | Data scope and object inventory | Business + IT | 2h | Prepare | Source system data dictionary |
| W-02 | Data quality assessment | Data owners | 2h | Prepare | Data profiling report |
| W-03 | Migration tool demonstration | Tech team | 2h | Explore | Tool documentation |
| W-04 | Mock load 1 review | Business SMEs | 1h | Realize | Mock load results |
| W-05 | Go-live readiness — data | All | 1h | Deploy | Final reconciliation report |

### 7. Risks and mitigations
- Top 5 data migration risks with mitigations
- `{{industry}}`-specific data retention or regulatory constraints

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | move-data-migration-approach | SuccessLabs Academy`
