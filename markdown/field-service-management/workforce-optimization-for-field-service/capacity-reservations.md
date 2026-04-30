---
title: Capacity Reservations reservation rules
description: Capacity Reservations reservation rules enable you to efficiently distribute total work capacity among work order tasks based on their different attributes, such as work type, location, so on.Create reservation rules based on different types of work to reserve the workload capacity for work order tasks.Reserve a specific percentage of capacity for different attributes of work order tasks, such as work type, location, and so on.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Capacity Reservations reservation rules

Capacity Reservations reservation rules enable you to efficiently distribute total work capacity among work order tasks based on their different attributes, such as work type, location, so on.

You can create multiple reservation rules for different attributes of work order tasks based on priority and demand. Each reservation rule consists of a single or multiple rules and a percentage allocation for the selected attribute that satisfies the condition.

## Reserve the workload capacity for work order tasks

Create reservation rules based on different types of work to reserve the workload capacity for work order tasks.

### Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Reservations**.

2.  Click **New**.

3.  On the form, fill the fields.

4.  |Field|Description|
|-----|-----------|
|Name|Name of the reservation.|
|Description|Description of the reservation category.|
|Table|wm\_task table on which the condition applies. This field is read only.|

5.  In the **Exclude** field, click **Add Filter Condition** or **Add "Or" Clause** to add a condition that excludes the existing Capacity Reservations rule.

    For example, if **Priority level = 1** is added as an exclude condition, the existing reservation rules will be excluded for work orders with a priority level of 1 \(Critical\).

6.  Click **Submit**.


## Create a reservation rule for work order tasks

Reserve a specific percentage of capacity for different attributes of work order tasks, such as work type, location, and so on.

### Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager, sn\_fsm\_tp.fsm\_territory\_manager, sn\_fsm\_tp.fsm\_territory\_planner

### About this task

Manage work assignments by using reservation rules based on defined capacity. For example, you can allocate 25% of total work capacity for installation tasks. Similarly, reserve a portion of a group's or agent's availability to meet specific demands, such as 60% for Break-Fix work types and 40% for Install work types.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Reservations**.

2.  Open a Capacity Reservation from the list.

3.  In the Capacity Reservation Rules related list, click **New**.

4.  On the form, fill the fields.

5.  |Field|Description|
|-----|-----------|
|Name|Name of the reservation rule.|
|Demand Channel|Select the demand channel for the reservation rule. For more information, see [Create a demand channel](../task/create-a-demand-channel.md).|
|Table|wm\_task table on which the condition applies. This field is read only.|

6.  In the **Condition** field, click **Add Filter Condition** or **Add "Or" Clause** to set the filter condition for reserving the workload capacity.

    For example, to reserve workload capacity for particular type of work, you would click Add Filter Condition and create the condition **\[Work Type\] \[is\] \[Install\] AND \[Active\] \[is\] \[true\]**.

7.  On the form, fill the remaining fields.

8.  |Field|Description|
|-----|-----------|
|Percentage Allocated|Percentage to be allocated to the particular work type.|
|Allow overflow|Option for allowing tasks to be assigned beyond the specified capacity if the total capacity is not yet breached.|
|Order|Order in which the reservation rules are evaluated while assigning work.|

9.  Click **Submit**.


