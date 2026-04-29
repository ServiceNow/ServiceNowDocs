---
title: Reminder table
description: The Reminder \[reminder\] table provides a way to auto-generate reminders for a task.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Task table structure, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Reminder table

The Reminder \[reminder\] table provides a way to auto-generate reminders for a task.

Any table that extends the Task table, such as the Incident \[incident\] table, can use the Reminder \[reminder\] table.

You can add Reminders as a related list to the Incident form by opening the form context menu, navigating to **Configure** &gt; **Related Lists**, and then adding **Reminders-&gt;Task**.

By default, only an administrator can create or modify a Reminder record. To enable non-administrators to create reminders, you must add create and read ACL rules to the Reminder \[reminder\] table and specify the user's role.

**Note:** You can only create reminders for active task records.

To access the Reminder table, type `reminder.do` in the filter navigator.

<table id="table_ndl_xgh_vz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task

</td><td>

Refers to the parent task record.

</td></tr><tr><td>

User

</td><td>

Specifies the user who has logged in to the system.

</td></tr><tr><td>

Remind me

</td><td>

Specifies the time before which the reminder must be sent. Available values are: **15 minutes**, **30 minutes**, **1 hour**, and **2 hours**. You can add values to this field as required. **Note:** Internally in the system, the value is always converted to minutes and then stored in the **Remind me** field.

</td></tr><tr><td>

Before

</td><td>

Refers to a date field on the parent task record.

 **Note:** The **Activity due** and **SLA due** fields are legacy fields with an **UNKNOWN** value that you can't use. You can only use the **Due date** and **Follow up** fields.

 Note the following details about using the **Before** field.

 -   The parent task record must have a value in the field you specify. For example, if you select **Due date**, the parent task record must have a value in **Due date** before you can save the reminder.
-   You can use a date field other than **Due date** or **Follow up** by performing the following steps:
    1.  Select either **Due date** or **Follow up**in the **Before** field.
    2.  Save the reminder.
    3.  Find the reminder in a list view using one of the following methods:
        -   In the parent task record, configure the form, and then add Reminders as a related list.
        -   Navigate to `reminder.do` and search for the reminder.
    4.  In the list view, change the **Before** field value to a different date field from the parent task. Use the field name and make sure the field has a value. For example, enter `work_start` to use the **Actual start** field instead.

Note that you can't make additional changes on the reminder form without changing the **Before** field value back to either **Due date** or **Follow up**.


</td></tr><tr><td>

Using

</td><td>

Specifies the method by which the reminder must be sent. Available options are: **Send an Email** and **Outlook Calendar**.

</td></tr><tr><td>

Subject

</td><td>

Specifies the subject or the reason of the reminder. Maximum number of characters allowed on this field is 100.

</td></tr><tr><td>

Notes

</td><td>

Provides a space where you can enter your comments regarding the reminder. Maximum number of characters allowed on this field is 8000.

</td></tr></tbody>
</table>**Parent Topic:**[Task table structure](../../table-administration/concept/task-table-structure.md)

