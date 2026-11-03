---
name: discover-solution-vision
description: Produce a solution vision document covering the to-be architecture, integration landscape map, and technology design for any enterprise platform implementation. Use in Discover phase to align architects, sponsors, and delivery teams on what is being built. Product and industry agnostic.
superlabs: SAL (Strategy & Architecture Lab)
architecture_streams: Enterprise Architect, Application Architect
activate_phase: "1 - Discover"
version: "1.0"
---

# discover-solution-vision

Produces a **Solution Vision Document** establishing the to-be architecture and integration landscape for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | SAP SF, S/4HANA, Workday, Oracle Fusion, Salesforce, ServiceNow, custom |
| `{{module}}` | Core HR, Payroll, Finance GL, CRM, ITSM, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{architecture_stream}}` | Enterprise, Application, Integration, Data, AI (default: Enterprise) |
| `{{deliverable_format}}` | Google Doc, Slides, Markdown |

## What to produce

### 1. Vision statement
- One-paragraph to-be state description
- Key architectural principles (3–5) guiding the solution

### 2. Solution landscape diagram (described in text / table form)
- Core platform: `{{product}}` / `{{module}}`
- Adjacent systems: upstream, downstream, middleware
- Integration touchpoints and protocols (API, iDoc, file, event-driven)
- Data flows: what moves where and when

### 3. Architecture layers
| Layer | To-Be Design |
|---|---|
| Presentation / UX | ... |
| Application | ... |
| Integration | ... |
| Data / Analytics | ... |
| Infrastructure / Cloud | ... |
| Security & IAM | ... |

Fill each layer with specifics for `{{product}}` where known; otherwise describe the design intent.

### 4. Key design decisions
- At least 5 decisions with rationale and alternatives considered
- Flag decisions that are `{{industry}}`-specific (e.g., data residency for Healthcare, OT/IT for Energy)

### 5. Integration catalogue (initial)
| Interface | Source | Target | Direction | Protocol | Frequency |
|---|---|---|---|---|---|
| ... | ... | ... | ... | ... | ... |

### 6. Non-functional requirements
- Security, compliance, performance, availability, scalability
- `{{industry}}`-specific NFRs (e.g., NERC-CIP, HIPAA, SOX, GDPR)

### 7. Architecture risks and open questions
- At least 3 risks with mitigation
- Open questions requiring Explore phase workshops

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | discover-solution-vision | SuccessLabs Academy`
