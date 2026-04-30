---
title: Enable Dispatcher Workspace settings
description: Determine what is displayed in the Dispatcher Workspace so you only see the information most relevant to your work.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Using Dispatcher Workspace, Assigning WOTs from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Enable Dispatcher Workspace settings

Determine what is displayed in the Dispatcher Workspace so you only see the information most relevant to your work.

## Before you begin

Role required: wm\_dispatcher

## About this task

Quick settings in Dispatcher Workspace provide access to certain capabilities of Field Service Management while assigning the work order tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select the Dispatcher Workspace.

3.  Click the Settings icon \(![Settings icon.](../image/IconPersonalizeList.png)\).

    The options on the Settings dialog box are arranged in a multiple-tabbed layout.

    -   The **General** tab contains options for setting up the general Field Service Management configurations.
    -   The **Tasks** tab contains options for enabling the fields or information to show in the task card.
    -   The **Calendar** tab contains options for enabling the fields or information to show in the calendar.
    -   The **Resources** tab contains options for enabling the fields or information to show in the agent card or calendar view.
    -   The **Events** tab contains options for enabling the fields to show in a calendar event.
    -   The **Metrics** tab contains options for enabling group or agent metrics. Group metrics are displayed in the schedule. Agent metrics are displayed in the contextual side panel.
4.  Fill in the fields on the **General** tab.

<table id="table_r23_r2c_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable tasks in the task panel, schedule, and map to filter at the same time when an assignment group is selected

</td><td>

Option to synchronize the resource filter with the task panel, tasks, and map for selected assignment groups.

</td></tr><tr><td>

Select the type of group you want to show

</td><td>

Option to choose if you want to see Assignment groups or Dispatch groups when you search in the task panel.

</td></tr><tr><td>

Enable Auto-refresh

</td><td>

Automatically refreshes the agent's calendar when an event such as a meeting, training, time-off request, personal, or an ad hoc work event is created.**Note:** This option appears only when the Enable Auto-refresh system property is enabled. For more information, see [Configure settings for Dispatcher Workspace](configure-workspce-settings.md).

</td></tr><tr><td>

Enable single-select groups / territories

</td><td>

Allows only one assignment group, dispatch group, or territory to load when selecting them in the task panel.

</td></tr><tr><td>

Groups

</td><td>

Enter the default groups to you want selected when you open the **Note:** If you have the Territory Planning plugin installed, then the **Groups** tab becomes the **Territories** tab. Enter the default territories to you want selected when you open the Dispatcher Workspace.

</td></tr></tbody>
</table>5.  Click the **Tasks** tab and fill in the fields.

<table id="table_thq_dfc_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scheduled start

</td><td>

Option to display the scheduled start date and start time of the task.

</td></tr><tr><td>

Territory

</td><td>

Option to display the assigned territory. **Note:** This field appears when the Territory Planning plugin is activated. For more information, see [Activate Field Service Territory Planning](Activate-fsm-territory-planning.md) and [Enable the Field Service territory model](enable-territory-model.md).

</td></tr><tr><td>

Assignment group

</td><td>

Option to display the assignment group of the task.

</td></tr><tr><td>

Default Location

</td><td>

Option to display the default location of the field service agent.**Note:** This field appears when the Territory Planning plugin is activated.

</td></tr><tr><td>

Timezone

</td><td>

Shows the time zones tasks are located in on the task card.

</td></tr><tr><td>

Select where you want new tasks to be loaded

</td><td>

Option to select where new tasks should be added to the task list. You must have **Enable auto-refresh** turned on to use this setting.

</td></tr><tr><td>

Notify me of new tasks before adding them to the list

</td><td>

Option to show a notification at the top of the task list when a new task is added to the task list. You must have **Enable auto-refresh** turned on to use this setting.

</td></tr></tbody>
</table>6.  Click the **Calendar** tab and fill in the fields.

<table id="table_w4t_cjd_mzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default calendar view

</td><td>

Default view of Dispatcher Workspace calendar in days, work day, or week.

</td></tr><tr><td>

Default start day of the week

</td><td>

Option to change the calendar start day of the week when in week view.

</td></tr><tr><td>

Default calendar display days

</td><td>

Option to update the number of days per week that show on the Dispatcher Workspace calendar.**Note:** When this is enabled, a **Flexible days** option is available to choose when you select **Day**, **Work day**, or **Week**.

</td></tr><tr><td>

Start of day time

</td><td>

Option to choose the hour that the work day starts on.

</td></tr><tr><td>

End of day time

</td><td>

Option to choose the hour that the work day ends on.

</td></tr><tr><td>

Intervals of time to show

</td><td>

The amount of time that each column in the Dispatcher Workspace calendar represents.

</td></tr><tr><td>

Drag and drop unassigned tasks on top of already scheduled tasks on the calendar

</td><td>

Determine how overlapping tasks are assigned. You can also adjust how often the overlapping tasks pop-up window appears.

</td></tr><tr><td>

Show task Window-start on task selection

</td><td>

Option to display the assignment window expiration date and time when a task is selected.

</td></tr><tr><td>

Automatically load resources

</td><td>

Option to load more agents or crews while scrolling down Dispatcher Workspace.

</td></tr><tr><td>

Schedule based on travel start time

</td><td>

Enables tasks assigned from the task panel to start based on an agent's travel time.

</td></tr><tr><td>

Automatically adjust overlapping tasks

</td><td>

Option to reschedule an existing task after a new task is assigned where an existing task is scheduled. When dragging a new task over an existing tasks, this shifts existing task to the right of the new task.**Note:** If Field Service Task Bundling plugin is installed, dragging bundles will also shift existing tasks, and existing bundles will shift when overlapped.

</td></tr><tr><td>

Select time zones for calendar

</td><td>

Entry to choose which time zones are available from the time zone drop-down on the Schedule and Hybrid views of Dispatcher Workspace. You can choose one or more.

</td></tr><tr><td>

Show multiple time zone rows

</td><td>

Enable multiple time zone rows to show on the calendar in Dispatcher Workspace. The time zones available for selection are input in the **Select time zones for calendar** field. Additional time zones are stacked on top of the default time zone on the calendar.

</td></tr></tbody>
</table>7.  Click the **Resources** tab and fill in the fields.

    **Note:** Disable Available Parts, Matching skills, and Distance to Task to prevent Dispatcher Workspace from reloading each time a new task is selected.

<table id="table_al5_gfc_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory

</td><td>

Option to display the assigned territory. For more information, see [Activate Field Service Territory Planning](Activate-fsm-territory-planning.md) and [Enable the Field Service territory model](enable-territory-model.md).

</td></tr><tr><td>

Groups

</td><td>

Option to display the dispatch group or assignment group of an agent in the agent card.

</td></tr><tr><td>

Location

</td><td>

Option to display the location of an agent in the agent card.

</td></tr><tr><td>

Available Parts

</td><td>

Option to determine if the parts are available with the agent.

</td></tr><tr><td>

Matching Skills

</td><td>

Option to determine if agent has the matching skills.

</td></tr><tr><td>

Agent Status

</td><td>

Option to determine the status of the agent, such as on site, off shift, and so on.

</td></tr><tr><td>

Schedule Status

</td><td>

Option to determine the schedule status of the agent, such as on time, behind, and so on.

</td></tr><tr><td>

Distance to Task

</td><td>

Option to determine the distance to task locations based on the route taken by the agent.

</td></tr><tr><td>

Timezone

</td><td>

Shows the time zones agents are located in on the agent card.

</td></tr><tr><td>

Distance to Unit

</td><td>

Unit of measurement used when calculating the distance to task locations, either miles or kilometers.

</td></tr><tr><td>

Crew size

</td><td>

The number of members in the crew.

**Note:** Crews must be enabled to see this setting.

</td></tr><tr><td>

View crew membership by schedule

</td><td>

When enabled, a yellow line shows on the calendar indicating the agent is working with a crew at that time.

**Note:** Crews must be enabled to see this setting.

</td></tr><tr><td>

Operational Status

</td><td>

Current status of the equipment. For example, a bucket truck is Unavailable because there is maintenance being completed on it. The available values are:

-   Available
-   In Use
-   Unavailable
**Note:** Equipment must be enabled to see this setting.

</td></tr><tr><td>

Category

</td><td>

Name of the category for the equipment.

**Note:** Equipment must be enabled to see this setting.

</td></tr></tbody>
</table>8.  Click the **Events** tab and fill in the fields.

<table id="table_lc3_rfc_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Option to display the short description of work order task in the task card.

</td></tr><tr><td>

Number

</td><td>

Option to display the work order task number in the calendar event card.

</td></tr><tr><td>

Show SLA

</td><td>

Option to display the SLA for the tasks that are already assigned and appear on the calendar view.

</td></tr><tr><td>

Show travel time indicator

</td><td>

Option to display the time taken by the agent to reach the task location.

</td></tr><tr><td>

Show travel home time indicator

</td><td>

Option to display the time taken by the agent to return home from the last task of the day.

</td></tr></tbody>
</table>9.  Select the **Metrics** tab and enable the fields.

    **Note:** Metrics show N/A if there are no tasks assigned to the agent or assignment group. Assign tasks to agents to see metrics.

<table id="table_rcf_z33_fxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tasks

</td><td>

The number of tasks the agent or group has to complete.

</td></tr><tr><td>

Work time

</td><td>

The total work time of the agent or group.

</td></tr><tr><td>

Travel time

</td><td>

The total travel time of the agent or group.

</td></tr><tr><td>

Utilization

</td><td>

The percentage of work hours that the agent or group has scheduled tasks for. The utilization value is calculated by adding the work time to the travel time and dividing that by the shift time.**Note:** This **Utilization** field appears only when the agent has a set schedule.

</td></tr><tr><td>

Productivity

</td><td>

The percentage of work tasks the agent or group has completed for the day. Productivity is calculated by dividing the work time by the shift time.**Note:** This field appears only when the agent has a set schedule.

</td></tr></tbody>
</table>10. Select **Save**.


