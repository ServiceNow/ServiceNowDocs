---
title: Configure KPI and metrics preferences
description: Include or exclude KPIs and metrics as needed in your organization, and configure system behaviour when CIs fail metric health tests.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure KPI and metrics preferences

Include or exclude KPIs and metrics as needed in your organization, and configure system behaviour when CIs fail metric health tests.

## Before you begin

To start collecting and reporting CMDB health KPIs and metrics, you must first [enable and configure the CMDB Health Dashboard jobs](t_EnableCMDBHealthDashboardJob.md).

Role required: sn\_cmdb\_admin or itil\_admin \(on top of sn\_cmdb\_editor or itil\)

## About this task

If Domain Support - Domain Extensions is activated, then you can configure aggregation preferences per domain.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Health Preference**.

2.  Select **Health Metrics** on the right-hand side bar.

    1.  In the **Select Metric** drop-down list select the **Completeness**, **Compliance**, or the **Correctness** KPI and toggle **Active** to included that KPI and its associated metrics in CMDB Health analysis and reporting.

    2.  In the **Select Metric** drop-down list select a metric, such as **Required**, and configure its associated fields.

        For a metric:

<table id="table_mrm_fst_q5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activate the metric to include it in the aggregated health report for the respective KPI.

</td></tr><tr><td>

Failure Threshold

</td><td>

Threshold number of CIs that can fail the health metric test. When reached, health processing stops for the metric for this cycle.

 Maximum number is 100,000, even if you specify a higher number.

</td></tr><tr><td>

Create Task

</td><td>

If a CI fails the metric test, create a task with details about the failure. You can then view any generated tasks in the [CMDB Workspace store app](../concept/cmdb-workspace.md)or in [Service Graph Workspace store app](../concept/sg-workspace.md), and configure remediation for the task.

</td></tr><tr><td>

Task Assignee Group

</td><td>

An assignment group for the task.

</td></tr></tbody>
</table>3.  Select **Save**.


