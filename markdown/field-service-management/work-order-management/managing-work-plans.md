---
title: Configuring work plans
description: Planned Work Management enables you to create, maintain, and schedule flexible work plans for any recurring activity that requires regular maintenance.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Planned Work Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configuring work plans

Planned Work Management enables you to create, maintain, and schedule flexible work plans for any recurring activity that requires regular maintenance.

You can create a work plan for a product model, or other criteria, such as location, asset, CI, or so on, and specifies the work to be performed. The planned work schedule specifies the timing, by specifying how often and when to perform the work.

For example, You can configure a work plan to perform automobile service for a newly purchased car. The work schedule can specify to perform service every six months for two years from the date of purchase or after completing 10,00 miles, whichever comes first.

## Configuration overview

The steps for setting up work plans are:

1.  [Create a work plan](../task/create-work-plan.md)

    Use work plans to define how and when the work should be performed for any activity.

2.  [Configure a work schedule](../task/configure-work-plan.md)

    Use work schedules define specific criteria to determine when the plan should be executed. This includes defining the start date and end date for the plan's execution.

3.  [Associate a work order template to a work schedule](../task/associate-work-schedule-to-wotemplate.md)

    Map one or more conditions to a planned work schedule. For example, you can set up maintenance for two printers from different brands at the same time. To do this, you must create a schedule for these machines and then map it to different work order templates.

4.  [Create planned work records](../task/create-planned-work-records.md)

    Create work records for work that has been mapped to a work plan. Apply a work plan to the matching records and schedules to create planned work records.

5.  \(Optional\) [Suppress schedule occurrences of your planned work orders](../task/suppress_schedules_of_your_work_plans.md)

    Use schedule suppression to streamline tasks by removing duplicate tasks when schedules overlap. During the schedule suppression period, the system automatically cancels the identified duplicate scheduled tasks so they aren't executed as originally planned.

6.  \(Optional\) [Reschedule the planned work order](../task/modify_so_pwm.md)

    Avoid generating duplicate work orders for overlapping schedule occurrences by changing the start or end date, either advancing or delaying the maintenance work as needed.


