---
title: Cancel a resource plan
description: If a resource plan is no longer needed, you can cancel it which also cancels its past and future allocations.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Cancel a resource plan

If a resource plan is no longer needed, you can cancel it which also cancels its past and future allocations.

## Before you begin

The resource plan to be canceled must be in the Planning, Requested, Confirmed, or Allocated state.

Role required: resource\_manager

## About this task

Project and demand managers can also [cancel resource plans from a project, project task, planning console, or demand](cancel-resource-plan-from-project-or-demand.md).

**Note:** You can also cancel a resource plan from the [Allocation Workbench](manage-resources-allocation-workbench.md).

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **All**.

2.  Open the resource plan record that you want to cancel.

3.  On the form header, select **Cancel**.


## Result

-   The resource plan moves into the Cancelled state.
-   All past and future allocations for the resource plan are also canceled. If there are any actual hours logged against an allocation, that allocation isn’t deleted. But the allocated hours become zero and the actual hours are retained.

## What to do next

If you want to make changes and use the plan again, edit a canceled plan. To move the resource plan back to Planning state, select **Re-plan**.

**Note:** The state of a resource plan can be changed back from Cancelled to Planning, only if it has no past allocations.

-   **[Cancel a resource plan from a project, planning console, or demand record](cancel-resource-plan-from-project-or-demand.md)**  
If a project or a project task is marked Closed, the project manager can cancel the associated future resource plans. Similarly, the demand manager can cancel the future resource plans for a Closed or Deferred demand.

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

[Complete a resource plan](t_CloseAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

