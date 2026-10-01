# Order Data Contract Checklist

The order is the operational truth of what was sold. Use this checklist before an order can be marked booked. Every unchecked box is a future provisioning failure, billing dispute, or renewal surprise.

## Account and contacts

- [ ] Account is a matched CRM record, not free text
- [ ] Billing contact named with verified email
- [ ] Technical / provisioning contact named (if different)

## Products and pricing

- [ ] Every line item is a catalog SKU (no typed-in product names)
- [ ] Quantities and unit prices match the final signed quote version
- [ ] Discounts match approved discount levels
- [ ] One-time vs. recurring correctly classified per line

## Dates and terms

- [ ] Subscription start and end dates present and logical
- [ ] Billing frequency set (monthly / quarterly / annual / upfront)
- [ ] Payment terms set (e.g., Net 30) and match the quote
- [ ] Auto-renewal flag set per policy
- [ ] PO number present where the customer requires one

## Special terms (structured fields, not a notes blob)

- [ ] Service-level commitments recorded
- [ ] Implementation / onboarding scope attached
- [ ] Price holds or caps documented with expiry
- [ ] Termination and data-export terms confirmed

## Amendments

- [ ] Linked to the original order (upgrade / downgrade / co-term)
- [ ] Proration calculated per documented rules
- [ ] Prior entitlements correctly superseded, not duplicated

## Handoff readiness

- [ ] Provisioning system can fulfill from this payload alone (no "check with the rep")
- [ ] Billing system can invoice from this payload alone
- [ ] CS can see what was sold, when it starts, and who to onboard

## Sign-off

| Role | Name | Date |
|------|------|------|
| Order booked by | | |
| Reviewed by (RevOps / Deal Desk) | | |

Amendments use the same checklist. "It is just a small change" is how billing disputes are born.
