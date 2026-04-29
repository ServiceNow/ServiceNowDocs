---
title: Cancel a clone
description: You can cancel a clone that is scheduled, requested, or in progress until the Node Repoint state. Canceling a clone retains the target instance as-is in its pre-clone state with its original data.Scheduled clones aren't able to be modified, you must cancel scheduled clones and make a new clone schedule.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
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


## Cancel scheduled clones \(legacy\)

Scheduled clones aren't able to be modified, you must cancel scheduled clones and make a new clone schedule.

### Before you begin

Role required: clone\_admin

### Procedure

1.  Select **Instance Clone** &gt; **Active Clones** &gt; **&lt;one-of-your-clones&gt;**.

2.  In the **Related Links**, select **Cancel Clone**.

    Clones can only be canceled up to Node Repoint stage. The clone can be rolled back once it completes.

    The system stops any current cloning activities and sets the **State** to **Canceled**.


