---
title: Update cost plan related to a resource plan
description: If a resource plan is associated to a project, project task, or demand and has a related cost plan, then a requester or a resource manager can update the related cost plan after updating the resource plan.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Update cost plan related to a resource plan

If a resource plan is associated to a project, project task, or demand and has a related cost plan, then a requester or a resource manager can update the related cost plan after updating the resource plan.

## Before you begin

Role required: resource\_user or resource\_manager or it\_project\_manager or it\_demand\_manager

## About this task

If a resource plan does not have a related cost plan, the **Update Cost Plan** related link is not displayed for the resource plan.

## Procedure

1.  Save the updates to the resource plan.

2.  Click the **Update Cost Plan** related link.

    The cost plan associated to a resource plan is automatically updated as soon as the **Planned cost** in the resource plan is updated. The planned cost on resource plan gets updated when there is a change in:

    -   Planned hours
    -   User
    -   State
    -   Start and end dates

## Result

The cost plan associated to the resource plan is updated as follows:

-   If the resource plan is in Planning or Requested state, planned hours is updated in the cost plan.
-   If the resource plan is in Confirmed/Allocated state and the Confirmed/Allocated hours are less than planned hours, then the higher of the planned cost and Confirmed/Allocated cost is updated in the cost plan.
-   If the resource plan is in Confirmed/Allocated state and the Confirmed/Allocated hours are equal to or more than planned hours, then the Confirmed/Allocated cost is updated in the cost plan.

Cost from resource plan will be interfaced to the unit\_cost field on the Cost Plan \[cost\_plan\] table.

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

[Complete a resource plan](t_CloseAResourcePlan.md)

[Cancel a resource plan](t_CancelAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

