---
title: Create a schedule plan
description: Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedule, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Create a schedule plan

Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

You can set the number of days to cache agent schedules using the **sn\_shift\_planning.number\_of\_days\_to\_cache** [system property](../reference/components-installed-configurable-wfo-cs.md). The **Total coverage/demand** row displays the number of agents covering each shift in a day. The day view displays the demand for the number of agents forecast for every hour in a day. For example, 4/5 shows that you have four agents scheduled for an hourly time slot, 11 AM to 12 PM and the agent demand forecast for that hour is 5.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon.](../image/schedule-new.png)\) icon.

3.  Create a schedule plan.

    1.  Click the **Team Calendar** tab.

        **Note:** You can analyze the staff alignment for a day, week, or month.

    2.  In the contextual side panel, click the show schedules icon ![Show Schedules icon.](../image/show-schedule-new.png) to display the schedules.
    3.  In the Schedules panel, click ![Create New Schedule icon.](../image/create-schedule-new.png) icon.
    4.  In the **Name** field, enter a name for the schedule plan.
    5.  From the **Start Date** field, select a date to start the schedule plan and click **OK**.
    6.  From the **End Date** field, select a date to end the schedule plan and click **OK**.
    7.  Click **Save schedule**.
    You can view the schedule of all agents in the assignment group that you directly or additionally manage.

4.  Add a work shift to the schedule plan.

    **Note:** To add more shifts to an existing schedule plan, select the schedule plan and then add the work shift.

    1.  In the contextual side panel, click **Add Shift**.
    2.  In the **Shift** field, select the work shift that you want to add to the schedule plan.
    3.  In the **Event type** field, select the work event that categorizes the work shift.
5.  Add agents to the work shift.

    1.  In the **Agents** field, search for agents and add one or more agents to add to the shift.
    2.  Click **Save**.
    **Note:** It may take a few minutes for the screen to refresh.


## Result

The schedule plan is created in Draft state.

## What to do next

[Publish a schedule plan for visibility into team coverage](generate-preview-schedule-plan-configurable-wfo-cs.md).

**Parent Topic:**[Schedule in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)

