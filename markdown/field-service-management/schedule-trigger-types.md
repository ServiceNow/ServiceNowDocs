---
title: Learn about triggers for work schedules
description: Trigger types determine the initiation of the execution of the work plan.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-19"
reading_time_minutes: 5
breadcrumb: [Reference, Field Service Management]
---

# Learn about triggers for work schedules

Trigger types determine the initiation of the execution of the work plan.

It defines when the schedule should run based on predefined criteria. The following triggers are available for Planned Work Management.

## Duration

Maintenance is performed based on time \(duration\) and is ideal for periodic tasks like inspections and servicing. You can define single or multiple schedules for a same task.

Duration-based schedules can be defined based on trigger types motioned in the following table.

<table id="table_zpq_54h_mhc"><thead><tr><th>

Trigger type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Interval

</td><td>

Generates work orders at defined intervals. For example, you can create a schedule for maintenance to be performed every 15 days.

</td></tr><tr><td>

Weekly

</td><td>

Generates recurring work orders at specified weekly intervals. For example, you can define a maintenance schedule to generate work order once in every three weeks.

</td></tr><tr><td>

Multiple days of the week

</td><td>

Generates work orders on multiple days each week.For example, you can define a schedule to generate work orders on Monday and Wednesday of every third week of the month.

</td></tr><tr><td>

Monthly

</td><td>

Generates recurring work orders at monthly intervals.For example, you can define a schedule to generate work orders once in two months.

</td></tr><tr><td>

Annually

</td><td>

Generates work orders that are repeated annually.For example, you can define a schedule to generate work order on July 25 every year for the specified number of years.

Annual work schedules can either be floating or fixed.

-   **Floating**: The work order is generated on the specified date and month.
-   **Fixed**: The work order is generated on the effective start date of the maintenance plan.

</td></tr><tr><td>

Week in month

</td><td>

Generates recurring work orders that are scheduled for a specified week each month. For example, you can define a schedule to generate work orders for the first week of every month.The available options are:

-   **First**: Generates work orders for the first week of every month.
-   **Second**: Generates work orders for the second week of every month.
-   **Third**: Generates work orders for the third week of every month.
-   **Fourth**: Generates work orders for the fourth week of every month.
-   **Fifth**: Generates work orders for the fifth week of every month.
-   **Sixth**: Generates work orders for the sixth week of every month.

</td></tr><tr><td>

Day in week in month in year

</td><td>

Generates work orders that recur on a particular day of the specified week and month every year.For example, you can define a schedule to generate work orders on Monday of the third week of January every year.

</td></tr></tbody>
</table>When you define a duration-based work schedule that is triggered annually \(fixed\), monthly \(fixed\), or at specific intervals, the occurrence of the next schedule depends on the **Preserve calculated interval** \(PCI\) setting.

|PCI Setting|Behavior|Example|
|-----------|--------|-------|
|Selected \(True\)|The next work order is scheduled based on the original planned interval, regardless of when the last work order was completed.|If the schedule interval is 10 days, the next work order will be created 10 days after the last scheduled date, even if the previous work was done late.|
|Not Selected \(False\)|The next work order is scheduled based on the actual completion date of the last work order.|If the interval is every 10 days and the last work order was completed late, the next one will be scheduled 10 days after that late completion date.|

**Note:** Plan carefully when defining duration-based work schedules. Multiple work schedules for a same task could create a conflict.

## Meter

Maintenance is performed based on count.

Mater-based work schedules consider **Preserve calculated meter** \(PCM\) setting and **sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading** property setting to determine the next schedule.

If the sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading property is turned on, the system uses the initial meter reading when creating the first maintenance schedule. If this setting is off, the first schedule ignores the initial reading and is planned based on the meter details provided \(such as the value in the Every field\).

For example, consider a meter-based work schedule that creates a schedule for every 1000 values of the attribute selected in **Field**.

When both PCM and sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading property are enabled, the maintenance schedule is created for every 1000 occurrences. The first maintenance schedule depends on the initial meter value and the meter value is preserved for calculating the next schedules.

If the sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading property isn’t enabled, the initial value isn’t considered. The next schedule is created for every 1000 values. Both the above scenarios don’t consider the actual schedule occurrence value. The following table shows the next maintenance schedule depending on different settings.

|PCM|Consider initial meter value|Initial meter value|Next schedule occurrence values|
|---|----------------------------|-------------------|-------------------------------|
|True|True|500|1500, 2500, 3500|
|True|True|1600|2600, 3600, 4600|
|True|False|500|1000, 2000, 3000|
|True|False|1600|2000, 3000, 4000|

When PCM isn’t enabled, the next schedule occurrence value depends on the sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading and the actual occurrence value of the previous schedule. The following table shows the next maintenance schedule depending on different settings.

|PCM|Consider initial meter value|Initial meter value|Planned schedule occurrence value \(meter value\)|Actual schedule occurrence value \(meter value\)|Next schedule occurrence values|
|---|----------------------------|-------------------|-------------------------------------------------|------------------------------------------------|-------------------------------|
|False|True|500|1500|1700|2700|
|False|True|500|2700|2800|3800|
|False|True|1600|2600|2700|3700|
|False|True|1600|3700|3800|4800|
|False|False|500|1000|1200|2200|
|False|False|500|2200|2300|3300|
|False|False|1600|2000|2200|3200|
|False|False|1600|3200|3300|4300|

## Condition

Maintenance is scheduled when the specified conditions are met. Work orders for condition-based maintenance schedules are created only when the conditions are met.

For example, you can specify a condition stating that maintenance should be triggered if the installation date of the asset is more than two years old.

## Script

You can apply advanced customized criteria for initiating the schedule through a script. The maintenance is scheduled when the criteria specified in the script are met, and the script returns True.

## Duration or Meter

Maintenance is to be performed based on both time and count, whichever comes first. Verify that you include both the time duration and meter details when setting up the maintenance schedule.

For example, consider a maintenance plan for checking coolant levels for a HVAC system. You can select the trigger as **Duration or Meter** and specify the duration as six months and meter value as 500 hours. The maintenance is scheduled when either of the conditions are met.

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

