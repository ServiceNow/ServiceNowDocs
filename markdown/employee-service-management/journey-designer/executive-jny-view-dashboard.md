---
title: Executive journey view dashboard
description: Executive-focused dashboard with reports containing information such as the number of employees completing their journeys, SLA breaches, average days to complete journeys, and other metrics executives would be interested in.
locale: en-US
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Journey designer dashboards and reports, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Executive journey view dashboard

Executive-focused dashboard with reports containing information such as the number of employees completing their journeys, SLA breaches, average days to complete journeys, and other metrics executives would be interested in.

![Executive journey view dashboard](../image/jny-executive-dashboard.png)

## Required ServiceNow AI Platform roles

The sn\_jny.reader role is needed to access this dashboard.

## Access the Executive journey overview dashboard

To open the dashboard, navigate to **All** &gt; **Journey designer** &gt; **Administration** &gt; **Executive journey view**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_o2x_3k1_dbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Leaders/Business executives/HR coordinators

</td><td>

Review and comprehend the significance of journey, quickly summarize them, and review task completion outcomes.

</td></tr></tbody>
</table>## Reports

<table id="table_pqc_vx2_cbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overdue journey accelerator tasks

</td><td>

Single score

![](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

Journey Accelerator Task \[sn\_ja\_task\]

</td><td>

Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.

</td></tr><tr><td>

Overdue lifecycle events tasks

</td><td>

Single score ![](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

Task \[task\]

</td><td>

The Task table provides means for creating and completing Tasks, as well as tracking their workflow in your instance.

</td></tr><tr><td>

Employee journey status

</td><td>

Donut ![](../../../use/reporting/image/inline-data-vis-96px-donut.png)

</td><td>

Journey \[sn\_jny\_journey\]

</td><td>

Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.

</td></tr><tr><td>

Service level agreement breached cases

</td><td>

Bar ![](../../../use/reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Task SLA \[task\_sla\]

</td><td>

Task table provides means for creating and completing Tasks, as well as tracking their workflow in your instance.

</td></tr><tr><td>

Journeys opened each month

</td><td>

Line ![](../../../use/reporting/image/inline-data-vis-96px-line.png)

</td><td>

Journey \[sn\_jny\_journey\]

</td><td>

Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.

</td></tr><tr><td>

Employees onboarding each month

</td><td>

Area ![](../../../use/reporting/image/inline-data-vis-96px-area.png)

</td><td>

Task \[task\]

</td><td>

Task table provides means for creating and completing Tasks, as well as tracking their workflow in your instance.

</td></tr><tr><td>

Average number of days to complete a journey

</td><td>

Bar ![](../../../use/reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Average no of days to complete a journey \(indicator\)

</td><td>

Provides the number of data it takes to complete a journey.

</td></tr></tbody>
</table>## Filters

<table id="table_rqc_vx2_cbc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Multi-select

</td><td>

Displays various tasks based on the location of the journey employee.

</td></tr><tr><td>

Department

</td><td>

Multi-select

</td><td>

Displays tasks based on the department the task assignee belongs to.

</td></tr><tr><td>

Journey start date

</td><td>

Choice

</td><td>

Displays tasks based on the journey start date.

</td></tr><tr><td>

Journey type

</td><td>

Multi-select

</td><td>

Displays tasks based on the journey type.

</td></tr><tr><td>

Employee start date

</td><td>

Choice

</td><td>

Displays tasks based on the start date of the employee.

</td></tr></tbody>
</table>**Parent Topic:**[Journey designer dashboards and reports](../reference/jny-report-dashboards.md)

