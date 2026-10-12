# Process Maps: Procure-to-Pay, Current State vs. Future State

> Fictional portfolio project. Diagrams use Mermaid, which GitHub renders automatically.

## Current state: purchasing in QuickBooks + email

```mermaid
flowchart LR
    A[Warehouse notices low stock] --> B[Purchasing emails PDF PO to vendor]
    B --> C[Goods arrive]
    C --> D[Warehouse updates Excel stock sheet]
    C --> E[Vendor invoice arrives by email]
    E --> F[Controller searches email for PO]
    F --> G{PO and receipt match?}
    G -- No --> H[Chase warehouse and vendor]
    H --> F
    G -- Yes --> I[Enter bill in QuickBooks]
    I --> J[Pay vendor]
    D --> K[Month-end: manual inventory adjustment]
```

**Pain points:** no approval before spend · stock updated in a separate file · invoice matching done by hand · inventory adjusted manually at close.

## Future state: purchasing in Odoo

```mermaid
flowchart LR
    A[Reorder rule creates draft PO] --> B{PO over $5,000?}
    B -- Yes --> C[Controller approves in Odoo]
    B -- No --> D[Confirm PO and send to vendor]
    C --> D
    D --> E[Warehouse validates receipt in Odoo]
    E --> F[Stock and GL update automatically]
    D --> G[Vendor bill created from PO]
    E --> G
    G --> H{3-way match: PO, receipt, bill}
    H -- Match --> I[Bill approved for payment]
    H -- Mismatch --> J[Exception routed to purchasing]
    J --> G
    I --> K[Payment and bank reconciliation]
```

**Improvements:** approval before spend · stock and accounting update together · automatic 3-way match · no manual month-end inventory adjustment.

## Month-end close: before and after

| Step | Current (days) | Future (days) | What changes |
|---|---|---|---|
| Bank reconciliation | 2 | 0.5 | Daily bank feeds |
| AP cut-off and accruals | 2 | 1 | Received-not-billed report from Odoo |
| Inventory reconciliation | 3 | 1 | Perpetual valuation posts to GL |
| AR review | 1 | 1 | No change |
| Reporting | 1 | 1.5 | Adds budget vs. actual review |
| **Total** | **9** | **5** | |
