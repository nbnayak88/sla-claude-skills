---
name: design-solution-document
description: Build a solution design document for any enterprise platform covering structures, schemas, configuration values, process flows, and design decisions. Use in Explore phase after Fit-Gap to document what will be built. Works for any product, module, and industry.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Application Architect, Domain Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# design-solution-document

Produces a **Solution Design Document (SDD)** for any platform and module.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{process_area}}` | HR, Finance, Procurement, ITSM, any |
| `{{design_depth}}` | High-level blueprint / Detailed configuration design |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Document purpose and scope
- What this SDD covers
- What it does not cover
- Related documents (Fit-Gap register, data model, integration design)

### 2. Solution overview
- Process area: `{{process_area}}`
- Key functional areas configured
- Configuration approach summary

### 3. Business process flows
For each major process in scope:
- As-is (current state) — brief
- To-be (future state) — detailed with system steps
- Key differences and change impacts

### 4. Configuration design — structure tables
| Object Type | Object Name | Code / Key | Description | Linked Objects |
|---|---|---|---|---|

Populate with representative objects for `{{module}}` and `{{industry}}`. Include:
- Organisational structures (company, cost centre, department, location)
- Classification structures (job family, grade, category)
- Period/calendar structures
- Code lists and value sets

### 5. Key configuration values
| Setting | Value | Rationale | `{{country}}`-specific? |
|---|---|---|---|

### 6. Regulatory and compliance design
- How `{{country}}` and `{{industry}}` statutory requirements are met
- Configuration vs. process controls

### 7. Design decisions log
| # | Decision | Options | Chosen | Rationale | Date | Owner |
|---|---|---|---|---|---|---|

### 8. Open items and assumptions
- Items requiring further business input
- Assumptions made in this design

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | design-solution-document | SuccessLabs Academy`
