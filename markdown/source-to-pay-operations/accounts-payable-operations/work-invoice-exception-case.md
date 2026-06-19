---
title: Work on an invoice exception
description: As an Accounts Payable Specialist, analyze the invoice exceptions, create exception tasks, and assign them to the relevant individuals to resolve the invoice exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/work-invoice-exception-case.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, invoice exception, admin, AP specialist]
breadcrumb: [Invoice exceptions, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Work on an invoice exception

As an Accounts Payable Specialist, analyze the invoice exceptions, create exception tasks, and assign them to the relevant individuals to resolve the invoice exceptions.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

For a description of the field values and information about the available tabs on the invoice exception form, see [Invoice exception form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/exception-form-fields.md). For details about the available tabs for an exception task, see [Invoice task form tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-task-form-related-list.md).

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Do one of the following:

<table id="table_crv_zwr_2wb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View exceptions from the List page

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **Invoice exceptions**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **Invoice exceptions**.
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

    For more information, see [Create an exception task for an invoice exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-exception-task.md).

    After all the invoice exception tasks are completed, the status of the invoice updates to No exceptions found. The invoice processing case remains in the Work in progress state.

5.  To view all the invoice exceptions tasks and the exception tasks that are assigned to you, do the following:

    1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.
    2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).
    3.  Do one of the following:
        -   Navigate to **Lists** &gt; **My Work** &gt; **Open tasks**.
        -   Navigate to **Lists** &gt; **All Work** &gt; **All open tasks**.

-   **[Create an exception task for an invoice exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-exception-task.md)**  
Create an exception task to assign it to a user or an assignment group to resolve the invoice exception.
-   **[Mark an exception task as complete from Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/complete-exception-task-ec.md)**  
Mark an assigned invoice exception task as complete from Employee Center when you have finished working on the task.
-   **[Edit a purchase for an Insufficient Funds invoice exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/edit-purchase-insufficient-funds.md)**  
Edit a purchase to resolve invoice exceptions of type Insufficient Funds \(Amount variance\) and Insufficient Funds \(Quantity variance\).
-   **[Resolve unverified sender source exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/resolve-unverified-sender-exception.md)**  
Review an unverified sender source exception in APO and resolve it by adding the sender as a supplier contact or rejecting the invoice.
-   **[Confirm receipt of your order from Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/confirm-receipt-task.md)**  
Confirm the receipt of the ordered items so that the payment is made to the supplier.
-   **[Bypass an invoice exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/bypass-invoice-exception.md)**  
Bypass an invoice exception if you find that it is not applicable to the invoice.

**Parent Topic:**[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md)

