---
title: Block the calendar of a field agent based on an Emergency Exposure Management diagnostic report
description: Block the calendar of affected and potentially affected agents based on an Emergency Exposure Management diagnostic report.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Emergency Exposure Management, Agent availability and calendars, Managing workforce, Use, Field Service Management]
---

# Block the calendar of a field agent based on an Emergency Exposure Management diagnostic report

Block the calendar of affected and potentially affected agents based on an Emergency Exposure Management diagnostic report.

## Before you begin

Role required: wm\_manager

## About this task

As the Field Service manager, you can view a diagnostic report and take appropriate action to mitigate the spread of infection. You can promote agent safety by blocking the availability of the affected and potentially exposed agents for future dates on the calendar. For more information about the agent calendar, see [Configure the agent calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-agent-calendar.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Diagnostic Reports**.

2.  In the Diagnostics Request form, click the number of the diagnostic request.

3.  Click **Block Agent Calendar** to block the affected agent's calendar.

4.  On the Schedule Entry new record form, fill in the fields.

<table id="table_x4l_nxd_1mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Name of the agent.

</td></tr><tr><td>

Name

</td><td>

Descriptive name for the event.

</td></tr><tr><td>

Type

</td><td>

Type of event scheduled for the agent.**Note:** The event type configurations are inactive by default. For information about activating them, see [Create an event configuration for the agent calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-agent-calendar-event-config.md).

 The event types are:

 -   **Time off**: Personal or work-related event
-   **Appointment**: Appointment for a service
-   **Meeting**: Work-related meeting
-   **Phone call**: Work-related phone call
-   **Excluded**: User is not available for task assignments
-   **On call**: Event created while on call with user
-   **Time off- in approval**: Approved personal or work-related event
-   **Time off- rejected**: Rejected personal or work-related event


</td></tr><tr><td>

When

</td><td>

Start date and time of the personal event.

</td></tr><tr><td>

To

</td><td>

End date and time of the personal event.

</td></tr><tr><td>

All day

</td><td>

Option for indicating that the event lasts all day.

</td></tr><tr><td>

Notes

</td><td>

Enter notes for the event, if any.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  If there are potentially affected agents, block their calendars by doing the following:

    1.  Click the **Impacted field agents** tab.

    2.  In the Field Service Impacted Users list, click the diagnostic request number.

    3.  Repeat steps 3 through 5 to block the calendar of a potentially affected agent for future dates.


**Parent Topic:**[Use Emergency Exposure Management for Field Service agent monitoring and assignments](../concept/use-exposure-management-fsm.md)

