---
title: Use the Field Service Management Overview dashboard
description: Use the Field Service Management Overview dashboard to review the work orders by their order of priority. You can also view tasks by their assignment groups.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Use the Field Service Management Overview dashboard

Use the Field Service Management Overview dashboard to review the work orders by their order of priority. You can also view tasks by their assignment groups.

![Overview dashboard with charts showing work order and work order task information.](../../../product/field-service-management/image/fsm-overview.png)

## Required ServiceNow AI Platform roles

The wm\_basic role is needed to track the status of work orders.

## Use cases

The following use case provides an example of how an internal manager would use this dashboard.

|User|Dashboard use|
|----|-------------|
|All users with the wm\_basic role|Reviews the work order tasks by priority. Understands the state of the work order tasks.|

## Data visualizations

<table id="table_mcs_hfk_hsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work order by priority

</td><td>

Pie![](../../reporting/image/icon-pie-report.png)

</td><td>

\[wm\_order\]

</td><td>

Overview of work orders based on their priority.

</td></tr><tr><td>

Work order SLA by stage

</td><td>

Pie![](../../reporting/image/icon-pie-report.png)

</td><td>

\[task\_SLA\]

</td><td>

Overview of work order tasks by their stage, such as In progress, Achieved, or Breached.

</td></tr><tr><td>

Work order tasks by state

</td><td>

Bar![](../../reporting/image/icon-bar-report.png)

</td><td>

\[wm\_task\]

</td><td>

Overview of work order tasks by their current state of progress.

</td></tr><tr><td>

Work order tasks by assignment group

</td><td>

Bar![](../../reporting/image/icon-bar-report.png)

</td><td>

\[wm\_task\]

</td><td>

Overview of work order tasks based on the different assignment groups.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

