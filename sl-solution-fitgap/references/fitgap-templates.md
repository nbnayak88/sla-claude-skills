# Fit-Gap templates

## Row template
| Field | Notes |
|---|---|
| REQ ID | From CAP |
| Requirement | One testable sentence |
| Process / data object | e.g. Hire-to-Retire / Position |
| Product | Name + module + release |
| Capability evidence | Doc title + link + date or `Unverified` |
| Code | F1 F2 F3 G1 G2 G3 P X U |
| Resolution | Config / extension / partner / process change / defer |
| Option B | Alternative with trade-off (required for G rows) |
| E R V D | 1-5 each |
| Owner | Business + IT |
| Test ref | Test scenario ID |
| Activate phase | Explore fit-to-standard session / Realize sprint |
| Decision status | Proposed / Agreed / Rejected |

## Gap decision record
Context - Requirement(s) - Options - Choice - Rationale - Cost/TCO estimate (basis) - Upgrade/clean-core impact - Risk - Owner - Review date - Reversal criteria.

## Multi-product comparison
Rows = REQ IDs; columns = products; cell = code + 1-line note. Add totals per product by code and weighted score by priority (Must x3, Should x2, Could x1). Report must-have gaps separately; a product with an unresolved Must gap cannot "win" on score alone.

## Fit-to-standard session agenda (SAP Activate Explore)
1. Scope and process hierarchy. 2. Demo standard process on a prepared tenant. 3. Capture deltas live as REQ updates. 4. Classify and assign owners. 5. Agree gap resolution candidates. 6. Sign-off on fit-to-standard results.
