---
name: build-config-log
description: Generate a configuration log for tracking the setup of any enterprise platform's objects, structures, and settings across development, test, and production environments. Use throughout Realize phase. Works for any product, module, and industry.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Application Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# build-config-log

Produces a **Configuration Log** for tracking configuration status across environments.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{environments}}` | Dev, Test, UAT, Prod |
| `{{sprint}}` | Sprint number or iteration |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Configuration log — one row per configuration item

Columns: `Config ID | Object Type | Object Name / Code | Description | Config Value | Environment | Status (Not Started / In Progress / Complete / Verified) | Dev Done | Test Done | UAT Done | Prod Done | Configured By | Verified By | Notes`

Group rows by object category:
1. Organisational structures (company, business unit, department, location, cost centre)
2. Job and classification structures (job family, job, grade, position)
3. Process configuration (workflow, approval, notification, calculation rules)
4. Security and access (roles, permission groups, data scopes)
5. Integration configuration (connection settings, API endpoints, credential references)
6. Analytics / reporting configuration (report definitions, dashboard tiles, data sources)
7. `{{module}}`-specific objects

Generate minimum 40 configuration items.

### Environment promotion tracker
| Config ID | Object | Dev ✅ | Test ✅ | UAT ✅ | Prod ✅ | Promoted By | Date |
|---|---|---|---|---|---|---|---|

### Sign-off summary
| Category | Total Items | Complete | Pending | Sign-off Owner |
|---|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | build-config-log | SuccessLabs Academy`
