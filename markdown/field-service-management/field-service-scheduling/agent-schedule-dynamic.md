---
title: Set up agent schedules for dynamic scheduling
description: Dynamic scheduling uses Field Service agent schedules to determine work order tasks to assign to agents. There’s an order in which dynamic scheduling checks agent schedules to see if agents are available.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Set up agent schedules for dynamic scheduling

Dynamic scheduling uses Field Service agent schedules to determine work order tasks to assign to agents. There’s an order in which dynamic scheduling checks agent schedules to see if agents are available.

The first place that dynamic scheduling checks for agent schedules is in the work schedule of an agent. For more information, see [Create a work schedule for agents](../../customer-service-management/task/create-agent-work-schedule.md). If there’s a work schedule available, then that is what dynamic scheduling uses. If no work schedule exists, then dynamic scheduling checks the second place.

The second place that dynamic scheduling checks for an agent schedule are in the Default Agent Work Schedule entry on the WOT Child Dynamic Scheduling Config Page. WOT Child Dynamic Scheduling Config Page is part of Dynamic Scheduling Configuration.

To use this value as a schedule for agents:

1.  First, you must turn on the Allow Dynamic Scheduling to only use work schedule/WFO system property. For more information on turning on the Allow Dynamic Scheduling to only use work schedule/WFO system property, see: [Dynamic scheduling system properties](../reference/dynamic-sched-system-properties.md).
2.  Then, you must verify there’s a value for the Default Agent Work Schedule. If there’s no default agent work schedule, then you must add one. For more information on Adding a value to the Default Agent Work Schedule, see: [Add a default agent work schedule](../task/add-agent-schedule.md).

