---
title: Publish a schedule plan for visibility into team coverage
description: Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.
locale: en-US
release: xanadu
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scheduling in Workforce Optimization for HR, Using Workforce Optimization for HR, Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Publish a schedule plan for visibility into team coverage

Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.

## Before you begin

Role required: sn\_hr\_wfo.admin

## About this task

You can make a copy of a schedule and update it to create a new schedule. Updates could include modifying the schedule start and end dates as well as adding or removing shifts or agents.

When you make a copy of the schedule, the following updates are automatically made to the schedule copy:

-   The start date is set to the current date and the end date to 30 days from the current date.
-   The schedule state changes to **Draft**. You can make the necessary changes to the shift and click **Save**.
-   The schedule only displays agents in the assignment group of the current logged in user.

You can also unpublish a schedule make updates, and then publish it again.

-   If the start date is the either the current date or had occurred in the past, the schedule state remains as **Published** and the end date changes to tomorrow.
-   If the start date is in the future, the scheduler changes the schedule state and agent schedules to **Draft**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).

3.  Generate a schedule preview.

    1.  Click the **Team Calendar** tab.
    2.  Click the Show Schedules \(![Show Schedules icon.](../image/show-schedule-new.png)\) icon to display in the contextual side panel.
    The team calendar refreshes and generates the preview when you save a work shift.

4.  Publish a schedule.

    1.  Select a schedule and edit the schedule if necessary.
    2.  Edit the schedule if necessary and click **Save**.
    3.  Click **Publish**.

        **Note:** You can click **Delete** in **Draft** state and delete the schedule if you no longer need it.


## Result

All the schedules that are in **Draft** state move to **Published** state. You can view the published schedule in the team calendar.

