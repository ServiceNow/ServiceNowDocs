---
title: Create a demand task
description: Create tasks for a demand to delegate cost, effort, risk, and benefit assessment activities. Assign a resource or group to the demand task to track the actual time and effort spent on performing the specified activities.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a demand task

Create tasks for a demand to delegate cost, effort, risk, and benefit assessment activities. Assign a resource or group to the demand task to track the actual time and effort spent on performing the specified activities.

## Before you begin

Role required: it\_demand\_manager

## About this task

You create demand tasks to plan the work for demands rather than for the target work entity such as a project, change, defect, or enhancement. For more information, see [Demand tasks](../concept/demand-task.md).

-   Planned dates, actual dates, and original dates are part of project tasks not demand tasks.
-   The due date indicates the date on which the task is targeted for completion and doesn’t affect the demand workflow. Project tasks, however, affect the project completion dates if the planned dates and actual dates are changed.
-   Don’t support the creation of nested demand tasks.
-   Don’t support task constraints such as the settings Start ASAP and Start on a specific date.
-   Don’t support an execution type such as Agile, Waterfall, or Hybrid.
-   You assign resources for a demand task use the **Assigned to** field, **Additional Assignee** list, and **Assignment Group** fields.

Resources assigned to a demand task can submit the time spent on it using a time card.

If you’re creating a demand task with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and Demand Currency view enabled, additional fields become available in addition to the Default view. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency in Demand Management](../concept/multicurrency-demand.md) and [Multicurrency fields in demand-related forms](../reference/multicurrency-fields-demand.md).

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Select the demand to which you want to add tasks.

3.  Add or edit a demand task from the **Demand Tasks** related list:

    -   To add a demand task, select **New**.
    -   To update the details of an existing demand task, select the record and then select **Edit**.
4.  On the Demand Task form, fill in the fields.

    For a description of the field names, see [Demand task form](../reference/demand-task-form.md).

5.  Select **Save**.

    After completing your work on the demand task, select **Update** to return to the demand page.

    **Note:** Team members can access demand tasks assigned to them from Collaborative Work Management. For more information, see [Managing SPM work in Collaborative Work Management](../../collab-work-mgmt/concept/cwm-team-member-roles.md).


## What to do next

Create resource assignments and add cost plans, benefit plans, and risks to the demand depending on your role. Use the following related links to access these tasks.

|Related Links|Description|
|-------------|-----------|
|Add Cost Plan to Demand|Add a cost plan to capture the costs of demands. Create a cost plan to specify the unit cost of a cost type for a fiscal period. This link appears if the **Category** value is set to Cost estimate and the user has the `it_project_manager` or `it_demand_manager` role. Select the link to open the cost plan form and fill in the details. For more information, see [create a cost plan](../../project-management/task/t_CreateAProjectCostPlan.md).|
|Add Resource Plan to Demand|Create a resource plan to find the availability of resources and add the resource plan to the demand. This link appears if the **Category** value is set to Effort estimate and the user has the `it_resource_user` role. Select the link to navigate to the Resource Plans page and request resources. For more information, see [Create and manage resource assignments for a demand](create-manage-resource-plans-demand.md).|
|Add Benefit Plan to Demand|Create a benefit plan to capture the potential benefits accrued by the demand when the demand is executed. This link appears if the **Category** value is set to Benefit estimate and the user has `it_project_manager` or `it_demand_manager` role. Select the link to open the benefit plan form and fill in the details. For more information, see [Create a monetary benefit plan for a demand](create-demand-benefit-plan.md).|
|Add Risk to Demand|Add risks that can potentially impact the success or outcome of the execution of the demand. This link appears if the **Category** value is set to Risk estimate and the user has `it_project_manager` or `it_demand_manager` role. Select the link to open the risk form and fill in the details. For more information see, [add a risk](../concept/c_EnhancingDemands.md).|

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

