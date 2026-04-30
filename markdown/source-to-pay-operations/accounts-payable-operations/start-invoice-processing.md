---
title: Start the processing for an invoice imported via integration with third-party applications
description: Start the processing for an invoice that doesn't have an associated invoice processing case.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Start the processing for an invoice imported via integration with third-party applications

Start the processing for an invoice that doesn't have an associated invoice processing case.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

In a few scenarios, the invoice can be imported via integration with third-party applications. If an invoice is ingested into Accounts Payable Operations via integration, the invoice processing is not initiated. No invoice processing case is created for the invoice.

In such situations, the Accounts Payable Specialist must open the invoice and select the **Start invoice processing** option, which creates an invoice processing case for the invoice and starts processing the invoice.

The **Start invoice processing** option is displayed for invoices of type PO and Non-PO only.

The **Start invoice processing** option is not displayed for invoices that are in the Canceled, Closed duplicate, Approved, Pending payment, or Paid status.

**Note:** Accounts Payable Operations includes the Start Invoice Processing for Orphan Invoices flow, which automatically picks up all the PO and Non-PO invoice type records that are in the Draft status that don't have an invoice processing case associated to them and starts their processing.

You don't need to perform this manual task if you've activated the Start Invoice Processing for Orphan Invoices flow. For more information, see [Activate the Start Invoice Processing for Orphan Invoices flow](activate-start-invoice-processing-flow.md).

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open the invoice that is imported into Accounts Payable Operations via integration.

5.  Select **Start invoice processing**.

    An invoice processing detailed record and an invoice processing case is created for the invoice and the invoice processing begins.

    After an invoice processing case is created for the invoice, the **Start invoice processing** option is replaced by the **View invoice processing case** option on the Invoice form.

    The invoice is processed based on its current status. For example, if the invoice is in the Received status, the duplicate check process is run, if the invoice is in the PO matching completed status, the exception engine is run, if the invoice is in the No exceptions found status, the approval engine is run, and so on.

    The invoices for which an invoice processing case is not created automatically, a scheduled job runs at regular intervals to pick up such invoices, creates an invoice case for each invoice, and starts the processing for the invoices. The scheduled job enables you to start the processing for all such invoices in bulk, without requiring you to start the processing for each invoice individually.


-   **[Activate the Start Invoice Processing for Orphan Invoices flow](activate-start-invoice-processing-flow.md)**  
Activate the **Start Invoice Processing for Orphan Invoices** flow to start the processing of an invoice that doesn’t have an associated invoice case.

**Parent Topic:**[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice](view-invoice-case.md)

[Review an invoice in Document Intelligence](review-invoice-docintel.md)

[Enter the missing required invoice information and submit an invoice](enter-missing-docintel.md)

[Confirm whether an invoice is a duplicate](confirm-duplicate-invoice.md)

[Convert invoice type](convert-invoice-case.md)

[Reset an invoice to the Received status](reset-invoice-to-received.md)

[Check for invoice exceptions on a single invoice](identify-exceptions-manually.md)

