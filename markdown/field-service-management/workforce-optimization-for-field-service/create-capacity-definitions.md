---
title: Create a capacity definition
description: Allocate work to different task attributes based on their reserved capacity percentage and defined source of capacity.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a capacity definition

Allocate work to different task attributes based on their reserved capacity percentage and defined source of capacity.

## Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager, sn\_fsm\_tp.fsm\_territory\_manager, sn\_fsm\_tp.fsm\_territory\_planner

## About this task

You can define capacity and frequency of work to be performed based on the selected source of capacity, such as number of hours, tasks, or agent's schedule.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Definition**.

2.  Click **New**.

3.  On the form, fill the fields.

4.  <table id="table_dbt_xqp_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the capacity definition.

</td></tr><tr><td>

Description

</td><td>

Description of the capacity definition.

</td></tr><tr><td>

Set capacity by buckets

</td><td>

An option to make the appointment booking slots available based on the defined capacity of work on a daily basis. ORAn option to set the work capacity at bucket level, such as morning, noon, or evening, so that the appointment slots are available throughout the day until the capacity is not breached.

 -   This option is available only when Tasks or Hours is selected from the **Capacity by** field.
-   This option is available only when Daily is selected from the **Frequency** field.


</td></tr><tr><td>

Capacity by

</td><td>

Source of the capacity definition, such as agent schedule, tasks, or hours.

</td></tr><tr><td>

Capacity

</td><td>

Capacity of work to be performed, such as the number of tasks or number of hours. This value is based on an agent's per-day capacity.This field appears only when Tasks or Hours is selected from the **Capacity by** field.

</td></tr><tr><td>

Frequency

</td><td>

Frequency of the work to be performed, such as daily, weekly, monthly, or yearly. This value is based on the total capacity of the assigned work group.-   This field is available only when Tasks or Hours is selected from the **Capacity by** field.
-   This field is automatically set to **Daily** if the Set capacity by buckets option is selected.


</td></tr><tr><td>

Allocation Schedule

</td><td>

Name of the allocation schedule to be linked to the capacity definition record. So that the right amount of capacity is released for the work order tasks till the last available appointment booking slot. This field appears only when the Set capacity by buckets option is cleared.

</td></tr><tr><td>

Reservation name

</td><td>

Name of the capacity reservation.This field appears only when the Set capacity by buckets option is cleared. For more information, see [Capacity reservation rules](../concept/capacity-reservations.md#).

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

Work is allocated to each task attribute based on its reserved capacity.

