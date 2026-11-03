---
name: validate-test-strategy
description: Create a test strategy and master test plan for any enterprise platform implementation covering test types (unit, integration, UAT, performance, security), test phases, entry/exit criteria, defect management, and tooling. Use in Explore phase. Works for any product and any GICS industry.
superlabs: QAL (Quality Assurance Lab)
architecture_streams: Application Architect
activate_phase: "3 - Explore"
version: "1.0"
---

# validate-test-strategy

Produces a **Test Strategy and Master Test Plan** for any enterprise platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{test_tool}}` | SAP Cloud ALM, Jira/Zephyr, Azure DevOps, HP ALM, any |
| `{{go_live_date}}` | Target go-live |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Test strategy overview
- Objectives and scope
- Test approach and philosophy (risk-based, requirement-based)
- Test environments: Dev, Test, UAT, Performance, Security
- Tooling: `{{test_tool}}`
- Defect management process

### 2. Test types and coverage
| Test Type | Scope | Owner | Environment | Entry Criteria | Exit Criteria | Phase |
|---|---|---|---|---|---|---|
| Unit / String test | Individual config objects | Functional lead | Dev | Config complete | 100% pass | Realize |
| Integration test | End-to-end process flows | Tech lead + Functional | Test | Integration deployed | All critical flows pass | Realize |
| UAT | Business acceptance | Business SMEs | UAT | Integration test passed | Agreed defect threshold | Realize |
| Regression test | Existing functionality after changes | QA lead | Test | Any config change | No new critical defects | Realize |
| Performance test | System under load | Tech lead | Performance | UAT passed | SLA thresholds met | Realize |
| Security test | Access, pen test | Security architect | Test | Security config complete | No critical vulnerabilities | Realize |
| Cutover / smoke test | Core processes post go-live | All | Production | Cutover complete | Critical flows green | Deploy |

### 3. Test calendar
| Phase | Test Activity | Start | End | Duration |
|---|---|---|---|---|

Map to `{{go_live_date}}` and work backwards.

### 4. Test data strategy
- Test data requirements per test type
- Anonymisation / masking approach (GDPR, `{{industry}}` regulations)
- Data refresh cadence

### 5. `{{industry}}`-specific test considerations
- Compliance test requirements (SOX controls for Financials, clinical safety for Healthcare, OT security for Utilities)
- Regulatory sign-off requirements

### 6. Defect management
- Severity and priority classification
- Defect lifecycle
- Go-live defect threshold by severity

### 7. Test sign-off and UAT acceptance criteria
- UAT sign-off authority
- Acceptance criteria definition

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | validate-test-strategy | SuccessLabs Academy`
