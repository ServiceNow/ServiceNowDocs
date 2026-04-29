---
title: Create capacity buckets to distribute the workload capacity for a day
description: Create capacity buckets for the selected capacity definition to distribute the workload capacity at different appointment slots throughout the day.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a capacity definition, Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Create capacity buckets to distribute the workload capacity for a day

Create capacity buckets for the selected capacity definition to distribute the workload capacity at different appointment slots throughout the day.

## Before you begin

Select the **Set capacity by buckets** option to create capacity buckets.

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager, sn\_fsm\_tp.fsm\_territory\_manager, sn\_fsm\_tp.fsm\_territory\_planner

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Definitions**.

2.  Open a capacity definition from the list.

3.  In the Capacity Buckets related list, click **New**.

4.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the capacity bucket.|
    |Start|Start time from when the bucket is available to assign the work order tasks/book appointments.|
    |End|End time until when the bucket is available to assign the work order tasks/book appointments.|
    |% Capacity|Percentage of workload capacity assigned to the bucket.|
    |Allocation Schedule|Name of the allocation schedule to be linked to the capacity bucket.|
    |Reservation Name|Name of the reservation rule to be linked to the capacity bucket.|

5.  Click **Submit**.

6.  Repeat steps 3 through 5 until the complete capacity is distributed throughout the day.


## Result

The defined capacity is distributed among the newly created capacity buckets.

