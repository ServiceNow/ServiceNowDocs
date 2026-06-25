---
title: Confirm whether an invoice is a duplicate
description: Review invoices flagged as suspected duplicates and confirm or reject the duplicate status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/confirm-duplicate-invoice.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, duplicate invoice detection, AP specialist, invoice processing]
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Confirm whether an invoice is a duplicate

Review invoices flagged as suspected duplicates and confirm or reject the duplicate status.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice in the Suspected duplicate status.

5.  Select **View invoice processing case**.

    The invoice processing case opens and displays the following notification at the top:

    `Invoice is a potential duplicate. Review invoices in "Potential duplicate invoices" tab to confirm or reject duplicate.`

6.  Do one of the following:

<table><thead><tr><th>

Option

</th><th>

Action

</th></tr></thead><tbody><tr><td>

To mark an invoice as not a duplicate

</td><td>

1.  Select **Not a duplicate**.

A message appears asking you for a confirmation.

2.  Select **Yes**.

The status of the invoice changes to Accepted.

</td></tr><tr><td>

To mark an invoice as a duplicate

</td><td>

1.  Select **Confirm duplicate**.

A message appears asking you for a confirmation.

2.  Select **Yes**.

The status of the invoice changes to Confirmed duplicate and the state of the invoice processing case changes to Closed incomplete.

</td></tr></tbody>
</table>
**Parent Topic:**[Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice]()

[Review an invoice in Document Intelligence]()

[Enter the missing required invoice information and submit an invoice]()

[Convert invoice type]()

[Reset an invoice to the Received status]()

[Check for invoice exceptions on a single invoice]()

[Start the processing for an invoice imported via integration with third-party applications]()

