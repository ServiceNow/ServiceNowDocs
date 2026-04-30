---
title: Scheduling in Workforce Optimization for Customer Service
description: By using Scheduling, you can manage your workforce resources efficiently by planning and managing schedules, staffing, and shifts across your teams all from one location. You can also integrate with on-call scheduling and create shifts and schedule for on-call rotations.Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.Create, update, or monitor your teams' schedule from one location. You can approve or reject requests for swapping shifts or time off for agents within your assignment group.Set recurring meetings or training sessions for your team from the Schedule tab. You can create daily, weekly, monthly, or yearly meetings.Use schedule adherence to evaluate whether or not your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.Create a meeting, training, time-off request, or an ad hoc work event from the team calendar.Swap an agent's shift in your assignment group with another agent who can work on that shift and skip the approval process.Empower your teams to sign up for work shifts based on their availability and preference.Specify one or more shifts in a schedule plan for which you would prefer to sign up.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 30
breadcrumb: [Using Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Scheduling in Workforce Optimization for Customer Service

By using Scheduling, you can manage your workforce resources efficiently by planning and managing schedules, staffing, and shifts across your teams all from one location. You can also integrate with on-call scheduling and create shifts and schedule for on-call rotations.

With Scheduling, you can do the following:

-   Add meetings, training, time-off requests, or ad hoc work shifts by using the team calendar.
-   Filter agents in the team calendar based on their location, region, assignment groups, or any field in the agent's record.
-   Create shift and schedule plans for agents.
-   Approve or reject agents' time-off and shift-swap requests.
-   Track and manage the team's schedule on the team calendar by viewing the planned shifts versus the actual clock-in and clock-out times for the selected day or week.
-   Analyze whether your team members are following the schedules. If you see a potential issue, you can easily alert your team so that they can take immediate action.
-   Use historical adherence reports to analyze and recommend coaching opportunities for your agents.

To delve into more information behind your key performance indicators, filters and sidebars, see [Exploring indicators with KPI Details](https://www.servicenow.com/docs/access?context=kpi-details-components&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

**Parent Topic:**[Using Workforce Optimization for Customer Service](use-configurable-wfo-cs.md)

## Create a shift plan

Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

In the **Shifts** tab, the shifts are grouped by active and inactive shifts. The contextual side panel displays the active and then the inactive shifts in the order it is displayed in the **Shifts** tab.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../image/schedule-new.png)\) icon.

3.  Click the **Shifts** tab.

4.  Click the plus \(+\) icon.

5.  Create a shift.

<table id="choicetable_ynn_t3g_v4b"><thead><tr><th align="left" id="d44847e196">

To

</th><th align="left" id="d44847e199">

Do this

</th></tr></thead><tbody><tr><td id="d44847e205">

**Create a work shift**

</td><td>

1.  Create a work shift.
    1.  Click **Work shift**.
    2.  In the **Name** field, enter a name for the shift.
    3.  Select the time window for the shift.
        1.  In the **Time Zone** field, select the time zone of the users that you want to allocate to the shift.

**Note:** To add a shift for agents working in their local time zones, select the **Use agent time zone** option. The system uses the time zone that is specified in the agent's user record.

        2.  In the **Start Time** field, enter the time of day when you want to start the shift.
        3.  In the **End Time** field, enter the time of day when you want to end the shift.
    4.  Select the days of the week for which you want to add this shift.
    5.  Click **Save**.
2.  Add schedule breaks to the shift.

    1.  Select the shift that you created.
    2.  Click **Add break**.
    3.  In the **Name** field, enter a name for the break.
    4.  Set a duration for the break.
        1.  In the **Duration** field, enter the length of time for the break.
        2.  In the **Earliest Start Time** field, enter the earliest time to start the break.
        3.  In the **Latest End Time** field, enter the latest time to end the break.

For example, you can set the earliest start time as 11:00, the latest end time as 15:00, and the duration of the break as one hour. If you add four agents to that work shift, the Scheduling application automatically staggers the break duration for each agent. Stagger breaks to ensure that your four agents can cover the entire shift span.

        4.  Click **Save**.
You can view the number of agents for each hour or day on the shift span window.

</td></tr><tr><td id="d44847e323">

**Create an on-call shift**

</td><td>

1.  Create an on-call shift.
    1.  Click **On-call shift**.
    2.  In the **Name** field, enter a name for the shift.
    3.  From the **Group** field, select a group that you want to assign for the shift.
    4.  Select the time window for the shift.
        1.  In the **Start Time** field, enter the time of day when you want to start the shift.
        2.  In the **End Time** field, enter the time of day when you want to end the shift.
        3.  From the **Time Zone** menu, select the time zone of the users that you want to allocate to the shift.
    5.  Select the days of the week for which you want to apply the shift.
    6.  In the **Rotation start date** field, click the calendar icon, select the on-call rotation start date for the shift and click **OK**.
    7.  Click **Save**.
2.  Create the on-call rotation.

    1.  Select the shift that you created.
    2.  Click **Create Rotation**.
    3.  From the **Agents** field, select the names of the agents you would like to be part of the shift. When you click the field, the name of all agents that belong to the group that the on-call shift is being created for is displayed.
    4.  From the **Rotate interval** field, select if you want the rotation to be daily or weekly.
    5.  Click **Save**.
**Note:** The **Escalation Type** field is auto-populated with **Rotate through rosters** field value if multiple rosters have been created for the rotation. If not, it is populated with **Rotate through members** field value.

3.  Click **Publish** to make the shift active and publish it on the schedule.
 **Note:**

-   You can select an active on-call shift and click **Unpublish** to make the shift inactive and remove it from the schedule.
-   You can view all on-call shifts that have been published on the schedule in the agent and team calendar. When you add new agents to the on-call rotation, it might take some time to refresh the data on the team calendar.
-   You can click on an on-call shift in the team calendar to see more details.
You can view the name of the primary agent for each on-call shift on the shift calendar.

</td></tr></tbody>
</table>6.  Click **Submit**.


## Create a schedule plan

Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

You can set the number of days to cache agent schedules using the **sn\_shift\_planning.number\_of\_days\_to\_cache** [system property](../reference/components-installed-configurable-wfo-cs.md). The **Total coverage/demand** row displays the number of agents covering each shift in a day. The day view displays the demand for the number of agents forecast for every hour in a day. For example, 4/5 shows that you have four agents scheduled for an hourly time slot, 11 AM to 12 PM and the agent demand forecast for that hour is 5.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon.](../image/schedule-new.png)\) icon.

3.  Create a schedule plan.

    1.  Click the **Team Calendar** tab.

        **Note:** You can analyze the staff alignment for a day or for the week.

    2.  In the contextual side panel, click the show schedules icon ![Show Schedules icon.](../image/show-schedule-new.png) to display the schedules.
    3.  In the Schedules panel, click ![Create New Schedule icon.](../image/create-schedule-new.png) icon.
    4.  In the **Name** field, enter a name for the schedule plan.
    5.  From the **Start Date** field, select a date to start the schedule plan and click **OK**.
    6.  From the **End Date** field, select a date to end the schedule plan and click **OK**.
    7.  Click **Save**.
    You can view the schedule of all agents in the assignment group that you directly or additionally manage.

4.  Add a work shift to the schedule plan.

    **Note:** To add more shifts to an existing schedule plan, select the schedule plan and then add the work shift.

    1.  In the contextual side panel, click **Add Shift**.
    2.  In the **Shift** field, select the work shift that you want to add to the schedule plan.
    3.  In the **Event type** field, select the work event that categorizes the work shift.
5.  Add agents to the work shift.

    1.  In the **Agents** field, search for agents and add one or more agents to add to the shift.
    2.  Click **Save**.
    **Note:** It may take a few minutes for the screen to refresh.


## Publish a schedule plan for visibility into team coverage

Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

You can make a copy of a schedule and update it to create a new schedule. Updates could include modifying the schedule start and end dates as well as adding or removing shifts or agents.

When you make a copy of the schedule, the following updates are automatically made to the schedule copy:

-   The start date is set to the current date and the end date to 30 days from the current date.
-   The schedule state changes to **Draft**. You can make the necessary changes to the shift and click **Save**.
-   The schedule only displays agents in the assignment group of the current logged in user.

You can also unpublish a schedule make updates, and then publish it again.

-   If the start date is the either the current date or had occurred in the past, the schedule state remains as **Published** and the end date changes to tomorrow.
-   If the start date is in the future, the scheduler changes the schedule state and agent schedules to **Draft**.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../image/schedule-new.png)\).

3.  Generate a schedule preview.

    1.  Click the **Team Calendar** tab.
    2.  Click the Show Schedules \(![Show Schedules icon.](../image/show-schedule-new.png)\) icon to display in the contextual side panel.
    The team calendar refreshes and generates the preview when you save a work shift.

4.  Publish a schedule.

    1.  Select a schedule and edit the schedule if necessary.
    2.  Edit the schedule if necessary and click **Save**.
    3.  Click **Publish**.

        **Note:** You can click **Delete** in **Draft** state and delete the schedule if you no longer need it.


### Result

All the schedules that are in **Draft** state move to **Published** state. You can view the published schedule in the team calendar. Agents can view their published schedules and approved leaves on MS Outlook after synchronizing their team calendars and events with Microsoft Outlook.

## Track and manage your teams' schedule

Create, update, or monitor your teams' schedule from one location. You can approve or reject requests for swapping shifts or time off for agents within your assignment group.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

Using the calendar, you can do the following:

-   View all of your agents by assignment group.
-   Get insights into team compliance with published schedules.
-   View an agent's work schedule that is actual shift time vs clock-in and clock-out times.
-   Filter the team calendar based on the **Assignment Group**, **Location**, **Skills**, **Shift Plan**, and **Events** for a customized view.
-   Modify the agent's shift, clock-in, and clock-out timings, if necessary.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select the Schedule \(![Schedule icon.](../image/schedule-new.png)\) icon.

3.  Modify an agent's shift.

    The schedule that includes this shift must be in **Preview** or **Published** state.

    1.  In the **Team Calendar** tab, navigate and hover over the shift for the agent that you want to modify the schedule for.
    2.  In the shift pop-up window, select the Edit \(![Edit icon.](../image/edit-new.png)\) icon.
    3.  Modify the agent's shift or the shift time.

        **Note:** If the existing shift has a break, you can add more breaks to the shift.

        -   Select **Select shift times** and modify the **Start time** or **End time** fields to change the timing of the shift.
        -   Select the **Select preset shift** option and from the Shift plan list, select an existing shift to assign another shift plan to the agent. For more info on creating a shift plan, see [Create a shift plan](scheduling-configurable-wfo-cs.md#).
    4.  Select **Save**.
4.  Approve or reject an agent's time off or shift-swap with another agent.

    **Note:** You must approve a request two days before the time-off or shift-swap start date. If not, the approval is auto-rejected. An administrator can change this default setting. For more information, see Setting the due date for time-off and shift-swap request approvals in [Components installed with Workforce Optimization for Customer Service](../reference/components-installed-configurable-wfo-cs.md) Overlapping time-off requests by an agent is rejected.

    |Tab|Description|
    |---|-----------|
    |**Shift approvals**|View all agent requests and the details for each request and approve or reject a single request.|
    |**Time off requests**|Approve or reject multiple time off requests.|
    |**Shift swap requests**|Approve or reject multiple shift swap requests.|

    If you approve the request, the schedule gets updated in the team calendar based on the approvals.


## Create recurring meetings

Set recurring meetings or training sessions for your team from the Schedule tab. You can create daily, weekly, monthly, or yearly meetings.

### Before you begin

Role required: sn\_shift\_planning.admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select the Schedule \(![Schedule icon.](../image/schedule-new.png)\) icon.

3.  Navigate to **+New** &gt; **Meeting**.

4.  Enter the title of the meeting in the **Title** field.

5.  Enter the name of the participants in the **Attendees** field.

6.  Enter the start and end dates of the meeting in the **Start date** and **End date** fields.

7.  Enter the start and end time of the meeting in the **Start time** and **End time** fields.

8.  Select the **All day** option if the meeting duration is for the entire day.

9.  Select one of the following options from the Repeats list.

<table id="choicetable_mk5_vhk_bcc"><thead><tr><th align="left" id="d44847e1278">

Option

</th><th align="left" id="d44847e1281">

Steps

</th></tr></thead><tbody><tr><td id="d44847e1287">

**Does not repeat**

</td><td>

It is a one-time meeting only.

</td></tr><tr><td id="d44847e1296">

**Daily**

</td><td>

1.  Select a value in **Repeat every** field. For example, if you select 2, the meeting repeats every two days.
2.  Select a date in **Repeat until** field to select the date when the meeting series will end.


</td></tr><tr><td id="d44847e1320">

**Weekly**

</td><td>

1.  Select a value in **Repeat every** field. For example, if you select 2, the meeting repeats every two weeks.
2.  Select the days of the week when you want the meeting to occur. For example, if you select Monday and Thursday, then the meeting occurs on Monday and Thursday every two weeks.
3.  Select a date in **Repeat until** field to select the date when the meeting series will end.


</td></tr><tr><td id="d44847e1347">

**Monthly**

</td><td>

1.  Select a value in **Repeat every** field. For example, if you select 1, the meeting repeats every month.
2.  Select a day from the **Monthly type** list:
    -   **Day of the month**: The meeting occurs on the selected day of the month only.
    -   **Last day of the month**: The meeting occurs on the last day of the month.
    -   **Last week day of the month**: For example, if you selected a Thursday in the Start day field, the meeting occurs on the last Thursday of every month.
3.  Select a date in **Repeat until** field to select the date when the meeting series will end.


</td></tr><tr><td id="d44847e1395">

**Yearly**

</td><td>

1.  Select a value in **Repeat every** field. For example, if you select 2, the meeting repeats every two years on the day you selected in Start date field.
2.  Select a date from **Repeat until** field to select the date when the meeting series will end.


</td></tr></tbody>
</table>10. Enter some details and agenda about the meeting in the **Description** field.

11. Select **Save**.

    The meeting invite is sent to the participants selected in the Attendees field.


### What to do next

You can view the meeting series on your team calendar. You can select the meeting invite on the team calendar and edit the whole meeting series or a particular meeting in the whole series.

## Monitor schedule adherence of your agents

Use schedule adherence to evaluate whether or not your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

-   Adherence is a metric to analyze how closely agents follow their schedule in completing the work assignments. Conformance measures the work completed, regardless of when it was completed.
-   A high adherence rate indicates that agents are sticking to their schedules and offering customer service when expected. Low adherence suggests changing the processes or decisions to manage the team efficiently. The numbers are highlighted in red for non-adherent agents.
-   Schedule adherence and conformance calculations are based on the formulas, agents' actual and planned work timings. The following are the default formulas that are used to calculate adherence and conformance for agents. However, your administrator can change the [formulas](setup-scheduling-configurable-wfo-cs.md#), as required. The following components and formulas are used to calculate adherence and conformance:
    -   The **shift\_planning\_clock-in** and **shift\_planning\_clock-out** scripts generate the agents' clock-in and clock-out events from the login and logout sessions. The business rule **Agent Time Work Event Trigger** generates clock-in and clock-out events whenever there is a change in agent's presence state.
    -   **Schedule Adherence**= \(Minutes worked in shift/Scheduled shift time in minutes + Overtime\)
    -   **Conformance**= \(Minutes worked in shift + Overtime\)/Scheduled shift time in minutes
-   The ideal adherence percentage by default is above 70, and conformance is between 80 to 120. However, your administrator can change the threshold values. For more information, see [Configure properties for schedule adherence and conformance](setup-scheduling-configurable-wfo-cs.md#). The agents who do not qualify to the defined threshold values are considered as non-adherent and are highlighted in red.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../image/schedule-new.png)\).

3.  Monitor the schedule adherence of your agents.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View schedule adherence at the organization or team level

</td><td>

1.  Click the **Schedule Adherence** tab.

The bar chart appears with the schedule adherence percentage and conformance percentage of your teams.

2.  View the graph and drill down further to view the analytics of your team members by clicking on the bar.


</td></tr><tr><td>

Analyze planned vs. actual scheduling for your team members

</td><td>

1.  Click the **Team Calendar** tab.
2.  Select the date.
3.  View the **Time Worked** summary by clicking on the bar representing the agent's actual time worked.
 **Note:** The clock-in and clock-out timings are the actual work timings of your agents. The events are generated based on the agent's login, logout actions, and presence state. If an agent forgets to clock out, the system automatically generates the clock-out event after 60 minutes by default. However, your administrator can change it using **Default threshold time for clock-out event generation \(in Minutes\)** system property.

Example: A clock-in event gets generated when an agent logs in or changes the presence status to **Available**. Similarly, a clock-out event gets generated when an agent logs out of the system or changes the presence status to either Offline or Break. If an agent fails to clock-out past 60 minutes of the shift end time, the system automatically generates the clock-out event.

</td></tr></tbody>
</table>    The following team calendar snapshot illustrates how to measure how well your team members are adhering to their work schedules. The blue bar indicates the planned work shift time and next to that is the actual worked time. The default representations are purple for clock-in time, green for agent's available duration, red for the clock-out time, and grey for agent's non-available time.

    ![Schedule view in the Team Calendar displaying agent availability.](../image/schedule-adherence-cs.png)


## Analyze adherence and conformance from the time worked summary

View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

Adherence and conformance calculations are based on the [defined configuration](setup-scheduling-configurable-wfo-cs.md#) and your agents' actual and planned work schedules.

**Note:** Your administrator can disable schedule adherence or change the configuration for adherence and conformance. For more information, see [Configure properties for schedule adherence and conformance](setup-scheduling-configurable-wfo-cs.md#).

For information about schedule adherence, see the "Schedule adherence" section of [Scheduling in Workforce Optimization for Field Service](https://www.servicenow.com/docs/access?context=scheduling-wfo-fsm&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Drill down to view the time attendance and time worked summary of your agents.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Analyze time worked summary of your team

</td><td>

1.  Click the Lists icon \(![Lists icon.](../image/list-new.png)\).
2.  Under Schedule Adherence, click **Time Worked Summary**.

**Note:** The **Available Non Planned** time captures the time the agent was available and clocked in outside of the agent's scheduled work events. For example, if an agent is scheduled to attend a training from 13:00 to 14:00 but forgets to clock out that attendance, that time is considered the clocked-in time. The training time from 13:00 to 14:00 is captured as the available non-planned time.

</td></tr><tr><td>

View your agents' time attendance

</td><td>

1.  Click the Lists icon \(![Lists icon.](../image/list-new.png)\).
2.  Under Schedule Adherence, click **Time Attendance**.


</td></tr></tbody>
</table>    The following schedule adherence example shows how to measure how well your team is adhering and conforming with their work schedules.

    ![Complete summary of the attendance, schedule adherence, and conformance of all the agents in the team.](../image/time_worked_summary_new.png)


### Example

To understand the computations of the fields in a time worked summary, consider Fatima Alonzo's work day:

-   Shift time begins at 8 a.m. and goes to 4 p.m. = 8 hours
-   Planned time = 8 hours = 480 minutes​
-   Clocks in 8 a.m. and clocks out at 12 p.m. for a break. Back from the break, clocks in at 12:30 p.m. and clocks out at 4 p.m.
-   Minutes worked in shift = 480 - 30 = 450 minutes​
-   Schedule adherence= \(minutes worked in shift/scheduled shift time in minutes + overtime\) = 450/\(480+65\) = 82.57%
-   Conformance= \(minutes worked in shift + overtime\)/scheduled shift time in minutes = \(450 + 65\) / 480 = 107.29 percent​.

**Note:** Fatima Alonzo is adherent because the schedule adherence and conformance are within the threshold. To see which agents are non-adherent, look for the numbers highlighted in red.

## Analyze staff alignment using Demand Forecast

Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.

### Before you begin

Role required: sn\_agent\_forecast.user

### About this task

Using Demand Forecast, you can:

-   Monitor agent or team shift coverage for any day or week.
-   Analyze if you are overstaffed, understaffed, perfectly staffed, or not aligned well with your staffing needs.
-   Adjust the staff alignment depending on the coverage you need and the schedule of your teams.
-   Analyze staff alignment as you are creating a schedule.
-   You can analyze the agent coverage you have and the actual demand for the number of agents based on assignment groups and work shifts in a day.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../image/schedule-new.png)\) icon.

3.  Click the **Team Calendar** tab.

4.  Analyze staff alignment for each shift.

    You can click the filter icon and select the assignment groups and shift plans for which you want to view the staff alignment.

<table id="choicetable_pwx_2tw_nnb"><thead><tr><th align="left" id="d44847e2004">

To analyze staff alignment

</th><th align="left" id="d44847e2007">

Do the following

</th></tr></thead><tbody><tr><td id="d44847e2013">

**For each day**

</td><td>

Select **Day** from the list.The **Total resources needed** row displays the demand for the number of agents for that day at the selected intervals of 15,30, and 60-minute.

 For example, at 15-minute intervals, a number 16 between 0700 and 0715 means that the agent demand forecast is 16.

 The time slots are color-coded as below to show the coverage of agents in a particular interval:

|Highlight color for each day for a group|Description|
|----------------------------------------|-----------|
|Green|The number of agents you have scheduled for that interval and demand for that interval are an exact match—your staffing needs are perfectly aligned.|
|Yellow|The number of agents you have scheduled are more than the demand you have for that interval.|
|Red|The number of agents you have scheduled are less than the demand you have for that interval.|
|Grey|The demand for the number of agents and the number of agents scheduled is zero for that interval.|

</td></tr><tr><td id="d44847e2097">

**For a given week**

</td><td>

1.  Select **Week** from the list.

The **Total coverage/demand** row has indicators for the staff alignment.

    |If the row displays|Then|
    |-------------------|----|
    |An arrow points downward|The predicted forecast is lower than the number of agents you need for that day|
    |An arrow points upward|The predicated forecast is higher than the number of agents you need for that day|
    |A checkmark|The perfect alignment of the predicted forecast and the required number of agents.|

2.  Click any of the indications displayed in the **Total coverage/demand** row to analyze further details on the forecast.
 You can also view the coverage and demand for every hour for each group.

</td></tr></tbody>
</table>    The following scheduling snapshots provide you an example to analyze staff alignment using Demand Forecast. The misaligned staffing indicator in the pop-up shows that the forecast manager has scheduled certain number of agents for each shift but they need more agents to cover them.

    ![Demand Forecast to analyze staff alignment.](../image/demand_forecast_and_scheduling.gif)


## Add events to the team calendar

Create a meeting, training, time-off request, or an ad hoc work event from the team calendar.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

You can create custom event types and add or remove the desired fields. For more information, see [Create event types to display them on the team calendar](setup-scheduling-configurable-wfo-cs.md#).

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../image/schedule-new.png)\).

3.  Click the **Team Calendar** tab.

4.  Click **+New**.

5.  Create an event.

<table id="choicetable_yff_2rw_1nb"><thead><tr><th align="left" id="d44847e2308">

To

</th><th align="left" id="d44847e2311">

Do this

</th></tr></thead><tbody><tr><td id="d44847e2317">

**Create a meeting, training, or time-off request.**

</td><td>

1.  Determine the type of event you are creating.
    -   To schedule a meeting, select **Meeting**.
    -   To create a training event, select **Training**.
    -   To create a time-off request, select **Time-off**.
2.  Fill in the event form.
    1.  In the **Title** field, enter a name for the meeting.
    2.  Add the required names for the event:

        -   For a meeting, in the **Attendees** field, enter the names of the meeting attendees.
        -   For training, enter the names of the agents to be trained in the **Trainees** field.
        -   For a time-off request, enter the names of the agents in the **Agents** field.
In the **Attendees** field, start typing the name of each of the attendees for the meeting and select the name.

    3.  In the **Start date** field, click the calendar icon and select the date you want to start the meeting and click **OK**.
    4.  In the **End date** field, click the calendar icon and select the date you want to end the meeting and click **OK**.
    5.  If the meeting spans for the whole day, click the **All Day** slider.
    6.  In the **Description** field, enter a description for the meeting.


</td></tr><tr><td id="d44847e2423">

**Create a work shift**

</td><td>

1.  Click **Work**.
2.  In the **Agents** field, start typing the name of each agent to be assigned to the work shift and select the name.
3.  In the **Start date** field, click the calendar icon, select the date you want to start the work shift, and click **OK**.
4.  In the **End date** field, click the calendar icon, select the date you want to end the work shift, and click **OK**.
5.  Click the **Select Shift** field and select a shift.


</td></tr></tbody>
</table>6.  Click **Save**.


## Swap your agents' shifts in Workforce Optimization for Customer Service

Swap an agent's shift in your assignment group with another agent who can work on that shift and skip the approval process.

### Before you begin

Role required: sn\_shift\_planning.admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../image/schedule-new.png)\).

3.  In the **Team Calendar** tab, navigate and point to the shift for the agent that you want to swap with another agent.

4.  In the shift pop-up window, click the Shift Swap icon \(![Shift Swap icon.](../image/shift_swap_icon.png)\).

5.  In the **Requested Shift** section, click the **Agent** field and select the agent who can work on that shift.

6.  Click **Submit**.

    The team calendar displays the updated schedule.


## Enable your teams to sign up for work shifts

Empower your teams to sign up for work shifts based on their availability and preference.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

When a schedule plan is enabled for sign-up, you can receive notifications. You can also receive notifications when the schedule plan that's open for sign up is due on the current day or when it's due soon.

**Important:** Your administrator must set the value in the **glide.ui\_notification.max\_recipients** property to the maximum number of agents for which you want to send the notifications.

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for CSM** &gt; **Manager Workspace**

2.  Select the Schedule icon \(![Schedule icon](../image/schedule-icon.png)\).

3.  Add a schedule plan.

    1.  Select the **Team Calendar** tab.

    2.  In the Contextual side panel, click the Show Schedules icon ![Show Schedules icon.](../image/show-schedules-icon.png) to display the schedules.

        **Tip:** Select the filter icon \(![Filter schedule](../image/show-filter-icon.png)\) and then select the desired sign-up state and sign-up dates to narrow down the schedule plans enabled for sign-up.

<table id="table_fnk_m3l_bvb"><thead><tr><th>

In the filters, to add the desired

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

**Sign-up state**

</td><td>

1.  Double-click one or more sign-up states in the **Available** column to move them to the **Applied** column.
2.  Select **Apply**.


</td></tr><tr><td>

**Sign-up dates**

</td><td>

1.  Select a predefined option such as **Last 7 days** or select the start and end date for which you want to see the schedule plans enabled for sign-up.
2.  Select **Apply**


</td></tr></tbody>
</table>    3.  In the Schedules panel, select the + icon.

        You can duplicate an existing schedule to create another one. After you duplicate a schedule that has the shift sign up enabled, you can update the start date, end date, and the date for which the agents must sign up for the schedule.

        **Note:** If there are no agents associated with the schedule, then the shifts associated with the schedule aren’t duplicated.

    4.  Fill in the required fields on the form.

        The image below shows an example of a filled-in Schedule form.

        ![Create shift sign-up](../image/create-shift-signup.png)

    5.  To enable your agents to sign up for work shifts, do the following:

        1.  Enable the **Request Agent Signup** check box.
        2.  In the **Agents must sign-up by** field, enter the date by which they must sign up for shifts within that schedule.
        **Tip:** If your agents have signed up for their preferred shifts, the **Assigned To** field is auto-populated with those agents.

    6.  Select **Save schedule**.

4.  Add a work shift to the schedule plan.

    1.  Select the schedule plan you've created.

        The image below displays the schedule plan that was created.

        ![Select schedule for shift sign-up](../image/select-schedule-shift-signup.png)

    2.  Select **Add Shift**.

        The image below provides an example of a form to enter the details for a shift.

        ![Add shift sign-up](../image/add-shift-signup.png)

    3.  In the **Shift** field, select the work shift that you want to add to the schedule plan.

        **Note:** If the schedule plan has been enabled for agents to sign up for shifts, the following fields are automatically enabled:

        -   **Request agent sign-up**
        -   **Enable auto-assignment of agents**
        If you want to assign agents manually, you can disable these check boxes at any time.

    4.  If the shifts are enabled for sign-up, you can select **Send for signup**.

        All shifts that have been enabled for sign-up are sent to the agents to sign up for their shifts. You can select **Close sign-up** to close agent sign-up for a shift before the sign-up due date and manually assign the agents.

        -   The **Enabled for sign-up** highlighted label changes to **Closed for sign-up**.
        -   The system will automatically close the sign ups after the sign-up due date.
5.  Add agents to the work shifts.

<table id="choicetable_ejp_3fs_dvb"><thead><tr><th align="left" id="d44847e2969">

To

</th><th align="left" id="d44847e2972">

Do this

</th></tr></thead><tbody><tr><td id="d44847e2978">

**Auto-assign agents**

</td><td>

Enable the **Enabled for auto-assignment for agents** check box. Your agents who have set the shift to be their top preference is auto-assigned. The number of shifts auto-assigned is based on the value set in the **sn\_shift\_planning.max\_shifts\_to\_autoassign** system property.

</td></tr><tr><td id="d44847e2993">

**Assign agents manually**

</td><td>

1.  In the **Assign agents** field, search for agents and add one or more agents to add to the shift.
2.  To add agents who had signed up for shifts, select **+Add signed up agents**

You can view the agents who had signed up and their preferred ranking to work on that shift. If you don't want to display the agents who have already been assigned to a shift in that schedule plan, enable the **Hide agents already assigned to other shifts** toggle button.

**Note:** This option is only available after you've closed agent sign-ups for the shift.

3.  Select **Save selection**.


</td></tr></tbody>
</table>6.  Select **Save shift**.

    The state for the schedule plan changes to **Generating Preview**.

7.  To publish the schedule plan, select **Publish**.

    **Note:** It may take a few minutes for the screen to refresh.

    The table describes the different shift sign-up states in the schedule plan.

<table id="table_j1v_nsl_bvb"><thead><tr><th>

Schedule plan sign up state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sign-up not enabled

</td><td>

The schedule plan isn’t enabled for sign-up.

</td></tr><tr><td>

Enabled for sign-up

</td><td>

-   Schedule plan is enabled for sign-up but isn’t yet ready for agents to sign up for shifts.
-   Schedule plan can’t be published when enabled for sign-up.
 ​

</td></tr><tr><td>

Open for sign-up

</td><td>

-   Schedule plan is enabled for sign-up and is ready for agents to sign up.
-   Schedule plan can’t be published or deleted when it's open for sign-up.
-   When open for sign-up:
    -   The sign-up due date can’t be changed.
    -   The work shift details can’t be changed.
    -   New shifts can’t be added.
    -   If enabled for auto-assign, the agent assignment in a shift can’t be changed.


</td></tr><tr><td>

Closed for sign-up

</td><td>

Schedule plan is closed for agents to sign up.

</td></tr></tbody>
</table>
## Sign up for your preferred shifts

Specify one or more shifts in a schedule plan for which you would prefer to sign up.

### Before you begin

Role required: sn\_shift\_planning.agent

### About this task

You can receive notifications when your manager makes a schedule plan available for sign up. You can also receive notifications when the schedule plan that's open for sign up is due on the current day or when it's due soon.

### Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Schedule icon \(![Schedule icon.](../image/schedule-icon.png)\).

3.  Select the **Sign up shifts** tab.

    You can use keywords to search the schedule plans, and view all schedules with active shifts for your assignment groups that you can sign up for. Use the pagination to scroll through all available schedule plans.

    The current state of each schedule plan displays as a highlight in each card. The table below describes the highlighted value.

    |Highlighted value|Description|
    |-----------------|-----------|
    |Available|Shifts for the schedule plan are available for sign up.|
    |Draft|Shifts you've considered for sign-up but have not completed the sign-up process.|
    |Completed|Submitted one or more preferred shifts within the schedule plan.|
    |Closed Incomplete|The schedule plan currently does not have shifts for which you could sign up.|
    |Closed Complete|The schedule plan has at least one preferred shift for which you've signed up.|

4.  Select the Overlapping time off icon \(![Overlapping time off.](../image/overlapping-time-off-icon.png)\) to analyze if the time off you have requested or the ones that have been approved overlap with the schedule plan available to you for sign up.

5.  To sign up for your preferred shifts, select **Add shifts**.

    You can only sign up for shifts in the schedule plan that have not been published yet.

    The Add shifts pop-up appears. You can search for shift using the search bar and select shifts to save as draft.

    You can sign up for a maximum number of shifts that your administrator has set up in the **sn\_shift\_planning.max\_shifts\_allowed\_for\_signup** system property.

6.  To save the selected shifts for sign-up, select **Save Shifts** and then select **Save as draft**.

7.  Select the plus \(+\) sign and sign up for additional shifts.

    When you have more than one shift, you can reorder them by using the up or down arrows in card for each shift.

8.  Select **Submit**.

    All shifts you have added for sign up will be submitted.


