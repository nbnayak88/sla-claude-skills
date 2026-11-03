---
name: discover-business-case
description: Generate a concise business case document for any enterprise technology transformation — ROI, compliance drivers, strategic benefits, and risk of inaction. Use in Discover phase for executive sponsorship, budget approval, or programme justification. Works for any product, platform, or industry.
superlabs: PIL (Product Innovation Lab)
architecture_streams: Business Architect, Domain Architect
activate_phase: "1 - Discover"
version: "1.0"
---

# discover-business-case

Produces a **Business Case Summary** for any enterprise transformation initiative, structured for executive sign-off.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | SAP SuccessFactors ECP, S/4HANA Finance, Workday Payroll, ServiceNow ITSM, any |
| `{{module}}` | Payroll, Finance, HR Core, Procurement, ITSM, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{org_size}}` | Headcount or revenue |
| `{{current_state}}` | Brief description of legacy system / pain points |
| `{{deliverable_format}}` | Google Doc, Slides executive deck, Markdown |

## What to produce

### 1. Executive summary (half page)
- What is being proposed
- Why now (regulatory, competitive, operational driver)
- Expected outcome in one sentence

### 2. Current state pain points
- 5–7 bullet points specific to `{{current_state}}` and `{{industry}}`
- Quantify where possible (manual hours, error rates, compliance gaps)

### 3. Proposed solution overview
- `{{product}}` / `{{module}}` capability summary
- How it addresses each pain point
- Deployment model (`{{delivery_model}}` if provided)

### 4. Business benefits
| Benefit Category | Description | Indicative Value |
|---|---|---|
| Cost reduction | ... | $X or X% |
| Compliance risk mitigation | ... | Regulatory fine avoidance |
| Productivity gains | ... | FTE hours saved |
| Strategic enablement | ... | Qualitative |

Tailor benefit categories to `{{industry}}` — e.g., NERC-CIP compliance for Utilities, SOX for Financials, HIPAA for Healthcare.

### 5. Risk of inaction
- Regulatory exposure
- Operational risk
- Competitive disadvantage
- Technical debt growth

### 6. Investment summary
- Indicative cost categories (licence, implementation, training, change management)
- Payback period estimate
- NPV/ROI range (if data provided)

### 7. Recommendation
- Clear go/no-go recommendation
- Proposed next step (move to Prepare phase)

## Format instructions
- Keep to 3–5 pages maximum
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | discover-business-case | SuccessLabs Academy`
