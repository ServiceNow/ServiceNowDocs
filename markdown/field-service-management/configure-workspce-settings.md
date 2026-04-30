---
title: Configure settings for Dispatcher Workspace
description: Automate processes and provide dispatchers with more information so they can get their job done more effectively.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure settings for Dispatcher Workspace

Automate processes and provide dispatchers with more information so they can get their job done more effectively.

## Before you begin

Role required: admin, wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Workspace Settings**.

2.  Select the workplace settings.

<table id="table_h4y_tfj_rnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Auto-refresh

</td><td>

Automatically refreshes the agent's calendar when an event such as a meeting, training, time-off request, personal, or an ad hoc work event is created in Dispatcher Workspace. Enabling the feature here gives dispatchers the option to enable or disable this setting on Dispatcher Workspace.**Note:** Ensure the system property **Enable Shift Scheduling for FSM to Determine Availability** is enabled. For more information, see [Activate Workforce Optimization for Field Service](activate-wfo-fsm.md).

</td></tr><tr><td>

Enable group metrics setting

</td><td>

Enables the option for dispatchers to turn on metrics for assignment groups in the Dispatcher Workspace. Assignment groups metrics show in the schedule of the Dispatcher Workspace.

</td></tr><tr><td>

Enable agent metrics settings

</td><td>

Enables the option for dispatchers to turn on metrics for agents in the Dispatcher Workspace. Agent metrics show in the contextual side panel of the Dispatcher Workspace.

</td></tr><tr><td>

Enable task assignment modal

</td><td>

Enables the task assignment modal to pop up. When this is enabled, and a task from the task panel is dragged to the schedule, a task assignment modal window will pop up with the details of the task before it’s assigned. This is useful to add a confirmation step to the assignment process.

</td></tr><tr><td>

Schedule based on travel start time

</td><td>

Enables tasks assigned from the task panel to start based on an agent's travel time. Enabling the feature here gives dispatchers the option to enable or disable this setting on Dispatcher Workspace.

</td></tr><tr><td>

Enable navigation to task assignment window

</td><td>

Enables the **Go to assignment window** option to appear in the task panel. The option brings the calendar to the window start of the selected task.**Note:** Select a different task in the task panel to close the assignment window.

</td></tr><tr><td>

Enable icon display on calendar event

</td><td>

Enables icons to display for calendar events on the calendar in Dispatcher Workspace.

</td></tr><tr><td>

Enable showing only available agents and hide off shift agents.

</td><td>

Enables icon to display that allows dispatchers to hide any agents that are not on shift from the calendar in Dispatcher Workspace.

</td></tr><tr><td>

Enable on event hover popover on the dispatcher workspace.

</td><td>

Enables more details to show when you hover over a work order task or a personal event on the calendar in Dispatcher Workspace.

</td></tr><tr><td>

Enable the SLA timer shown within the Work order task cards inside the Task Panel of the Dispatcher workspace

</td><td>

Enables the SLA time to appear on work order task cards in Dispatcher Workspace.

</td></tr><tr><td>

Select SLA timer type shown within the Work order task cards inside the task panel. By default the SLA timer is nonlive.

</td><td>

Enables the SLA time to load on work order task cards either in real-time, or only once when Dispatcher Workspace initially loads.

</td></tr><tr><td>

Add agents by searchable fields.

</td><td>

These are the fields that dispatchers can use to search for agents when they use the Add Agents feature. By default, dispatchers can search for agents by their name, email address, or employee number. You can enable dispatchers to search for agents by any field on the system user records page.

</td></tr><tr><td>

Enable dispatcher to add agents outside of their assigned assignment groups / territories.

</td><td>

Allows dispatchers to use the Add agents feature to search for any agent, even those outside of the assignment group or territory they manage.**Note:** Dispatchers can search for any agent, but they can only assign tasks to agents within their managed assignment group or territory.

</td></tr></tbody>
</table>3.  Select **Save**.


