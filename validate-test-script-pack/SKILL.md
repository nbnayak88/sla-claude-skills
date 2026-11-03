---
name: validate-test-script-pack
description: Create a comprehensive test script pack for any enterprise platform module — covering end-to-end scenarios, positive and negative cases, integration scenarios, and country/industry-specific regulatory scenarios. Use in Realize phase. Works for any product, module, and GICS sector.
superlabs: QAL (Quality Assurance Lab)
architecture_streams: Application Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# validate-test-script-pack

Produces a **Test Script Pack** for any platform, module, and industry.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{test_type}}` | Unit, Integration, UAT, Regression, All |
| `{{test_tool}}` | SAP Cloud ALM, Jira/Zephyr, Azure DevOps, any |
| `{{deliverable_format}}` | Google Sheet, Excel, Markdown |

## What to produce

### Test script register — one row per test case

Columns: `Script ID | Test Type | Process Area | Scenario Name | Prerequisites | Test Steps | Expected Result | Actual Result | Pass/Fail | Defect ID | Tester | Date | Notes`

Generate minimum 40 test scripts across these categories:

#### A. Happy path / positive scenarios (minimum 15)
- Core end-to-end process flows for `{{module}}`
- Standard country scenarios for `{{country}}`

#### B. Negative / error scenarios (minimum 10)
- Invalid data inputs
- Missing mandatory fields
- Boundary value tests
- Unauthorised access attempts

#### C. Integration scenarios (minimum 8)
- Data flow from `{{product}}` to adjacent systems
- Inbound data validation
- Error handling and retry

#### D. `{{country}}`-specific statutory scenarios (minimum 5)
- Statutory calculation scenarios
- Regulatory compliance checks
- Country-specific process variants

#### E. `{{industry}}`-specific scenarios (minimum 4)
- Sector-specific process flows
- Compliance test scenarios (SOX, HIPAA, NERC-CIP, etc. per `{{industry}}`)

### Test coverage summary
| Category | Scripts | Automated | Manual | Critical | High | Medium | Low |
|---|---|---|---|---|---|---|---|

### Defect severity classification guide
| Severity | Definition | Resolution SLA |
|---|---|---|
| Critical | System unavailable or data corruption | Same day |
| High | Core process broken, workaround not possible | 2 business days |
| Medium | Process impaired, workaround exists | 5 business days |
| Low | Minor cosmetic or non-critical issue | Next release |

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | validate-test-script-pack | SuccessLabs Academy`
