---
title: Configuring work plans
description: Planned Work Management enables you to create, maintain, and schedule flexible work plans for any recurring activity that requires regular maintenance.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring work plans

Planned Work Management enables you to create, maintain, and schedule flexible work plans for any recurring activity that requires regular maintenance.

You can create a work plan for a product model, or other criteria, such as location, asset, CI, or so on, and specifies the work to be performed. The planned work schedule specifies the timing, by specifying how often and when to perform the work.

For example, You can configure a work plan to perform automobile service for a newly purchased car. The work schedule can specify to perform service every six months for two years from the date of purchase or after completing 10,00 miles, whichever comes first.

## Configuration overview

The steps for setting up work plans are:

1.  Do one of the following:
    -   [Create a work plan](../task/create-work-plan.md)

        Use work plans to define how and when the work should be performed for any activity.

    -   [Migrate maintenance plans to Planned Work Management](../task/migrate-maint-plans-pwm.md)

        Migrate maintenance plans from Planned Maintenance to Planned Work Management.

2.  \(Optional\) [Add grouping criteria](../task/add-grouping-criteria.md)

    Enable grouping of work orders and add the criteria for grouping.

3.  [Configure a work schedule](../task/configure-work-plan.md)

    Use work schedules define specific criteria to determine when the plan should be executed. This includes defining the start date and end date for the plan's execution.

4.  [Associate a work order template to a work schedule](../task/associate-work-schedule-to-wotemplate.md)

    Specify the work order template that must be used to generate work orders when the specified conditions are met.

5.  [Associate a task plan template to a work schedule](../task/map-schedule-to-task-template.md)

    Specify the task plan template that must be used to generate tasks or cases when the specified conditions are met.

6.  [Create planned work records](../task/create-planned-work-records.md)

    Create work records for work that has been mapped to a work plan. Apply a work plan to the matching records and schedules to create planned work records.

7.  [Generate work orders](generate-work-orders.md)

    Generate work orders for the maintenance schedules.

8.  \(Optional\) [Suppress schedule occurrences of your planned work](../task/suppress_schedules_of_your_work_plans.md)

    Use schedule suppression to streamline tasks by removing duplicate tasks when schedules overlap. During the schedule suppression period, the system automatically cancels the identified duplicate scheduled tasks so they aren't executed as originally planned.

9.  \(Optional\) [Reschedule the planned work order](../task/modify_so_pwm.md)

    Avoid generating duplicate work orders for overlapping schedule occurrences by changing the start or end date, either advancing or delaying the maintenance work as needed.


