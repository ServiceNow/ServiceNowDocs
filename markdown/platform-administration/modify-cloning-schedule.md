---
title: Modify cloning schedules
description: You can cancel scheduled clonings but not modify them.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify cloning schedules

You can cancel scheduled clonings but not modify them.

## Before you begin

Role required: admin

## About this task

This topic assumes that you have a [cloning schedule](schedule-cloning.md) that you want to modify. Cloning schedules cannot be modified. Instead, you have to cancel scheduled clonings and create a new cloning schedule.

## Procedure

1.  Click **System Clone** &gt; **Active Clones** &gt; **&lt;one-of-your-clones&gt;**.

    The **System Clone**record opens for your cloning instance.

2.  To delete one or more scheduled clonings, on the **Recurring Clones**tab, select the check box next to the row\(s\) you want to cancel and on **Actions on selected rows**, click **Delete**.

3.  If you deleted all future clonings, you can create a new [cloning schedule](schedule-cloning.md).

    You cannot create more than one cloning schedule for a target instance.

4.  To stop a cloning that is already in progress, under **Related Links**, click **Cancel Clone**.

    The system stops any current cloning activities and sets the **State** to **Canceled**. Future, scheduled clonings are not deleted.


