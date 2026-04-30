---
title: DevOps Insights properties
description: DevOps Insights properties configure how DevOps Insights workspace data is displayed in reports.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Insights reports, DevOps Change Velocity, IT Service Management]
---

# DevOps Insights properties

DevOps Insights properties configure how DevOps Insights workspace data is displayed in reports.

Role required: sn\_devops.admin

You can view the Insights properties from the DevOps Change Workspace by navigating to **Workspaces** &gt; **DevOps Change Workspace** &gt; **System configuration** &gt; **Insights properties**.

## Properties installed with DevOps Insights

<table id="table_sby_s4t_xqb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

X hours per Developer time

</td><td>

The time taken per developer to work on a single work item in hours. This value is used to calculate the Developer hours saved report.

 For example, for every work item associated to a change request, a developer saved X hours in having to associate the work items, commits, test results, and other related DevOps data for their work.

</td><td>

1

</td></tr><tr><td>

Change Request Awaiting States

</td><td>

The states that are reported as awaiting a change request in the Changes awaiting approval report.Use the following values for the other states:

-   New: -5
-   Assess: -4
-   Authorize: -3
-   Schedule: -2
-   Implement -1
-   Review: 0
-   Closed: 3
-   Canceled: 4

</td><td>

-5, -4

</td></tr><tr><td>

Average Hourly Developer Cost

</td><td>

The average hourly cost of a developer working on DevOps changes in the selected currency. This value is used to calculate the Change acceleration savings report, where we multiply the Developer hours saved by this developer cost to estimate an ROI.

</td><td>

100

</td></tr></tbody>
</table>