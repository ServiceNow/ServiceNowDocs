---
title: Use the Field Service Management Overview dashboard
description: Use the Field Service Management Overview dashboard to review the work orders by their order of priority. You can also view tasks by their assignment groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/Use\_field\_service\_management\_overview\_dashboard.html
release: zurich
product: Field Service Management
classification: field-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting, Field Service Management]
---

# Use the Field Service Management Overview dashboard

Use the Field Service Management Overview dashboard to review the work orders by their order of priority. You can also view tasks by their assignment groups.

\[Omitted image "fsm-overview.png"\] Alt text: Overview dashboard with charts showing work order and work order task information.

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

Pie\[Omitted image "icon-pie-report.png"\] Alt text:

</td><td>

\[wm\_order\]

</td><td>

Overview of work orders based on their priority.

</td></tr><tr><td>

Work order SLA by stage

</td><td>

Pie\[Omitted image "icon-pie-report.png"\] Alt text:

</td><td>

\[task\_SLA\]

</td><td>

Overview of work order tasks by their stage, such as In progress, Achieved, or Breached.

</td></tr><tr><td>

Work order tasks by state

</td><td>

Bar\[Omitted image "icon-bar-report.png"\] Alt text:

</td><td>

\[wm\_task\]

</td><td>

Overview of work order tasks by their current state of progress.

</td></tr><tr><td>

Work order tasks by assignment group

</td><td>

Bar\[Omitted image "icon-bar-report.png"\] Alt text:

</td><td>

\[wm\_task\]

</td><td>

Overview of work order tasks based on the different assignment groups.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and reporting for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/analytics-reporting-fsm.md)

