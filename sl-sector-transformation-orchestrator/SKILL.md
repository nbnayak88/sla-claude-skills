---
name: sl-sector-transformation-orchestrator
description: Master workflow for SuccessLabs sector transformation work. Use when given a case study (e.g. GICS01 OmniVerse Energy) or a client scenario plus ANY product or solution (SAP or non-SAP) and asked to analyze it, run a Fit-Gap, and plan implementation with SAP Activate. Works for all 11 GICS sectors. Routes to sl-case-analyzer, sl-gics-sector-profiles, sl-solution-fitgap and sl-activate-implementation.
---

# SL Sector Transformation Orchestrator

One pipeline: **Analyze case → Frame solution → Fit-Gap → SAP Activate plan → Deliverables.**
The pipeline is sector-agnostic. Sector knowledge comes from `sl-gics-sector-profiles`; the product is a *parameter*, never hard-coded.

## Hard boundaries
- **Never edit or overwrite the SuccessLabs SAP Activate ECP Payroll Skill Catalog** (`SuccessLabs_SAP_Activate_Skill_Catalog_v1.xlsx`, IDs like `DISC-GOV-01`). It is a read-only reference for phase structure and naming style.
- New artifacts use their own ID prefix: `SL-<PHASE>-<TYPE>-<SEQ>` (see `sl-activate-implementation`).
- Case facts are fictional learning inputs unless the user says it is a real client. Do not import outside facts into a case silently.
- Do not name Josh Bersin / JBA in learner-facing outputs. Attribution line: **"Approved By: SuccessLabs Academy Board Members"**.

## Inputs to collect (ask at most one question, only if truly missing)
| Parameter | Example | Default |
|---|---|---|
| Case source | Notion/GitHub URL, pasted text, attached file | required |
| Sector | GICS01 Energy ... GICS11 Real Estate | infer from case; else ask |
| Product / solution | SuccessFactors EC, S/4HANA, Ariba, Salesforce, Workday, ServiceNow, custom build | required for Fit-Gap |
| Mode | `learning-case` or `client-engagement` | learning-case |
| Scope | enterprise, one value stream, one domain (HR01...) | infer |
| Output format | per user; else Doc + Sheet | Docs/Sheets artifacts; Slides on request |

If the product is missing, run Step 1 only and stop with a proposed shortlist of candidate solutions per capability gap.

## Pipeline
1. **Analyze** — run `sl-case-analyzer`. Output: Case Analysis Pack (CAP). Gate: evidence tags + validation backlog present.
2. **Sector calibrate** — load `sl-gics-sector-profiles` for the sector (Energy has a worked calibration from OmniVerse). For sectors without a calibrated case, use the profile's research-first rule.
3. **Fit-Gap** — run `sl-solution-fitgap` with CAP requirements + the named product. Output: Requirements catalog, Fit-Gap matrix, resolution plan, clean-core / extension decisions.
4. **Implement with SAP Activate** — run `sl-activate-implementation`. Output: phase plan, deliverables, quality gates, RAID, test/cutover/change plans, 90-day Wave 0.
5. **Package** — executive brief (1-2 pages) + Fit-Gap workbook + Activate roadmap. Final check: every Fit-Gap row traces to a CAP requirement and a case source; every Activate deliverable traces to a Fit-Gap decision.

## Mode behavior
- **learning-case:** include learner prompts, rubric hooks, 9P4V mapping where the case supplies it.
- **client-engagement:** drop learner scaffolding; add commercial assumptions, effort ranges flagged as estimates, and a decision log for the steering committee.

## Multi-sector / multi-product
Same engine, new parameters. Keep outputs sector-labeled (`GICS0X-<Company>-<Product>-<Artifact>`). Reuse requirement IDs across products so Fit-Gap results can be compared.

## Quality bar
- Facts vs assumptions are tagged; forecasts never presented as achieved results.
- Safety / regulatory / security constraints from the sector profile appear explicitly in requirements.
- Effort, cost and timeline numbers are labeled **estimate** with basis. No invented vendor facts: verify product capability against current vendor documentation (use web search when available) and mark unverified items `Unverified`.
