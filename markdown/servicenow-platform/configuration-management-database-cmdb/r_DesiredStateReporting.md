---
title: Desired State reporting
description: The Desired State application includes reports to assess your audit results.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Desired State, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Desired State reporting

The Desired State application includes reports to assess your audit results.

These reports are available to all users whose role gives them access to the [Reporting](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) application. Users with the admin role can share these reports with specific users of groups or change the display options.

Navigate to **Reports** &gt; **View / Run**. In the Reports search field, enter all or part of the report name such as `Desired State`. You can also scroll to the designated category and select one of the reports.

In addition to these reports, you can generate your own reports.

<table id="table_axy_lr5_cq"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Category

</th></tr></thead><tbody><tr><td>

Desired State Discrepancies

</td><td>

This report displays all desired state audit results that have a follow-on task that is not yet in the Closed Complete state. This report displays by column name.-   Type: bar chart
-   Table: Audit Result \[cert\_audit\_result\]

</td><td>

Audit Result

</td></tr><tr><td>

Desired State Result with Stability Unstable

</td><td>

This report displays all audit results where the Stability field has the value Unstable. This report displays by CI and stacked by audit.-   Type: bar chart
-   Table: Audit Result \[cert\_audit\_result\]

</td><td>

Audit Result

</td></tr><tr><td>

Desired State Result with Threshold Exceeded

</td><td>

This report displays all audit results where the Threshold field has the value Exceeded. This report displays by CI and stacks by each audit.-   Type: bar chart
-   Table: Audit Result \[cert\_audit\_result\]

</td><td>

Audit Result

</td></tr><tr><td>

Upcoming Desired State Audits

</td><td>

This report displays the desired state audits that are scheduled to run in the next two quarters.-   Type: List \(tabular\) report
-   Table: Audit \[cert\_audit\]

</td><td>

Audit

</td></tr><tr><td>

30/60/90 Day Desired State Task Aging

</td><td>

This report displays the number of follow-on tasks that are not Closed Complete for desired state audit types. The report is grouped by aging level.-   Type: Horizontal bar chart
-   Table: Follow On Task \[cert\_follow\_on\_task\]

</td><td>

Follow On Task

</td></tr><tr><td>

Desired State Hierarchical Task Roll Up

</td><td>

This report displays similar data to the Task Aging report, but groups the results by manager.-   Type: Horizontal bar chart
-   Table: Follow On Task \[cert\_follow\_on\_task\]

</td><td>

Follow On Task

</td></tr><tr><td>

Outstanding Desired State Tasks

</td><td>

This report displays similar data to Task Aging report, but groups the results by short description.-   Type: List \(tabular\) report
-   Table: Follow On Task \[cert\_follow\_on\_task\]

</td><td>

Follow On Task

</td></tr></tbody>
</table>