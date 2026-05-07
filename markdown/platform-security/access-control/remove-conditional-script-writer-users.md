---
title: Remove users from the Conditional Script Writer group
description: Use the Manage scripting access to manually add or remove users from the Conditional Script Writer group to control who has scripting access.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-04-09"
reading_time_minutes: 2
keywords: [scripting governance tool, conditional script writer group, manage scripting access, schedule removal, remove scripting access]
breadcrumb: [Use SGT, Scripting Governance Tool, Access Management]
---

# Remove users from the Conditional Script Writer group

Use the Manage scripting access to manually add or remove users from the **Conditional Script Writer** group to control who has scripting access.

## Before you begin

Role required: security\_admin

**Important:**

-   You must have elevate your role `security_admin`. See [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).
-   Until auto-assignment is turned off, a background job continues adding existing and new users to the **Conditional Script Writer** group, which assigns the `snc_required_script_writer_permission` role. It is recommended that you deactivate auto-assignment and manage the removal process to confirm only users with a legitimate scripting need remain in the group.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Scripting Governance Tool**.

2.  Select **Manage scripting access**.

3.  Add the users who should retain scripting access in the **Users to keep in the conditional script writers group** field.

    Only users added to this field are retained in the group after the removal job runs. All other group members are removed. Search and select users by name.

    ![Manage users](../image/sgt-manage-user.png)

4.  Select **Next**.

    The Manage users in the conditional script writer group page opens with the **Keep list** card displays the number of users retained, and the **Keep in the conditional script writer group** table lists the users you selected.

5.  Review the keep list to confirm it is correct, then select **Schedule removal**.

    ![Schedule removal](../image/sgt-schedule-removal.png)

    The **Schedule removal** dialog opens and displays a summary of the pending changes:

6.  Select when the removal job should run in the **Start processing** field:

    The following options are available:

    -   Immediately — runs the removal job as soon as you confirm.
    -   In 1 hour
    -   In 2 hours
    -   In 3 hours
    -   In 5 hours
    -   In 8 hours
    -   In 13 hours
7.  Select **Confirm** to schedule the removal.

    A banner confirms that the `Conditional script writer group member removal job is running or scheduled`. The removal job removes all users not on the keep list from the **Conditional Script Writer** group and disables auto-assignment.


## Result

Users not included in the keep list are removed from the **Conditional Script Writer** group at the scheduled time and lose the `snc_required_script_writer_permission` role. Removal does not affect any other permissions those users hold on the instance. Auto-assignment is also disabled, preventing the background job from re-adding users to the group automatically.

## What to do next

After the removal job completes, verify the outcome using the **View removals** section at the bottom of the SGT dashboard.

