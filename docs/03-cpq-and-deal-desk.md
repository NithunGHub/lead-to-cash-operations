# 03 - CPQ and Deal Desk

CPQ (configure, price, quote) is where deal economics get set. The deal desk is the human function that keeps those economics sane. Together they protect margin without slowing deals to a crawl.

## Product catalog design

The catalog is the foundation. Get it wrong and every quote is custom.

- **SKUs that match how you sell and provision.** If provisioning needs to know the edition, the SKU must carry the edition.
- **Bundles for common motions**, à la carte for the rest. Too many bundles and reps cannot find anything; too few and every deal is bespoke.
- **Version control.** Price changes take effect on a date, apply to new quotes, and never silently rewrite in-flight quotes.
- **Retire ruthlessly.** Legacy SKUs with no new sales in 12 months get sunset paths, not permanent residence.

## Pricing and discount governance

| Element | Design |
|---------|--------|
| List price | Single source in the catalog; reps never type prices |
| Discount authority | Tiered by role: rep (e.g., up to 10%), manager (20%), deal desk / VP (beyond) |
| Approval chains | Triggered by discount %, non-standard terms, or product mix; parallel where possible, serial where judgment is needed |
| Guardrails | Floor prices, margin thresholds, and term-length minimums enforced by rules, not by memory |

Approvals should take hours, not days. If your approval chain is the bottleneck, simplify the chain before blaming the tool.

## Quote integrity

A quote is a promise the business must keep. Requirements:

1. **Generated from the catalog**, not assembled in a spreadsheet.
2. **Terms structured**, not free text: start/end dates, billing frequency, payment terms, auto-renewal as fields.
3. **Versioned.** Every customer-facing revision is a new version; the audit trail shows what changed and who approved it.
4. **Matches the contract.** The signed agreement and the final quote version agree on products, prices, and terms. Reconcile before booking.

## The deal desk

A small team (or a part-time function early on) that:

- Reviews non-standard deals for margin, risk, and precedent ("if we do this for them, we will do it for everyone").
- Owns the approval workflow and its SLA.
- Maintains the discount and terms playbook reps actually use.
- Reports on discount distribution, approval cycle time, and win rate by discount band.

Deal desk is not "the team that says no." It is the team that says "yes, and here is the structure that makes it work."

## Salesforce implementation notes

- Product and Price Book entries as the catalog; validation rules on discount thresholds.
- Approval processes or Flow-based approvals with clear entry criteria and delegation for PTO.
- Quote object with versioning; sync quote-to-opportunity for forecasting on quote amounts, not rep-typed amounts.
- Keep CPQ configuration in version control where possible; document every price rule's business intent, not just its logic.
