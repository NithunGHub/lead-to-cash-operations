# 05 - Quote-to-Cash RACI

Who does what across the revenue chain. R = responsible (does the work), A = accountable (one throat to choke), C = consulted, I = informed.

## The matrix

| Stage | AE | Deal Desk | Legal | RevOps | Finance | CS / AM |
|-------|----|-----------|-------|--------|---------|---------|
| Qualification → quote request | R/A | C | - | I | - | - |
| Quote build (catalog pricing) | R | C | - | A (rules) | - | - |
| Discount / terms approval | R | A | C | C | I | - |
| Contract redlines | C | C | R/A | I | - | - |
| Order booking | I | C | - | R/A | I | I |
| Provisioning | I | - | - | A | - | R (validate) |
| Invoicing | I | - | - | C | R/A | I |
| Collections | I | - | - | I | R/A | C (at-risk accounts) |
| Renewal (120/90/60/30) | I | C | C | A (data) | I | R/A |

## Reading it

- **Exactly one A per row.** Two accountables means zero accountables.
- **RevOps is A for the rules, not the deals.** RevOps owns discount policy, approval workflow, and data contracts; the deal desk and AEs work inside them.
- **Finance is A for invoice correctness and collection**, but the quote is where payment terms get set. Terms renegotiated at collection time mean the quote process failed.
- **CS owns renewal motion; RevOps owns renewal data.** The renewal opportunity, contract terms, and usage data must exist before CS can act.

## Common RACI failures

- Deal desk approving deals with no published policy (approvals become vibes).
- Nobody A for provisioning status visibility (customer signed, nobody knows if they are live).
- Legal as bottleneck on standard terms (fix with pre-approved clause library, not more lawyers).
- Handoffs with no RACI at all: closed-won to order, order to provisioning. These are the rows most teams never write down, and exactly where deals stall.
