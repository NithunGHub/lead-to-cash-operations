# 01 - Lead-to-Cash Overview

Lead-to-cash is the spine of a SaaS business: the connected process from first qualified opportunity to collected revenue. This doc maps the chain and names where it typically leaks.

## The stages

| Stage | Owner | System of record | Done means |
|-------|-------|-----------------|------------|
| Qualified opportunity | AE | CRM | Exit criteria met, next step dated |
| Quote | AE + Deal Desk | CPQ | Priced per catalog, approvals complete |
| Contract | Legal + AE | CLM / e-signature | Signed, terms match quote |
| Order | RevOps / Ops | CRM order object or ERP | Booked with products, dates, terms |
| Provisioning | Ops / Engineering | Provisioning system | Customer can use what they bought |
| Billing | Finance | Billing platform | Accurate invoice on schedule |
| Collections | Finance | Billing / AR | Cash collected, dunning on rails |
| Renewal / Expansion | CS / AM | CRM | Contracted before expiry, expansion quoted |

## Where value leaks

1. **Quote to contract drift.** Terms negotiated after the quote that never update the quote or the forecast. Fix: the signed contract regenerates the quote, or the quote is the contract (one-doc motion).
2. **Closed-won to order gap.** The opportunity says won; the order details are incomplete or wrong. Fix: required closed-won fields consumed by provisioning, validated before the stage can change.
3. **Provisioning lag.** Customer signed but cannot use the product for days. Fix: order-triggered provisioning with status visible to CS and the AE.
4. **Billing surprises.** First invoice does not match what sales promised. Fix: billing preview from the quote before signature; proration rules documented.
5. **Renewal ambush.** Nobody owns the renewal until 30 days out. Fix: renewal opportunities auto-created at 120/90 days with a named owner.

## Data contracts between stages

Each handoff passes a defined payload. Example: Opportunity → Order.

Required: account (matched, not text), products with quantities and SKU, start/end dates, billing frequency, payment terms, PO number if required, special terms as structured fields (not a notes blob).

If the receiving stage cannot do its job from the payload alone, the contract is incomplete. "Check with the rep" is not a data contract.

## Metrics across the chain

- Quote cycle time (opportunity qualified → quote sent)
- Approval cycle time and discount distribution (deal health)
- Order accuracy rate (orders provisioned without correction)
- Time-to-first-value (signature → customer live)
- Billing accuracy (invoices issued without credit/rebill)
- DSO and collection effectiveness
- Gross/net revenue retention

## Maturity

- Level 1: Quotes in spreadsheets, billing manual, renewals reactive.
- Level 2: CPQ-lite or templated quotes, defined handoffs, basic dunning.
- Level 3: Integrated quote-to-cash, deal desk, automated provisioning triggers, renewal motions.
- Level 4: Self-serve and sales-assisted on one catalog, usage-based billing handled natively, expansion motion instrumented.

Each doc in this repo goes one level deeper on its stage.
