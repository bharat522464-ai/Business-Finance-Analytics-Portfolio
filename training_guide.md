# User Training Guide: Receiving a Purchase Order in Odoo

> Fictional portfolio project. Audience: warehouse staff at Lakeside Supply Co.

## When to use this guide

Use it every time a vendor delivery arrives. Receiving in Odoo updates stock **and** the accounting records at the same time, so it must be done the same day goods arrive.

## Steps

1. **Open the receipt.** Go to *Inventory → Receipts* and search for the vendor name or PO number on the packing slip.
2. **Check the delivery.** Count each item and compare it with the quantities on screen.
3. **Enter what arrived.** Type the quantity received in the *Quantity* column for each line. Leave nothing blank.
4. **Handle a short delivery.** If fewer items arrived than ordered, click **Validate**, then choose **Create Backorder**. Odoo keeps the rest open for the next delivery.
5. **Handle damaged items.** Do not receive them. Add a note in the chatter with a photo, and tag the purchasing lead.
6. **Validate.** Click **Validate**. The receipt status changes to *Done*, and stock levels update immediately.

## Common mistakes

| Mistake | What happens | How to avoid it |
|---|---|---|
| Validating before counting | Stock and the vendor bill are overstated | Always count first |
| Receiving against the wrong PO | Bill matching fails | Match the PO number on the packing slip |
| Skipping the backorder | Remaining items are forgotten | Always choose *Create Backorder* for short deliveries |

## Who to ask

- Missing or wrong PO: Purchasing lead
- System error: Odoo super-user (Operations)
