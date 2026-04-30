---
title: Schedule cloning
description: You can use System Clone to schedule automatic cloning, which is the easiest way to keep your cloned instances up to date.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule cloning

You can use System Clone to schedule automatic cloning, which is the easiest way to keep your cloned instances up to date.

## Before you begin

Role required: admin

## About this task

Instead of manually cloning instances, you can schedule cloning that happens automatically. You create a cloning schedule in the same interface you use to [create a clone](t_StartAClone.md). This topic assumes that you created a clone but not a cloning schedule for it.

## Procedure

1.  Click **System Clone** &gt; **Active Clones** &gt; **&lt;one-of-your-clones&gt;**.

2.  **Note:** \(Optional\) if the **Options** panel is not already displayed.

    Click the **Options** arrowhead so it turns downward.

    The **Options** panel appears.

    ![](../image/schedule-conflict-calendar.png)

3.  **Note:** A target instance must be selected or an error message appears.

    Select the **Conflict calendar** to view a calendar with their current clone time and potential conflicts if you want to schedule for a different time.

    The conflict calendar appears in a new tab.![](../image/schedule-conflict-calendar-view.png)

4.  Enter values in the following fields to schedule automatic clonings.

<table id="choicetable_wdr_dfs_fhb"><thead><tr><th align="left" id="d241257e134">

Field

</th><th align="left" id="d241257e137">

Description

</th></tr></thead><tbody><tr><td id="d241257e143">

**Clone frequency**

</td><td>

Defines how often this target automatically receives clone data and the maximum number of occurrences. -   Weekly – The maximum number of occurrences is 25.
-   Bi-Weekly – The maximum number of occurrences is 13.
-   Monthly – The maximum number of occurrences is 7.

</td></tr><tr><td id="d241257e171">

**No. of occurrences**

</td><td>

Specify the number of automatic clonings. The maximum value you can enter depends on the value selected for the clone request in the **Clone Frequency** field.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The system displays the **Authenticate Target** modal.

6.  Enter the **Username** and **Password** for an administrator account on the target instance and click **Authenticate**.

    The System Clone form displays for the target clone.

7.  To see the cloning schedule for this target, click the **Recurring Clones** tab.

    Each line in the list shows a separate, scheduled cloning session.

8.  To see log messages for past clonings on this target, click the **Clone Log** tab.

9.  To see cloning schedules for all the clones in the system, click **System Clone** &gt; **Live Clones** &gt; **Clone History**.

    The **System Clones** page lists all the cloning instances in the system along with their scheduled clonings.


