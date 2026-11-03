---
name: sl-solution-fitgap
description: Run a requirements-to-solution Fit-Gap for ANY product or solution (SAP such as SuccessFactors, S/4HANA, Ariba, BTP, Cloud ALM, or non-SAP such as Workday, Salesforce, ServiceNow, or custom) against requirements from a case analysis. Produces requirement catalog, Fit-Gap matrix, gap resolution options, clean-core/extension decisions and effort-risk view. Use after sl-case-analyzer or when the user supplies a product and requirements.
---

# SL Solution Fit-Gap

Product-agnostic. The product is an input; capability evidence comes from current vendor documentation, not memory.

## Inputs
- Requirements (REQ list from CAP, or user-supplied). If none, run `sl-case-analyzer` first.
- Product(s) and edition/scope (e.g. "SuccessFactors Employee Central + Compensation, 2H 2026 release").
- Constraints (sector profile), landscape (systems of record), deployment preferences.

## Procedure
1. **Scope the product.** List modules/components in scope and out of scope. For SAP, anchor on SAP Help Portal, SAP Signavio / Best Practices Explorer / Activate Roadmap Viewer, Cloud ALM; for others use vendor docs. Search the web when available; record source + release/date per capability claim. No source = `Unverified`.
2. **Normalize requirements.** One testable statement each; merge duplicates; attach process step and data object.
3. **Classify each requirement** (see scale). Judge against standard configuration of the stated release, not custom ideas.
4. **Decide the resolution path** for non-Fit items.
5. **Score** effort, risk, value and sequence.
6. **Check traceability** and produce outputs.

## Fit-Gap scale
| Code | Meaning | Typical path |
|---|---|---|
| F1 | Fit - standard, no setup beyond default | Use as is |
| F2 | Fit with configuration | Config; document in config workbook |
| F3 | Fit with in-app extensibility | Key-user extensibility / MDF / custom fields / rules |
| G1 | Gap - side-by-side extension | Extension on a platform (e.g. SAP BTP), API-based, loosely coupled |
| G2 | Gap - third-party / partner / other product | Buy or integrate; assess TCO and support |
| G3 | Gap - custom development | Last resort; needs sponsor approval and upgrade-safety plan |
| P | Process change | Adopt vendor/best-practice process; change plan |
| X | Out of scope / deferred | Record rationale and revisit date |
| U | Unverified | Needs vendor confirmation or proof of concept |

## Resolution rules
- **Clean core first (SAP):** prefer standard, then in-app, then side-by-side; touch core only with explicit approval. Non-SAP: prefer vendor-supported configuration/extension frameworks.
- **Process before configuration:** challenge whether the requirement is a policy habit before building around it.
- **Safety/regulatory requirements cannot be marked X** without owner sign-off; they may need G1/G2 even at high cost.
- **System-of-record test:** if the product would hold data it should not own (e.g. medical, hazardous-work authorization), classify as integration, not capability.
- **Integration requirements** include direction, trigger, payload owner, error handling, reconciliation, support owner.
- **Data requirements** state migration source, cleansing, ownership.

## Scoring (1-5)
Effort (E), Risk (R), Business value (V), Dependency readiness (D). Priority score = V x (6-R) adjusted by D; rank, but do not pretend precision. Effort bands (S/M/L/XL) are estimates with stated basis - never quote days without a basis.

## Output (Sheet + short Doc)
Workbook tabs: `Summary`, `Requirements`, `FitGap` (REQ ID, requirement, process step, product capability, source/release, code, resolution, owner, E/R/V/D, test ref, Activate phase), `Gaps`, `Integrations`, `Data`, `Decisions`, `Open Questions`.
Summary shows counts by code, % fit, top 10 gaps, top risks, decisions needed. Include an **Option view** when comparing products: same REQ IDs across columns.

## Checks before delivering
- Every row has a source trace to CAP and a capability source or `Unverified`.
- Gap rows have at least two resolution options with trade-off.
- No requirement duplicated across rows; integrations and data not buried inside functional rows.
- Counts reconcile to total requirements.

See `references/fitgap-templates.md` and, for SAP SuccessFactors/EC use, `references/sap-hcm-fitgap-patterns.md`.
