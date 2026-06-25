---
title: Convert invoice type
description: Convert an invoice type between PO and Non-PO to correctly classify an invoice based on updated information from buyers or suppliers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/convert-invoice-case.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, supplier, AP specialist]
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Convert invoice type

Convert an invoice type between PO and Non-PO to correctly classify an invoice based on updated information from buyers or suppliers.

## Before you begin

Role required: Account Payable Specialist

## Procedure

1.  Navigate to **All** &gt; **Source-to-Pay Workspace** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **My work** &gt; **My open invoice processing cases** and open an invoice processing case.

    An alternate way is by navigating to **Lists** &gt; **Primary Data** &gt; **&gt;Invoices** &gt; **Open invoice**.

    **Note:** Type conversion is supported only for invoices from **Draft** state to **No exceptions found** state. You cannot convert invoice type once it is submitted for approval.

4.  Select **View invoice processing case**.

5.  Select **More Actions** \[Omitted image "more-actions.png"\] Alt text: more actions&gt;**Change invoice type**.

    You can choose to convert invoice types to:\[Omitted image "change-invoice-type.png"\] Alt text: Change invoice type

    -   PO to Non-PO invoice and vice versa
    -   Credit memo invoice to PO invoice, Non-PO invoice and vice versa
    A message appears asking for your confirmation.

6.  Select **Change invoice type**.

7.  Select **Save**.

    The status of the invoice changes to **Draft**. The invoice is reprocessed and re-validated.


**Parent Topic:**[Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice]()

[Review an invoice in Document Intelligence]()

[Enter the missing required invoice information and submit an invoice]()

[Confirm whether an invoice is a duplicate]()

[Reset an invoice to the Received status]()

[Check for invoice exceptions on a single invoice]()

[Start the processing for an invoice imported via integration with third-party applications]()

