---
title: Accept or reject a work order task
description: Accept a work order task that has been assigned to you. You can reject the task if, for example, you do not have the required skills or you are not available at the required time.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Accept or reject a work order task

Accept a work order task that has been assigned to you. You can reject the task if, for example, you do not have the required skills or you are not available at the required time.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## About this task

Unlike other work order tasks, the task card for a work order task related to a linear asset includes the start and end location details. This information helps agents identify that the task is specific to a linear asset and provides them with a clear understanding of the segment they need to focus on while executing the task.

## Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **My Work**.

3.  Perform one of the following actions.

<table id="choicetable_udq_gsr_4fb"><thead><tr><th align="left" id="d110736e95">

Option

</th><th align="left" id="d110736e98">

Details

</th></tr></thead><tbody><tr><td id="d110736e104">

**Accept a task**

</td><td>

Do one of the following:

 -   To accept a task from the work order task list, select the desired task, swipe to the left and select **Accept**.
-   To accept a task after reviewing the work order task details:
    -   Select and open the desired task.
    -   Review the task details.
    -   Tap **Accept**.
When you accept a task, the work order task state changes to **Accepted**.

</td></tr><tr><td id="d110736e145">

**Reject a task**

</td><td>

Do one of the following:

 -   To reject a task from the work order task list, select the desired task, swipe to the left and select **Reject**.
-   To reject a task after reviewing the work order task details:

    -   Select and open the desired task.
    -   Review the task details.
    -   Tap **Reject**.
The Reject Task pop-up appears.

-   From the **Reason** list, select a reason for the rejecting the task.

Available options:

    -   Schedule conflict – you have another appointment scheduled for the same time window.
    -   Skills mismatch – the skills you have do not match the skills required to work on the task.
    -   Location mismatch – the location specified for the task is not the location you could work.
    -   Duplicate task – another record of this task exists.
    -   Parts unavailable – you do not have the required parts to work on this task.
    -   Customer unavailable – customer is not available for the scheduled task time-window.
    -   Other – any reason other than the ones listed earlier.
-   In the **Details** field, enter additional information for rejecting the task. This field will be mandatory if you choose Other from the **Reason** list.
-   Do one of the following:
    -   On an iOS device, tap **Submit**.
    -   On an Android device, tap the done icon.
 The reason for rejecting the task is populated in the work notes and the task moves to **Pending Dispatch** state.

 **Note:** The rejected task is not dynamically scheduled to the same agent for the next 24 hours. This is controlled by the **work.management.rejected.technician.duration** [system property](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md). However, as an agent you can manually assign the work order task back to yourself or as a dispatcher you can assign it back to the same agent.

</td></tr></tbody>
</table>
## What to do next

Start work on a task using the Now Mobile Agent application.

