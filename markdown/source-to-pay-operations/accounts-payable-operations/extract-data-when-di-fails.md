---
title: Extract data when Document Intelligence fails
description: You must manually create an invoice for processing when Document Intelligence fails to process the task.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Intelligence processing with playbook, Playbook for updating the invoice primary data, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Extract data when Document Intelligence fails

You must manually create an invoice for processing when Document Intelligence fails to process the task.

## Before you begin

Role required: Accounts Payable admin, Accounts Payable specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md).

4.  Select **View invoice processing case**.

    A playbook is created for the invoice processing case.

5.  Select **Validate invoice**&gt;**Capture invoice details** activity card.

    An alert message displays as: `Invoice extraction has run into some technical issues. Please contact your system administrator. To continue processing, manually create an invoice or close the case`.

6.  Select **Create invoice** manually for creation of an invoice.

    **Note:** You can choose to close the case if you do not want to proceed.

    For more information on manual creation of invoices, see [Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

7.  Select **Review header details** to populate the header fields.

8.  Select **Review invoice lines** and add the invoice line fields or populate the required fields.

9.  Select **Submit**.

    If no further processing is required, then you can close the invoice case. A pop-up window prompts you to enter the reason for closing the invoice processing case. The playbook is canceled and the supplier is notified about the closure of the invoice processing case. The **Notify supplier** card is activated by default and displays the email sent to the supplier.


**Parent Topic:**[Document Intelligence processing with playbook](../concept/use-di-with-playbook.md)

