---
title: Convert invoice type
description: You can convert invoice type from PO to Non-PO invoice and vice versa based on interaction between buyers and suppliers of business services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/accounts-payable-operations/convert-invoice-case.html
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Convert invoice type

You can convert invoice type from PO to Non-PO invoice and vice versa based on interaction between buyers and suppliers of business services.

## Before you begin

Role required: Account Payable Specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **My work** &gt; **My open invoice processing cases** and open an invoice processing case.

    An alternate way is by navigating to **Lists** &gt; **Primary Data** &gt; **&gt;Invoices** &gt; **Open invoice**.

    **Note:** Type conversion is supported only for invoices from **Draft** state to **No exceptions found** state. You cannot convert invoice type once it is submitted for approval.

4.  Choose the **Type** drop-down to convert an invoice.

    \[Omitted image "apo-change-invoice-dialog.png"\] Alt text: Select new invoice type

    -   When you choose to convert an invoice from PO to Non-PO invoice, the **Purchase order** field is hidden.
    -   When you choose to convert an invoice from Non-PO to PO invoice, the **Purchase order** field is displayed and you must populate the purchase order field.
    A message appears asking for your confirmation.

5.  Select **Continue**.

6.  Select **Save**.


## Result

The status of the invoice changes to new invoice type. The invoice is reprocessed and re-validated.

**Parent Topic:**[Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice]()

[Review an invoice in Document Intelligence]()

[Enter the missing required invoice information and submit an invoice]()

[Confirm whether an invoice is a duplicate]()

[Reset an invoice to the Received status]()

[Check for invoice exceptions on a single invoice]()

[Start the processing for an invoice imported via integration with third-party applications]()

