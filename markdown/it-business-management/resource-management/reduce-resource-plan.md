---
title: Reduce the duration of a resource plan
description: Reduce the duration of an allocated or confirmed resource plan and deallocate resources in one action without having to do it individually for each resource.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Reduce the duration of a resource plan

Reduce the duration of an allocated or confirmed resource plan and deallocate resources in one action without having to do it individually for each resource.

## Before you begin

**Important:** Resource plans in Resource Management will no longer be available for new customers from future releases.

You're encouraged [migrate your existing resource plans](../concept/rsrc-plans-rsrc-asgmnts.md) to work on resource assignments which offers more flexibility and start using Resource Management Workspace.

Resource requester can [move an assigned or unassigned resource assignment](../../resource-management-workspace/task/move-ra-rmw.md) using Resource Management Workspace.

Role required: resource\_user, resource\_manager

## About this task

You can reduce an allocated or confirmed resource plan only if the resource plan's end date is later than the current date.

You can reduce the duration of an operational resource plan only if its state is allocated.

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **All**.

2.  Open a resource plan and select **Reduce**.

    Reducing the resource plan end date releases all resources by deleting resource allocations after the new end date.

    If no actuals are posted for the future in the resource plan, then all the allocated or confirmed hours of the resources will be released when you reduce the resource plan.

    If actuals are posted for the future, then the resource plan end date is updated to the future date on which actuals are present, and all allocated or confirmed hours of all the resources from the date on which actuals are present to the original end date are released.

3.  Enter the new end date of the resource plan in the **End date** field.

4.  Select **Yes** in the confirmation message.


## Result

-   The end date of the resource plan is updated to the new reduced end date.
-   The state of the resource plan remains the same.
-   If no actuals are posted for the future in the resource plan, all allocated or confirmed hours of the resources are released.
-   If actuals are posted for the future, then the resource plan end date is updated to the future date on which actuals are present, and all the allocated or confirmed hours of all the resources from the date on which actuals are present to the original end date are released.

## Resource allocation concerning actuals

Say a resource plan was created for 1 FTE from January 1, 2021, to December 31, 2021, and on March 1, 2021, the resource plan end date was updated to March 1, 2021. Then, all the allocated or confirmed hours of the resources on this plan between March 1, 2021, to December 31, 2021, would be released. If actuals are posted for the future, for example, May 25, 2021, then the resource plan end date will be updated to May 25, 2021, and all confirmed or allocated hours between March 1, 2021 to December 31, 2021 will be released.

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

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

