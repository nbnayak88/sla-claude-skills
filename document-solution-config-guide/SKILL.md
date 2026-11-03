---
name: document-solution-config-guide
description: Generate or update a solution configuration guide for any enterprise platform, module, country, or industry sector — serving as the single reference document for how a specific solution is configured. Use throughout Run phase and for new country/module onboarding. Works for any product.
superlabs: KAL (Knowledge Keystone Lab)
architecture_streams: Application Architect, Industry Architect
activate_phase: "6 - Run"
version: "1.0"
---

# document-solution-config-guide

Produces a **Solution Configuration Guide** — the permanent reference for how a solution is configured.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{version}}` | Guide version (default 1.0) |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Document header
- Product: `{{product}}`
- Module: `{{module}}`
- Country / Region: `{{country}}`
- Industry: `{{industry}}`
- Version: `{{version}}`
- Last updated, owner, review date

### 2. Solution overview
- What is configured and why
- Key business processes supported
- Out-of-scope items

### 3. Technical environment
| Environment | URL / Instance | Version | Last Patched | Owner |
|---|---|---|---|---|
| Development | ... | ... | ... | ... |
| Test | ... | ... | ... | ... |
| Production | ... | ... | ... | ... |

### 4. Configuration reference — by area
For each configured area, document:
- Configuration object / setting name
- Current value
- Rationale / business rule
- `{{country}}`-specific notes
- Last changed date

Areas (adapt to `{{module}}`):
- Organisational structures
- Job and classification structures
- Process and workflow configuration
- Calculation and rules configuration
- Security / role configuration
- Integration configuration
- Analytics / reporting configuration
- `{{country}}`-specific statutory settings
- `{{industry}}`-specific settings

### 5. Known issues and workarounds
| Issue | Impact | Workaround | Permanent Fix ETA | Owner |
|---|---|---|---|---|

### 6. Change history
| Version | Date | Change Description | Changed By | Approved By |
|---|---|---|---|---|

### 7. Contacts and support
| Role | Name | Email | Scope |
|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Version footer: `v{{version}} | document-solution-config-guide | SuccessLabs Academy`
