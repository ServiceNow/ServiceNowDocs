---
title: Create and publish maintenance plans
description: Create a maintenance plan for workplace assets and locations. Associate multiple services to different plan records based on the type of workplace maintenance activity.
locale: en-US
release: yokohama
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2025-09-08"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Create and publish maintenance plans

Create a maintenance plan for workplace assets and locations. Associate multiple services to different plan records based on the type of workplace maintenance activity.

## Before you begin

Ensure that the following plugins are installed:

-   Workplace Central
-   Enterprise Model and Asset Classes \(sn\_ent\)
-   Workplace Service Delivery
-   Workplace Core
-   Workplace Indoor Mapping
-   Workplace Case Management
-   Workplace Reservation Management

Role required: sn\_wsd\_maintenance.manager, sn\_wsd\_maint.admin

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Workplace Central**.

2.  Select the **Preventative Maintenance** tab icon \(![Preventive Maintenance icon.](../images/wsd-preventive-maintenance-icon.png)\).

3.  Select **All plans** &gt; **New** on the home page.

    ![Create a new maintenance plan form.](../images/wsd-create-maint-plan.png)

4.  On the form, fill in the fields.

<table id="table_ctm_hmd_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Title of the maintenance plan.

</td></tr><tr><td>

State

</td><td>

All maintenance plans start in a Draft state by default

</td></tr><tr><td>

Active

</td><td>

The active check mark is selected by default.

</td></tr><tr><td>

Start date

</td><td>

The start date of a maintenance plan. Select a date and select **OK**.

</td></tr><tr><td>

End date

</td><td>

The end date of a maintenance plan. Select a date and select **OK**.

</td></tr><tr><td>

Plan type

</td><td>

Enterprise assets \(models\) and workplace spaces \(locations or buildings\). Select **Model** or **Location** from the drop-down list.

Models: List of enterprise models or assets that need maintenance. For example, printers, coffee machines, fire extinguishers, and so on.

Locations: Option to select a Workplace location \(sn\_wsd\_core\_workplace\_location\). Select a building from the list of buildings.

**Note:** For Optimize cleaning activities AI agent, select the Plan type as **Location**. Model plan type is not optimized by the agentic AI workflow. For more information about how to optimize a maintenance plan record using the Agentic AI workflow, see [Optimize cleaning activities agent overview](../../now-assist-wsd/concept/optimise-cleaning-agent-overview.md).

</td></tr><tr><td>

Model/Building

</td><td>

Select assets or locations. If the selected building or model doesn’t show a maintenance item, select **Go back** to select another asset or location.

Based on your selection in the **Plan type** field, different options for locations or assets are displayed.

If you have selected **Model**, then assets or models are available for you to select.

if you have selected **Location**, then**Buildings** are available for selection.

For example: Select **Building B**.

</td></tr></tbody>
</table>5.  Select **Next**.

6.  The maintenance items for a selected location or model are filtered based on your selection of a model or location in Step 4.

    ![Maintenance items tab showing workplace models or assets for maintenance.](../images/wsd-cal-maint-items.png)

    Select one or more maintenance items.

    If you’ve selected a building in step 4, the floors, spaces, and areas associated with that building are displayed and included as part of the maintenance item.

    **Note:** The Optimized Cleaning Activities Agentic AI workflow only optimizes spaces at the floor level of a selected building. AI agents autonomously optimizes a space in a floor to get the space utilization threshold. For more information, see [Optimize cleaning activities agentic workflow](../../now-assist-wsd/concept/optimize-cleaning-activities-agent.md).

7.  Select **Go back** to make updates or edits on the maintenance details page.

8.  Select **Next**.

    The new maintenance plan is saved in a **Draft** state.

    The maintenance items go to the next step for scheduling.

9.  Select **Create a schedule** or **Copy a schedule** from the drop-down list.

    Select the **Skip scheduling** option if you don’t want to create a schedule now and prefer to create it later. After publishing a maintenance plan, you can create a schedule or copy an existing schedule for a plan.

    For more information, see [Create or copy a maintenance schedule](create-maint-schedule.md). For more information about how the scheduled job creates maintenance cases for a plan record, see [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md) and [Components installed with Workplace Maintenance Management](../reference/components-installed-with-maintenance-mgmt.md).

10. Select **Save**.

11. Select **Publish**.

    The maintenance plan is published. A contextual sidebar is available for you to search for schedules, view workplace maintenance case details, and view attachments for a plan.

    **Note:** The **Publish** option is not available when you select **Skip Scheduling**. You must open the maintenance plan again separately and select **Publish** to publish the plan.

    The published maintenance plan is available for you to view in a calendar view. For more information, see [Maintenance plan calendar view](cal-view-overview.md).

12. Review the maintenance plan details on the calendar view.

    Status of the maintenance plan moves to the **In progress** state. For more information about the calendar view, see [Maintenance plan calendar view](cal-view-overview.md).

    The **Schedules tab** shows the **Next run time** for a scheduled job. The scheduled job **Workplace Maintenance Nightly run** runs every 48 hours \(2 days\) and creates maintenance cases for active plan records. The schedule job can be scheduled on a daily or hourly basis. For more information, see [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

    Optimize cleaning activities Agentic AI workflow autonomously optimizes maintenance plan record Ids based on maintenance threshold data for a selected location. For more information, see [Optimize cleaning activities agent overview](../../now-assist-wsd/concept/optimise-cleaning-agent-overview.md).


**Parent Topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Previous topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Next topic:**[Maintenance plan calendar view](cal-view-overview.md)

