---
name: discover-analytics-config-guide
description: Produce an analytics and reporting configuration guide for any enterprise platform — covering embedded reporting setup, dashboard design, KPI definitions, data source configuration, and sector-specific analytics requirements. Use in Realize phase. Works for any platform with embedded analytics, BI tool, or data warehouse.
superlabs: GIL (Global Industry Intelligence Lab)
architecture_streams: Data Architect, AI Architect
activate_phase: "4 - Realize"
version: "1.0"
---

# discover-analytics-config-guide

Produces an **Analytics and Reporting Configuration Guide** for any platform.

## Runtime parameters
| Parameter | Examples |
|---|---|
| `{{product}}` | Any platform |
| `{{analytics_tool}}` | Embedded / SAP Analytics Cloud / Power BI / Tableau / Looker / any |
| `{{module}}` | Any module |
| `{{industry}}` | Any GICS sector |
| `{{country}}` | ISO country or "global" |
| `{{report_consumers}}` | Executives, Managers, HR, Finance, Regulators, any |
| `{{deliverable_format}}` | Google Doc, Markdown |

## What to produce

### 1. Analytics architecture overview
- Analytics tool: `{{analytics_tool}}`
- Data sources (live connection vs. extract vs. semantic layer)
- Security model for analytics (row-level, role-based)
- Refresh frequency

### 2. KPI catalogue
| KPI ID | KPI Name | Definition | Formula | Data Source | Dimension | Frequency | Owner | `{{industry}}` Benchmark |
|---|---|---|---|---|---|---|---|---|

Generate minimum 20 KPIs for `{{module}}` and `{{industry}}` (e.g., headcount, turnover for HR; days payable for Finance; SLA compliance for ITSM).

### 3. Report catalogue
| Report ID | Report Name | Type (Operational/Strategic/Compliance) | Audience | Data Source | Filters | Frequency | `{{country}}`-specific |
|---|---|---|---|---|---|---|---|

Generate minimum 15 reports.

### 4. Dashboard design
| Dashboard | Audience | KPIs / Widgets | Refresh | Access Role |
|---|---|---|---|---|
| Executive Summary | CEO, CFO, CHRO | ... | Daily | Executive |
| Operational | Team managers | ... | Real-time | Manager |
| Compliance | Auditors, Regulators | ... | Monthly | Compliance |

### 5. Data source configuration
| Source ID | Source System | Connection Type | Credentials | Refresh Schedule | Data Volume |
|---|---|---|---|---|---|

### 6. `{{industry}}`-specific analytics
- Regulatory reporting requirements (e.g., EEO for US Industrials, gender pay gap for UK Financials, NERC compliance for Utilities)
- Sector benchmarks and industry KPIs

### 7. Analytics governance
- Report ownership and maintenance process
- Version control for calculated measures
- Data quality monitoring for analytics layer

## Format instructions
- Output as `{{deliverable_format}}`
- Footer: `v1.0 | discover-analytics-config-guide | SuccessLabs Academy`
