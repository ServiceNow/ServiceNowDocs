---
title: Review an invoice in Document Intelligence
description: Review the invoice details, enter the required invoice field values, and submit the invoice if Document Intelligence encounters an extraction error.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Review an invoice in Document Intelligence

Review the invoice details, enter the required invoice field values, and submit the invoice if Document Intelligence encounters an extraction error.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

If Document Intelligence encounters an extraction error, the invoice processing case is created in Accounts Payable Operations integration with Document Intelligence. The invoice is not created or associated with that case. You must review the invoice details in Document Intelligence, enter the required values in the invoice fields, and submit the invoice to create the invoice.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice that is in the Draft status.

5.  Select **View invoice processing case**.

    The invoice processing case opens and displays the following notification at the top:

    `Invoice has a data extraction error. Review invoice with automation to continue processing.`

6.  Select **Review invoice**.

7.  Refer to the invoice document and fill in the fields for the invoice.

8.  Select **Submit**.

    The invoice and invoice line records are created and the invoice is associated with this invoice processing case.

9.  Open the invoice processing case and select **Submit invoice**.

    A message appears asking you for a confirmation.

10. Select **Yes**.

    The invoice is submitted for further processing and the status of the invoice changes to Received.


**Parent Topic:**[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice](view-invoice-case.md)

[Enter the missing required invoice information and submit an invoice](enter-missing-docintel.md)

[Confirm whether an invoice is a duplicate](confirm-duplicate-invoice.md)

[Convert invoice type](convert-invoice-case.md)

[Reset an invoice to the Received status](reset-invoice-to-received.md)

[Check for invoice exceptions on a single invoice](identify-exceptions-manually.md)

[Start the processing for an invoice imported via integration with third-party applications](start-invoice-processing.md)

