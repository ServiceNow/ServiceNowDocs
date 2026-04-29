---
title: Configure an agent's profile
description: Configure shifts, skills, schedules, and schedule attributes for agents in your organization.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Users, Set up workforce, Configure, Field Service Management]
---

# Configure an agent's profile

Configure shifts, skills, schedules, and schedule attributes for agents in your organization.

## Before you begin

Role required: admin

Ensure you have created a user and added the user to the appropriate user group applicable for agents.

## About this task

Configuring an agent appropriately is essential for scheduling and assigning tasks to agents. An accurately configured profile ensures the right responsibilities to each agent based on their skills, permissions, and availability.

Field Service Management capabilities like Route Optimization, Territory Planning, Dynamic Scheduling, or Intelligent Task Recommendations consider an agent’s scheduling attributes \(Resource Schedule Attributes table\) from the agent's profile for the given day to optimize capacity and task assignment.

**Note:** An agent can access and use Field Service Management capabilities based on the roles and permissions configured for the agent.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select an agent name.

    The agent profile preview appears.

3.  In the **Skills** related list, either add new skills or edit existing skills for the agent.

<table id="table_lvj_2tk_nkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Add new skills

</td><td>

1.  Select **New**.
2.  In the **Name** field, enter a skill name.
3.  In the **Description** field, enter the description for the skill.
4.  Select **Submit**.


</td></tr><tr><td>

Edit existing skills

</td><td>

1.  Select **Edit**.
2.  Add skills from the **Available** to the **Selected** column.
3.  Select **Save**.


</td></tr></tbody>
</table>    The selected skill is added to the **Skills** list in the user profile.

4.  Add or update agent schedules.

    1.  In the **Agent Schedules** related list, do one of the following:

        -   To view an agent schedule, select a schedule record.
        -   To add a new schedule for the agent, select **New**.
        -   In the **Agent Work Schedule** form, fill in the fields as needed:

            |Field|Description|
            |-----|-----------|
            |From Date|The start date of the agent work schedule.|
            |To Date|The end date of the agent work schedule.|
            |User|Name of the agent.|
            |Work Schedule|Name of the work schedule.|
            |Type|The type of schedule.|

    2.  Select **Submit** to create a new record, or **Update** to modify the record.

5.  Add or update schedule attributes.

    1.  In the **Resource Schedule Attributes** related list, do one of the following:

        -   To view, modify, or delete agent schedule attributes, select a record.
        -   To add a new schedule attributes for the agent, select **New**.
        In the **Resource Schedule Attributes** form, fill in or modify the fields as needed.

        **Note:** You can switch the agent's user profile view to **FSM Profile** or add the **Resource Schedule Attributes** related list to the form if it doesn't appear by default.

<table id="table_svz_v3s_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rank

</td><td>

Sets a ranking rule to prioritize the schedule attributes. The record with the highest rank overrides the other records for a date range.

 The default rank is 10.

</td></tr><tr><td>

Default

</td><td>

If selected, this schedule attribute will be set as the default.

</td></tr><tr><td>

Agent

</td><td>

Name of the agent.

</td></tr><tr><td>

Start location

</td><td>

The location where the agent starts work.

</td></tr><tr><td>

From

</td><td>

The schedule attribute start date.

</td></tr><tr><td>

End location

</td><td>

The location where the agent ends work.

</td></tr><tr><td>

To

</td><td>

The schedule attribute end date.

</td></tr><tr><td>

Travel outside of work hours

</td><td>

Indicates whether the agent can travel outside of work hours.

</td></tr><tr><td>

Post shift max work overtime

</td><td>

The maximum overtime allowed for the agent beyond the scheduled shift.

</td></tr><tr><td>

Distance Unit

</td><td>

The unit of distance. The available units are:

-   Miles
-   Kilometers
 The default unit is **Miles**.

</td></tr><tr><td>

Pre shift max travel time

</td><td>

The maximum travel time allowed before the agent starts the scheduled shift.

</td></tr><tr><td>

Maximum travel radius

</td><td>

The maximum distance \(measured in the specified distance unit\) from the agent's starting location to consider when assigning work order tasks in the Dispatcher Workspace, work order form, or dynamic scheduling.

 A warning message appears if the assigned task is outside of the radius between the task location and the agent's location.

</td></tr><tr><td>

Post shift max travel time

</td><td>

The maximum travel time allowed after the agent ends the scheduled shift.

</td></tr><tr><td>

Maximum part search radius

</td><td>

The maximum distance \(measured in the specified Distance Unit\) from the current location to search for stockrooms to request an inventory.

 The default value is 50 miles.

 **Note:** The stockroom map screen in the Now Mobile Agent application displays the distance in kilometers.

</td></tr><tr><td>

Maximum travel time between stops

</td><td>

The maximum duration the agent can travel between stops.

 **Note:**

This duration is applicable for scheduling and assigning tasks with Schedule Optimization.

</td></tr><tr><td>

Work penalty per hour

</td><td>

The penalty applied for each hour worked by the agent during their scheduled work time.

 This penalty helps to optimizing schedules based on agent optimization weight through Schedule Optimization.

</td></tr><tr><td>

Travel penalty per hour

</td><td>

The penalty applied for each hour the agent travels during work assignments.

</td></tr><tr><td>

Overtime penalty per hour

</td><td>

The penalty applied for each overtime hour the agent works during work assignments.

</td></tr></tbody>
</table>    2.  Select **Submit** to create a new record, or **Update** to modify the record.


## Result

The agent's profile is configured with the appropriate details.

