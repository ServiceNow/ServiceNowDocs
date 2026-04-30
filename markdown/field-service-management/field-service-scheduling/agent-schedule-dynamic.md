---
title: Setting up agent schedules for dynamic scheduling
description: Dynamic scheduling determines how work order tasks are assigned to agents by checking their availability.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Setting up agent schedules for dynamic scheduling

Dynamic scheduling determines how work order tasks are assigned to agents by checking their availability.

Dynamic scheduling systematically evaluates agent schedules to ensure optimal task allocation:

1.  Check agent work schedule: Dynamic scheduling first looks at the individual work schedule assigned to an agent. If an agent has a specific work schedule defined, this schedule is used to determine their availability for tasks. For more information, see [Create a work schedule for an agent or technician](../../customer-service-management/task/create-agent-work-schedule.md).
2.  Default agent work schedule: If no specific work schedule is found for an agent, dynamic scheduling then checks the default agent work schedule. This setting is found on the **WOT Child Dynamic Scheduling Config** page, part of dynamic scheduling configuration. To ensure dynamic scheduling uses the default agent work schedule, follow these steps:
    -   Enable system property: Set the system property `Allow Dynamic Scheduling to only use work schedule/WFO`. This ensures that the dynamic scheduling process adheres to the default work schedule when no specific work schedule is available. For more information, see [Dynamic scheduling system properties](../reference/dynamic-sched-system-properties.md).
    -   Set a default agent work schedule: Ensure a value is defined for the Default Agent Work Schedule. If it’s missing, you must add one to avoid scheduling issues. For more information, see: [Add a default agent work schedule](../task/add-agent-schedule.md).

