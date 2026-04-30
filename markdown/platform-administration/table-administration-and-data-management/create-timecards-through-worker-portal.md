---
title: Create time cards and log time through Time Sheet Portal
description: After you create time cards in Time Sheet Portal, log time in the time cards.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Time Sheet Portal, Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create time cards and log time through Time Sheet Portal

After you create time cards in Time Sheet Portal, log time in the time cards.

## Before you begin

-   Time sheet portal supports [resource assignments created using Project Workspace](https://www.servicenow.com/docs/access?context=create-resource-assignment-prj-wksp&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US). Once the time cards are approved, Project Managers can view the planned vs actual hours for an assignment in Project Workspace and Resource Management Workspace heatmap view.
-   Role required: timecard\_user

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Sheet Portal**.

2.  Create time cards in the **Logged Time Cards** section using any of the following options.

<table id="choicetable_uks_jpt_vz"><thead><tr><th align="left" id="d372022e113">

Option

</th><th align="left" id="d372022e116">

Steps

</th></tr></thead><tbody><tr><td id="d372022e122">

**Generate time cards for assigned projects or project tasks**

</td><td>

1.  Click ![Down arrow](../image/downarrowworkerportal.png) choice list next to **Submit**.
2.  Select **Generate Time Cards**. The option also appears in the **Logged Time Cards** section when a user has no time cards for the selected week.

**Note:**

    -   If a time card exists for a project task during the selected week, a duplicate time card is not created.
    -   Time cards are generated only for those project tasks that are in progress or planned for the selected week.
    -   The **Allow time card reporting on** field on the [project form](https://www.servicenow.com/docs/access?context=t_CreateAProject&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) determines the level at which the time cards are created for project tasks.


</td></tr><tr><td id="d372022e174">

**__Copy time cards from a previous time sheet__**

</td><td>

1.  Click ![Down arrow](../image/downarrowworkerportal.png) choice list next to **Submit**.
2.  Select **Copy from previous Time Sheet**. The option also appears in the **Logged Time Cards** section when a user has no time cards for the selected week.

**Note:**

    -   Time cards for all the project tasks that are in progress or planned in the current week are copied from the selected time sheet. If a time card for a project task exists, a duplicate time card is not created while copying.
    -   Time cards for all the non-task categories, such as meetings and trainings, are copied from the selected time sheet. If a time card for a non-task category exists, a duplicate time card is created while copying.


</td></tr><tr><td id="d372022e219">

**Create a time card from the Tasks, Group Tasks, or Other tab**

</td><td>

1.  On the **Tasks**, **Group Tasks**, or **Other** tab, point to a task \(card\) that you want to create a time card for.
2.  Click **Add to Time Sheet**.

**Note:** **Add to Time Sheet** creates a time card with the default rate type of the user, if it exists.

</td></tr><tr><td id="d372022e253">

**Create multiple time cards from the Tasks tab**

</td><td>

1.  On the **Tasks** tab, select multiple tasks that you want to create time cards for.
2.  Click **Add selected to Time Sheet**.


</td></tr><tr><td id="d372022e278">

**Create a time card for unassigned task**

</td><td>

1.  In the **Logged Time Cards** section, click **Add unassigned tasks to Time Sheet**.
2.  Enter the task number or short description of the task you worked on during the selected week.


</td></tr></tbody>
</table>    Based on the **Allow time card reporting on** field settings in the **Preferences** tab of a project, the **Add to Time Sheet** and **Add selected to Time Sheet** options are displayed in Time Sheet Portal.

    If a duplicate time card exists for a time card, you can merge both time cards to become a single one, except for time cards in the processed, approved, or recalled state. A duplicate time card is identified by comparing the values in the **Short description**, **State**, **Task**, **Category**, **Rate Type**, **Resource Plan**, or **Project Time Category** fields in the time card.

3.  In the **Logged Time Cards** section, log time in a time card.

<table id="choicetable_ixh_s1h_d1b"><thead><tr><th align="left" id="d372022e357">

Option

</th><th align="left" id="d372022e360">

Steps

</th></tr></thead><tbody><tr><td id="d372022e366">

**Through inline editing**

</td><td>

1.  Select a row and press **Enter**. You can also double-click a row.
2.  Edit the values as required.


</td></tr><tr><td id="d372022e387">

**Through time card form**

</td><td>

1.  Point to a row and click the more actions icon ![More actions icon](../image/MoreActionsIcon.png).
2.  To open the Time Card form, click **Open Form View**.
3.  Enter hours on the time card form.
4.  Click **Save**.


</td></tr><tr><td id="d372022e423">

**Add notes to time cards**

</td><td>

1.  Point to a row and click the more actions icon.
2.  To add a note, click **Add Note**.


</td></tr></tbody>
</table>
## Result

Your time cards are created and time is logged for the selected week.

## What to do next

If you encounter issues with time card creation or time logging, try the following:

-   Time cards not generating: Verify that your project tasks are in progress or planned for the selected week, and that the **Allow time card reporting on** field is configured on the project.
-   Missing tasks in the portal: Ensure you are assigned to the project tasks and that the task dates overlap with the selected time sheet week.
-   Duplicate time cards: Use the merge option to combine duplicate time cards. Duplicates are identified by matching Short description, State, Task, Category, Rate Type, Resource Plan, or Project Time Category fields.
-   Incorrect rate type: Verify your default rate type on your user profile. Contact your time card administrator \(timecard\_admin role\) to update rate type settings.

For issues you cannot resolve, contact your system administrator or the user with the timecard\_admin role in your organization.

**Parent Topic:**[Time Sheet Portal](../concept/worker-portal.md)

**Related topics**  


[Submit time sheet through Time Sheet Portal](submit-timesheet-workerportal.md)

[Log time and submit time sheets of your resources](submit-time-sheet-other-users.md)

