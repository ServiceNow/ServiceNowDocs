---
title: Complete a resource plan
description: After all associated tasks and projects are complete or canceled, a resource manager can move the resource plan to the Complete state, which closes it.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Complete a resource plan

After all associated tasks and projects are complete or canceled, a resource manager can move the resource plan to the **Complete** state, which closes it.

## Before you begin

The resource plan to be completed must be in the Allocated state.

Role required: resource\_manager

## About this task

Project and demand managers can [complete resource plans from a project, project task, planning console, or demand](complete-resource-plan-from-project-or-demand.md).

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **Allocated**.

2.  Open the resource plan that you want to complete.

3.  Verify all the information on the form.

    **Note:** The **Actual Hours** and **Actual Cost** fields show the time spent on plan tasks and the resource costs. These fields are derived from time card information and can’t be edited on the resource plan.

4.  Add notes.

5.  Select **Complete**.

6.  In the **Confirm** dialog box, select the completion date of the resource plan and select **Yes**.

    By default, the system date or resource plan end date, whichever is earlier, is populated in **Completion Date**.

    **Note:** The **Completion Date** can’t be earlier than the resource plan start date.


## Result

-   The resource plan moves to the Completed state.
-   If the completion date is earlier than the resource plan end date, the end date of the resource plan is updated with the completion date. If the completion date was entered later than the resource plan end date, the resource plan end date is retained.
-   All the requested and resource allocations for the resource plan post the completion date are deleted. If there are any actual hours logged against an allocation, that allocation record isn’t deleted. But the allocated hours become zero and the actual hours are retained. The available and allocated hours for the resources are also updated in the aggregate tables.

## Example

Example 1: A resource plan of Allocation type **Monthly** from 1 November to 31 January is completed on 15 December. On completion,

-   the resource allocation entry for January is deleted from the \[Resource\_Allocation\] table.
-   the resource allocation end date for December is updated to the completion date of the resource plan.
-   the entries in the \[Resource\_Allocation\_Daily\] table for the December month post the completion date are deleted.

Example 2: If the same resource plan has Allocation type as **Planned Duration**, no allocations are deleted, and the end date of the allocation is updated to the completion date.

-   **[Complete a resource plan from a project, planning console, or demand record](complete-resource-plan-from-project-or-demand.md)**  
If a project or a project task is marked Closed, the project manager can complete the associated Allocated resource plans. Similarly, the demand manager can complete the resource plans for a Closed or Deferred demand.

**Parent Topic:**[Resource plans](../concept/c_ResourcePlans.md)

**Related topics**  


[Create a resource plan](t_CreateResourcePlanProjectTask.md)

[Use Resource Finder to analyze resource availability](create-resource-plan-with-finder.md)

[Create an operational resource plan](create-operational-plan.md)

[Request resources](t_RequestResourcePlanApproval.md)

[Confirm a resource plan](confirm-resource-plan.md)

[Confirm and allocate a resource plan](confirm-allocate-resource-plan.md)

[Request a change to a resource plan](t_RequestAChangeToAResourcePlan.md)

[Recalculate costs of a resource plan of a project or demand](recalculate-resource-costs.md)

[Update cost plan related to a resource plan](t_UpdateRelatedCostPlan.md)

[Cancel a resource plan](t_CancelAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

