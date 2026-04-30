---
title: Schedules within SLA
description: Schedules within SLA enable you to define the time periods during which the SLAs accumulate business time.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Schedules within SLA

Schedules within SLA enable you to define the time periods during which the SLAs accumulate business time.

Schedules are typically based on the working hours of the resource or departments to whom a task is allocated. When you define an SLA, you can select a schedule during which the SLA will accumulate business time. You can specify the schedule that each SLA must use in the SLA definition form.

## Schedules in SLA definitions

You can specify the schedule to be used when creating new task SLAs in the **Schedule source** field. You can specify one of the following options:

-   **No schedule**: If the **No Schedule** option is selected, the SLA will calculate based on a 24 x 7 schedule.
-   **SLA definition**: If the **SLA definition** option is selected, the **Schedule** drop-down list appears.
-   **Schedule**: Specify the hours during which the SLA timer runs. These set of schedules are defined in the core configuration. For example, you can select a schedule of **8-5 weekdays** or **8-5 weekdays excluding holidays**.
-   **Task table field**: This option picks its title from the option selected in the **Table** field earlier on the **SLA Definition** form. For example, if **Incident** is selected in the **Table** field, then this option appears as **Incident field**. If the **Task table field** option is selected, the **Schedule source field** drop-down list appears.
-   Schedule source field: This option allows you to select the appropriate field from the task such as an incident or problem that will provide the schedule. For example, Configuration item &gt; Schedule.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

