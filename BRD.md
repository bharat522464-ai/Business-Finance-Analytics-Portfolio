# Business Requirements Document: Lakeside Supply Co. Odoo Implementation

> Fictional portfolio project. Version 1.0.

## 1. Purpose

Replace QuickBooks Desktop and spreadsheets with Odoo for Sales, Purchasing, Inventory, and Accounting, so that every team works from one system and month-end close drops from 9 to 5 working days.

## 2. Scope

| In scope | Out of scope (phase 2) |
|---|---|
| Sales quotations and orders | eCommerce website |
| Purchase orders and approvals | Manufacturing |
| Inventory: receipts, deliveries, stock counts | Payroll |
| Accounting: GL, AP, AR, bank reconciliation, month-end close | CRM pipeline |
| Data migration: customers, vendors, products, open balances | Historical transactions older than 2 years |

## 3. Stakeholders

| Role | Interest | Interview focus |
|---|---|---|
| Owner / CEO | Growth, visibility | Reporting needs, success measures |
| Controller | Accurate books, faster close | Close steps, reconciliations, approvals |
| Purchasing lead | Fewer stockouts | PO process, vendor terms, reorder rules |
| Warehouse lead | Accurate stock | Receiving, picking, counts |
| Sales team (4) | Promise dates they can keep | Stock visibility, quoting |

## 4. Current-state pain points

1. Inventory lives in Excel, so book and physical stock differ by about 6% at month-end.
2. Purchase orders have no approval; spend is seen only at invoice.
3. Vendor invoices are matched to receipts by hand, causing duplicate payments twice last year.
4. Sales cannot see stock, so about 1 in 12 orders ships late.
5. Month-end close takes 9 working days.

## 5. Business requirements

| ID | Requirement | Priority |
|---|---|---|
| BR-01 | Sales staff can see on-hand and forecasted stock when quoting | Must |
| BR-02 | Purchase orders over $5,000 need controller approval | Must |
| BR-03 | Vendor bills are matched to the PO and receipt before payment (3-way match) | Must |
| BR-04 | Stock moves post to the general ledger automatically (perpetual inventory) | Must |
| BR-05 | Reorder rules create draft purchase orders when stock falls below a minimum | Should |
| BR-06 | Bank feeds import daily and reconcile against open invoices | Must |
| BR-07 | Month-end checklist tracks close tasks and owners | Should |
| BR-08 | Customer credit limits block new orders when exceeded | Should |
| BR-09 | Budget vs. actual report by department | Should |
| BR-10 | Cycle counts by product category without a full warehouse shutdown | Could |

Full list of 24 requirements with fit-gap results: [fit_gap_analysis.xlsx](fit_gap_analysis.xlsx).

## 6. Success measures

| Measure | Today | Target (6 months after go-live) |
|---|---|---|
| Month-end close | 9 working days | 5 working days |
| Book vs. physical inventory difference | ~6% | under 1% |
| Late shipments | ~8% of orders | under 3% |
| Duplicate vendor payments | 2 per year | 0 |

## 7. Assumptions and risks

- **Data quality:** product and vendor lists contain duplicates and must be cleaned before migration.
- **Adoption:** warehouse staff are used to paper; training and quick-reference guides are critical.
- **Customization:** staying with standard Odoo features keeps upgrades simple; every gap is challenged before building anything custom.
