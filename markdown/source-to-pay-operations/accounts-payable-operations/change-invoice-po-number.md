---
title: Update the purchase order on an invoice
description: Correct the purchase order associated with an invoice when the wrong purchase order is linked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/change-invoice-po-number.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, purchase order, PO, AP specialist]
breadcrumb: [Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Update the purchase order on an invoice

Correct the purchase order associated with an invoice when the wrong purchase order is linked.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **Invoices** &gt; **All open invoices**.

4.  Open a PO Invoice.

5.  Under Summary Details, in the **Purchase order** field, search for and select a purchase order.

    The following confirmation message is displayed: `Updating the Purchase order may require PO matching again. Do you want to continue?`

6.  Select **OK**.

    The confirmation message is not displayed if you update the purchase order on a PO invoice that is in the Draft, Received, or Accepted status.

    The confirmation message is displayed if you update the purchase order on a PO invoice either before or after PO matching is completed. If you select **OK** after you change the purchase order in the **Purchase order** field, the invoice lines are mapped with the purchase order lines of the newly associated purchase order. Subsequently, the automated PO matching process is run and the invoice status moves to PO matching error or PO matching completed.


**Parent Topic:**[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)

