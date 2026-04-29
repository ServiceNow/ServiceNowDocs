---
title: Configure optimization for prioritized events
description: Configure prioritized event optimization to enable schedule adjustments in response to critical, same-day events.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Optimization for prioritized events, Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure optimization for prioritized events

Configure prioritized event optimization to enable schedule adjustments in response to critical, same-day events.

## Before you begin

To set the system properties for the prioritized event mode, see [Schedule Optimization properties](../reference/schedule-optimization-properties.md).

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Event Types**.

2.  In the **Prioritized** and **Active** fields, set the values to true for the event types you want to include in immediate optimization.

    **Note:** Only three event types may be enabled for prioritized optimization at one time. Confirm that only the most critical events are enabled.

3.  Open the record for each event type you selected.

4.  Verify that the **Active** and **Prioritized** check boxes are checked.

5.  Select **Save** if you have made any changes to the record.

6.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Configurations**.

7.  Open the non-default intraday configuration that you want to enable prioritized mode for.

8.  In the **Qualifiers** tab, set **Enable prioritized event optimization** to true for the group or territory you want to include in immediate optimization.

    If the qualifier is not listed, select **Edit** to add an existing qualifier to the list and **Save** your changes.

    **Note:**

    -   **Overlapping territories.** When priority optimization runs for an overlapping territory, the scope of the optimization will be limited to the impacted territory only. Tasks and technicians from the overlapping territories will not be considered.
    -   **Technician Assignment:** If a technician is part of two territories, they will only be sent to one. Confirm that each technician is assigned to the most appropriate territory to simplify the process and maintain maximum performance.
9.  Select **Update**.


## Result

When the selected event type occurs, optimization runs shortly after. The optimization run creates an event for the task, which then generates a prioritized job. The task is assigned accordingly. When an event no longer meets the defined condition, it's removed from prioritized optimization and also from the scheduled intraday run to maintain consistency.

**Related topics**  


[Activate intraday optimization](activate-intraday-optimization.md)

[Configure intraday optimization](configure-intraday-optimization.md)

