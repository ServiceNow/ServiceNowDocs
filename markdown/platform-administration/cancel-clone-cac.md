---
title: Cancel a clone
description: You can cancel a clone that is scheduled, requested, or in progress until the Node Repoint state. Canceling a clone retains the target instance as-is in its pre-clone state with its original data.You can cancel a clone that is scheduled, requested, or in progress until the Node Repoint state. Canceling a clone retains the target instance as-is in its pre-clone state with its original data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer]
---

# Cancel a clone

You can cancel a clone that is scheduled, requested, or in progress until the Node Repoint state. Canceling a clone retains the target instance as-is in its pre-clone state with its original data.

## Before you begin

Role required: clone\_admin

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select the tile of the clone that you must cancel.

3.  Select the **Cancel** option on the page.

4.  Select a reason for the cancellation.

5.  Select **OK**.

    The system stops any current clone activities and sets the **State** to **Canceled**.


**Parent Topic:**[Managing Instance Clone](using-instance-clone.md)

## Cancel a clone \(legacy\)

You can cancel a clone that is scheduled, requested, or in progress until the Node Repoint state. Canceling a clone retains the target instance as-is in its pre-clone state with its original data.

### Before you begin

Role required: clone\_admin

### About this task

After a clone starts, you can view log messages within the related lists at the bottom of the clone request form.

### Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Live Clones** &gt; **Active Clones**.

    The system displays the list of currently active clones.

2.  Select the clone that you want to cancel.

    The system displays the Instance Clone record.

3.  From the **Related Links**, select **Cancel Clone**.

    The **Cancel Clone** modal displays.

    ![Cancel clone](../image/cancel-clone-legacy.png)

4.  In **Specify Reason** select a reason for the cancellation.

5.  Select **OK**.

    The system stops any current clone activities and sets the **State** to **Canceled**.


### What to do next

If you want to restart a canceled clone, you must create a [new clone request](t_StartAClone.md).

