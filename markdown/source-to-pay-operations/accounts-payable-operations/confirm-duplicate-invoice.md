---
title: Confirm whether an invoice is a duplicate
description: Confirm whether an invoice that is in the Suspected duplicate status is indeed a duplicate to determine if the invoice should be considered for processing.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Specialist manual tasks, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Confirm whether an invoice is a duplicate

Confirm whether an invoice that is in the Suspected duplicate status is indeed a duplicate to determine if the invoice should be considered for processing.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Primary Data** &gt; **Invoices**.

4.  Open an invoice in the Suspected duplicate status.

5.  Select **View invoice processing case**.

    The invoice processing case opens and displays the following notification at the top:

    `Invoice is a potential duplicate. Review invoices in "Potential duplicate invoices" tab to confirm or reject duplicate.`

6.  Do one of the following:

    ![Working with duplicate invoices](../image/apo-duplicates.png)

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
## Result

The invoice in the Suspected Duplicate status is confirmed as duplicate or not.

**Parent Topic:**[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)

**Related topics**  


[View the invoice processing case associated with an invoice](view-invoice-case.md)

[Review an invoice in Document Intelligence](review-invoice-docintel.md)

[Enter the missing required invoice information and submit an invoice](enter-missing-docintel.md)

[Convert invoice type](convert-invoice-case.md)

[Reset an invoice to the Received status](reset-invoice-to-received.md)

[Check for invoice exceptions on a single invoice](identify-exceptions-manually.md)

[Start the processing for an invoice imported via integration with third-party applications](start-invoice-processing.md)

