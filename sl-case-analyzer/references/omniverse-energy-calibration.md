# Worked calibration - GICS01 OmniVerse Energy Ltd. (fictional)

Source: Notion "GICS01. OmniVerse Energy Ltd. - Business Transformation Case Study" (GitHub-first narrative edition 2026-10-19 over preserved original research). Use as the reference pattern; re-read the live source before reuse.

## Case header
USD 85B revenue, 68,000 employees, 42 countries, founded 1978, HQ Mumbai and Houston. Segments: Upstream 35%, Refining/Petrochem 28%, Retail 18%, Power 12%, Renewables 7%. Assets: 8 refineries (2.1M bpd), 12,500 stations, 25,000 km pipeline, 15 GW power (60/40 thermal/renewable), 5 GW renewables operating + 2 GW in development.

## Source layers
1. Narrative edition (6 Acts, 16 fictional stakeholders, 12 simulations, 7 derived streams).
2. Original research (company profile, TOGAF Phases A-D, AI portfolio, zero trust, roadmap, business case, KPIs).
3. Section 14 alignment blueprint (7 workstreams).
4. Section 15 9P4V architecture (Vision/Value/Victory/Venture, 18-stage journey, 12-stream architecture, experiment gates, shock exercise).
5. SF EC foundation labs (Legal Entity -> BU -> Division -> Department -> Location), HR data model, Compensation sprint, 13 HR domain cases (HR01-HR12 + studio).

## Value streams (case's own)
Resource-to-Energy, Asset-to-Reliability, Customer-to-Service, Insight-to-Decision; 9P4V variants: Explore-to-Produce, Plan-to-Deliver, Asset-to-Outcome, Insight-to-Action.

## Core problems
Siloed BUs; 200+ apps with point-to-point integration; 15-year-old core; manual maintenance/trading; inconsistent data; OT/IT cyber exposure; reactive asset management (maturity L2); manual ESG (L1).

## Strategy options (case) and stated preference
A local lighthouse / B foundation first / C federated value-stream. Preference to test: **C**, gated by safety, investment and adoption evidence.

## Investment and value (all unvalidated)
USD 900M / 36 months (Tech 450, Data 180, Digital Experience 120, Cyber 85, Change 65). Annual benefit categories USD 635M (285+150+75+125); stated 3-yr NPV figures lack cash-flow and discount-rate evidence. Predictive maintenance USD 45M may sit inside efficiency/asset benefit - do not double count.

## KPIs (baseline -> Y3 target)
OEE 72->85; unplanned downtime 8->2; energy efficiency 89->95; process automation 15->75; NPS 35->65; digital adoption 25->85; digital services revenue 2->15; AI models 0->45; employee digital capability 35->90.

## Validation backlog (from case)
Roadmap years vs 2027 vision; net-zero 2050 / carbon-neutral 2030 boundaries; application rationalization counts (45+70+25+15 vs 200+ -> 85); NPV evidence; power vs renewable capacity nesting; automation/uptime/safety ambitions scope.

## Energy-specific constraints
Process safety and permit-to-work; OT/SCADA segmentation; NERC CIP-style obligations; rotating shifts and bargaining units; safety certifications (H2S, confined space, offshore); multi-country payroll; ESG assurance; remote/offline connectivity; human authority over AI actions.

## HR/EC boundary rules reusable in any sector
EC = system of record for person, employment, job, position, org. Payroll results, learning/certification, contractor, detailed medical, badge logs are separate sources. HR status alone never authorizes hazardous work; badge provisioning and safety clearance are separate controlled decisions.

## Example requirement cluster (Workforce, Energy)
- REQ-WRK-01 Org/foundation model (LE, BU, Division, Dept, Location, cost center) with consistent coding standard TYPE-COUNTRY-DETAIL and a common effective date.
- REQ-WRK-02 Position management with critical-position vacancy trigger.
- REQ-WRK-03 Identity provisioning to directory (e.g. Azure AD) on hire/transfer/termination with reconciliation.
- REQ-WRK-04 Credential/certification status ingested from approved source before site readiness.
- REQ-WRK-05 Compensation cycle: merit + bonus, eligibility, guidelines, budgets, workflow, statements, payroll handoff with reconciliation.
- REQ-INT-01 Versioned API/event contracts with retry, idempotency, reconciliation.
