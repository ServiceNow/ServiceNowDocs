---
title: Schedule recurring clones \(legacy\)
description: Schedule recurring clones to keep your cloned instances up to date.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule recurring clones \(legacy\)

Schedule recurring clones to keep your cloned instances up to date.

## Before you begin

Role required: clone\_admin

## About this task

Instead of manually cloning instances, you can schedule cloning that happens automatically. You create a cloning schedule in the same interface that you use to [create a clone](t_StartAClone.md#). This topic assumes that you created a clone but not a cloning schedule for it.

## Procedure

1.  Select **Instance Clone** &gt; **Active Clones** &gt; **&lt;one-of-your-clones&gt;**.

2.  **Note:** \(Optional\) if the **Options** panel isn’t already displayed.

    Select the **Options** arrowhead so it turns downward.

    The **Options** panel appears.

3.  **Note:** A target instance must be selected or an error message appears.

    Select the **Conflict calendar** to view a calendar with the current clone time and potential conflicts if you want to schedule for a different time.

    The conflict calendar appears in a new tab.![The schedule conflict calendar.](../image/schedule-conflict-calendar-new.png)

4.  Enter values in the following fields to schedule automatic clones.

<table id="choicetable_wdr_dfs_fhb"><thead><tr><th align="left" id="d280794e138">

Field

</th><th align="left" id="d280794e141">

Description

</th></tr></thead><tbody><tr><td id="d280794e147">

**Clone frequency**

</td><td>

Defines how often this target automatically receives clone data and the maximum number of occurrences. -   Weekly – The maximum number of occurrences is 25.
-   Twice a week – The maximum number of occurrences is 13.
-   Monthly – The maximum number of occurrences is 7.

</td></tr><tr><td id="d280794e177">

**No. of occurrences**

</td><td>

Specify the number of automatic clonings. The maximum value you can enter depends on the value selected for the clone request in the **Clone Frequency** field.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The system displays the **Authenticate Target** modal.

6.  Enter the **Username** and **Password** for an administrator account on the target instance and select **Authenticate**.

7.  To see the cloning schedule for this target, select the **Recurring Clones** tab.

    Each line in the list shows a separate, scheduled cloning session.

8.  To see log messages for past clones on this target, select the **Clone Log** tab.

9.  To see cloning schedules for all the clones in the system, select **Instance Clone** &gt; **Live Clones** &gt; **Clone History**.

    The **Instance Clones** page lists all the cloning instances in the system along with their scheduled clones.


