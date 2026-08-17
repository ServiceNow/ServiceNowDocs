---
title: SLA duration types
description: You can select one of two SLA duration types to define the length of time within which a task must be completed before the SLA is breached.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/c\_SLADuration.html
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# SLA duration types

You can select one of two SLA duration types to define the length of time within which a task must be completed before the SLA is breached.

If an SLA schedule is defined, the duration works along with the schedule. In a user-specific duration, you can choose to specify the length of time that an SLA must run before it is marked as breached. Relative durations specify durations that are relative to the start time of the task SLA and are defined using a script.

When you define an SLA, you can select either a **user specified duration** or a **relative duration**.

-   **User specified duration**

    Specifies a static duration period, such as **8 hours**, along with a business schedule. Use the **Duration** field to set the time limit \(days, hours, minutes, seconds\) before the SLA is breached. The number of days specified in the **Duration** field is converted to 24- hour blocks.

    When you set a duration, the form displays an example breach time message showing how the breach date is calculated."

    For example, a 10-hour duration starting January 1, 2015 at 10:30 a.m. with no schedule shows: `An SLA starting now will breach on 2015-01-01 20:30 (Actual elapsed time: 10 Hours)`.

-   **Relative duration**

    Specifies a duration relative to the start time of the task SLA and is defined using a script. Provision of an end date and time in the future is necessary to set a relative duration. For example, you can select a relative duration such as **Breach on Due Date**, **End of next business day** or **Next business day by 4pm**. The set of relative durations is defined in the core configuration using script-based duration calculations.


**Note:** Pause conditions aren't compatible with relative durations.

-   **Specify a relative duration**

    Select a relative duration option such as **Next business day by 4pm** or **End of next business day** from the **Duration type** field.

    When you select a relative duration such as **Next business day by 4pm**, the **Relative duration works on** field is displayed. You can use **Task record** or **SLA record**. The selected record is available as **current** for the relative duration script.

    The **Breach on Due Date** sets the breach time of the SLA to the date and time from the **Due Date** field of the task that the SLA is attached to.

    If the **Due Date** field is empty or contains a past date, the breach time is set to one second after the task SLA start time. If the date and time in **Due Date** falls outside the task SLA schedule, the breach time moves to the next available scheduled time. For example, with an 08:00-16:00 schedule and the **Due Date** value set to **Wednesday 11th Jan 2017 20:30**, the breach time is set to **Thursday 12th 2017 Jan 08:00**.

    If your task record has a target date and time field, you can create an SLA with a relative duration based on that field.


## Relative duration and schedule interaction

When an SLA uses relative duration with a schedule, workflow timer behavior requires additional configuration.

By default, SLA workflows with relative duration ignore the configured schedule and calculate percentage timers \(50%, 75%\) based on actual elapsed time instead of business elapsed time. This means workflow notifications may fire outside scheduled hours even when a schedule is defined.

To make relative duration workflows respect the SLA schedule, create the system property **com.glideapp.workflow.duration.relative\_uses\_schedule** and set it to `true`. When enabled, the workflow calculates percentage timers using business elapsed time based on the schedule.

For more information, see [Define a relative duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DefineARelativeDuration.md) and [Use a relative duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_UseARelativeDuration.md).

**Parent Topic:**[Service Level Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/service-level-management-reference.md)

