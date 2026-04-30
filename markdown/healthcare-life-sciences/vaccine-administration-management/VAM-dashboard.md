---
title: Vaccine Administration Management dashboard
description: Use the Vaccine Administration Management dashboard to view vaccine appointments by day, week, and month. You can view scheduled, completed, and no-show appointments, as well as filter appointments by the vaccine center, date, method, and clinician.
locale: en-US
release: xanadu
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Vaccine Administration Management dashboard

Use the Vaccine Administration Management dashboard to view vaccine appointments by day, week, and month. You can view scheduled, completed, and no-show appointments, as well as filter appointments by the vaccine center, date, method, and clinician.

![Vaccine Administration Management dashboard displaying appointment metrics in single score and bar chart form. For more information on these reports, refer to the Reports section.](../image/vaccine-appointment-dashboard.png "Vaccine Administration Management dashboard")

## Required ServiceNow AI Platform roles

-   The sn\_vaccine\_sm.report\_manager role is required to view and edit the dashboard and reports.
-   The sn\_vaccine\_sm.report\_viewer role is required to view the dashboard and reports.

## Access the Vaccine Administration Management dashboard

To open the dashboard, navigate to **Vaccine Administration Management** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_ntt_vml_qqb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Vaccine Administration Management dashboard manager

</td><td>

Can view and edit the Vaccine Administration Management dashboard.

</td></tr><tr><td>

Vaccine Administration Management dashboard viewer

</td><td>

Can view the Vaccine Administration Management dashboard.

</td></tr></tbody>
</table>## Reports

<table id="table_stt_vml_qqb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scheduled Appointments

</td><td>

Single Score ![Single score icon.](../image/icon-single-score-report.png)

</td><td>

Vaccination Task \[sn\_vaccine\_sm\_task\]

</td><td>

Number of scheduled appointments.

</td></tr><tr><td>

Completed Appointments

</td><td>

Single Score ![Single score icon.](../image/icon-single-score-report.png)

</td><td>

Vaccination Task \[sn\_vaccine\_sm\_task\]

</td><td>

Number of completed appointments.

</td></tr><tr><td>

No-Show Appointments

</td><td>

Single Score ![Single score icon.](../image/icon-single-score-report.png)

</td><td>

Vaccination Task \[sn\_vaccine\_sm\_task\]

</td><td>

Number of users who fail to turn up to the scheduled appointments.

</td></tr><tr><td>

Appointments Trending

</td><td>

Column ![Column report icon.](../image/icon-column-report.png)

</td><td>

Vaccination Task \[sn\_vaccine\_sm\_task\]

</td><td>

Segregation of number of scheduled, completed, and no-show appointments.

</td></tr></tbody>
</table>## Filters

<table id="table_utt_vml_qqb"><thead><tr><th>

Name

</th><th>

Filter type

</th><th>

UI control type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vaccine Center

</td><td>

Reference

</td><td>

Select Multiple Input

</td><td>

Filter the report results based on the selected vaccine center.

</td></tr><tr><td>

Date

</td><td>

Date

</td><td>

Select Single Input

</td><td>

Filter the report results based on the selected date.

</td></tr><tr><td>

Method

</td><td>

Reference

</td><td>

Select Multiple Input

</td><td>

Filter the report results based on the selected vaccine method.

</td></tr><tr><td>

Clinician

</td><td>

Reference

</td><td>

Select Multiple Input

</td><td>

Filter the report results based on the selected clinician.

</td></tr></tbody>
</table>**Parent Topic:**[Using Vaccine Administration Management](using-vaccine-administration-management.md)

