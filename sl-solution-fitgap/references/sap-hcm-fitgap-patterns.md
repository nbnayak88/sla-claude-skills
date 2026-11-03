# SAP HCM (SuccessFactors) Fit-Gap patterns

Starting patterns only - confirm against the current release on SAP Help Portal before classifying.

| Requirement pattern | Likely class | Notes |
|---|---|---|
| Legal entity / BU / division / department / location / cost center hierarchy | F2 | Foundation Objects; agree coding standard and effective date up front |
| Position management with vacancy trigger | F2/F3 | Rules and workflows; confirm mass-change and position-to-job sync design |
| Country-specific fields and rules | F2/F3 | Country-specific data models; localization per country |
| Custom fields/objects | F3 | Configuration, MDF; watch object and field limits |
| Workflow approvals and role-based permissions | F2 | RBP design, separation of duties tests |
| Identity provisioning to directory (e.g. Azure AD) | F2/G1 | Standard integration + IAM; reconcile joiner/mover/leaver |
| Credentials / certifications gating work readiness | G1/G2 | Source system owner decision; HR status alone must not authorize hazardous work |
| Shift rosters, rotating schedules, overtime rules | F2/G2 | Time tracking vs workforce scheduling; check both before assuming |
| Compensation merit + bonus cycle | F2 | Eligibility, guidelines, budgets, worksheets, workflow, statements, payroll handoff |
| Payroll in the cloud (ECP) with multi-country | F2/G2 | Country payroll availability and partner coverage differ; validate per country |
| Badge/physical access | G1/G2 | Integration; separate from safety clearance |
| People analytics | F2/G1 | Native reporting vs analytics platform; data-privacy governance |
| Contractor / contingent workforce | F2/G2 | Often separate system of record |

Always add: data migration (cleansing, mapping, loads), integration inventory (SAP Integration Suite or alternative), test scripts per REQ, cutover rehearsal.
