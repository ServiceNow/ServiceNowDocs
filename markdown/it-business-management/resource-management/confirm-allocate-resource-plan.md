---
title: Confirm and allocate a resource plan
description: After the resource plan is requested, as a resource manager, you can directly allocate the resources. To confirm and allocate, the resource plan must be in the Requested state.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Confirm and allocate a resource plan

After the resource plan is requested, as a resource manager, you can directly allocate the resources. To confirm and allocate, the resource plan must be in the Requested state.

## Before you begin

**Important:** Resource plans in Resource Management will no longer be available for new customers from future releases.

You're encouraged [migrate your existing resource plans](../concept/rsrc-plans-rsrc-asgmnts.md) to work on resource assignments which offers more flexibility and [Create resource assignments and operation resource assignments in Resource Management Workspace](../../resource-management-workspace/task/create-ra-rmw.md) using Resource Management Workspace or Project Workspace.

Resource managers can [assign and approve the unassigned resource assignments](../../resource-management-workspace/task/allocate-resources-rmw.md) using Resource Management Workspace.

Role required: resource\_manager

## About this task

Modify or [cancel](t_CancelAResourcePlan.md) a resource plan that is in the Allocated state.

If the resource type in a resource plan is a group, you can request resources only if that group has active members.

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **Requested**.

2.  Open the resource plan \(Requested\) that you want to confirm and allocate, and select **Confirm and Allocate**.


## Result

The resource plan automatically moves to the Allocated state from the Requested state. Soft allocations are converted to [hard allocations](../reference/r_AllocatingResources.md) when the resource plan moves to the Allocated state.

Any errors or warnings during allocations are logged in the Resource Plan Logs related list on the Resource Plan form. The log is generated if a resource is allocated over 24 hours for a given day. You can review these logs to take correct actions for further resource allocation.

**Parent Topic:**[Resource plans](../concept/c_ResourcePlans.md)

**Related topics**  


[Create a resource plan](t_CreateResourcePlanProjectTask.md)

[Use Resource Finder to analyze resource availability](create-resource-plan-with-finder.md)

[Create an operational resource plan](create-operational-plan.md)

[Request resources](t_RequestResourcePlanApproval.md)

[Confirm a resource plan](confirm-resource-plan.md)

[Request a change to a resource plan](t_RequestAChangeToAResourcePlan.md)

[Recalculate costs of a resource plan of a project or demand](recalculate-resource-costs.md)

[Update cost plan related to a resource plan](t_UpdateRelatedCostPlan.md)

[Complete a resource plan](t_CloseAResourcePlan.md)

[Cancel a resource plan](t_CancelAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

