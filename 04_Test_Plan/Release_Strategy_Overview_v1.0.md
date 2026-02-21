# Release Strategy Overview (v1.0)
## Healthcare eCommerce Simulation Platform (ECSP)

## Release Model (2016–2018 style)
- Agile feature delivery in 2-week sprints
- Release candidate created after Sprint 2 and Sprint 4
- Mandatory regression + integration validation before production release
- Release sign-off based on risk, defect trend, and traceability coverage

## Sprint-to-Release Plan
- Sprint 1: Product Catalog foundation
- Sprint 2: Customer + Authentication → Release Candidate 1 (RC1)
- Sprint 3: Cart & Checkout
- Sprint 4: Payment + OMS/WMS/ERP touchpoints → Release Candidate 2 (RC2)
- Sprint 5: Returns/Refunds + Stabilization → Production Release readiness

## Regression Strategy
- Smoke suite for every build (critical user journeys)
- Regression for every Release Candidate (RC)
- Priority order for regression:
  1) Checkout + Payment
  2) Order lifecycle (OMS)
  3) Inventory sync (WMS)
  4) ERP batch reconciliation
  5) Returns/Refunds

## Integration Validation (must-pass)
- Payment authorization success/fail paths
- OMS status transitions and audit trail
- WMS stock deduction + reconciliation mismatch handling
- ERP end-of-day posting + refund reconciliation

## UI Wireframes (Key Screens)
See: ../08_UI_Mockups/ECSP_Key_UI_Wireframes_v1.0.pdf
