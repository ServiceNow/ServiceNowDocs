---
title: Capacity reservation rules
description: Capacity Reservations enable you to efficiently distribute the total work capacity among work order tasks based on their attributes, such as work type, location, and priority.Create reservation rules based on different types of work to reserve the workload capacity for work order tasks.Reservation rules help allocate a specific percentage of capacity for different attributes of work order tasks, such as work type, location, or priority. This confirms efficient task management and meets specific workload demands.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Capacity reservation rules

Capacity Reservations enable you to efficiently distribute the total work capacity among work order tasks based on their attributes, such as work type, location, and priority.

You can create multiple reservation rules to manage and prioritize work order tasks based on their attributes, such as priority and demand. Each rule assigns a percentage of the total capacity to a specific task type or condition. This helps distribute workloads efficiently and make the best use of available resources.

## Reserve the workload capacity

Create reservation rules based on different types of work to reserve the workload capacity for work order tasks.

### Before you begin

Role required: wm\_admin, wm\_manager, and wm\_internal\_contractor\_manager

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Reservations**.

2.  Click **New**.

3.  On the form, fill the fields.

4.  |Field|Description|
|-----|-----------|
|Name|Name of the reservation \(e.g., "Daily Task Allocation"\).|
|Description|Description of the reservation category \(e.g., "Reservation for daily Install and Breakfix tasks"\).|
|Table|wm\_task table on which the condition applies. This field is read only.|

5.  In the **Exclude** field, click **Add Filter Condition** or **Add "Or" Clause** to define a condition that excludes the existing capacity reservation rule.

    For example, if **Priority level = 1** is added as an exclude condition, the existing reservation rules will be excluded for work orders with a priority level of 1 \(Critical\).

6.  Click **Submit**.


## Create a reservation rule

Reservation rules help allocate a specific percentage of capacity for different attributes of work order tasks, such as work type, location, or priority. This confirms efficient task management and meets specific workload demands.

### Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_manager, wm\_manager, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_tp.fsm\_territory\_planner, wm\_admin, wm\_contractor\_manager\_int

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Capacity Reservations**.

2.  Open a Capacity Reservation from the list.

3.  In the **Capacity Reservation Rules** related list, select **New**.

4.  On the form, fill the fields.

5.  <table id="table_zsy_hfp_jnb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the reservation rule.

</td><td>

 

</td></tr><tr><td>

Demand Channel

</td><td>

Select the demand channel for the reservation rule. For more information, see [Create a demand channel](../task/create-a-demand-channel.md). **Note:** Applies only if territory plugin is installed.

</td><td>

Example: `"Install"` or `"Breakfix"`.

</td></tr><tr><td>

Table

</td><td>

The default table is wm\_task on which the rule applies. \(This is read only.\)

</td><td>

 

</td></tr><tr><td>

Condition

</td><td>

Define conditions to filter the workload. **Note:** Applies only if territory plugin is not installed.

</td><td>

Example: Reserve capacity for Install tasks: ```
[Work Type] [is] [Install] AND [Active]
      [is] [true]
```

.

</td></tr><tr><td>

Percentage Allocated

</td><td>

The percentage of total capacity reserved for this rule. Sum of all percentage allocated should not exceed 100 of all the reservation rules within the reservation.

</td><td>

Example:-   Total daily capacity: 4 tasks.
-   If 25% is allocated for "Install" tasks, 1 task capacity is reserved for Install.


</td></tr><tr><td>

Allow Overflow

</td><td>

Enable or disable overflow for tasks beyond the reserved percentage. When enabled, enables tasks to exceed their reserved percentage if there’s unused capacity.

</td><td>

Example: Two Reservation Rules are defined:-   25% allocated to "Install"
-   25% allocated to "Breakfix"
This means only 25% + 25% = 50% capacity is allocated via the defined reservation rules. Hence, there is 100% - 50% = 50% additional capacity that has not been allocated to any rule.

When **Allow Overflow** is enabled and incoming work exceeds the predefined 25% allocation for either "Install" or "Breakfix," this excess will be taken from the remaining 50% unallocated capacity pool.

</td></tr><tr><td>

Maximum Overflow Percent

</td><td>

Define the maximum percentage that a reservation can exceed its allocation.

</td><td>

Example:-   "Install" is allocated 25% with a maximum overflow of 50%.
-   If the total capacity is assumed to be 4 tasks then Install can take 1 reserved task plus up to 1 additional tasks, for a maximum of 2 tasks \(50% total\).


</td></tr><tr><td>

Order

</td><td>

Determines the sequence in which rules are applied during task assignment.

</td><td>

Example:-   Order 1: Reserve 25% to "Install or Priority 1"
-   Order 2: Reserve 50% to "Install"
For any installation type of tasks as both the rules will satisfy the first order rule will be picked up.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The reservation rule is saved.


### Capacity allocation based on reservation rules

-   Total capacity: 8 tasks
-   Reservation Rules:

    -   Install: 25% \(2 tasks reserved\)
    -   Breakfix: 25% \(2 tasks reserved\)
    **Note:** Unallocated Capacity: 50% \(4 tasks\)


Case 1: Allow Overflow is disabled for Breakfix:

-   The **Allow Overflow** option is disabled for the "Breakfix" service.
-   Scenario: "Breakfix" receives 3 incoming tasks.
    -   2 tasks are assigned based on the reservation rules.
    -   Since **Allow Overflow** is disabled, no additional tasks are allocated from the unreserved capacity.

Case 2: Allow Overflow Handling for Breakfix:

-   The **Allow Overflow** option is enabled for the "Breakfix" service.
-   The **Maximum Overflow Percent** is set to 50%.
-   Scenario: "Breakfix" receives 3 incoming tasks.
    -   2 tasks are assigned following the reservation rules.
    -   1 additional task is allocated from the unreserved capacity \(utilizing up to 50% overflow\).
    -   The system makes room to accommodate 1 more task within the overflow threshold.

