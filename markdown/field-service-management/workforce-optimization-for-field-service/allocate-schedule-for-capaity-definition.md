---
title: Create capacity allocation schedule
description: The capacity allocation schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Create capacity allocation schedule

The capacity allocation schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_manager, wm\_manager, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_tp.fsm\_territory\_planner, wm\_admin, wm\_contractor\_manager\_int

## About this task

-   Allocate certain amount of capacity to different schedules so that the right amount of capacity is released for the work order task.
-   Regularly review and adjust your allocation schedule based on historical data and changing business needs.
-   Use the allocation schedule to balance the workload and avoid overburdening your resources.
-   The default percentage of capacity will be allocated for all the days when the relative start date and relative end date of the allocation schedule is not defined.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Allocation Schedules**.

2.  Click **New**.

3.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the allocation schedule record.|
    |Description|Full description of the allocation schedule.|
    |Default % allocation|Default percentage of capacity to be allocated for the schedule. This value is based on the frequency value defined in the capacity definition record.|

4.  In the **Allocation Schedule Details** related list, click **New**.

5.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the schedule.|
    |Relative start|Start date of the allocation schedule.|
    |Relative end|End date of the allocation schedule.|
    |% allocation|Percentage of capacity that should be allocated.|

    The capacity allocation schedule is created.


## Capacity allocation schedule

Let's assume you have three technicians working in a specific area, each working an 8-hour shift, giving you a total daily capacity of 24 hours. The goal is to ensure some capacity is always available for high-priority same-day tasks.

The available capacity and the reserved capacity is relative to the current day. As a new day begins, the capacities will be automatically updated as per the allocation schedule.

-   Day 0 \(Today\): 100% of the available capacity \(24 hours\) can be booked.
-   Day 1 to 3: Only 80% of the available capacity can be booked. This means for each of these days, only 19.2 hours can be booked in advance, reserving 4.8 hours for same-day tasks.
-   Day 4 to 7: Only 60% of the available capacity can be booked, which means 14.4 hours per day, reserving 9.6 hours for same-day tasks.
-   Day 8 and beyond: 50% of the available capacity can be booked. So, only 12 hours per day can be booked in advance, reserving the remaining 12 hours for same-day tasks.

The available capacity and the reserved capacity is relative to the current day. As a new day begins, the capacities will be automatically updated as per the allocation schedule. See the following table representation.

By creating this allocation schedule, you ensure that enough capacity is reserved for urgent tasks that may arise on the same day, while still allowing a significant portion of your capacity to be booked in advance.

![Tabular representation of capacity allocation schedule for Day 0 to Day 10](../image/capacity-allocation-schedule.png)

