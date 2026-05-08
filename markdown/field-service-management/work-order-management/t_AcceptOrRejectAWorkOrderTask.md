---
title: Accept or reject a work order task
description: Accept a work order task if you are ready to work on that task. Reject the task and provide a reason if you cannot work on that task.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Execute work order tasks, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Accept or reject a work order task

Accept a work order task if you are ready to work on that task. Reject the task and provide a reason if you cannot work on that task.

## Before you begin

Role required: wm\_agent

## About this task

The task must be in **Assigned** state for an agent to accept or reject the task. Dispatchers can view the task rejection history in the work order tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

    You can view a list of all work order tasks assigned to you.

2.  Open a work order task.

3.  Accept or reject the task.

<table id="choicetable_mqd_4y5_djb"><thead><tr><th align="left" id="d110929e116">

To

</th><th align="left" id="d110929e119">

Do the following

</th></tr></thead><tbody><tr><td id="d110929e125">

**Accept the task**

</td><td>

Click **Accept**. The work order task moves to **Accepted** state.

</td></tr><tr><td id="d110929e140">

**Reject the task.**

</td><td>

1.  Click **Reject**.

The Reject Task pop-up appears.

2.  From the **Reason** list, select a reason for the rejecting the task.

Available options:

    -   Schedule conflict – you have another appointment scheduled for the same time window.
    -   Skills mismatch – the skills you have do not match the skills required to work on the task.
    -   Location mismatch – the location specified for the task is not the location you could work.
    -   Duplicate task – another record of this task exists.
    -   Parts unavailable – you do not have the required parts to work on this task.
    -   Customer unavailable – customer is not available for the scheduled task time-window.
    -   Other – any reason other than the ones listed earlier.
3.  In the **Details** field, enter additional information for rejecting the task.
4.  Click **OK**.

The reason for rejecting the task is populated in the work notes and the task moves to **Pending Dispatch** state.

 **Note:** The rejected task is not dynamically scheduled to the same agent for the next 24 hours. This is controlled by the work.management.rejected.technician.duration [system property](../reference/r_PropInstallWFieldServMgmnt.md). However, as an agent you can manually assign the work order task back to yourself or as a dispatcher you can assign it back to the same agent.

</td></tr></tbody>
</table>    ![accept and reject buttons](../../field-service-management/image/accept-reject-task.png)


## Result

In case an agent accepts a successor \(downstream\) task that is dependent on another task, the successor \(downstream\) task can be started before the predecessor \(upstream\) task is complete.

When the agent selects **Start Work**, a message states that open task dependencies exist and asks if the agent wants to start work.

