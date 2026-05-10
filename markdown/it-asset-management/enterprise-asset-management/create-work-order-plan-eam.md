---
title: Create a work order plan for enterprise assets
description: Create and manage a work order plan to organize, assign, schedule, and track complex asset tasks for enterprise assets and asset groups.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Asset work order plans, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a work order plan for enterprise assets

Create and manage a work order plan to organize, assign, schedule, and track complex asset tasks for enterprise assets and asset groups.

## Before you begin

In the **Field Service Configuration** module, the **Apply Work Order template in draft status** setting must be enabled.

Role required: sn\_eam.asset\_manager

## About this task

A work order plan can be created for individual enterprise assets and asset group.

## Procedure

1.  Create a work order plan.

<table id="choicetable_zfb_tsx_j3c"><thead><tr><th align="left" id="d297226e75">

Create from

</th><th align="left" id="d297226e78">

Steps

</th></tr></thead><tbody><tr><td id="d297226e84">

**Work management view**

</td><td>

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.
2.  Select the **Work order plans** tab.

A list of existing work order plans is displayed.

3.  Select **New**.


</td></tr><tr><td id="d297226e125">

**Asset group**

</td><td>

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate**.
2.  Select the **Asset groups** tab.

A list of existing asset groups is displayed.

3.  Select an asset group for which you want to create a work order plan.
4.  Select **Create plan**.


</td></tr></tbody>
</table>2.  In the **Create work order plan** dialog box, complete the fields.

    1.  In the **Work order plan template** field, select the work order plan template that you want to apply to the work order plan.

        **Note:** If you’re creating a work order plan from an asset group, only the work order plan templates associated with that asset group are shown.

    2.  In the **Plan name** field, enter a name for the work order plan.

        **Note:** If you selected a work order plan template, the **Plan name** field is automatically populated with the template name. You can update the name if needed.

    3.  Select **OK**.

    The Work order plan playbook displays the following activities that you must complete in the sequence:

    1.  **Details**
    2.  **Review affected assets**
    3.  **Review work order tasks** including **Review assignments** and **Review schedule**
    4.  **Track status**
    All the activities are in Pending status before you start working on them.

3.  In the **Details activity**, complete the work order plan details.

    **Note:** If you selected a work order plan template, the following fields on the Details form are automatically populated from the template:

    -   **Description**
    -   **Location**
    -   **Primary target**
    -   **Work order template**
    -   **Additional assets**
    1.  On the Details form, review and update the fields as needed.

<table id="table_s5k_zlw_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the work order plan.

</td></tr><tr><td>

Description

</td><td>

Description of the work order plan.

</td></tr><tr><td>

Location

</td><td>

Location of the primary target.**Note:** If you select a location first, the **Primary target** and **Additional assets** fields are filtered to show only assets in that location.

</td></tr><tr><td>

Primary target

</td><td>

Asset or asset group for which the work order plan is created.

</td></tr><tr><td>

Work order template

</td><td>

Work order template that defines the collection of tasks to be performed on the assets included in the work order plan.

</td></tr><tr><td>

Additional assets

</td><td>

Additional assets to include in the work order plan along with the primary target.

</td></tr><tr><td>

Due date

</td><td>

Date and time by which the work order plan must be completed.

</td></tr></tbody>
</table>        **Note:** Name, Location, Primary target, and Work order template fields are required.

    2.  Select **Save as template** to save the work order plan configuration as a template for future use.

    3.  Select **Update** to save your changes and continue editing.

    4.  Select **Mark complete** to save your changes and move to the next activity in the playbook.

4.  In the **Review affected assets** activity, confirm the assets to include in the work order plan.

    -   To remove an asset, select the asset and then select **Remove**.
    -   To confirm the assets and proceed to the next activity, select **Mark complete**.

5.  In the **Review work order tasks**, assign the work order tasks to technicians and schedule the tasks.

    1.  In the **Review assignments** activity, assign an assignment group to each work order task.

        1.  In the **Assignment group** field, select the assignment group.

            **Note:** To assign multiple work order tasks to the same assignment group, select the tasks and then select the assignment group.

        2.  \(Optional\) In the **Assigned to** field, select the technician to whom you want to assign the work order task.

            **Note:** All work order tasks must have an assignment group specified before you can complete this activity. The **Assigned to** field is optional; however, the schedule is populated for work order tasks in the Review schedule activity only when a technician is specified in the Assigned to field.

        3.  Select **Mark complete** to proceed to the next activity.
    2.  In the **Review schedule** activity, schedule the work order tasks.

        1.  -   To schedule a task manually, inline edit the **Scheduled start** field directly. The **Estimated end** field is automatically populated based on the Estimated work duration.
-   To schedule a task using the calendar view, the task must have a technician assigned in the Review assignments activity.

    -   Select **Calendar view** to schedule tasks visually by dragging the edges of a work order task to adjust the scheduled start and estimated end times.
    -   Reposition the task on the calendar view as needed.
    -   Double-click a work order task to open the corresponding record for detailed review.
    **Note:** Tasks appear in the calendar view only when assigned to a technician. If only an assignment group is specified, the task isn't displayed. The calendar view also displays active tasks from other work orders, maintenance plans, incidents, and ad hoc work orders.

        2.  Select **Ready for work** so that technicians can begin working on the work order tasks.

            **Note:** After you select **Ready for work**, the scheduled start and end times can't be modified.

        3.  Select **Mark complete** to proceed to the **Track status** activity.
6.  In the **Track status** activity, monitor the progress of the work order tasks.

    The following fields are updated automatically based on the technician's actions:

    -   **State**: Current state of the work order task.
    -   **Actual work start**: Date and time at which the technician started the task.
    -   **Actual work end**: Date and time at which the technician closed and completed the task.
    **Note:** Select **Calendar view** to get a visual overview of the scheduled work order tasks. The calendar view displays only tasks that are in the Work in progress state. Completed tasks aren't displayed.

    You can track the status of the work order tasks at any time through the associated work order plan.


**Parent Topic:**[Manage asset-centric work tasks using work order plans](../concept/manage-work-order-plans.md)

**Related topics**  


[Create a work order plan template](creat-work-plan-template.md)

