---
title: Assessment dashboard in Configurable Workspace of Cloud Migration Assessment
description: Use the ServiceNow Cloud Migration Assessment application to plan, organize, and track the process of relocating your enterprise IT resources and workloads to cloud platforms. Analyze the IT resources using dashboards that visualize and summarize information on resources by different categories. Use the Assessment dashboard to review the statistics of the migration tasks and monitor the migration progress.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Migration Assessment reference, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Assessment dashboard in Configurable Workspace of Cloud Migration Assessment

Use the ServiceNow® Cloud Migration Assessment application to plan, organize, and track the process of relocating your enterprise IT resources and workloads to cloud platforms. Analyze the IT resources using dashboards that visualize and summarize information on resources by different categories. Use the Assessment dashboard to review the statistics of the migration tasks and monitor the migration progress.

## Required ServiceNow AI Platform roles

sn\_cloud\_migration.operator, uses Cloud Migration Assessment.

## Access the Assessment dashboard

To open the dashboard, navigate to **All** &gt; **** &gt; **Cloud Migration** &gt; **Cloud Migration Workspace**, and then select **Assessment dashboard** ![Assessment dashboard icon](../../../product/itom-governance/image/cm-assessment-dashboard-navigation.png).

![Assessment dashboard](../../../product/itom-governance/image/cm-assessment-dashboard.png "Assessment dashboard")

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|sn\_cloud\_migration.operator|Review the statistics of the migration tasks and monitor the migration progress. Drill down to see detailed information on resources in relevant categories.|

## Indicators

-   **Resources in new assessments**

    The resources of all categories assigned to assessment tasks in **New** state.

-   **Resources in review and approved resources**

    The resources of all categories assigned to tasks in **Review** or **Approved** state.

-   **Unassigned on-premise resources**

    The resources that you haven't assigned to any assessment tasks.

-   **Blocked resources**

    The resources of all categories assigned to tasks in **Blocked** state.


## Data visualizations

The following visualizations are available on the Overview tab of Cloud Migration Assessment.

<table id="table_lcd_5vt_yrb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resources by assessment state

</td><td>

Donut![Donut report icon](../../reporting/image/icon-donut-report-p.png)

</td><td>

Assigned Resource for Migration \[sn\_cloud\_migration\_task\_resource\_m2m\]

</td><td>

A donut report that shows resources of all categories by their assessment task state.

</td></tr><tr><td>

Assigned resources by state and migration wave

</td><td>

Bar![Bar report icon](../../reporting/image/icon-bar-report-p.png)

</td><td>

Assigned Resource for Migration \[sn\_cloud\_migration\_task\_resource\_m2m\]

</td><td>

A bar report that presents resources by state and migration wave.

</td></tr><tr><td>

Resources by target architecture and cloud providers

</td><td>

Bar![Bar report icon](../../reporting/image/icon-bar-report-p.png)

</td><td>

Assigned Resource for Migration \[sn\_cloud\_migration\_task\_resource\_m2m\]

</td><td>

A bar report that presents resources by target architecture and cloud providers.

</td></tr><tr><td>

Resources by assessment R-disposition

</td><td>

Donut![Donut report icon](../../reporting/image/icon-donut-report-p.png)

</td><td>

Assigned Resource for Migration \[sn\_cloud\_migration\_task\_resource\_m2m\]

</td><td>

A donut port that shows resources by the migration strategy \(R-disposition\) selected for their respective assessments.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Migration Assessment reference](../../../product/itom-governance/reference/cloud-migration-reference.md)

