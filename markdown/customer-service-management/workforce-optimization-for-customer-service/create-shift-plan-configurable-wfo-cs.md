---
title: Create a shift plan
description: Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Schedule, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Create a shift plan

Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

In the **Shifts** tab, the shifts are grouped by active and inactive shifts. The contextual side panel displays the active and then the inactive shifts in the order it is displayed in the **Shifts** tab.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../image/schedule-new.png)\) icon.

3.  Click the **Shifts** tab.

4.  Click the plus \(+\) icon.

5.  Create a shift.

<table id="choicetable_ynn_t3g_v4b"><thead><tr><th align="left" id="d214095e111">

To

</th><th align="left" id="d214095e114">

Do this

</th></tr></thead><tbody><tr><td id="d214095e120">

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

</td></tr><tr><td id="d214095e238">

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


**Parent Topic:**[Schedule in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)

