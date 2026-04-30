---
title: Recalculate costs of a resource plan of a project or demand
description: Recalculate the resource costs of an individual resource plan for a project or demand whenever the hourly rates change in the associated rate model.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Recalculate costs of a resource plan of a project or demand

Recalculate the resource costs of an individual resource plan for a project or demand whenever the hourly rates change in the associated rate model.

## Before you begin

Ensure the following setup:

-   The project or demand must have an active rate model assigned.
-   The resource plan must be in either Planned, Requested, Confirmed, or Allocated states.

Role required: resource\_manager

## About this task

To update the costs of all the resource plans of a project or demand in one go, you can use the **Recalculate Resource Costs** option from the [project form](../../project-management/task/recalculate-resource-costs-of-a-project.md) or [demand form](../../planning-and-policy/task/recalculate-resource-costs-of-a-demand.md).

## Procedure

1.  To open a resource plan of a project or demand, perform one of the following actions.

    -   Navigate to **Project** &gt; **Projects** &gt; **All**, and open a project.
    -   Navigate to **Demand** &gt; **Demands** &gt; **All**, and open a demand.
2.  From the **Resource Plans** related list, open a resource plan for which you want to recalculate the costs.

3.  On the Resource Plan form, select the **Recalculate Resource Cost** related link.

4.  In the Recalculate Resource Costs dialog box, specify the recalculation period in the **Start date** and **End date** fields.

    By default, the **Start date** field has the current date and the **End date** field has the end date of the resource plan.

5.  To recalculate the planned cost, select the **Include planned costs** option.

    The **Include planned costs** option is available for a resource plan in the Confirmed or Allocated state. The option isn’t selected by default.

6.  Select **OK**.


## Result

-   Recalculates the selected resource costs based on the latest hourly rates derived from the rate model associated with the project or demand.
-   Updates the recalculated resource costs on the respective cost fields on the resource plan form and the **Resource Plans** related list of the associated project or demand.
-   Reflects the revised values on the respective cost fields of associated project or demand.

**Parent Topic:**[Resource plans](../concept/c_ResourcePlans.md)

**Related topics**  


[Create a resource plan](t_CreateResourcePlanProjectTask.md)

[Use Resource Finder to analyze resource availability](create-resource-plan-with-finder.md)

[Create an operational resource plan](create-operational-plan.md)

[Request resources](t_RequestResourcePlanApproval.md)

[Confirm a resource plan](confirm-resource-plan.md)

[Confirm and allocate a resource plan](confirm-allocate-resource-plan.md)

[Request a change to a resource plan](t_RequestAChangeToAResourcePlan.md)

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

