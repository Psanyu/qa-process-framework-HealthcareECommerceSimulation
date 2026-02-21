# Non-Functional Requirements (NFR) (v1.0)

## Performance
- NFR-P01: Product listing loads within 3 seconds under normal load
- NFR-P02: Checkout completes within 5 seconds excluding payment authorization delay

## Reliability & Recovery
- NFR-R01: No duplicate orders on payment retry
- NFR-R02: OMS/WMS/ERP failures are logged and retried or flagged for manual review

## Security
- NFR-S01: RBAC enforced for all admin endpoints
- NFR-S02: Account lockout after 5 failed login attempts
- NFR-S03: Sensitive fields masked in logs (simulation)

## Data Integrity
- NFR-D01: Order totals consistent across UI/OMS/ERP postings
- NFR-D02: Inventory never drops below zero; mismatch triggers alert/report

## Auditability
- NFR-A01: Transaction IDs traceable across Storefront → OMS → WMS → ERP (simulated)
- NFR-A02: All status transitions recorded with timestamp and actor
