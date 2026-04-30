---
title: Setting up Soft Booking
description: Soft Booking allows dispatchers to schedule tasks without triggering immediate notifications or downstream workflows. This feature provides dispatchers with a "planning buffer" to optimize agent schedules before confirming tasks.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Setting up Soft Booking

Soft Booking allows dispatchers to schedule tasks without triggering immediate notifications or downstream workflows. This feature provides dispatchers with a "planning buffer" to optimize agent schedules before confirming tasks.

Soft Booking enables dispatchers to design an optimal automated scheduling solution without notifying the assigned agent or triggering assignment workflows right away. Field service agents receive notifications on their work order tasks only when dispatchers confirm work assignments, ensuring that schedules are well-planned and efficient.

## Configuration overview

As an administrator, you can enable the 'Use scheduled state' from All &gt; Field Service Administration &gt;Configuration. Modify the Update task state from Scheduled to Assigned property. By default, tasks scheduled within the next 12 hours are set to "Assigned".

When enabled, a new state "Scheduled" appears in work order request and task records \(state sequence varies based on whether qualification is enabled or not\).

Turning off Use scheduled state moves all tasks from Scheduled to Assigned. A prompt appears indicating this shift. Be cautious when turning the Use scheduled state property on or off, as it affects all tasks in the Scheduled state.

**Related topics**  


[Configure the Scheduled state](../task/configure-scheduled-state.md)

