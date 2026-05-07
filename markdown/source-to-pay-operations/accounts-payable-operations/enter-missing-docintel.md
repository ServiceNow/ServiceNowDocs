---
title: Enter the missing required invoice information and submit an invoice
description: If Document Intelligence encounters a transformation error, the invoice is created and associated with an invoice processing case. However, not all required information is populated on the invoice. You must manually enter the required information and submit the invoice for further processing.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Enter the missing required invoice information and submit an invoice

If Document Intelligence encounters a transformation error, the invoice is created and associated with an invoice processing case. However, not all required information is populated on the invoice. You must manually enter the required information and submit the invoice for further processing.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice in the Draft status.

5.  Select **View invoice processing case**.

    ![View invoice processing case](../image/apo-view-inv-process-case.png)

    The invoice processing case opens and displays the following notification at the top:

    `Required information for invoice has one or more errors. Review required fields and currency in "Details" tab to continue processing.`

6.  On the **Details** tab, under Summary details, enter the missing details in the fields.

7.  Select the **Invoice lines** tab, and ensure that you add at least one invoice line.

8.  Select **Submit invoice**.

    A message appears asking you for a confirmation.

9.  Select **Yes**.

    The invoice is submitted for further processing and the status of the invoice changes to Received.


**Parent Topic:**[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice](view-invoice-case.md)

[Review an invoice in Document Intelligence](review-invoice-docintel.md)

[Confirm whether an invoice is a duplicate](confirm-duplicate-invoice.md)

[Convert invoice type](convert-invoice-case.md)

[Reset an invoice to the Received status](reset-invoice-to-received.md)

[Check for invoice exceptions on a single invoice](identify-exceptions-manually.md)

[Start the processing for an invoice imported via integration with third-party applications](start-invoice-processing.md)

