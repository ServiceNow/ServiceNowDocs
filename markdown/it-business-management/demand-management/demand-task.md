---
title: Demand tasks
description: A demand task is a unit of work, created within a demand, to break down initial planning activities before converting the demand into a project, change, enhancement, or defect.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Demand tasks

A demand task is a unit of work, created within a demand, to break down initial planning activities before converting the demand into a project, change, enhancement, or defect.

You can [create a demand task](../task/create-demand-task.md) from the **Demand Tasks** related list to delegate activities that are helpful for assessing demand feasibility. Demand tasks differ from project tasks in the following aspects:

-   Planned dates, actual dates, and original dates are part of project tasks not demand tasks.
-   The due date indicates the date on which the task is targeted for completion and does not affect the demand workflow. Project tasks, however, affect the project completion dates if the planned dates and actual dates are changed.
-   Do not support creation of nested demand tasks.
-   Do not support task constraints such as the settings Start ASAP and Start on specific date.
-   Do not support an execution type such as Agile, Waterfall, or Hybrid.

## Resource assignment

Assign resources for a demand task using the **Assigned to**, **Additional Assignee list**, and **Assignment Group** fields. Do not create and use resource assignments for allocating resources or groups to a demand task or to submit the time spent on the demand. If you associate a resource assignment with a demand task, the associated resource plan is not transferred to the work entity created from that demand.

The resource assignments are not associated with the demand by default. Make sure that you do not use the resource assignments that you created for the future work entity created from the demand to submit the time spent on a demand.

When you submit a time card for a demand, the time and cost incurred are not transferred to the work entity created from the demand and remain within the demand as the demand cost and effort.

Resources assigned to a demand task can submit the time spent on it using a time card. For more information, see [Submit a time card for a demand task](../task/submit-time-for-demand.md).

## Actual cost and effort for a demand task

The actual effort of the work performed on the demand task is derived from the time card. The actual cost is derived from the hourly resource rate defined in the rate model, default labor rate, or default system property. The actual cost and effort for a demand task are then rolled up to derive the actual cost and effort for the associated demand. For more information, see [Actual cost and effort calculation for a demand and demand task](actual-cost-effort-calculation-demand.md).

## Add work items to a Demand

Based on the selected demand task category and role assigned to you, you can use the demand task form to:

-   [Add a cost plan to a Demand](../../project-management/task/t_CreateAProjectCostPlan.md)
-   [Add a resource assignment to a Demand](../task/create-manage-resource-plans-demand.md)
-   [Add a benefit plan to a Demand](../task/create-demand-benefit-plan.md)
-   [Add risks to a Demand](c_EnhancingDemands.md)

**Parent Topic:**[Demand Management reference](../../service-portfolio-management2/concept/demand-management-reference.md)

