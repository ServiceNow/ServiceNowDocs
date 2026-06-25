---
title: Check for invoice exceptions on a single invoice
description: Manually check for exceptions on a single invoice in the Source-to-Pay Workspace when you want to identify and resolve issues before continuing to process the invoice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/identify-exceptions-manually.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice exception, AP specialist]
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Check for invoice exceptions on a single invoice

Manually check for exceptions on a single invoice in the Source-to-Pay Workspace when you want to identify and resolve issues before continuing to process the invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

The **Check exceptions** option is available for all invoices that are in **Exceptions found** state.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice that is in the **Exceptions found** state.

5.  Select **View invoice processing case**.

    **Note:** If you open an invoice processing case for an invoice that is in Exceptions found status, the invoice processing case form displays the following notification at the top:

    `Invoice has one or more exceptions. Resolve all issues in "Invoice exceptions" to continue processing.`

6.  On the invoice processing case form, select **Check exceptions**.

    \[Omitted image "apo-check-exception.png"\] Alt text: Check exceptions

7.  Select **Yes**.

    While exceptions are being identified on the invoice, the status of the invoice changes to **Checking exceptions** for a short period of time and the following occurs:

    -   If no exceptions are found on the invoice, the status of the invoice changes to No exceptions found.
    -   If exceptions are found on the invoice, the status of the invoice remains as Exceptions found.

**Parent Topic:**[Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice]()

[Review an invoice in Document Intelligence]()

[Enter the missing required invoice information and submit an invoice]()

[Confirm whether an invoice is a duplicate]()

[Convert invoice type]()

[Reset an invoice to the Received status]()

[Start the processing for an invoice imported via integration with third-party applications]()

