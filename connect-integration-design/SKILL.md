---
name: connect-integration-design
description: Produce an integration design document covering the interface catalogue, middleware topology, API design, data synchronisation patterns, and analytics scope for any enterprise platform implementation. Use in Explore phase. Works for any product pair, middleware, and GICS industry.
superlabs: IEL (Integration Intelligence Lab)
architecture_streams: Integration Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# connect-integration-design

Produces an **Integration Design Document** and interface catalogue for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Primary platform |
| `{{adjacent_systems}}` | List of connected systems |
| `{{middleware}}` | SAP BTP Integration Suite, MuleSoft, Azure Integration Services, Dell Boomi, any |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{integration_patterns}}` | API-first, event-driven, batch file, point-to-point, any |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Integration architecture overview
- Integration topology diagram (described in table form)
- Integration platform / middleware: `{{middleware}}`
- Key design principles (API-first, event-driven, etc.)

### 2. Interface catalogue — one row per interface
| Interface ID | Name | Source System | Target System | Direction | Protocol | Format | Frequency | Criticality | Owner |
|---|---|---|---|---|---|---|---|---|---|

Generate minimum 10 interfaces for `{{product}}` ↔ `{{adjacent_systems}}`.

### 3. Interface design cards (for top 5 interfaces)
Per interface:
- Business purpose
- Data objects exchanged
- Field mapping (source → target, transformation rules)
- Error handling and retry strategy
- Monitoring and alerting approach

### 4. API design standards
- Authentication method (OAuth 2.0, API key, certificate)
- Versioning strategy
- Rate limiting and throttling
- Error response format

### 5. Event-driven design (if applicable)
- Event topics / queues
- Publisher and subscriber mapping
- Dead-letter queue handling

### 6. `{{industry}}`-specific integration requirements
- Sector-standard protocols (e.g., HL7 FHIR for Healthcare, SWIFT for Financials, IEC 61968 for Utilities)
- Regulatory data exchange requirements

### 7. Analytics and reporting integration scope
- Data extracts for reporting / analytics platform
- Real-time vs. batch analytics feeds
- Data warehouse / lake integration (if in scope)

### 8. Integration testing strategy
- Integration test scenarios per interface
- Mock service strategy for unavailable systems
- Performance and load test requirements

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | connect-integration-design | SuccessLabs Academy`
