---
title: Journey overview dashboard
description: Journey Overview is a comprehensive dashboard that allows you to efficiently track and manage ongoing tasks and journeys within the organization.
locale: en-US
release: xanadu
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2024-08-07"
reading_time_minutes: 3
breadcrumb: [Journey designer dashboards and reports, Using Journey designer, Journey designer, HR Service Delivery, Employee Service Management]
---

# Journey overview dashboard

Journey Overview is a comprehensive dashboard that allows you to efficiently track and manage ongoing tasks and journeys within the organization.

On the dashboard you can view details about different journeys, including the number of journeys that are due, journeys tasks, journey tasks by role and by activity type, and other relevant journey specific information.![Journey overview dashboard](../image/jny-overview-dashboard.png)

## Required ServiceNow AI Platform roles

The sn\_jny.reader role is needed to access this dashboard.

## Access the Journey overview dashboard

To open the dashboard, navigate to **All** &gt; **Journey designer** &gt; **Administration** &gt; **Journey overview**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_kqc_vx2_cbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Journey/HR Coordinator

</td><td>

Access the journey overview dashboard to efficiently manage and analyze different journeys within the organization.

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

Single score ![](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

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

Journey accelerator tasks due soon

</td><td>

Single score ![](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

Journey Accelerator Task \[sn\_ja\_task\]

</td><td>

Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.

</td></tr><tr><td>

Lifecycle events tasks due soon

</td><td>

Single score ![](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

Task \[task\]

</td><td>

Task table provides means for creating and completing Tasks, as well as tracking their workflow in your instance.

</td></tr><tr><td>

Overdue journey accelerator tasks by role

</td><td>

Bar ![](../../../use/reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Journey Accelerator Task \[sn\_ja\_task\]

</td><td>

Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.

</td></tr><tr><td>

Overdue lifecycle events tasks by activity type

</td><td>

Bar ![](../../../use/reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Task \[task\]

</td><td>

Task table provides means for creating and completing tasks, as well as tracking their workflow in your instance.

</td></tr><tr><td>

Journey status

</td><td>

Line ![](../../../use/reporting/image/inline-data-vis-96px-line.png)

</td><td>

Task \[task\]

</td><td>

Task table provides means for creating and completing tasks, as well as tracking their workflow in your instance.

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

