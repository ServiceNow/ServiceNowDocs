---
title: Create a time card
description: You can create time cards to log time against the work you have done.
locale: en-US
release: australia
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Time cards, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a time card

You can create time cards to log time against the work you have done.

## Before you begin

Role required: timecard\_user

## About this task

Starting Australia release, users can select a resource assignment to associate it with time cards to calculate the actual efforts and tag them to the respective projects.

The **Allow time card reporting on** field on the [project form](../../../product/project-management/task/t_CreateAProject.md) determines the level at which the time cards for the project tasks can be created.

**Note:** Time Cards created from Project form do not populate Resource plans automatically to avoid random allocations. For more information, see [KB0814884](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0814884) article in the Now Support Knowledge Base.

Time cards can be created automatically or manually.

-   Automatic: Use the following options to automatically generate the time cards:

    -   By updating task:
        -   **Auto create time card on task update**

            Configure time cards to be created when a user updates a task record. The **Auto create time card on task update** setting in the assigned [time sheet policy](create-time-sheet-policy.md) controls this behavior and is set to false by default.

        -   **Auto fill time card with time worked entries**

            Configure time cards to be created when a user records **Time worked**. A time card is created if a time card does not exist for the task. The time sheet policy **Auto fill time card with time worked entries** controls this behavior and is set to false by default.

            In **Project Task**, **Incident**, **Problem**, and **Change** records, the [**Time worked**](../concept/c_RecordTimeWorked.md) field does not appear by default and must be configured on the form.

    -   By scheduled job: Configure time cards for the project tasks to be generated automatically for users through a [scheduled job](auto-generate-time-cards.md). Only the admin can configure a scheduled job.
    **Note:** Time cards cannot be created automatically when you use the mobile interface. Use the desktop interface if you want to use the automatic time card feature.

-   Manual: Create a time card for each task and enter the time manually.

## Procedure

1.  Create the time card using one of the following options.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d160115e216">

Option

</th><th align="left" id="d160115e219">

Steps

</th></tr></thead><tbody><tr><td id="d160115e225">

**From the Time Sheet Portal**

</td><td>

1.  Navigate to **Time Sheets** &gt; **Time Sheet Portal**.
2.  Open the week on the **Calendar** for which you want to create the time card.


</td></tr><tr><td id="d160115e255">

**From a Time sheet related list**

</td><td>

1.  Open the time sheet that you want to create the time card for.
2.  In the **Time Cards** related list, click **New**.


</td></tr><tr><td id="d160115e279">

**From a Time sheet related link**

</td><td>

1.  Open the time sheet for which you want to create the time card.
2.  Click any of the following related links:

    -   **Generate Time Cards**: This option generates the time cards for all project tasks assigned to the user for the time sheet week. With this option, time cards are generated only for the project tasks that are in progress or planned in that week.
    -   **Copy from previous time sheet**: This option [copies](copy-time-sheet.md) all the time cards \(for project and non-project tasks\) from a selected time sheet.
**Note:**

When using the related links for creating time cards:

    -   If a time card exists for a project task for the time card week, a duplicate time card is not created.
    -   Time cards are generated only for those project tasks that are in progress or planned in that week.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_w21_qdm_qx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Week starts on

</td><td>

Starting date of the week of the time sheet.**Note:** The [time sheet policy](create-time-sheet-policy.md#time_sheet_policy_form) **Week starts on** controls the start day of the week. A message is displayed when you try to associate a resource plan with a time card when the week on which the time card starts is outside the resource plan dates.

</td></tr><tr><td>

State

</td><td>

Current state of the time card. All new time cards begin in the Pending state.Different states of a time card are Pending, Submitted, Approved, Processed, Rejected, and Recalled.

</td></tr><tr><td>

Category

</td><td>

Type of task for which the time card is created.

</td></tr><tr><td>

Task

</td><td>

Task that is associated to the time card.

</td></tr><tr><td>

Project time category

</td><td>

Type of activity in the project that time is reported for.This field appears when you select **Project/Project Task** or **Task work** in the **Category** field.

</td></tr><tr><td>

User

</td><td>

Name of the user that the time card is created for.

</td></tr><tr><td>

Resource assignment

</td><td>

Select a resource assignment assigned to the user. When the time card is approved, the actual hours are used to view the planned vs actual hours in the heatmap view in Project Workspace and Resource Management Workspace.A resource assignment is associated with the time card in the following ways:

-   If the user has multiple resource assignments, you can select the appropriate assignment.
-   If the user has only one resource assignment, that plan is selected by default.


</td></tr><tr><td>



</td><td>



</td></tr><tr><td>



</td><td>



</td></tr><tr><td>



</td><td>



</td></tr></tbody>
</table>3.  Click **Submit**.


## Result

-   The time card is created for the selected time card period.
-   If the time sheet for the week does not exist, a time sheet is created for the time card week.

## What to do next

After the time card is created, the hours for that task can be incremented automatically from the **Time worked** field in the task record. The time sheet policy **Auto fill time card with time worked entries** controls the way the time is updated in time cards. The policy is set to false by default. If automatic updates for time worked are not configured, the user must manually update the time card.

-   **[Copy time cards from a previous time sheet](copy-time-sheet.md)**  
Another option for creating time cards is to copy them from an existing timesheet, which copies all the time cards \(for project as well as non-project tasks\) from a selected time sheet.
-   **[Auto-generate time cards](auto-generate-time-cards.md)**  
As an admin, you can configure a scheduled job to generate time cards automatically for project tasks assigned to time card users.

**Parent Topic:**[Time cards](../concept/c_TimeCards.md)

**Related topics**  


[Map a time card category with operational work types](map-time-card-category.md)

