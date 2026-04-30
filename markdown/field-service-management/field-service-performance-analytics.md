---
title: Field Service Platform Analytics dashboard
description: The Field Service Platform Analytics dashboard displays the daily and weekly progress of work orders and work order tasks for your assignment groups.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Field Service Management Platform Analytics Solutions, Setting up FSM reports and analytics, Configuring Field Service Management, Field Service Management]
---

# Field Service Platform Analytics dashboard

The Field Service Platform Analytics dashboard displays the daily and weekly progress of work orders and work order tasks for your assignment groups.

![Overview dashboard with charts showing work order and work order task information organized by priority, stage, state, and assignment group.](../../../product/field-service-management/image/fsm-overview.png)

## Required ServiceNow AI Platform roles

-   wm\_admin to Install and activate this Analytics and Reporting Solution.
-   The wm\_manager role is needed to view the performance of work orders and work order tasks.

## Access the Field Service Performance Analytics dashboard

To open the dashboard, navigate to **Field Service** &gt; **Performance Analytics**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_djw_fkq_g5b"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Field Service Manager

</td><td>

Measures overall agent productivity and agent utilization.Compares performance of agents within the assignment group.

 Measures variance from planned durations of tasks.

</td></tr></tbody>
</table>## Indicators

The Field Service Performance Analytics dashboard presents the following key performance indicators:

-   **Open work orders**

    Number of work orders that are not yet closed.

-   **Mean time to resolve work orders**

    The average time taken to resolve work orders.

-   **% Productive time for work order tasks**

    Number of hours agents spent working on the tasks in the last 60 days.

-   **% Agent utilization for work order tasks**

    Number of agents assigned to work on the tasks in the last 60 days.

-   **Closed work orders**

    Number of work orders in the closed state.

-   **Weekly new work orders vs closed work orders**

    Comparison of total number of work order open in a week, and the number of work order closed in that week

-   **Planned vs Actual duration for work order tasks \(hours\)**

    Comparison of total planned hours, for work order tasks and actual time taken to resolve work order tasks by agents.

-   **Weekly Variance from planned work order task duration**

    Difference in hours between the planned duration and actual time taken to complete the work order tasks in a week.


## Breakdowns

-   Assignment Group
-   State
-   Assigned To
-   Priority

## Filters

<table id="table_kjw_fkq_g5b"><thead><tr><th>

Name

</th><th>

Type

</th><th>

UI control type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Group

</td><td>

Reference

</td><td>

Select Single Input

</td><td>

Filter the work order tasks indicator results based on the selected assignment group.

</td></tr></tbody>
</table>