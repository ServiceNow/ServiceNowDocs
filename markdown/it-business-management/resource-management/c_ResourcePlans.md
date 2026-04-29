---
title: Resource plans
description: Resource plans are the key element in resource management.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource plans

Resource plans are the key element in resource management.

**Important:** Resource plans in Resource Management will no longer be available for new customers from future releases.

You're encouraged to work on resource assignments which offers more flexibility [Create resource assignments and operation resource assignments in Resource Management Workspace](../../resource-management-workspace/task/create-ra-rmw.md) using Resource Management Workspace or Project Workspace.

Resource requesters, such as project managers, [create resource plans](../task/t_CreateResourcePlanProjectTask.md) to ask for resources, track effort, and track costs. Resource managers modify and approve resource plans before the plans are used.

All resource plans for a task appear on the **Resource Plan** related list of the Project task form, where resource requesters can access them.

Resource plans progress through several states.

<table id="table_qy4_lx4_4s"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planning

</td><td>

Planning is the default state when a resource requester creates a resource plan. Any plan in this state can be edited. [Requested Allocations](../task/request-allocation.md) are created when a resource plan is in Planning state.

 When a resource requester asks for a change to a plan that was already submitted, the plan reverts to the Planning state.

</td></tr><tr><td>

Requested

</td><td>

Resource requester submits a resource plan for resource managers review by selecting **Submit**. The resource plan then moves into the Requested state. Resource managers confirm and allocate resources or reject the plan, and finally close the plan. The resource requester can request a group, specific users in a group, or a specific user to work on the selected task. After you submit the plan for review, a resource manager can confirm, and then allocate some or all the requested users.

 If the task requires more than one user or groups, multiple resource plans can be created for the given task.

</td></tr><tr><td>

Rejected

</td><td>

Resource manager can reject a resource plan by selecting **Reject**. The resource plan then moves into the Rejected state. Rejected plans stay in that state until changes are made and the requester can re-request the resources.

</td></tr><tr><td>

Confirmed

</td><td>

After the plan is requested, the resource manager can block/confirm the resources for future projects and demands. The resource plan then moves into the Confirmed state. Only a resource manager can modify the plans in Confirmed state.

 Soft allocations are created when the resource plan moves to the Confirmed state.

</td></tr><tr><td>

Allocated

</td><td>

After the plan is confirmed, the resource manager can review the plans, view availability, change resource preferences and perform the resource allocation. The resource plan moves into the Allocated state. A resource manager can only cancel, complete, or modify it.

 Soft allocations are converted to hard allocations when the resource plan moves to the Allocated state.

 **Note:** You can also set a plan to the Allocated state directly from the Requested state using **Confirm and Allocate** option.

</td></tr><tr><td>

Completed

</td><td>

After all associated tasks and projects are complete or canceled, an Allocated resource plan can be completed. This deletes all the resource allocations for the resource plan post the completion date.

</td></tr><tr><td>

Canceled

</td><td>

A plan can be canceled if the allocations are no longer required. This removes all past and future allocations. A canceled resource plan can be brought back to the Planning state if it has no past allocations.Resource plans in Planning, Requested, Confirmed, or Allocated state can be canceled.

</td></tr></tbody>
</table>**Note:** When a resource requester wants to change a plan that was already submitted for review \(in Requested or Confirmed state but not yet allocated\), the requester can [request a change](../task/t_RequestAChangeToAResourcePlan.md). The plan then moves back to the Planning state.

Resource Management supports time zones, which are important in the My Calendar and Resource Workbench modules.

## Modifications in Confirmed or Allocated state

Only a resource manager can modify a resource plan in the Confirmed or Allocated state.

The effects of modification in header area on a resource plan form in Confirmed state are:

-   All soft [allocations](../reference/r_AllocatingResources.md) are deleted.
-   Requested allocations are re-created with changed values.
-   Resource plan moves back to the Requested state.

The effects of modification in header area on a resource plan form in Allocated state are:

-   All resource allocations \(soft and hard\) are deleted.
-   Requested allocations are re-created with changed values.
-   Resource plan moves back to the Requested state.

The resource manager can also modify or delete the past dated resource allocations for Allocated resource plans if no actual hours are recorded for those resource allocation records. When a user submits a time card, upon approval of the time card, actual hours are updated for an allocation record.

**Note:** The resource plan does not move back to the Requested state if the changes are made to allocation records only.

## Request type

You can request a resource plan using one of the following options:

-   Hourly: The request is in terms of the number of hours the resources are necessary.
-   FTE: The request is in terms of an equivalent value that represents full-time work. When the request type is FTE, planned hours are calculated as: `Average Daily FTE * number of working days in resource plan * the FTE value`. The average daily FTE hours are specified in User and Group records. If there is no value specified at User or Group record, the average daily FTE hours is taken from the **Default Average Daily FTE** property.

    The number of working days is calculated based on the users schedule for a user resource or the default schedule for group resources. The default schedule is taken from the Default Schedule Name property.

    For example, say that the average daily FTE for a group is 40 hours, the resource plan period is from September 1 to September 10, and the FTE is 0.5.

    Assuming 8 working days during the plan period, planned hours = `40 * 8 * 0.5` =160 hours.

    **Note:** Capacity is not derived from FTE, but from schedules. Both FTE and schedules must be in synchronization with each other.

-   Person days: The request is in terms of person days. When the request type is person days, planned hours are calculated as: `Total number of person days * Average Daily FTE Hours/Hours Per Person Day`.

    For example, say the Average Daily FTE Hours/Hours Per Person Day for a group is 8 hours, and the person days is 3. Then, planned hours = `8 * 3` = 24 hours.


## Resource plan costs

Resource plan costs can be tracked directly in the [resource plan](../reference/rsrc-plan-form.md) record. Resource plan costs are divided into planned, allocated, and actual.

If the **Rate override** option in a resource plan is selected, the hourly rate for calculating the corresponding resource plan cost is derived from the rate specified in the **Resource rate** field.

If a [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) is associated to the project or demand, the hourly rate is derived from the rate model. Whenever the hourly rates in the associated rate model change, you must [recalculate the resource costs](../task/recalculate-resource-costs.md) of the resource plan to reflect the new rates.

If rate model is not available, the hourly rate for calculating the corresponding resource plan cost is derived from labor rate card.

Projects and Demands can have multiple resource plans. The aggregated costs for all resources plans roll up to the **Planned Cost** and **Allocated Cost** fields and the **Resource Cost** section of both projects and demands.

-   **[Create a resource plan](../task/t_CreateResourcePlanProjectTask.md)**  
You can create a resource plan from the Resource Management application for any task such as demand, project, project task, incident, problem, or change. You can edit and adjust the plan until you submit it for approval.
-   **[Use Resource Finder to analyze resource availability](../task/create-resource-plan-with-finder.md)**  
Search and analyze resource availability using the Resource Finder, so that you can create resource plans for a project or demand.
-   **[Create an operational resource plan](../task/create-operational-plan.md)**  
Create an operational resource plan and allocate a certain portion of your team capacity for operational work, such as administration, meeting, or training.
-   **[Request resources](../task/t_RequestResourcePlanApproval.md)**  
After you create a resource plan, request resources from the resource manager.
-   **[Confirm a resource plan](../task/confirm-resource-plan.md)**  
As a resource manager, you can confirm or block the resources after a resource plan is requested. The resource plan must be in the Requested state to be confirmed.
-   **[Confirm and allocate a resource plan](../task/confirm-allocate-resource-plan.md)**  
After the resource plan is requested, as a resource manager, you can directly allocate the resources. To confirm and allocate, the resource plan must be in the Requested state.
-   **[Request a change to a resource plan](../task/t_RequestAChangeToAResourcePlan.md)**  
Request a change to the resource plan to modify a resource plan after you’ve submitted it for review.
-   **[Recalculate costs of a resource plan of a project or demand](../task/recalculate-resource-costs.md)**  
Recalculate the resource costs of an individual resource plan for a project or demand whenever the hourly rates change in the associated rate model.
-   **[Update cost plan related to a resource plan](../task/t_UpdateRelatedCostPlan.md)**  
If a resource plan is associated to a project, project task, or demand and has a related cost plan, then a requester or a resource manager can update the related cost plan after updating the resource plan.
-   **[Complete a resource plan](../task/t_CloseAResourcePlan.md)**  
After all associated tasks and projects are complete or canceled, a resource manager can move the resource plan to the **Complete** state, which closes it.
-   **[Cancel a resource plan](../task/t_CancelAResourcePlan.md)**  
If a resource plan is no longer needed, you can cancel it which also cancels its past and future allocations.
-   **[Delete a resource plan](../task/t_DeleteAResourcePlan.md)**  
Deleting a plan also deletes all associated resource allocations.
-   **[Extend a resource plan](../task/extend-resource-plan.md)**  
You can extend the date of an allocated resource plan and allocate resources for the extended period.
-   **[Request extension of an allocated resource plan](../task/request-extension-allocated-resource-plan.md)**  
As a project manager, you can request the extension of an allocated resource plan.
-   **[Allocate resources for the extended period](../task/allocate-resources-for-extended-period.md)**  
As a resource manager, you can allocate resources for the extended period.
-   **[Reduce the duration of a resource plan](../task/reduce-resource-plan.md)**  
Reduce the duration of an allocated or confirmed resource plan and deallocate resources in one action without having to do it individually for each resource.
-   **[Time zones in resource plans](c_TimeZonesInResourcePlans.md)**  
Time zones are important in resource management when the users and groups doing the resource tasks are located in different locations.
-   **[Associate a time card with a resource plan](../task/t_AssocATimeCardWithAResourcePlan.md)**  
If one resource is allocated to identically named tasks in two resource plans, use the following procedure to specify the resource plan the time card should be allocated to.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

