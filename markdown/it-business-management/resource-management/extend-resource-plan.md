---
title: Extend a resource plan
description: You can extend the date of an allocated resource plan and allocate resources for the extended period.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Extend a resource plan

You can extend the date of an allocated resource plan and allocate resources for the extended period.

## Before you begin

**Important:** Resource plans in Resource Management will no longer be available for new customers from future releases.

You're encouraged [migrate your existing resource plans](../concept/rsrc-plans-rsrc-asgmnts.md) to work on resource assignments which offers more flexibility and start using Resource Management Workspace.

Resource requester can [extend an assigned or unassigned resource assignment](../../resource-management-workspace/task/manage-resource-allocations-rmw.md) using Resource Management Workspace.

Role required: resource\_manager

## About this task

Assume that work on a project has started, but there is a need to extend the date of an allocated resource plan because the project has been extended. In this scenario, you can extend the date of the allocated resource plan. The new date by which the resource plan is extended does not have any impact on the existing allocated hours. While extending the resource plan, you can specify the new end date and the request type. Based on the request type selected, the required allocated hours are auto-filled.

For example, assume that you allocated 100 hours for 2 months, 50 hours for each month. Now, you want to extend the resource plan by one month. For the extended month, allocation records are created based on the request type selected.

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **All**.

2.  Open a resource plan and select **Extend Resource Plan**.

3.  Select **OK**.

4.  In the Extend resource plan dialog box, fill in the fields.

    For a description of the field names, see [Extend resource plan form](../reference/extnd-rsrc-plan.md).


## Result

-   The end date of the resource plan is updated.
-   The **Extension** field displays the state as Allocated.
-   For the extended period, allocation records are created based on the request type selected.
-   Number of requested FTE or hours or person days is divided equally for each allocation period and is pre-filled in each allocation record.
-   Extending the resource plan invokes the rate model for getting the hourly rates.

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

[Cancel a resource plan](t_CancelAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

