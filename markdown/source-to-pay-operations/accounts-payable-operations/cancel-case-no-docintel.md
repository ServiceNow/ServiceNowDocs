---
title: Close the additional invoice processing case for an invoice
description: Close the auto-created invoice processing case if one already exists for an invoice.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Invoice ingestion process when Document Intelligence is unavailable, Invoice processing cases, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Close the additional invoice processing case for an invoice

Close the auto-created invoice processing case if one already exists for an invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist

## About this task

If you create an invoice manually, a new invoice processing case is created for that invoice. As a result, the auto-generated invoice processing case becomes redundant and therefore you can close it.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice processing cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice processing cases**.
4.  Open the invoice processing case.

5.  Select **Close case**.

    The Close case dialog box is displayed.

6.  From the Closure code list, select one of the following options:

    -   **Duplicate invoice**
    -   **Invoice canceled**
    -   **Invoice approved**
7.  In the **Reason** field, enter the reason why you're closing the case.

8.  Select **Close case**.

    The invoice processing case is closed and its state updates to Closed complete.


**Parent Topic:**[Invoice ingestion process when Document Intelligence is unavailable](../concept/invoice-ingest-docintel-unavailable.md)

