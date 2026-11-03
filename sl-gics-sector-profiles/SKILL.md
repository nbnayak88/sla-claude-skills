---
name: sl-gics-sector-profiles
description: Reference profiles for the 11 GICS sectors (Energy, Materials, Industrials, Consumer Discretionary, Consumer Staples, Health Care, Financials, Information Technology, Communication Services, Utilities, Real Estate) - value chains, regulatory and safety constraints, workforce patterns, typical data domains, KPIs and solution footprints. Use when calibrating a case analysis, Fit-Gap or implementation plan to a sector, or when starting a sector with no calibrated case yet.
---

# SL GICS Sector Profiles

Calibration layer for the SuccessLabs pipeline. Energy is the calibrated reference (OmniVerse). Other sectors give a **starting hypothesis set** - confirm against the case and current sources before relying on them.

## How to use
1. Identify sector from the case (GICS numbering used by SuccessLabs: 01 Energy, 02 Materials, 03 Industrials, 04 Consumer Discretionary, 05 Consumer Staples, 06 Health Care, 07 Financials, 08 Information Technology, 09 Communication Services, 10 Utilities, 11 Real Estate).
2. Load `references/sector-profiles.md` for that sector.
3. Add profile items to the CAP as `Insight` (not Fact) unless the case states them.
4. For regulation, thresholds, vendor facts: verify with current sources; mark unverified.
5. Mixed-sector companies (e.g. integrated energy + utilities + retail): profile the dominant segment, then overlay others per segment share.

## Profile fields
Value chain - Constraints (safety, regulatory, security) - Workforce pattern - Critical data domains - Typical KPIs - Solution footprint families - Fit-Gap hot spots - Implementation risks.

## Rules
- A profile never overrides case facts.
- Constraints become explicit requirements (compliance/safety type) with an owner.
- Solution footprint lists are *families* (ERP, EAM, HCM, CX, GRC, analytics...), not endorsements; the user supplies the actual product for Fit-Gap.
