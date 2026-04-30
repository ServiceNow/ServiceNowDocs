---
title: Suppress schedule occurrences of your planned work orders
description: Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring work plans, Configuring Planned Work Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Suppress schedule occurrences of your planned work orders

Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

Use schedule suppression to streamline tasks by removing duplicate tasks when schedules overlap. During the schedule suppression period, the system automatically cancels the identified duplicate scheduled tasks so they aren't executed as originally planned.

For example, consider an MRI machine with scheduled maintenance plans for both monthly and quarterly. If monthly maintenance occurs on the 15th and quarterly maintenance on the 22nd of every third month, these schedules overlap every three months. Both schedules might include tasks, such as air vents cleaning. To avoid doing the same task twice, a suppression period \(for example, seven days\) is used to check for overlaps. If the monthly tasks are covered in the quarterly schedule, the system suppresses the monthly maintenance. This helps prevent duplication, saves resources, and maintains operational efficiency.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open your work plan.

3.  In the Planned Work Schedules related list, select a schedule that you want to suppress with another schedule.

4.  In the Schedule Suppressions related list, select **New**.

5.  On the form, fill in the fields.

6.  |Field|Description|
|-----|-----------|
|Suppress Period|Time period during which overlapping schedule occurrences are identified, allowing the system to suppress duplicate work order tasks.|
|Active|Option to enable this suppression rule.|
|Suppress by|Name of the work schedule that you want to have priority over the current schedule.|
|Order|Order in which this suppression rule is evaluated.|

7.  Select **Submit**.


## Result

The system changes the state of the schedule occurrence to suppressed and cancels the associated work order tasks.

