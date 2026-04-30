---
title: View CMDB benchmarks
description: CMDB calculates several CMDB Health benchmarks which then display in the Benchmarks dashboard. These benchmarks are based on various CMDB Health metrics, displaying monthly averages, trends, comparisons to industry averages of your ServiceNow peers, and global benchmarks.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CMDB benchmarks

CMDB calculates several CMDB Health benchmarks which then display in the Benchmarks dashboard. These benchmarks are based on various CMDB Health metrics, displaying monthly averages, trends, comparisons to industry averages of your ServiceNow peers, and global benchmarks.

## Before you begin

Role required: none

The CMDB Health Dashboard jobs must be enabled and health data must be collected. Also, navigate to **Benchmarks** &gt; **Setup** and ensure that the CMDB KPIs are enabled under **IT Operations Management**.

## About this task

CMDB provides the following benchmarks:

-   % of non-compliant CIs
-   % of duplicate CIs
-   % of stale CIs

For an instance, each of these benchmarks is the calculated monthly average for the corresponding CMDB Health metric. Calculating a monthly average requires that there is a metric result value for each day of the month. Therefore, each day on which the respective Health Dashboard job did not run, is assumed with the aggregated result from the run that is most recent to that day. The monthly average is then calculated based on the sum of all the daily aggregated results for the metric in that month, divided by the number of days of the month. For a CMDB Health Dashboard job that ran multiple times in a single day, only the results of the last run in that day are used for the monthly average calculation.

**Note:** The frequency of CMDB Health Dashboard job executions depend on whether the job is enabled, its schedule and on manual runs.

Global averages are based on the sum of monthly averages of all peer instances, divided by the number of instances \(aside from instances for which the monthly average is 0\).

## Procedure

1.  Navigate to **Benchmarks** &gt; **Dashboard**.

2.  Click the ![Select what to display benchmarks for.](../image/select-benchmark-bundle.png) icon and select **IT Operations Management**.

3.  Click **ALL** or **CMDB**.

4.  Click on a CMDB benchmark to drill down to trend data, and other benchmark details.


**Related topics**  


[CMDB Health](../concept/c_CMDBHealth.md)

