---
title: View and assign scheduled tasks
description: Learn about different ways to view tasks in the Scheduled state​.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# View and assign scheduled tasks

Learn about different ways to view tasks in the Scheduled state​.

## Before you begin

-   **A Work order task is moved to the Scheduled state only when all the following conditions are met:**
    -   The Use scheduled state property is enabled​
    -   The Assigned to field is not empty​
    -   The Assigned to or Expected start field changes, and the Expected start value is beyond the threshold \(12 hours by default\) from current time​
-   **Exceptions for the Scheduled state flow**
    -   Contractor tasks will not be in the Scheduled state.
    -   When an agent time-off event is created and overlaps with the work order task, the task will be moved to Pending dispatch. Similarly, for crew tasks, when the leader has a time-off event overlapping with the task time, the task will be moved to Pending dispatch.​
    -   If all child work order tasks of the work order are in the Scheduled state, the work order will be moved to Scheduled automatically.
    -   When dynamic scheduling is enabled, auto-assign is not available for scheduled tasks. Scheduled tasks are considered for re-assignment or un-assignment​.
    -   Scheduled tasks appear as blocked time when intelligent task recommendation considers technician availability.​

Role required: wm\_dispatcher, wm\_admin, and wm\_agent

## Procedure

1.  You can view tasks in the Scheduled state in one of the following roles​.

<table id="choicetable_upk_mcy_3sb"><thead><tr><th align="left" id="d133131e98">

role

</th><th align="left" id="d133131e101">

steps

</th></tr></thead><tbody><tr><td id="d133131e107">

**wm\_dispatcher**

</td><td>

1.  Navigate to **Field Service** &gt; **Dispatching** &gt; **My Scheduled Tasks**.
2.  View the list of scheduled tasks in the dispatcher group.


</td></tr><tr><td id="d133131e137">

**wm\_admin**

</td><td>

1.  Navigate to **Field Service** &gt; **Dispatching** &gt; **Scheduled Tasks**.
2.  View the list of all scheduled tasks.


</td></tr><tr><td id="d133131e167">

**wm\_agent**

</td><td>

1.  Log in to the mobile application.
2.  Tasks in the Scheduled state can be viewed in
    -   My Group Tasks applet
    -   Sibling Work Order Tasks related list on the WO screen
    -   Work Order Tasks related list on the WO screen
    -   Upcoming Work Orders related list on the Asset screen​


</td></tr></tbody>
</table>2.  Move scheduled work order tasks to the Assigned state using one of the methods.

<table id="simpletable_mw5_f5y_3sb"><thead><tr><th>

Method

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Manually move from Scheduled to Assigned

</td><td>

1.  Open a scheduled work order task in the form or list view.
2.  Click the **Confirm Assignment** button.
3.  Click **Save**.
​

</td></tr><tr><td>

Automatically move from Scheduled to Assigned

</td><td>

1.  Navigate to **Field Service** &gt; **Administration** &gt; **Scheduled Task Assignment confirmation**.
2.  To move all scheduled tasks to Assigned automatically, check the **Active** check box​.

It runs every hour by default to move the tasks within the threshold from Scheduled to Assigned​. To modify the frequency, admins can update the value of the Repeat Interval field.

</td></tr></tbody>
</table>
-   **[Update scheduled tasks on Dispatcher Workspace](scheduled-tasks-workspace.md)**  
As a dispatcher, you can move scheduled tasks to the Assigned state or move them back to the Pending dispatch state in Dispatcher Workspace.

**Parent Topic:**[Scheduling and dispatching work order tasks to agents](../concept/scheduling-and-dispatching-agents.md)

