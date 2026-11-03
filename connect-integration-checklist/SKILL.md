---
name: connect-integration-checklist
description: Generate an integration setup checklist for any enterprise integration landscape — covering connection configuration, API testing, middleware setup, data synchronisation verification, and go-live integration readiness. Use in Realize and Deploy phases. Works for any platform pair, middleware, and GICS industry.
superlabs: IEL (Integration Intelligence Lab)
architecture_streams: Integration Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# connect-integration-checklist

Produces an **Integration Setup and Go-Live Readiness Checklist** for any integration landscape.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Primary platform |
| `{{adjacent_systems}}` | Connected systems list |
| `{{middleware}}` | SAP BTP Integration Suite, MuleSoft, Azure Integration Services, any |
| `{{environment}}` | Dev / Test / Production |
| `{{industry}}` | Any GICS sector |
| `{{deliverable_format}}` | Google Sheet, Excel, Checklist Markdown |

## What to produce

### Checklist — one row per check

Columns: `Check ID | Interface ID | Category | Check Description | Environment | Owner | Status (✅/⚠️/❌) | Verified Date | Notes`

#### A. Connection configuration checks
- All system connections configured in `{{middleware}}`
- Authentication credentials (OAuth, API key, certificate) configured and tested
- Endpoint URLs confirmed for `{{environment}}`
- SSL/TLS certificates valid and installed
- Firewall rules and network connectivity verified

#### B. Data flow verification (per interface in interface catalogue)
- Test payload sent and received successfully
- Field mapping validated: source → target
- Data transformation rules applied correctly
- Character encoding and date format handling verified

#### C. Error handling checks
- Error notification configured (email/alerting)
- Dead-letter queue configured
- Retry logic tested (with defined retry count and back-off)
- Error logging visible in monitoring dashboard

#### D. Volume and performance checks
- Peak volume load test conducted
- Interface SLA (records per minute / latency) confirmed
- Monitoring thresholds set

#### E. Security checks
- Service accounts use principle of least privilege
- Credentials stored in secrets vault (not in config files)
- Audit logging enabled for all interfaces
- `{{industry}}`-specific security controls applied (e.g., HIPAA data in transit encryption, NERC-CIP network isolation)

#### F. Go-live readiness (production-specific)
- All interfaces tested end-to-end in production environment
- Hypercare monitoring dashboard live
- Runbook for each interface documented
- On-call contact list for integration issues confirmed

### Interface readiness summary
| Interface ID | Name | Dev ✅ | Test ✅ | Prod ✅ | Go-live Ready? |
|---|---|---|---|---|---|

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | connect-integration-checklist | SuccessLabs Academy`
