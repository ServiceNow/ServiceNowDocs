---
title: Update the purchase order on an invoice
description: If you find that the purchase order that is currently associated with an invoice is incorrect, you can associate the correct purchase order to the invoice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/change-invoice-po-number.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Update the purchase order on an invoice

If you find that the purchase order that is currently associated with an invoice is incorrect, you can associate the correct purchase order to the invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **Invoices** &gt; **All open invoices**.

4.  Open a PO Invoice.

5.  Under Summary Details, in the **Purchase order** field, search for and select a purchase order.

    The following confirmation message is displayed: `Updating the Purchase order may require PO mapping again. Do you want to continue?`\[Omitted image "apo-update-po.png"\] Alt text: Update purchase order on an invoice

6.  Select **OK**.

    The confirmation message is not displayed if you update the purchase order on a PO invoice that is in the Draft, Received, or Accepted status.

    The confirmation message is displayed if you update the purchase order on a PO invoice either before or after PO matching is completed. If you select **OK** after you change the purchase order in the **Purchase order** field, the invoice lines are mapped with the purchase order lines of the newly associated purchase order. Subsequently, the automated PO matching process is run and the invoice status moves to PO matching error or PO matching completed.


## Result

The correct purchase order is associated with the invoice.

**Parent Topic:**[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)

**Related topics**  


[Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md)

[Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-workspace.md)

[Invoice processing cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.md)

[Tolerance Rules and Variances for invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.md)

[Invoice approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-approvals.md)

