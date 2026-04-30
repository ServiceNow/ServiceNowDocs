---
title: Collect historical data
description: Run a historical data collection job to collect scores and snapshots for existing records. When collecting data for the first time, such as for a new indicator, run historical data collection once to generate scores and snapshots for existing records.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Collecting indicator scores, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collect historical data

Run a historical data collection job to collect scores and snapshots for existing records. When collecting data for the first time, such as for a new indicator, run historical data collection once to generate scores and snapshots for existing records.

## Before you begin

Role required: pa\_data\_collector or admin

## About this task

Performance Analytics regularly collects scores from your data on an ongoing basis. When you first set up Performance Analytics for an application, or when you create new indicators or indicator sources, run historical data collection to collect scores on your existing data. Historical data collection enables you to analyze data that existed prior to setting up Performance Analytics.

**Warning:**

-   Avoid running a historical collection job more than once. If for example you create a new indicator, consider creating a new data collection job for that indicator instead of adding it to an existing job.
-   A historical data collection job deletes any previously collected data for the periods and the indicators that the job covers. It does not delete data from outside that date range or for other indicators.

Historical jobs also collect snapshots of the existing data. Performance Analytics snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with **Collect records** selected.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Select a historical data collection job, such as \[PA Change\] Historic Data Collection, or create a new historic data collection job.

3.  If you are creating or editing the historic data collection job, follow the procedure in [Create or schedule a data collection job](t_CreatASchedDataCollJob.md).

    **Important:** For a historical data collection job, set **Run** to On demand. Do not run historical data collection jobs on a fixed schedule.

4.  In the job indicators, exclude any breakdowns that are based on fields whose value is likely to change during the historical collection period, as described in [Configure a job indicator](configure-job-indicator.md).

    For example, in the provided \[PA Incident SLA\] Historic Data Collection job, the job indicator 'Number of open and overdue incidents' excludes the Assignment Group and the State breakdowns. The value of both of these breakdowns could change over the data collection period, making the results meaningless.

5.  Click **Execute Now**.


## What to do next

After collecting historical data, use a scheduled data collection job to collect new scores regularly.

**Parent Topic:**[Collecting indicator scores](../concept/c_ClctData.md)

