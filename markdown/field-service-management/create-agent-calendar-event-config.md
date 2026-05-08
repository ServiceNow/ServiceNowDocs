---
title: Create an event configuration
description: Create event configurations to define and manage event types for the team calendar.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Workforce, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Create an event configuration

Create event configurations to define and manage event types for the team calendar.

## Before you begin

The schedule entry uses the Schedule Span \[cmn\_schedule\_span\] table to store different types of events.

The following types of schedule entries for event type configurations are available by default:

-   Event — Appointment
-   Event — Excluded
-   Event — Meeting
-   Event — Phone
-   Event — Time Off
-   Event — Other

These configurations are inactive by default. You can activate a configuration by navigating to **Agent Schedule** &gt; **Event Configuration**, selecting an event type configuration, and setting the **Active** field to **true** for one or more event configuration types you would like to activate. Each configuration displays as a separate event type on the team calendar.

Role required: agent\_schedule\_admin

## Procedure

1.  Navigate to **Agent Schedule** &gt; **Event Configuration** and perform one of the following actions.

<table id="choicetable_v4z_cfp_gfb"><thead><tr><th align="left" id="d151404e123">

Option

</th><th align="left" id="d151404e126">

Description

</th></tr></thead><tbody><tr><td id="d151404e132">

**Create a configuration from an existing event configuration**

</td><td>

1.  Select the desired configuration.
2.  Right-click the form header and click **Insert and Stay**.

A copy of the selected event type configuration is created.

</td></tr><tr><td id="d151404e155">

**Create a new event configuration**

</td><td>

Click **New**.

</td></tr></tbody>
</table>2.  Fill in the fields on the Event Configuration form, as necessary.

<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name for this configuration.

</td></tr><tr><td>

Config Label

</td><td>

Name displayed for this event in the agent calendar.

</td></tr><tr><td>

Color theme

</td><td>

Color used to display this type of schedule on the agent calendar.

</td></tr><tr><td class="sub-head" colspan="2" align="center">

Setup

</td></tr><tr><td>

Setup

</td><td>

Setup method for this configuration.-   **Simple:** use condition builder to set up this configuration.
-   **Scripted:** use advanced scripts to set up this configuration.


</td></tr><tr><td>

Table

</td><td>

The table where the tasks for this type of configuration are stored.

</td></tr><tr><td>

Filter

</td><td>

Use condition builder to create the desired conditions for the selected task type. For example, the event configuration for Case Tasks includes a filter on the task **State** field to display only those tasks that are open.

</td></tr><tr><td>

User Field

</td><td>

A field from the **Table** that provides the user assigned to the task. For example, the event configuration for Case Tasks uses the **Assigned To** field from the Task table \[sn\_customerservice\_task\]. When a case task is assigned, it appears on the agent calendar for the user selected in this field.

</td></tr><tr><td>

Event type

</td><td>

Type of schedule entry.

</td></tr><tr><td>

Display Field

</td><td>

A field from the **Table** that provides the information to be displayed for this event type on the agent calendar.For example, the event configuration for Case Tasks uses the **Subject** field from the Task table \[sn\_customerservice\_task\]. When a case task is assigned, the subject of the task appears on the agent calendar.

</td></tr><tr><td>

Start Date Field

</td><td>

A field from **Table** that provides the start date for the task. For example, the event configuration for Case Tasks uses the **Expected start** field from the Task table \[sn\_customerservice\_task\]. When a case task is assigned, it appears on the agent calendar starting on the date and time specified in this field. The **Expected start** field must contain a value for the event to appear in Workforce. If the field is empty, the event will not be displayed.

</td></tr><tr><td>

End Date Field

</td><td>

A field from the **Table** that provides the end date for the task. For example, the event configuration for Case Tasks uses the **Due date** field from the Task table \[sn\_customerservice\_task\]. When a case task is assigned, it appears on the agent calendar ending on the date and time specified in this field. The **Due date** field must contain a value for the event to appear in Workforce. If the field is empty, the event will not be displayed.

**Note:** Because the agent schedule administrator can select any fields from the **Task Table** for the **Start Date Field** and the **End Date Field**, it is possible that the end date may be earlier than the start date. In this event, the task is displayed on the agent calendar between the two points in time.

</td></tr><tr><td>

Script

</td><td>

Use advanced scripts to create the event configuration.**Note:** This field is available when the **Scripted** value is selected from the **Setup** field.

</td></tr></tbody>
</table>3.  Perform one of the following actions:

    -   If you created the configuration from an existing configuration, click **Update**.
    -   If you created a new configuration, click **Submit**.

