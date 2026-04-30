---
title: Create an exception task for an invoice exception
description: Create an exception task to assign it to a user or an assignment group to resolve the invoice exception.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work on an invoice exception, Invoice exceptions, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an exception task for an invoice exception

Create an exception task to assign it to a user or an assignment group to resolve the invoice exception.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Do one of the following:

<table id="table_qzk_by4_fwb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Create an exception task from the List page

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open tasks**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open tasks**.
2.  Select **New**.

The Create New Invoice task page is displayed. For a description of the field values, see [Create New Invoice task form](../reference/create-apm-task-form.md).

The **Type** field is set to **Case task** by default.

3.  In the **Parent case** field, select the parent case for the invoice.
4.  In the **Invoice exception** field, select the exception for which you want to create an exception task.
5.  After you select an exception, the Type field changes from **Case task** to **Exception task**.

**Note:** The **Type** field is read-only.

6.  Enter the required information in the **Assignment group**, **Assigned to**, **Short description**, and **Description** fields.
7.  Select **Save**.


</td></tr><tr><td>

Create an exception task from an invoice exception

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice exceptions**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice exceptions**.
2.  In the Number column, select the link to an invoice exception to open it.
3.  Select the **Exception tasks** tab and then select **New**.

The Create New Invoice task page is displayed. For a description of the field values, see [Create New Invoice task form](../reference/create-apm-task-form.md).

The **Parent case**, **Invoice exception**, and **Type** fields are auto-populated.

4.  Enter the required information in the **Assignment group**, **Assigned to**, **Short description**, and **Description** fields.
5.  Select **Save**.


</td></tr><tr><td>

Create an exception task from an invoice processing case

</td><td>

1.  Navigate to **Lists** &gt; **All Work** &gt; **All open invoice processing cases**.
2.  In the Number column, select the link to an invoice processing case to open it.
3.  Select the **Tasks** tab and then select **New**.

The Create New Invoice task page is displayed. For a description of the field values, see [Create New Invoice task form](../reference/create-apm-task-form.md).

The Parent case field is auto-populated. The **Type** field is set to **Case task** by default.

4.  In the **Invoice exception** field, select the exception for which you want to create an exception task.
5.  After you select an exception, the **Type** field changes from **Case task** to **Exception task**.

**Note:** The **Type** field is read-only.

6.  Enter the required information in the **Assignment group**, **Assigned to**, **Short description**, and **Description** fields.
7.  Select **Save**.


</td></tr></tbody>
</table>    The exception task gets assigned to the business owner specified on the invoice.


## What to do next

[Mark an exception task as complete from Employee Center](complete-exception-task-ec.md).

**Parent Topic:**[Work on an invoice exception](work-invoice-exception-case.md)

