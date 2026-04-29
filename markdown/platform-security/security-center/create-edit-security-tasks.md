---
title: Edit Security Tasks
description: Learn how to create, edit, delete, or export Security Tasks in Security Center
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Tasks, Security Center, Platform Security]
---

# Edit Security Tasks

Learn how to create, edit, delete, or export Security Tasks in Security Center

## Before you begin

Role required: admin or sn\_vsc\_task\_manager

## Procedure

1.  Access your Security Task list by navigating to **All** &gt; **Security Center** &gt; **Security Tasks**.

2.  From the Security Task list, you can edit your Security Tasks in two ways:

    -   **Edit in the Security Task form**

        Select a Security Task number from the list to open the Security Task record and see its details. Here you can edit, assign to another user, and add work notes.

        **Important:** Remember that users who are assigned tasks must be admins or have the sn\_vsc\_task\_manager role.

    -   **Edit from the Security Task list**

        Select one or more Security Tasks by selecting on its check box on the left and then select the **Edit** button.

3.  Fill in the fields as needed:

<table id="table_fxg_brj_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated number used to identity the task

</td></tr><tr><td>

Type

</td><td>

Select a task type:-   Metrics threshold breached
-   New Customer Action
-   Event notification
-   Hardening score deviation
-   New banner announcement


</td></tr><tr><td>

Short description

</td><td>

Brief description of the task

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group for the task

</td></tr><tr><td>

Assigned to

</td><td>

Person assigned to the task. This user must be in the assignment group selected in the **Assignment Group** field, and have the **admin** or **sn\_vsc\_task\_manager** role.

</td></tr><tr><td>

State

</td><td>

State of the task:-   Pending
-   Open
-   In Progress
-   Closed
-   Canceled


</td></tr><tr><td>

Priority

</td><td>

Priority of the task:-   1- Critical
-   2- High
-   3- Moderate
-   4- Low


</td></tr><tr><td>

Due status

</td><td>

Whether the task is **Upcoming** or **Overdue**, depending on the date in the **Due date** field.

</td></tr><tr><td>

Due date

</td><td>

The date and time by which the task needs to be completed.

</td></tr><tr><td>

Details

</td><td>

Used to provide details, links, or other information users need to know about this task.

</td></tr><tr><td>

Work notes

</td><td>

Notes about this task. Notes entered into this field are timestamped and displayed on the Activity list on the right of the screen.

</td></tr><tr><td>

Work notes \(private\)

</td><td>

Work notes can be privately added by entering them into this field and selecting the **Post work notes \(private\)** button.

</td></tr></tbody>
</table>4.  Select **Save** to save the Security Task record, if you are editing a record from the list, select **Update**.

5.  If needed, you can delete a task from the list by selecting on its check box on the right, and selecting **Delete**, or in the form by selecting the more icon \(...\), then selecting **Delete**.


**Parent Topic:**[Security Tasks](../concept/security-task-manager.md)

