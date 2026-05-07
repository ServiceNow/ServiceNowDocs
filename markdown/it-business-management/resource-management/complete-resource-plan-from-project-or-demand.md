---
title: Complete a resource plan from a project, planning console, or demand record
description: If a project or a project task is marked Closed, the project manager can complete the associated Allocated resource plans. Similarly, the demand manager can complete the resource plans for a Closed or Deferred demand.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Complete a resource plan, Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Complete a resource plan from a project, planning console, or demand record

If a project or a project task is marked Closed, the project manager can complete the associated Allocated resource plans. Similarly, the demand manager can complete the resource plans for a Closed or Deferred demand.

## Before you begin

The resource plan to be completed must be in the Allocated state.

Role required: it\_project\_manager or it\_demand\_manager

## About this task

When a project or a project task moves to Closed Complete, Closed Incomplete or Closed Skipped state, the system prompts a message on the project and project task forms, and in the planning console for completing the Allocated resource plans if the following conditions is met.

-   Corresponding resource plan is in the Allocated state.
-   Resource plan start date is less than or equal to the project or task actual end date.

A similar message for completing the resource plans appears on the Demand form when a demand moves to Closed or Deferred state.

## Procedure

1.  Open a project, task, or demand record in the Closed state.

<table id="choicetable_en2_dhy_bcb"><tbody><tr><td id="d108049e82">

**Open a Closed project record**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the project record in the Closed state.
3.  Select the **Details** tab to display the project form.


</td></tr><tr><td id="d108049e118">

**Open a Closed project task record**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the required project record.
3.  In the **Project Tasks** related list, open the project task record in the Closed state.


</td></tr><tr><td id="d108049e154">

**Open a Closed project in Planning Console**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the project record in the Closed state.
3.  Select the **Planning** tab to display the project in planning console.


</td></tr><tr><td id="d108049e190">

**Open a Closed or Deferred demand record**

</td><td>

1.  Navigate to **Demand** &gt; **Demands** &gt; **All**.
2.  Open the demand record in the Closed or Deferred state.


</td></tr></tbody>
</table>    The message for completing the associated resource plans appears at the top of the record.

    ![Screenshot for completing a resource plan message](../image/ResourcePlanCompleteMessage.png "Message for completing a resource plan")

    **Note:** In the Planning Console, irrespective of the Closed state of the project tasks, the message appears only when the project is in Closed state.

2.  To open the list of resource plans to be completed, select the link in the message.

    **Note:** In Planning Console, alternatively right-click the project and select **Complete Resource Plans**.

    -   The list contains only those resource plans for the record that should be completed.
    -   If the list is opened from the message link on a Project form, the resource plans for the project and project task are listed.
    -   If the list is opened from the message link on a Project task form, only the resource plans for the project task are listed.
3.  In the list, select the resource plan to be completed, and select **Complete**.

4.  In the **Confirm** dialog box, select the completion date of the resource plan and select **Yes**.

    By default, the system date or resource plan end date, whichever is earlier, is populated in **Completion Date**.

    **Note:** The **Completion Date** cannot be earlier than the resource plan start date.


## Result

-   The selected resource plan moves to the Completed state.
-   If the completion date is earlier than the resource plan end date, the end date of the resource plan is updated with the completion date. If the completion date was entered later than the resource plan end date, the resource plan end date is retained.
-   All the requested and resource allocations for the resource plan that are past the completion date are deleted. If there are any actual hours logged against an allocation, that allocation record is not deleted. But the allocated hours become zero and the actual hours are retained. The available and allocated hours for the resources are also updated in the aggregate tables.

**Parent Topic:**[Complete a resource plan](t_CloseAResourcePlan.md)

