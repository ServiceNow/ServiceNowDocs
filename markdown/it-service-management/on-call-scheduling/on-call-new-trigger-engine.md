---
title: On-Call Scheduling new trigger engine
description: On-Call Scheduling new trigger engine enables the on-call subflows to get launched via the flow runner queue instead of the event queue. Launching via the flow runner queue improves the on-call performance and helps to alert the on-call members faster than launching via event queue.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, On-Call Scheduling, IT Service Management]
---

# On-Call Scheduling new trigger engine

On-Call Scheduling new trigger engine enables the on-call subflows to get launched via the flow runner queue instead of the event queue. Launching via the flow runner queue improves the on-call performance and helps to alert the on-call members faster than launching via event queue.

When a trigger condition set for an on-call trigger rule matches, that trigger rule is run, and the defined subflow in the trigger rule is launched or triggered. The On-call new trigger engine is a mechanism by which on-call subflows get triggered or launched via the flow runner queue.

## Difference between old and new trigger engine

The old trigger engine supports both workflows and subflows. When a workflow or subflow gets triggered, an event is created and launched via the event queue. When multiple events are triggered at the same time, the events remain in the process queue and this causes slower process time and delayed response.

**Note:** The workflow gets processed in the event queue while the subflow gets processed in the flow runner queue.

The new trigger engine only supports on-call subflows and a subflow gets triggered via flow runner queue. Base on-call subflow are marked as high priority, and hence helps launch the on-call subflows faster via the flow runner queue compared to the traditional event queue. This improves the on-call performance and helps to alert the On-call members faster, especially when multiple events are triggered at the same time and are in the process queue.

**Note:** When the new trigger engine is active, the workflow has no impact and the subflow is both launched and processed via the flow runner queue.

Reminder notifications are also sent to user channels even when the instance is upgrading.

The new trigger engine is applicable only when the following conditions are met:

-   Subflows are used. The new engine is only applicable to on-call subflows and not the workflows.
-   The **On-Call rotation new trigger engine** \[**com.snc.on\_call\_rotation.new\_trigger\_engine**\] system property is set to `true`.

**Parent Topic:**[Exploring On-Call Scheduling](exploring-on-call-scheduling.md)

