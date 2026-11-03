---
name: discover-scope-document
description: Generate a structured implementation scope statement and phasing roadmap for any enterprise product, platform, or transformation programme. Use at the start of a Discover phase or when a client asks "what are we doing and in what order?" Works for SAP, Workday, Oracle, Salesforce, ServiceNow, or any custom platform, across all 11 GICS sectors.
superlabs: PIL (Product Innovation Lab)
architecture_streams: Enterprise Architect, Business Architect
activate_phase: "1 - Discover"
version: "1.0"
---

# discover-scope-document

Produces a complete **Implementation Scope Statement and Phasing Roadmap** for any product or transformation, parameterised at runtime.

## Runtime parameters — ask the user for any that are missing
| Parameter | Examples |
|---|---|
| `{{product}}` | SAP SuccessFactors, S/4HANA, Workday HCM, Oracle Fusion, Salesforce CRM, ServiceNow ITSM, custom |
| `{{module}}` | Employee Central, Payroll, Finance, Procurement, CRM, ITSM, any |
| `{{industry}}` | Energy, Financial Services, Manufacturing, Retail, Healthcare, Public Sector, any GICS sector |
| `{{country}}` | ISO country code(s) or "global" |
| `{{org_size}}` | Employee headcount band or revenue band |
| `{{delivery_model}}` | Cloud SaaS, On-Premise, Hybrid, BTP extension |
| `{{waves}}` | Number of deployment waves (default 1) |
| `{{deliverable_format}}` | Google Doc, Word, Notion page, Markdown (default Google Doc) |

## What to produce

### 1. Executive scope summary (1 page)
- Solution being implemented, key modules/workstreams
- In-scope countries, legal entities, employee populations
- Out-of-scope explicitly stated
- High-level business objectives (3–5 bullet points)
- Alignment to `{{industry}}` sector compliance requirements

### 2. Phasing roadmap table
Map to SAP Activate 6 phases (or equivalent methodology if non-SAP):

| Phase | Name | Duration | Key Milestones | Quality Gate |
|---|---|---|---|---|
| 1 | Discover | ... | ... | Business case accepted |
| 2 | Prepare | ... | ... | Project Preparation Gate |
| 3 | Explore | ... | ... | Scope and backlog baselined |
| 4 | Realize | ... | ... | UAT passed |
| 5 | Deploy | ... | ... | Go-live Gate |
| 6 | Run | ... | ... | Steady-state ops confirmed |

Adapt durations to `{{org_size}}` and `{{waves}}`.

### 3. Effort estimate framework
- Workstreams: Configuration, Integration, Data Migration, Testing, Change Management, Enablement, Security & IAM, Analytics
- Per-phase effort allocation (%) as a baseline
- Note: this is indicative; confirm with discovery workshops

### 4. Key assumptions and constraints
- List minimum 5 assumptions
- List known constraints (budget, timeline, resourcing, regulatory)
- Flag `{{industry}}`-specific regulatory or compliance dependencies

### 5. Phasing decision rationale
- Why this sequence
- Dependencies between waves (if `{{waves}}` > 1)
- Risk factors that could alter phasing

## Format instructions
- Output as `{{deliverable_format}}`
- Professional headers, numbered sections
- Use a table for the phasing roadmap
- Include a version footer: `v1.0 | discover-scope-document | SuccessLabs Academy`
- Do not hardcode vendor names — use `{{product}}` throughout unless the user has confirmed
