---
title: Use the ACL configuration watcher
description: Use the ACL configuration watcher after you elevate to security\_admin role.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACL configuration watcher, ACL debugging tools, Advanced ACL configuration, Access Control List Rules, Access Management]
---

# Use the ACL configuration watcher

Use the ACL configuration watcher after you elevate to security\_admin role.

## Before you begin

Role required: security\_admin

[Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md)

## Procedure

1.  Open an ACL that is a record-type ACL.

2.  Perform an action on the ACL, such as modifying it, or selecting an option from the context menu like **Insert**.

3.  If you modified any values on the Access Control form, right-click the header and select **Save** or click **Update** or **Delete**.

    The Security Rules window appears. The system did not yet perform the database action on the ACL, so the changes are not yet saved.

    These are examples of security rules on the Visual Task Board application's Private Task \[vtb\_task\] table. See [ACL configuration watcher](../concept/c_ACLConfigWatcher.md) for a description of the items on this window.

    ![Deactivating an ACL](../image/vtb_task_deativate.png)

    ![Adding an ACL](../image/vtb_task_add.png)

    ![Deleting an ACL](../image/vtb_task_read_delete.png)

    ![Modifying an ACL](../image/vtb_task_read_modify.png)

4.  Just as with the [execution plan](t_ShowACLExecutionPlan.md), you can click **Show all** to show all related ACLs, including those that are overridden and generic ACLs that apply to all records, or click **Show Effective** to show only the immediate ACLs related to the one you are viewing.

5.  Hover your mouse over any of the ACLs to see a description.


