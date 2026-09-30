# Lead-to-Cash Operations

How revenue actually happens: from a qualified opportunity through quoting, contracting, order, provisioning, billing, and collection. The full lead-to-cash chain, with the handoffs, controls, and system design that keep it from breaking.

This repo is the downstream companion to [go-to-market-architecture](https://github.com/NithunGHub/go-to-market-architecture) and [top-of-funnel-architecture](https://github.com/NithunGHub/top-of-funnel-architecture): once pipeline exists, this is how it becomes cash.

## Who this is for

- RevOps / Deal Desk / Billing Ops practitioners
- Salesforce architects designing CPQ, order, and billing flows
- Operators inheriting a quote-to-cash process held together by spreadsheets

## Contents

| Doc | What it covers |
|-----|---------------|
| [01 - Lead-to-Cash Overview](docs/01-lead-to-cash-overview.md) | The end-to-end chain, handoffs, and where value leaks |
| [02 - Lead to Quote](docs/02-lead-to-quote.md) | Opportunity stages, exit criteria, and qualification rigor |
| [03 - CPQ and Deal Desk](docs/03-cpq-and-deal-desk.md) | Product catalog, pricing, approvals, and quote integrity |
| [04 - Order to Cash](docs/04-order-to-cash.md) | Order, provisioning, invoicing, collections, and revenue operations |

## The chain

```
Qualified Opportunity → Quote (CPQ) → Contract → Order →
Provisioning → Billing → Collections → Renewal / Expansion
```

Every arrow is a handoff. Every handoff needs an owner, a data contract, and a fallback. Most lead-to-cash problems are handoff problems wearing a systems costume.
