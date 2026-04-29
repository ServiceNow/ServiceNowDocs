---
title: SLA duration types
description: You can select one of two SLA duration types to define the length of time within which a task must be completed before the SLA is breached.
locale: en-US
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

    Specifies a static duration period, such as **8 hours**, along with a business schedule. The **Duration** field is displayed, enabling you to specify the length of time in days, hours, minutes, and seconds that the SLA must run before it is marked as **breached**. The number of days specified in the **Duration** field is converted to 24- hour blocks.

    Each time that you set a duration, an example breach time information message is displayed at the top of the form. This information assists you in understanding how the breach date is calculated. For example, if the current date is January 1, 2015, the time is 10:30 am, and the duration is set to 10 hours and no schedule has been selected, the following information message is displayed: `An SLA starting now will end breach on 2015-01-01 20:30 (Actual elapsed time: 10 Hours)`.

-   **Relative duration**

    Specifies a duration relative to the start time of the task SLA and is defined using a script. For example, you can select a relative duration such as **Breach on Due Date**, **End of next business day** or **Next business day by 4pm**. The set of relative durations is defined in the core configuration using script-based duration calculations.


**Note:** Pause conditions are not compatible with relative durations.

You can use a relative duration within the Service Level Management application in the following ways:

-   Specify a relative duration.
-   Relative duration usage scenarios.

-   **Specify a relative duration**

    To specify a relative duration, select an option such as **Next business day by 4pm** or **End of next business day** from the list of available relative durations in the **Duration type** field.

    When you select a relative duration such as **Next business day by 4pm**, the **Relative duration works on** field appears. You can specify the record that the relative duration should be calculated for. You can select to use **Task record** or **SLA record** and the record you select is available as **current** for the relative duration script.

    **Note:** If a relative duration is selected, the example breach date information message is not displayed.

    If your task record has a target date and time field, you can create an SLA with a relative duration based on that field.

-   **Relative duration usage scenarios**

    If a schedule is selected in the SLA definition, the SLA duration works with the SLA schedule. For example, an SLA might have a user-specified duration of **16 hours** with the schedule as **8-5 weekdays**. If this SLA starts to run for a task at 8:00, it breaches at 16:00. The breach time is calculated from the schedule that defines working time as eight hours per day from Monday to Friday. So the 16-hours duration equates to two days later in the schedule.

    The **Breach on Due Date** sets the breach time of the SLA to the date and time from the **Due Date** field of the task that the SLA is attached to.

    If the **Due Date** field is empty or occurred in the past, the breach time of the task SLA is calculated to be one second ahead of the task SLA start time. If the date and time in the **Due Date** field is outside the schedule for the task SLA, the breach time is set to the next available scheduled time. For example, if the SLA definition specifies a task SLA schedule as 08:00-16:00 and the value in the **Due Date** field is **Wednesday 11th Jan 2017 20:30**, the breach time is set to **Thursday 12th 2017 Jan 08:00**.

    If your task record has a target date and time field, you can create an SLA with a relative duration based on that field.


**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

