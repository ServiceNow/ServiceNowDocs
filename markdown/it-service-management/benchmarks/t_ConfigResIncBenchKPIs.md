---
title: Configure resolved incident Benchmarks KPIs
description: The source for the KPIs containing resolved incident data is the resolved\_at field in the Incident \[incident\] table, which may not exist in some environments. In this case, additional configuration is required to use these KPIs.
locale: en-US
release: australia
product: Benchmarks
classification: benchmarks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure KPI participation, Benchmark KPIs, Benchmarks, IT Service Management]
---

# Configure resolved incident Benchmarks KPIs

The source for the KPIs containing resolved incident data is the **resolved\_at** field in the Incident \[incident\] table, which may not exist in some environments. In this case, additional configuration is required to use these KPIs.

## Before you begin

**Note:** If you have never tracked resolved incidents in your environment before, install the Incident Resolution Fields \(com.snc.incident\_resolution\_fields\) plugin, which automatically adds the **resolved\_at** field to the Incident table. No further steps are required.

Role required: sn\_bm\_client.benchmark\_admin

## About this task

If you are receiving errors in the Benchmarks Data Collection job log for resolved incident KPIs because you are using a custom \(user-created\) field to track resolved incidents, the following procedure is required for successful data retrieval using these Benchmarks KPIs.

-   % of high priority incidents resolved
-   % of incidents resolved on first assignment
-   % of incidents resolved within SLA
-   % of reopened incidents
-   Average time to resolve a high priority incident
-   Average time to resolve an incident
-   Number of incidents created per user

Configure the KPI conditions and script to use your custom field \(instead of the default **resolved\_at** field\) for resolved incident Benchmarks KPIs.

## Procedure

1.  Configure the Benchmark.Incidents.Resolved indicator source condition with your custom field.

    1.  Navigate to **Performance Analytics** &gt; **Sources** &gt; **Indicator Sources**.

    2.  Select the **Benchmark.Incidents.Resolved** indicator source and enter edit mode.

    3.  In the Conditions section, select your custom field from the list \(custom field names are typically preceded by `u_`\).

    4.  Click **Update**.

2.  Configure the Benchmark.Incident.ResolvedTime.Hours script with your custom field name.

    1.  Navigate to **Performance Analytics** &gt; **Automation** &gt; **Scripts**.

    2.  Select the **Benchmark.Incident.ResolveTime.Hours** script and enter edit mode.

    3.  Replace the `resolved_at` field name occurrence within the script with the name of your custom field \(custom field names are typically preceded by `u_`\).

    4.  Click **Update**.

3.  Verify that you are no longer receiving errors in the Benchmarks Data Collection job log.


**Parent Topic:**[Configure KPI participation](t_EnableABenchKPI.md)

