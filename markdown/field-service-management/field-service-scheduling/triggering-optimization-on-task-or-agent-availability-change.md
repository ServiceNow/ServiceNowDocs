---
title: Optimizing technician schedules in response to urgent events
description: Prioritized event optimization is a mode of intraday optimization that aims to run a faster, more focused intraday process. This mode specifically targets the most critical events.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimizing technician schedules, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Optimizing technician schedules in response to urgent events

Prioritized event optimization is a mode of intraday optimization that aims to run a faster, more focused intraday process. This mode specifically targets the most critical events.

## About intraday optimization for prioritized events

Prioritized event optimization enables same-day, event-driven schedule adjustments. It runs shortly after a prioritized event occurs. This mode enables targeted optimization of a specific group of Field Service technicians and tasks without adjusting the entire qualifier. The buffer window property determines the number of minutes to collect priority events before running the optimization job. If the buffer is set to one minute, the system waits one minute after a priority event to collect any additional events before optimizing.

For technicians, the optimization engine considers all those who have the qualifier role for optimization. Differing from default intraday optimization, the optimization engine ignores overlapping territories and only includes the territories directly impacted by the events.

For tasks, if the affected record is an active task that is not schedule-locked, the optimization engine considers it for optimization. If the affected record is a technician, the optimization engine considers any pending dispatch tasks that have an SLA breach or are due to end within the next hour. Additionally, for all tables, the optimization engine includes all currently scheduled or assigned tasks of the technicians being considered.

To set up intraday optimization for prioritized events, see [Configure immediate optimization for prioritized events](configure-immediate-optimization.md).

Custom event types and flows for intraday must be migrated to the new Intraday Event Type table. To create records for custom options, you must update the flows to populate the event type field with the corresponding references, converting from a drop-down to a new table.

**Related topics**  


[Schedule Optimization properties](../reference/schedule-optimization-properties.md)

