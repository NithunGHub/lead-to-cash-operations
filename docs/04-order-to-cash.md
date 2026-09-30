# 04 - Order to Cash

From signed contract to collected revenue: order booking, provisioning, invoicing, and collections. The least glamorous part of lead-to-cash and the part customers actually feel.

## Order booking

The order is the operational truth of what was sold. Book it from the final quote/contract, not by retyping.

Required order payload: account (matched record), products/SKUs with quantities, start and end dates, billing frequency, payment terms, PO number where required, and structured special terms.

- **Booked, not "sent to ops."** There is a system status for booked; email is not a status.
- **Amendments are orders too.** Upgrades, downgrades, and co-terms create amendment orders linked to the original, preserving history.

## Provisioning

The customer should be able to use what they bought as fast as the product allows.

- Order status triggers provisioning automatically where possible; manual steps get an SLA and an owner.
- Provisioning status is visible to CS and the AE, not trapped in an ops queue.
- Partial provisioning (licenses now, services later) is explicit, with dates.
- Failed provisioning alerts before the customer notices.

Measure **time-to-first-value**: signature to customer live. It predicts retention better than most CS metrics.

## Invoicing

- Invoices generate from the order/billing schedule, not from memory.
- Proration rules are documented and consistent: mid-cycle adds, co-termed renewals, usage overages.
- The first invoice gets extra scrutiny; it is where sales promises meet billing reality.
- Credit and rebill needs a reason code and an approval; track the rate as a quality metric.

## Collections and dunning

- Payment terms are set at quote time and flow to the invoice. Renegotiating terms at collection time means the quote process failed.
- Automated dunning cadence: reminder before due, at due, then escalating touches. Human outreach before legal, always.
- Disputed invoices pause dunning and start a resolution SLA; "in dispute" is a status with an owner, not a parking lot.
- Track DSO and collection effectiveness by segment; enterprise and SMB need different playbooks.

## Revenue operations across the tail

- **Order accuracy rate:** orders provisioned and billed without correction. Below ~95% means the handoff contract is broken.
- **Billing accuracy:** invoices issued without credit/rebill.
- **Renewal readiness:** renewal opportunities created at 120/90 days with complete contract data; CS owns the motion, RevOps owns the data.
- **Expansion:** usage and entitlement data flowing back to the CRM so AEs and AMs see whitespace.

## Closing the loop

Lead-to-cash is a loop, not a line. Billing and usage data feed back into scoring (expansion signals), routing (existing-account detection), and forecasting (renewal pipeline). The companies that treat order-to-cash as "finance's problem" wonder why their funnel metrics never quite reconcile. It is one system.
