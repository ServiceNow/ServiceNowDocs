---
title: Create action plan for KPIs
description: Create action plans linked to under-performing KPIs, enabling visual tracking of milestones and tasks. The tasks triggered by the action plans are assigned to the suppliers and they can see and complete those tasks in the Supplier Collaboration Portal.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 3
breadcrumb: [Using Supplier Relationship and Performance Management, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create action plan for KPIs

Create action plans linked to under-performing KPIs, enabling visual tracking of milestones and tasks. The tasks triggered by the action plans are assigned to the suppliers and they can see and complete those tasks in the Supplier Collaboration Portal.

Create action plan for KPIs. 

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under **Quick actions**, select **Manage my suppliers**.

3.  Under **My suppliers**, select the legal name of the supplier.

4.  Select the **KPI management** tab.

5.  Select **Create action plan**.

6.  Select the KPIs to be tracked.

    ![Select the KPIs to be tracked in the action plan](../image/add-action-plan.png "Add action plan KPIs")

7.  Select **Add**.

8.  On the form, fill in the fields.

    ![Action plan form details](../image/action-plan-form.png)

<table id="table_ssx_vwv_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated action plan ID

</td></tr><tr><td>

State

</td><td>

State of the action plan. By default it is in Draft state

</td></tr><tr><td>

Plan type

</td><td>

Type of action plan to be created:-   Quality improvement plan
-   Delivery improvement plan
-   Cost reduction plan
-   Sustainability and compliance plan
-   Communication and collaboration plan
-   Performance monitoring plan


</td></tr><tr><td>

Priority

</td><td>

Priority of the action plan

</td></tr><tr><td>

Supplier

</td><td>

Supplier related to the action plan

</td></tr><tr><td>

Opened by

</td><td>

User who created the action plan

</td></tr><tr><td>

Assigned to

</td><td>

User who is assigned the action plan**Note:** This field is not available for action plans created for automated KPIs.

</td></tr><tr><td>

Due date

</td><td>

Due date for the completion of the action plan

</td></tr><tr><td>

Created

</td><td>

Date of creation of the action plan

</td></tr><tr><td>

Watchlist

</td><td>

List of users included in the watchlist

</td></tr><tr><td>

Short description

</td><td>

Brief description of the action plan

</td></tr><tr><td>

Description

</td><td>

Detailed description of the action plan

</td></tr></tbody>
</table>9.  Navigate to **Action plan items** and select **Create**.

10. Create milestones or supplier tasks for each KPI to track the action plan.

    For more information on how to create milestones and supplier tasks, see [Create milestones for the action plan](create-milestones-for-the-action-plan.md) and [Create supplier tasks for the action plan](create-supplier-tasks-for-the-action-plan.md).

11. Select **Submit** to activate the action plan.

    The corresponding milestones and tasks are generated for the action plan.

    Internal users can add comments through the **Work notes** and the progress of the action plan can be tracked in the **Activity** stream section.

    ![Action plan with the Activity stream and work notes](../image/slo-action-plan-activity.png)


## Result

After the milestones are run, corresponding tasks are generated for the users assigned to those milestones. When they complete their tasks, performance metrics are recalculated to determine whether the KPIs are still on target or failing. If a KPI is linked to a milestone or an action plan, the dashboard highlights its status:

-   On Target – if the KPI is meeting or exceeding the target
-   Failing - if the KPI is not meeting its current target
-   Failing in a plan - if the KPI is in an action plan and isn’t meeting its milestone targets
-   Part of a Plan - if the KPI is in a plan and progressing but not failing

Emails are sent to the assignees when action plans are created. Emails are also sent in the following scenarios:

-   When there’s any change in the action plan
-   When an action plan fails \(tasks or milestones aren’t completed after the due date\)
-   When an action plan expires
-   When an action plan is completed

The action plan can be tracked continuously, with updates based on the subsequent KPI runs. Managers can monitor the progress of milestones and tasks using the Gantt chart.

![Action plans items showing Gantt chart](../image/slo-action-plan-gantt.png)

The following color code is followed to represent different tasks in the Gantt chart:

-   Teal: Active tasks within due date
-   Blue: Active tasks past due date and completed
-   Orange: Active tasks past due date but not completed

-   **[Create milestones for the action plan](create-milestones-for-the-action-plan.md)**  
Create milestones for the affected KPIs in the action plan.
-   **[Create supplier tasks for the action plan](create-supplier-tasks-for-the-action-plan.md)**  
Create supplier tasks for the affected KPIs in the action plan.

**Parent Topic:**[Using Supplier Relationship and Performance Management](../concept/using-supplier-relationship-and-performance-management.md)

