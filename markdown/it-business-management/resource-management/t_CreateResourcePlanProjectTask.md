---
title: Create a resource plan
description: You can create a resource plan from the Resource Management application for any task such as demand, project, project task, incident, problem, or change. You can edit and adjust the plan until you submit it for approval.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a resource plan

You can create a resource plan from the Resource Management application for any task such as demand, project, project task, incident, problem, or change. You can edit and adjust the plan until you submit it for approval.

## Before you begin

**Important:** Resource plans in Resource Management will no longer be available for new customers from future releases.

You're encouraged to [migrate your existing resource plans](../concept/rsrc-plans-rsrc-asgmnts.md) to work on resource assignments which offers more flexibility. [Create resource assignments and operation resource assignments in Resource Management Workspace](../../resource-management-workspace/task/create-ra-rmw.md) using Resource Management Workspace or Project Workspace.

Role required: resource\_user, resource\_manager, it\_project\_manager, demand\_manager, admin

## Procedure

1.  Create a resource plan using one of the following options.

<table id="choicetable_dws_ntk_xp"><tbody><tr><td id="d53522e119">

**From Resource tab in project workspace**

</td><td>

1.  Open a project record in project workspace. See [Access the new Project Workspace](../../project-workspace/task/access-new-project-workspace.md).
2.  On the **Resources** tab, click **New**.


</td></tr><tr><td id="d53522e153">

**From a project form**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open a project record.
3.  In the **Resource Plan** related list, click **New**.


</td></tr><tr><td id="d53522e192">

**From a demand form**

</td><td>

1.  Navigate to **Demand** &gt; **Demands** &gt; **All**.
2.  Open a demand.
3.  In the **Resource Plans** related list, click **Manage**.
4.  On the Resource Plans page, click **New**.


</td></tr><tr><td id="d53522e237">

**From a project task**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open a project record.
3.  Click the **Details** tab.
4.  In the **Project Tasks** related list, open a task.
5.  In the **Resource Plan** related list, click **New**.


</td></tr><tr><td id="d53522e288">

**From an existing resource plan**

</td><td>

1.  Open the resource plan record that you want to copy.
2.  In the related links, click **Copy Resource Plan**.
 **Note:** When you create a resource plan from an existing resource plan, all fields are copied to the new resource plan. The new plan is created in the Planning state.

</td></tr></tbody>
</table>2.  On the Resource Plan form, fill the fields.

    For a field descriptions of the field names, see [Resource Plan form](../reference/rsrc-plan-form.md).

3.  Click **Save** on the form header.

    The resource plan is saved and placed in the Planning state.

4.  Review update the values in the Resource Plan form tabs.

    For a field description of the field names, see [Resource Plan form tabs](../reference/rsrc-plan-form-tabs.md).

    **Note:** If the assigned rate model is removed or replaced, or the hourly rates in the rate model are changed, the cost fields on the associated resource plans are not recalculated automatically. You must [recalculate the resource costs](recalculate-resource-costs.md) of the resource plan to reflect new rates from the rate model.

    However, if any of the fields affecting the cost are updated on the resource plan, the rate model is invoked for getting the hourly rates. For example, extending a resource plan by modifying the end date of the resource plan invokes the rate model as there can be new rates available.


## Result

-   The resource plan is saved and placed in the Planning state.
-   When the resource plan is created from resource grid, the plan appears as top row in the resource plan list of the project or demand. The plan has one of the following prefixes:

    -   \[G\] for a resource plan created for a group.
    -   \[R\] for a role resource plan created for a role.
    -   \[U\] for a user resource plan created for a user.
    The prefix is based on the type of resource selected in the **Resource type** field.

-   The resource plan which is created last appears at the top in the resource plan list of the project or demand.

## What to do next

Use the [Resource Plan related links and lists](../reference/rsrc-plan-rltd-links-lists.md) to work on the resource plans, workbenches, or to modify the existing request allocations.

**Parent Topic:**[Resource plans](../concept/c_ResourcePlans.md)

**Related topics**  


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

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

