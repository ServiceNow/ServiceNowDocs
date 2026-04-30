---
title: Move an event
description: Accelerate the execution process by moving high priority events from the default queue to an isolated queue with just one click.
locale: en-US
release: xanadu
product: System Events
classification: system-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing system events, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# Move an event

Accelerate the execution process by moving high priority events from the default queue to an isolated queue with just one click.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Event registry**.

    A list of registered events shows up.

2.  Select the event you want to move.

    The Event Registration form of the selected event shows up.

3.  Select **Move to Default Queue** to move the event from the current queue and accelerate its execution.

    **Note:** If you are currently in the default queue, you will have the **Move to Adaptive Event Queue** option to select.

    The processor can execute only one event at a time. So, if you move an event to a queue, it gets executed only when the processor is available.

4.  Navigate to **System Diagnostics** &gt; **Stats** &gt; **Adaptive Events** to track the average execution time of the events.

    You can select any slow moving event and change the queue as required. You can also register an event to show up on the event registry list.


