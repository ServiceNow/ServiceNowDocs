---
title: Cancel a resource plan from a project, planning console, or demand record
description: If a project or a project task is marked Closed, the project manager can cancel the associated future resource plans. Similarly, the demand manager can cancel the future resource plans for a Closed or Deferred demand.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cancel a resource plan, Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Cancel a resource plan from a project, planning console, or demand record

If a project or a project task is marked Closed, the project manager can cancel the associated future resource plans. Similarly, the demand manager can cancel the future resource plans for a Closed or Deferred demand.

## Before you begin

The resource plan to be canceled must be in Confirmed, Planning, or Requested state. An Allocated resource plan can be canceled if the resource plan start date is later than the project, task, or demand end date.

Role required: it\_project\_manager or it\_demand\_manager

## About this task

When a project or a project task moves to Closed Complete, Closed Incomplete or Closed Skipped state, the system prompts a message on the project and project task forms, and in the planning console for canceling the resource plans if one of the following conditions is met.

-   Corresponding resource plan is in Confirmed, Planning, or Requested state.
-   Resource plan is in Allocated state with start date later than the project or task end date.

A similar message for canceling the resource plans appears on the demand form when a demand moves to Closed or Deferred state.

## Procedure

1.  Open a project, task, or demand record in the Closed state.

<table id="choicetable_en2_dhy_bcb"><tbody><tr><td id="d296175e98">

**Open a Closed project record**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the project record in the Closed state.
3.  Click the **Details** tab to display the project form.


</td></tr><tr><td id="d296175e137">

**Open a Closed project task record**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the required project record.
3.  In the **Project Tasks** related list, open the project task record in the Closed state.


</td></tr><tr><td id="d296175e176">

**Open a Closed project in Planning Console**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the project record in the Closed state.
3.  Click the **Planning** tab to display the project in planning console.


</td></tr><tr><td id="d296175e215">

**Open a Closed or Deferred demand record**

</td><td>

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.
2.  Open the demand record in the Closed or Deferred state.


</td></tr></tbody>
</table>    The message for canceling the associated resource plans appears at the top of the record.

    ![Screenshot for canceling a resource plan message](../image/ResourcePlanCancelMessage.png "Message for canceling a resource plan")

    **Note:** In the Planning Console, irrespective of the Closed state of the project tasks, the message appears only when the project is in Closed state.

2.  To open the list of resource plans to be canceled, click the link in the message.

    **Note:** In the Planning Console, alternatively right-click the project and select **Cancel Resource Plans** .

    -   The list contains only those resource plans for the record that can be canceled.
    -   If the list is opened from the message link on a Project form, the resource plans for the project and project task are listed.
    -   If the list is opened from the message link on a Project task form, only the resource plans for the project task are listed.
3.  In the list, select the resource plan to be canceled, and click **Cancel**.


## Result

-   The selected resource plan moves to the Canceled state.
-   All past and future allocations for the resource plan are canceled. If there are any actual hours logged against an allocation, that allocation is deleted. In this case, Allocated hours become zero and the actual hours are retained as is.

**Parent Topic:**[Cancel a resource plan](t_CancelAResourcePlan.md)

