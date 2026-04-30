---
title: Convert invoice type
description: You can convert invoice type from PO to Non-PO invoice and vice versa based on interaction between buyers and suppliers of business services.
locale: en-US
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

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **My work** &gt; **My open invoice processing cases** and open an invoice processing case.

    An alternate way is by navigating to **Lists** &gt; **Primary Data** &gt; **&gt;Invoices** &gt; **Open invoice**.

    **Note:** Type conversion is supported only for invoices from **Draft** state to **No exceptions found** state. You cannot convert invoice type once it is submitted for approval.

4.  Choose the **Type** drop-down to convert an invoice.

    ![Select new invoice type](../image/apo-change-invoice-dialog.png)

    -   When you choose to convert an invoice from PO to Non-PO invoice, the **Purchase order** field is hidden.
    -   When you choose to convert an invoice from Non-PO to PO invoice, the **Purchase order** field is displayed and you must populate the purchase order field.
    A message appears asking for your confirmation.

5.  Select **Continue**.

6.  Select **Save**.


## Result

The status of the invoice changes to new invoice type. The invoice is reprocessed and re-validated.

**Parent Topic:**[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice](view-invoice-case.md)

[Review an invoice in Document Intelligence](review-invoice-docintel.md)

[Enter the missing required invoice information and submit an invoice](enter-missing-docintel.md)

[Confirm whether an invoice is a duplicate](confirm-duplicate-invoice.md)

[Reset an invoice to the Received status](reset-invoice-to-received.md)

[Check for invoice exceptions on a single invoice](identify-exceptions-manually.md)

[Start the processing for an invoice imported via integration with third-party applications](start-invoice-processing.md)

