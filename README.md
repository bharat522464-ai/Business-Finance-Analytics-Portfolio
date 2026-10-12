ERP Implementation Case Study: Odoo for a Wholesale Distributor

> **Portfolio project.** Lakeside Supply Co. is a fictional company, created to practice the full business analysis cycle of an ERP implementation. All names and figures are illustrative.

## The business problem

Lakeside Supply Co. is a 45-person wholesale distributor of janitorial and packaging supplies. It runs on QuickBooks Desktop plus spreadsheets:

- Inventory is tracked in Excel, so stock counts drift from the books and month-end inventory adjustments are large.
- Purchase orders are emailed as PDFs with no approval step; the controller sees spend only when invoices arrive.
- Month-end close takes **9 working days**, mostly spent reconciling inventory and chasing missing invoices.
- Sales staff cannot see stock levels, so they promise orders that cannot ship.

**Goal:** move Sales, Purchasing, Inventory, and Accounting onto Odoo, cut close to 5 days, and give every team one source of truth.

## My approach

| Phase | What I did | Deliverable |
|---|---|---|
| 1. Discovery | Planned stakeholder interviews with the controller, warehouse lead, purchasing, and sales; listed pain points | [Business Requirements Document](BRD.md) |
| 2. Current state | Mapped how orders, purchases, and close work today | [Process maps](process_maps.md) |
| 3. Fit-gap | Compared 24 requirements to standard Odoo features: fit, configure, or gap | [fit_gap_analysis.xlsx](fit_gap_analysis.xlsx) |
| 4. Future state | Designed the to-be process using standard Odoo flows | [Process maps](process_maps.md) |
| 5. Testing | Wrote UAT test cases for each critical flow, with expected results | [uat_test_cases.xlsx](uat_test_cases.xlsx) |
| 6. Enablement | Wrote a step-by-step guide so users can work on their own | [User training guide](training_guide.md) |

## Key findings

- **20 of 24 requirements (83%)** are met by standard Odoo or configuration alone; only 4 need workarounds or add-ons. Staying close to standard keeps cost and upgrade risk low.
- The biggest win is **real-time inventory valuation** (perpetual, automated): stock moves post to the general ledger automatically, removing the manual month-end inventory adjustment.
- A **purchase approval rule** above $5,000 gives the controller visibility before money is committed.

## Skills demonstrated

Requirements gathering · stakeholder interviews · current-state and future-state process mapping · fit-gap analysis · ERP configuration planning (Accounting, Inventory, Purchase, Sales) · user acceptance testing (UAT) · user training and documentation · accounting processes (GL, AP, AR, inventory valuation, month-end close)

## Tools

Odoo (free trial) · Microsoft Excel · Markdown and Mermaid for process diagrams
