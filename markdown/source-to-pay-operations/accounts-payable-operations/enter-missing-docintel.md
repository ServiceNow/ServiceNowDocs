---
title: Enter the missing required invoice information and submit an invoice
description: Manually enter missing invoice data and submit the invoice when Document Intelligence encounters a transformation error and only partially populates invoice fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/enter-missing-docintel.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Enter the missing required invoice information and submit an invoice

Manually enter missing invoice data and submit the invoice when Document Intelligence encounters a transformation error and only partially populates invoice fields.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice in the Draft status.

5.  Select **View invoice processing case**.

    \[Omitted image "apo-view-inv-process-case.png"\] Alt text: View invoice processing case

    The invoice processing case opens and displays the following notification at the top:

    `Required information for invoice has one or more errors. Review required fields and currency in "Details" tab to continue processing.`

6.  On the **Details** tab, under Summary details, enter the missing details in the fields.

7.  Select the **Invoice lines** tab, and ensure that you add at least one invoice line.

8.  Select **Submit invoice**.

    A message appears asking you for a confirmation.

9.  Select **Yes**.

    The invoice is submitted for further processing and the status of the invoice changes to Received.


**Parent Topic:**[Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice]()

[Review an invoice in Document Intelligence]()

[Confirm whether an invoice is a duplicate]()

[Convert invoice type]()

[Reset an invoice to the Received status]()

[Check for invoice exceptions on a single invoice]()

[Start the processing for an invoice imported via integration with third-party applications]()

