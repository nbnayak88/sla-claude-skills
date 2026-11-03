# SuccessLabs Academy — Claude Skill Catalog v1.0

> **Product-agnostic • Industry-agnostic • Country-agnostic**
>
> 34 skills mapped to SAP Activate 6 phases, 20 SuperLabs, and 12 Architecture Streams.
> Every skill accepts runtime parameters: `{{product}}`, `{{module}}`, `{{industry}}`, `{{sector}}`, `{{country}}`, `{{org_size}}`, `{{phase}}`, `{{deliverable_format}}`.

---

## Catalog Overview

| Dimension | Coverage |
|---|---|
| SAP Activate Phases | 6 (Discover → Prepare → Explore → Realize → Deploy → Run) |
| Total Skills | 34 |
| Architecture Streams mapped | 12 |
| GICS Sectors supported | 11 (all) |
| SuperLabs mapped | 20 |
| Supported Products | Any — SAP SF, S/4HANA, Workday, Oracle Fusion, Salesforce, ServiceNow, custom |

---

## Phase 1 — Discover (4 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `discover-scope-document` | Implementation scope statement and phasing roadmap | PIL | Enterprise, Business |
| `discover-business-case` | Business case with ROI, compliance drivers, risk of inaction | PIL | Business, Domain |
| `discover-solution-vision` | To-be architecture, integration landscape, design principles | SAL | Enterprise, Application |
| `discover-ocm-briefing` | OCM approach document and stakeholder briefing | ECL | Business, Domain |

---

## Phase 2 — Prepare (5 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `build-project-charter` | Full project charter with RACI, governance, quality gates | IIL | Enterprise |
| `lead-stakeholder-plan` | Stakeholder map and communications calendar | PML | Business |
| `move-data-migration-approach` | Data migration approach and workshop schedule | MEL | Data |
| `build-project-plan` | 60+ task master project plan across all 6 phases | IIL | Enterprise |
| `validate-system-readiness` | System and environment readiness checklist | QAL | Infrastructure, Security |

---

## Phase 3 — Explore (8 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `discover-fit-gap-analysis` | Fit-to-Standard / Fit-Gap analysis with prioritised backlog | PIL | Application, Domain |
| `design-solution-document` | Solution design document with process flows and config design | SAL | Application, Domain |
| `design-master-data-blueprint` | Org and master data foundation blueprint | SAL | Data, Enterprise |
| `design-data-model` | Data model design with entity catalogue and regulatory mapping | SAL | Data |
| `design-business-rules-catalog` | Statutory, computation, workflow, and validation rules | SAL | Application, Domain |
| `design-access-matrix` | RBAC/ABAC permission matrix with SoD controls | SAL | Security |
| `connect-integration-design` | Integration design document and interface catalogue | IEL | Integration |
| `validate-test-strategy` | Test strategy and master test plan (all test types) | QAL | Application |

---

## Phase 4 — Realize (10 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `build-config-log` | Configuration log tracking status across environments | IIL | Application |
| `build-config-workbook` | Full configuration workbook (10 tabs) | IIL | Application, Domain |
| `build-workflow-rules-document` | Workflow, approval, notification, and automation rules | IIL | Application |
| `lead-change-impact-analysis` | Change impact analysis and workshop facilitation guide | PML | Business |
| `move-data-migration-strategy` | Data migration strategy + pre-built migration templates | MEL | Data |
| `validate-test-script-pack` | 40+ test scripts (happy path, negative, integration, statutory) | QAL | Application |
| `connect-integration-checklist` | Integration setup and go-live readiness checklist | IEL | Integration |
| `design-access-governance` | Provisioning design, SoD controls, access review process | SAL | Security |
| `discover-analytics-config-guide` | Analytics and reporting configuration guide | GIL | Data, AI |
| *(existing)* `sl-solution-fitgap` | Solution fit-gap — existing skill | — | Application |

---

## Phase 5 — Deploy (4 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `build-cutover-plan` | Detailed cutover plan with 50+ tasks and go/no-go criteria | IIL | Enterprise |
| `lead-training-plan` | Go-live OCM and end-user training plan | PML | Business, UI/UX |
| `validate-golive-readiness` | Go-live readiness checklist with RAG status | QAL | Enterprise |
| `support-hypercare-handover` | Hypercare and operations handover document | AMS | Domain, Infrastructure |

---

## Phase 6 — Run (4 skills)

| Skill Folder | Description | SuperLab | Architecture Streams |
|---|---|---|---|
| `support-run-plan` | Steady-state support plan, release cadence, adoption KPIs | AMS | Infrastructure, Domain |
| `support-ams-audit-analyzer` | AMS audit checklist analyzer — reads file, produces gap report | AMS | Domain, Industry |
| `document-solution-config-guide` | Permanent solution configuration reference guide | KAL | Application, Industry |
| `scale-learning-curriculum` | Learning curriculum by role and phase for any platform | SCALE | Domain |

---

## Existing Skills (kept as-is)

| Skill Folder | Description |
|---|---|
| `sl-activate-implementation` | End-to-end SAP Activate implementation orchestrator |
| `sl-case-analyzer` | SAP case / support ticket analyzer |
| `sl-gics-sector-profiles` | 11 GICS sector profiles for industry-specific delivery |
| `sl-sector-transformation-orchestrator` | Sector transformation orchestration skill |
| `sl-solution-fitgap` | Solution fit-gap analysis (original) |

---

## 12 Architecture Streams Coverage

| Stream | Skills Mapped |
|---|---|
| Enterprise Architect | `discover-scope-document`, `discover-solution-vision`, `design-master-data-blueprint`, `build-project-charter`, `build-project-plan`, `build-cutover-plan`, `validate-golive-readiness` |
| Business Architect | `discover-scope-document`, `discover-business-case`, `discover-ocm-briefing`, `lead-stakeholder-plan`, `lead-change-impact-analysis`, `lead-training-plan` |
| Data Architect | `move-data-migration-approach`, `design-master-data-blueprint`, `design-data-model`, `move-data-migration-strategy`, `discover-analytics-config-guide` |
| Application Architect | `discover-solution-vision`, `discover-fit-gap-analysis`, `design-solution-document`, `design-business-rules-catalog`, `validate-test-strategy`, `build-config-log`, `build-config-workbook`, `build-workflow-rules-document`, `validate-test-script-pack`, `document-solution-config-guide` |
| Integration Architect | `connect-integration-design`, `connect-integration-checklist` |
| Security Architect | `validate-system-readiness`, `design-access-matrix`, `design-access-governance` |
| Infrastructure Architect | `validate-system-readiness`, `support-hypercare-handover`, `support-run-plan` |
| AI Architect | `discover-analytics-config-guide` |
| UI/UX Architect | `lead-training-plan` |
| Domain Architect | `discover-business-case`, `discover-fit-gap-analysis`, `design-solution-document`, `design-business-rules-catalog`, `support-hypercare-handover`, `support-run-plan`, `support-ams-audit-analyzer`, `document-solution-config-guide`, `scale-learning-curriculum` |
| Industry Architect | `support-ams-audit-analyzer`, `document-solution-config-guide` |
| Technology Architect | *(leveraged across integration and infrastructure skills)* |

---

## SuperLabs Key

| Abbreviation | Full Lab Name |
|---|---|
| PIL | Product Innovation Lab |
| SAL | Strategy & Architecture Lab |
| IIL | Implementation Intelligence Lab |
| PML | Project Performance Lab |
| MEL | Migration Modernization Lab |
| QAL | Quality Assurance Lab |
| IEL | Integration Intelligence Lab |
| ECL | Experts Engagement Lab |
| GIL | Global Industry Intelligence Lab |
| AMS | Application Management Services Lab |
| KAL | Knowledge Keystone Lab |
| SCALE | School of Career Acceleration Lab for Excellence |

---

## Runtime Parameters (all skills accept these)

| Parameter | Description | Examples |
|---|---|---|
| `{{product}}` | Target platform | SAP SuccessFactors, S/4HANA, Workday HCM, Oracle Fusion, Salesforce, ServiceNow, custom |
| `{{module}}` | Module or process area | Employee Central, Payroll, Finance GL, Procurement, ITSM |
| `{{industry}}` | GICS industry sector | Energy, Financials, Health Care, Consumer Discretionary, Industrials |
| `{{sector}}` | GICS sector code | 1010, 4020, 3510 |
| `{{country}}` | ISO country code or region | US, UK, DE, AU, IN, SG, global |
| `{{org_size}}` | Organisation size | 500, 5000, 50000 employees |
| `{{phase}}` | Activate phase | 1 Discover, 2 Prepare, 3 Explore, 4 Realize, 5 Deploy, 6 Run |
| `{{deliverable_format}}` | Output format | Google Doc, Google Sheet, Google Slides, Markdown, Word, Excel |

---

*v1.0 | SuccessLabs Academy | SAP Activate Skill Catalog*
*Published: 2026-11-03*
