---
title: Use Benchmarks data for value management analysis
description: Manually collect historical Benchmarks data to analyze the benefits of year-over-year growth when you use the ServiceNow Benchmarks application.
locale: en-US
release: australia
product: Benchmarks
classification: benchmarks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Benchmark KPIs, Benchmarks, IT Service Management]
---

# Use Benchmarks data for value management analysis

Manually collect historical Benchmarks data to analyze the benefits of year-over-year growth when you use the ServiceNow Benchmarks application.

## Before you begin

Role required: sn\_bm\_client.benchmark\_admin, pa\_data\_collector, or admin

## About this task

If you want to analyze year-over-year performance, you must collect at least 24 months of Benchmarks data. Use the **sn\_bm\_client.months\_copy\_historical\_pa\_bm** system property to set the number of months from the current month for which you want to collect Benchmarks historical data.

## Procedure

1.  Set up Benchmarks historical data collection.

    1.  Navigate to **Performance Analytics** &gt; **Data Collection** &gt; **Jobs**.

    2.  Select the **Benchmarks Historical Data Collection** job.

    3.  In the **Relative start** field, enter the period of time for which you want to collect the data.

    4.  In the **Relative start interval** field, select the length of the time period to collect the data.

        Recommended interval is 24 months.

    5.  Select **Execute**.

        For detailed information on scheduling a data collection job, refer to [Create or schedule a data collection job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreatASchedDataCollJob.md).

2.  Upload the collected data to the centralized Benchmarks instance.

    1.  In the **Benchmarks Historical Data Collection** job, navigate to the **Job Logs** related list.

    2.  Make sure that the state for the historical data collection job is **Collected**.

        This state indicates that all data for the job has successfully run and all data has been gathered for the set time period.

    3.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    4.  Select **Copy historical scores from PA to Benchmarks table**.

    5.  Select **Execute Now**.

        The data is automatically sent for value management analysis. Connect with your account representative to receive the report and discuss the benefits for your organization's value management.


**Parent Topic:**[Benchmark KPIs](../concept/c_BenchKPIConfig.md)

