---
title: Create capacity allocation schedule
description: A Capacity Allocation Schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks. Allocate certain amount of capacity to different schedules so that the right amount of capacity is released for the work order task.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create capacity allocation schedule

A Capacity Allocation Schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks. Allocate certain amount of capacity to different schedules so that the right amount of capacity is released for the work order task.

## Before you begin

Role required: wm\_admin, wm\_manager, wm\_internal\_contractor\_manager, sn\_fsm\_tp.fsm\_territory\_manager, and sn\_fsm\_tp.fsm\_territory\_planner

## About this task

**Example:** Let's assume you have three technicians working in a specific area, each working an 8-hour shift, giving you a total daily capacity of 24 hours.

**Goal:** Ensure some capacity is always available for high-priority same-day tasks.

**Allocation Schedule:**

-   **Day 0 \(Today\):** 100% of the available capacity \(24 hours\) can be booked.
-   **Day 1 to 3:** Only 80% of the available capacity can be booked. This means for each of these days, only 19.2 hours can be booked in advance, reserving 4.8 hours for same-day tasks.
-   **Day 4 to 7:** Only 60% of the available capacity can be booked, which means 14.4 hours per day, reserving 9.6 hours for same-day tasks.
-   **Day 8 and beyond:** 50% of the available capacity can be booked. So, only 12 hours per day can be booked in advance, reserving the remaining 12 hours for same-day tasks.

**Table Representation:**

|Day Range|Allocation Percentage|Bookable Capacity \(Hours\)|Reserved Capacity \(Hours\)|
|---------|---------------------|---------------------------|---------------------------|
|0 \(Today\)|100%|24|0|
|1 to 3|80%|19.2|4.8|
|4 to 7|60%|14.4|9.6|
|8 and beyond|50%|12|12|

By creating this allocation schedule, you ensure that enough capacity is reserved for urgent tasks that may arise on the same day, while still allowing a significant portion of your capacity to be booked in advance.

The available capacity and the reserved capacity is relative to the current day. As a new day begins, the capacities will be automatically updated as per the allocation schedule.

**Table Representation:**

<table id="table_f3q_pjd_2cc"><tbody><tr><td>

**Day/Allocation**

</td><td>

**Day 0**

</td><td>

**Day 1**

</td><td>

**Day 2**

</td><td>

**Day 3**

</td><td>

**Day 4**

</td><td>

**Day 5**

</td><td>

**Day 6**

</td><td>

**Day 7**

</td><td>

**Day 8**

</td><td>

**Day 9**

</td><td>

**Day 10**

</td></tr><tr><td>

**Day 0**

</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

50%

</td><td>

50%

</td><td>

50%

</td></tr><tr><td>

**Day 1**

</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

50%

</td><td>

50%

</td></tr><tr><td>

**Day 2**

</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

50%

</td></tr><tr><td>

**Day 3**

</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td></tr><tr><td>

**Day 4**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td><td>

60%

</td></tr><tr><td>

**Day 5**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td><td>

60%

</td></tr><tr><td>

**Day 6**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td><td>

60%

</td></tr><tr><td>

**Day 7**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td><td>

80%

</td></tr><tr><td>

**Day 8**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td><td>

80%

</td></tr><tr><td>

**Day 9**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td><td>

80%

</td></tr><tr><td>

**Day 10**

</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>



</td><td>

100%

</td></tr></tbody>
</table>**Note:**

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


## Result

The capacity allocation schedule is created.

