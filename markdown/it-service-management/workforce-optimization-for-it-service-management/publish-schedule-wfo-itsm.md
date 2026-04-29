---
title: Publish a schedule plan for visibility into team coverage
description: Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scheduling your teams' work, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Publish a schedule plan for visibility into team coverage

Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

You can make a copy of a schedule and update it to create a new schedule. Updates could include modifying the schedule start and end dates as well as adding or removing shifts or agents.

When you make a copy of the schedule, the following updates are automatically made to the schedule copy:

-   The start date is set to the current date and the end date to 30 days from the current date.
-   The schedule state changes to **Draft**. You can make the necessary changes to the shift and click **Save**.
-   The schedule only displays agents in the assignment group of the current logged in user.

You can also unpublish a schedule make updates, and then publish it again.

When you unpublish a schedule:

-   If the start date is the either the current date or had occurred in the past, the schedule state remains as **Published** and the end date changes to tomorrow.
-   If the start date is in the future, the application changes the schedule state to **Draft**.
-   If you delete one or more groups in a schedule plan, all agents who are part of the deleted groups are removed from the shifts in the schedule. After you remove the groups, the schedule changes to draft state and the team calendar refreshes with the updated data.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png)\).

3.  Generate a schedule preview.

    1.  Click the **Team Calendar** tab.
    2.  Click the show schedules icon \( ![Show Schedules icon.](../image/show-schedules-icon.png)\)to display in the contextual side panel.
    The team calendar refreshes and generates the preview when you save a work shift.

4.  Publish a schedule.

    1.  Select a schedule and edit the schedule if necessary.
    2.  Edit the schedule if necessary and click **Save**.
    3.  Click **Publish**.

        **Note:** You can click **Delete** in **Draft** state and delete the schedule if you no longer need it.

    All the schedules that are in **Draft** state move to **Published** state. You can view the published schedule in the team calendar.

    **Note:** You can use pagination to scroll through your agents' schedules.


**Parent Topic:**[Scheduling your teams' work in Workforce Optimization for ITSM](../concept/scheduling-configurable-workforce-optimization-itsm.md)

