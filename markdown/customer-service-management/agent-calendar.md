---
title: Managing agent calendar
description: Customer service agents and field service technicians can use the agent calendar to see work schedules and assignments and also add personal events such as meetings or appointments.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage schedules and sites, Using Customer Service Management, Customer Service Management]
---

# Managing agent calendar

Customer service agents and field service technicians can use the agent calendar to see work schedules and assignments and also add personal events such as meetings or appointments.

The agent calendar provides a tool for maintaining different work schedules or shifts and assigning agents and technicians to shifts for specific time periods. The calendar has the flexibility to accommodate work schedules that are fixed or varied and shifts that rotate by week, month, or other patterns. The agent calendar administrator creates the calendar configuration, including a schedule configuration for each calendar user and the types of tasks to display on the calendar.

The schedule information stored in the agent calendar is used by other ServiceNow applications and features, such as the assignment workbench, central dispatch, and auto assignment. The assignment workbench uses agent availability, based on upcoming work schedules and personal time off, when evaluating predefined criteria and recommending agents for case assignment. Auto assignment in Service Management core applications, such as Field Service Management and Facilities Service Management, evaluate agent work schedules before assigning tasks.

The agent calendar administrator has access to the Agent Schedule menu in the application navigator. This menu includes the following modules:

-   **Event Configuration**: create a configuration for each type of event or task displayed on the agent calendar.
-   **Work Schedule**: create one or more work schedules for each calendar user.
-   **Agent Personal Events**: create personal schedules for each agent and add events to those schedules.
-   **Schedule**: create or modify schedules. For more information, see [Schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Viewing the calendar

Customer service agents and field service technicians with the agent\_schedule\_user role can access their personal calendars in the following ways:

-   **Customer Service** &gt; **My Schedule**
-   **Field Service** &gt; **Agent** &gt; **My Schedule**

**Note:** The agent calendar is supported in the mobile application and the mobile web.

![Calendar displaying an agent's schedule and daily assignments including work hours, tasks, personal meetings, and appointments.](../image/AgentCalendar.png "Agent Calendar")

The calendar can display a single day, a week, or a month. Buttons in the calendar header allow you to switch views as well as go backward or forward in time. An agent's scheduled work hours are highlighted in gray and the current day is highlighted in blue. The agent calendar displays work or tasks assigned to the agent as well as personal events. Each type of event is displayed on the calendar using a different color.

Agents can add events to their calendars by double-clicking a specific time slot and entering the details in the New Event popup window or by clicking and dragging. Agents can also move events by dragging and dropping. Click an event to display a popup with event details and double-click an event to open the event record.

## Plugins

The Agent Schedule plugin \(com.snc.agent\_schedule\) is activated as part of the Customer Service Management and Field Service Management plugins.

## Tables

The Agent Schedule plugin adds the following tables.

<table id="table_byk_1mz_gx"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Work Schedule\[agent\_work\_schedule\]

</td><td>

Stores one or more work schedules for each agent, including the date range for the schedule and the schedule type.

</td></tr><tr><td>

Agent Personal Schedule\[agent\_events\]

</td><td>

Stores personal calendar events for each agent, such as training, personal time off, or meetings.

</td></tr><tr><td>

Event Configuration\[agent\_schedule\_task\_config\]

</td><td>

Stores a configuration for each type of task displayed on the agent calendar, such as case tasks or work order tasks.

</td></tr><tr><td>

Agent Schedule User Config\[agent\_schedule\_user\_pref\]

</td><td>

Stores the agent’s personalization data for the calendar. A user configuration is created automatically when a user with the agent\_schedule\_user role accesses their personal calendar.

</td></tr><tr><td>

Agent Schedule Relationship\[agent\_schedule\_task\_config\_rel\_user\_pref\]

</td><td>

Stores the relationships between agent configurations and event configurations. Relationship entries are created automatically based on a user's read access to the task tables selected in the event configurations.

</td></tr><tr><td>

Agent Schedule Definition Theme\[agent\_schedule\_definition\_theme\]

</td><td>

Stores the colors used to display different types of tasks on the agent calendar.

</td></tr></tbody>
</table>## User Roles

The following user roles are included with the Agent Schedule \(com.snc.agent\_schedule\) plugin.

<table id="table_mvx_aem_gx"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent schedule administrator\[agent\_schedule\_admin\]

</td><td>

Sets up the Agent Calendar configuration. Contains roles:-   agent\_schedule\_user
-   schedule\_admin

</td></tr><tr><td>

Agent schedule user\[agent\_schedule\_user\]

</td><td>

Allows customer service agents and field service technicians to access and update their personal calendars.

</td></tr></tbody>
</table>**Related topics**  


[Creating and using schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

[Configuring an agent calendar](configure-agent-calendar.md)

