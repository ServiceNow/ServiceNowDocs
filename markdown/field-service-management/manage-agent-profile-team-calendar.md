---
title: Update an agent's profile
description: Update shifts, skills, schedules, work parameters, and work order tasks for agents in your assignment groups.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View an agent profile, Managing agents and agent groups on the team calendar, Using the team calendar, Workforce, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Update an agent's profile

Update shifts, skills, schedules, work parameters, and work order tasks for agents in your assignment groups.

## Before you begin

Role required: wm\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Workforce**.

2.  Select **Schedule** from the View Controls list.

3.  Select an agent name.

    The agent profile preview appears.

4.  To add or edit agent skills:

    1.  Click the agent's name.

    2.  In the **Skills** related list, either add new skills or edit existing skills for the agent.

<table id="table_lvj_2tk_nkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Add new skills

</td><td>

1.  Click **New**.
2.  In the **Name** field, enter a skill name.
3.  In the **Description** field, enter the description for the skill.
4.  Click **Submit**.


</td></tr><tr><td>

Edit existing skills

</td><td>

1.  Click **Edit**.
2.  Add skills from the **Available** to the **Selected** column.
3.  Click **Save**.


</td></tr></tbody>
</table>    The selected skill is added to the **Skills** list in the user profile.

5.  To view or modify an agent schedule:

    1.  In the **Agent Schedules** related list, do one of the following:

        -   To view an agent schedule, select a schedule record.
        -   To add a new schedule for the agent, click **New**.
        -   In the **Agent Work Schedule** form, fill in the fields as needed:

            |Field|Description|
            |-----|-----------|
            |From Date|The start date of the agent work schedule.|
            |To Date|The end date of the agent work schedule.|
            |User|Name of the agent.|
            |Work Schedule|Name of the work schedule.|
            |Type|The type of schedule.|

6.  To add work parameters:

    1.  In the **Work Parameters** related list, click **New**.

    2.  In the **Work Parameters** form, fill in the fields as needed.

<table id="table_svz_v3s_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Name of the agent.

</td></tr><tr><td>

Distance Unit

</td><td>

Select **Miles** or **kilometers**.

</td></tr><tr><td>

Travel outside of work hours

</td><td>

Select **Yes** or **No**.

</td></tr><tr><td>

Maximum travel radius

</td><td>

Radius in selected distance unit \(miles or kilometers\).

</td></tr><tr><td>

Maximum part search radius

</td><td>

Radius in selected distance unit \(miles or kilometers\). The default value is 50 miles. **Note:** The stockroom map screen in the Now Mobile Agent application displays the distance in kilometers.

</td></tr></tbody>
</table>    The maximum travel radius is considered as agent's work radius to assign the work order tasks in Dispatcher Workspace, work order form, or dynamic scheduling. A warning message appears if the assigned task is outside of the radius between task location and the agent's location.

7.  Click **Submit**.


**Parent Topic:**[View an agent profile](view-agent-profile.md)

