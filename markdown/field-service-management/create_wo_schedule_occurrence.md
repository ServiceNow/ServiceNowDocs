---
title: Create work orders for schedule occurrences
description: Create work orders for schedule occurrences to maintain a record of specific occurrences or maintenance cycles of the schedule. The work orders that are generated for each schedule occurrence are mapped to their corresponding occurrence, enabling the tracking of activities performed for different maintenance cycles.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Managing work orders for the planned work, Using Field Service Management, Field Service Management]
---

# Create work orders for schedule occurrences

Create work orders for schedule occurrences to maintain a record of specific occurrences or maintenance cycles of the schedule. The work orders that are generated for each schedule occurrence are mapped to their corresponding occurrence, enabling the tracking of activities performed for different maintenance cycles.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

You can generate a single work order or multiple work orders for a schedule occurrence depending on the number of work order templates associated with it. For example, if two work order templates are configured for a work schedule, the system generates two work orders for that particular schedule occurrence, based on each template.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open the work plan.

3.  In the Planned Work Schedules related list, select the schedule for which you want to review the schedule occurrences.

4.  In the Schedule Occurrences related list, select the schedule occurrence for which you want to create work orders.

5.  In the Related Links section, select **Generate work order**.

6.  View the work orders associated with the event from the Work Orders related list.


## Result

A list of work orders is automatically generated for the selected schedule occurrence, taking into account the number of work order templates associated with the schedule.

**Parent Topic:**[Managing work orders for the planned work](../concept/creating-work-orders-from-planned-work.md)

**Related topics**  


[Associate a work order template to a work schedule](associate-work-schedule-to-wotemplate.md)

