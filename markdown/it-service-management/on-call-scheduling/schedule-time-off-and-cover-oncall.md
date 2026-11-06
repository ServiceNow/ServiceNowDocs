---
title: Request time off and suggest who can cover
description: You can schedule your own time off and suggest a suitable cover from among fellow roster members.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/on-call-scheduling/schedule-time-off-and-cover-oncall.html
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Viewing schedules and request time-off, On-Call Scheduling, IT Service Management]
---

# Request time off and suggest who can cover

You can schedule your own time off and suggest a suitable cover from among fellow roster members.

## Before you begin

To request time off by members, the **com.snc.on\_call\_rotation.pto.configuration** system property for your on-call group must be **With approval** or **Without approval**. If the setting is **Not allowed**, you can't request time off. A user with the rota\_admin role sets the default for all groups with the system property. They can also override the setting for a specific group in the group's on-call settings.

Role required: itil

## Procedure

1.  Navigate to **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  Select the shift entry.

3.  In the **Actions** list, select **Manage Shift**.

4.  In the Manage Shift dialog box, select **Schedule time off** and then fill in the form.

    \[Omitted image "OC\_SchedTimeOff.png"\] Alt text: Manage Shift dialog box with fields for scheduling time off.

    |Field|Description|
    |-----|-----------|
    |Member|The member getting time off \(typically, yourself\).|
    |Starts and Ends|Start and end dates for the time off.|
    |Proposed cover|Name of a roster member who can provide cover in the absence. This field is required when the time off configuration for the group is **Time off without approval**.|
    |All day event|Option to specify that the time off period involves full workdays.|
    |Notes|Comments to help the shift manager understand the request.|

5.  Select **Schedule**.

    The time off is added to your On-Call calendar. If the time off configuration requires approval, the request remains pending until it is approved.


**Parent Topic:**[Viewing schedules and request time-off](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/on-call-scheduling/viewing-schedules-and-escalation.md)

