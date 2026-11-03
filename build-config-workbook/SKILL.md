---
name: build-config-workbook
description: Build a full configuration workbook for any enterprise platform module — capturing all configuration parameters, values, technical keys, and country or sector-specific settings in one structured reference document. Use in Realize phase. Works for any product, module, and GICS sector.
superlabs: IIL (Implementation Intelligence Lab)
architecture_streams: Application Architect, Domain Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# build-config-workbook

Produces a **Full Configuration Workbook** for any platform and module.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{config_depth}}` | High-level (key settings only) / Detailed (all parameters) |
| `{{deliverable_format}}` | Google Sheet, Excel |

## What to produce

One tab per configuration area. Minimum tabs:

### Tab 1 — General settings
| Parameter | Description | Value | `{{country}}`-specific | Mandatory | Source / Reference |
|---|---|---|---|---|---|

### Tab 2 — Organisational configuration
| Object | Code | Name | Parent | Country | Currency | Status |
|---|---|---|---|---|---|---|

### Tab 3 — Process configuration
| Process Area | Configuration Item | Setting | Value | Notes |
|---|---|---|---|---|

### Tab 4 — Period / calendar configuration
| Period Type | Start | End | Description | Applies To |
|---|---|---|---|---|

### Tab 5 — Calculation and rules configuration
| Rule ID | Rule Name | Input | Logic | Output | `{{country}}` | Statutory Reference |
|---|---|---|---|---|---|---|

### Tab 6 — Integration configuration
| Interface ID | Connection Name | Endpoint / URL | Auth Method | Schedule | Status |
|---|---|---|---|---|---|

### Tab 7 — Security configuration
| Role | Permission Set | Data Scope | Sensitive | Approved By |
|---|---|---|---|---|

### Tab 8 — `{{country}}`-specific settings
| Setting | `{{country}}` Value | Regulatory Reference | Effective Date |
|---|---|---|---|

### Tab 9 — `{{industry}}`-specific settings
| Setting | Value | Industry Standard | Notes |
|---|---|---|---|

### Tab 10 — Change log
| Version | Date | Changed By | Change Description | Approved By |
|---|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}` multi-tab workbook
- Footer on each tab: `v1.0 | build-config-workbook | SuccessLabs Academy`
