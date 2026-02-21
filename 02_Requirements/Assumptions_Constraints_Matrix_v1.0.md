# Assumptions & Constraints Matrix (v1.0)

## Assumptions
| ID | Assumption | Impact if Wrong | QA Mitigation |
|---|---|---|---|
| A-01 | Payment gateway is external (sandbox) | Unstable responses | Test retries, failure-path coverage |
| A-02 | ERP posting runs end-of-day batch | Financial status delays | Validate batch outputs + exception handling |
| A-03 | Inventory sync is near real-time | Stock drift/oversell risk | Reconciliation tests + mismatch alerts |
| A-04 | 2-week sprints with regression gates | Scope spillover | Carry-forward tracking + regression checklist |
| A-05 | RBAC enforced for admin actions | Unauthorized access | Access control test suite |

## Constraints
| ID | Constraint | Risk | QA Approach |
|---|---|---|---|
| C-01 | Cross-system dependencies (OMS/WMS/ERP) | Blocking testing | Mock data + staged integration testing |
| C-02 | Release windows tied to finance cycles | Tight timelines | Risk-based regression prioritization |
| C-03 | Sandbox limits for payment | False negatives | Test data rotation + controlled reruns |
| C-04 | Batch failures possible | Data inconsistency | Exception logs + reconciliation reports |
