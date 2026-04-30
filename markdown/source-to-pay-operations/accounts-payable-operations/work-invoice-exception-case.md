---
title: Work on an invoice exception
description: As an Accounts Payable Specialist, analyze the invoice exceptions, create exception tasks, and assign them to the relevant individuals to resolve the invoice exceptions.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Invoice exceptions, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Work on an invoice exception

As an Accounts Payable Specialist, analyze the invoice exceptions, create exception tasks, and assign them to the relevant individuals to resolve the invoice exceptions.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

For a description of the field values and information about the available tabs on the invoice exception form, see [Invoice exception form](../reference/exception-form-fields.md). For details about the available tabs for an exception task, see [Invoice task form tabs](../reference/invoice-task-form-related-list.md).

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Do one of the following:

<table id="table_crv_zwr_2wb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View exceptions from the List page

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice exceptions**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice exceptions**.
2.  Select the link to the invoice exception under the Number column to open the exception and view its details.


</td></tr><tr><td>

View exceptions from an invoice processing case

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice processing cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice processing cases**.
2.  Open an invoice processing case that contains exceptions.

**Note:** If an invoice processing case contains exceptions, the following message is shown at the top of the case:

`Invoice has one or more exceptions. Resolve all issues in "Invoice exceptions" to continue processing.`

3.  Select the **Invoice Exceptions** tab.
4.  Select the link to the invoice exception under the Number column to open the exception and view its details.


</td></tr></tbody>
</table>4.  Either work on the invoice exception yourself or create an exception task to assign it to a user or an assignment group to resolve the invoice exception.

    For more information, see [Create an exception task for an invoice exception](create-exception-task.md).

    After all the invoice exception tasks are completed, the status of the invoice updates to No exceptions found. The invoice processing case remains in the Work in progress state.

5.  To view all the invoice exceptions tasks and the exception tasks that are assigned to you, do the following:

    1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.
    2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).
    3.  Do one of the following:
        -   Navigate to **Lists** &gt; **My Work** &gt; **My open tasks**.
        -   Navigate to **Lists** &gt; **All Work** &gt; **All open tasks**.

## Result

The invoice exceptions are analyzed, exception tasks are created, and assigned to the relevant individuals to resolve them.

-   **[Create an exception task for an invoice exception](create-exception-task.md)**  
Create an exception task to assign it to a user or an assignment group to resolve the invoice exception.
-   **[Mark an exception task as complete from Employee Center](complete-exception-task-ec.md)**  
As a task owner, when you finish working on an assigned exception task, you can mark the task as complete from Employee Center.
-   **[Edit a purchase for an Insufficient Funds invoice exception](edit-purchase-insufficient-funds.md)**  
Edit a purchase to resolve invoice exceptions of type Insufficient Funds \(Amount variance\) and Insufficient Funds \(Quantity variance\).
-   **[Confirm receipt of your order from Employee Center](confirm-receipt-task.md)**  
Confirm the receipt of the items that you've ordered so that the payment is made to the supplier.
-   **[Bypass an invoice exception](bypass-invoice-exception.md)**  
Bypass an invoice exception if you find that it is not applicable to the invoice.

**Parent Topic:**[Invoice exceptions](../concept/work-with-invoice-exceptions.md)

