---
title: Publish a schedule plan for visibility into team coverage
description: Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedule, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Publish a schedule plan for visibility into team coverage

Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

You can make a copy of a schedule and update it to create a new schedule. Updates could include modifying the schedule start and end dates as well as adding or removing shifts or agents.

When you make a copy of the schedule, the following updates are automatically made to the schedule copy:

-   The start date is set to the current date and the end date to 30 days from the current date.
-   The schedule state changes to **Draft**. You can make the necessary changes to the shift and select **Save**.
-   The schedule only displays agents in the assignment group of the current logged in user.

You can also unpublish a schedule make updates, and then publish it again.

-   If the start date is the either the current date or had occurred in the past, the schedule state remains as **Published** and the end date changes to tomorrow.
-   If the start date is in the future, the scheduler changes the schedule state and agent schedules to **Draft**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select the Schedule icon \(![Schedule icon](../image/schedule-new.png)\).

3.  Generate a schedule preview.

    1.  Select the **Team Calendar** tab.
    2.  Select the Show Schedules \(![Show Schedules icon.](../image/show-schedule-new.png)\) icon to display in the contextual side panel.
    The team calendar refreshes and generates the preview when you save a work shift.

4.  Publish a schedule.

    1.  Select a schedule and edit the schedule if necessary.
    2.  Edit the schedule if necessary and select **Save**.
    3.  Select **Publish**.

        **Note:** You can select **Delete** in **Draft** state and delete the schedule if you no longer need it.


## Result

All the schedules that are in **Draft** state move to **Published** state. You can view the published schedule on the team calendar for the assigned agents. You can also analyze the scheduling gaps and staffing information by switch between the day, week, and monthviews in the drop-down. Agents can view their published schedules and approved leaves on MS Outlook after synchronizing their team calendars and events with Microsoft Outlook.

**Parent Topic:**[Schedule in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)

