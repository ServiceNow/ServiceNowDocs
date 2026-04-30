---
title: Update the purchase order on an invoice
description: If you find that the purchase order that is currently associated with an invoice is incorrect, you can associate the correct purchase order to the invoice.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Update the purchase order on an invoice

If you find that the purchase order that is currently associated with an invoice is incorrect, you can associate the correct purchase order to the invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Invoices** &gt; **All open invoices**.

4.  Open a PO Invoice.

5.  Under Summary Details, in the **Purchase order** field, search for and select a purchase order.

    The following confirmation message is displayed: `Updating the Purchase order may require PO matching again. Do you want to continue?`

6.  Select **OK**.

    The confirmation message is not displayed if you update the purchase order on a PO invoice that is in the Draft, Received, or Accepted status.

    The confirmation message is displayed if you update the purchase order on a PO invoice either before or after PO matching is completed. If you select **OK** after you change the purchase order in the **Purchase order** field, the invoice lines are mapped with the purchase order lines of the newly associated purchase order. Subsequently, the automated PO matching process is run and the invoice status moves to PO matching error or PO matching completed.


**Parent Topic:**[Work with invoices](../concept/work-with-invoices.md)

