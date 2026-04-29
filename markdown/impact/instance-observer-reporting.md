---
title: Instance performance telemetry reports
description: Quickly generate reports to download and share with your business stakeholders, making  organizations faster, smarter, and better in their  instance performance management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Instance Observer, Platform Health, Using Impact, Impact]
---

# Instance performance telemetry reports

Quickly generate reports to download and share with your business stakeholders, making  organizations faster, smarter, and better in their  instance performance management.

Visualize instance performance  telemetry over time and quickly generate reports to share with your team and business stakeholders.

Run a report on any instance to generate a downloadable summary on daily instance health, performance trend or database growth.

## Report options

Tailor various reports specific to your business needs with a few steps.

Navigate to **Instance Observer** &gt; **Reports**. Select the **Report Type**, the **Instance**, and the **Date Range** for the report.

Select **Generate report** and the report renders. On the report page, you have the option to download the report or to schedule the report to be run periodically.

![Report types.](../image/io-reports.png)

For additional information about a report, select **Help** &gt; **Metrics** from the main menu and select the option from the right-hand menu.

## Support matrix per Impact package

Some Instance Observer reporting features vary between the Impact package that you are subscribed to. Reference the support matrix for details.

-   ✓ = Supported
-   X = Not supported

| |Guided|Advanced|Total|
|---|:----:|:------:|:---:|
|Daily Performance Metrics report|✓|✓|✓|
|Performance Trend report|X|✓|✓|
|Database Growth report|✓|✓|✓|
|Data retention|45 days|6 months|6 months|
|Self Service Alerts|X|✓|✓|

**Note:** For more information on subscription support, see [Impact packages](impact-packages.md).

## Daily Performance Metrics Report

There are six daily performance metrics sub-reports that are available that show a current snapshot of the health of the instance.

<table id="table_jb5_k5q_mxb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Platform Health

</td><td>

-   Reflects node availability, response, and lag times.
-   Compares availability and anomalies from today and the last 30 days.
-   Reports are based on the system thresholds that are set in the system and color codes the anomalies accordingly, with Green, Yellow, or Red.

</td></tr><tr><td>

Health Indicator

</td><td>

-   Displays number of slow transactions, queries, and long running jobs.
-   Compares the counts between today, yesterday, and the last 30 day average.
-   Reports are based on the system thresholds that are set in the system and color codes the counts accordingly, with Green, Yellow, or Red.

</td></tr><tr><td>

Top 10 Slow Transactions

</td><td>

-   Finds the most executed transactions by total execution time and then takes the top 10 transactions that incur the highest average execution time.
-   Results list the instance page along with the average and total execution times, and the total count the page was executed.

 **Note:** Top 10 Slow Transactions is not available for Guided Impact customers in sub‑production instances.

</td></tr><tr><td>

Top 10 Slow Queries

</td><td>

-   Finds the most executed queries by total execution time and then takes the top 10 queries that incur the highest average execution time.
-   Results list the query along with the average and total execution times, and the total count the query was executed.

 **Note:** Top 10 Slow Queries is not supported for Guided Impact customers in sub-production instances.

</td></tr><tr><td>

Top 10 Long Running Jobs

</td><td>

-   Finds jobs that are incurring highest duration in minutes.
-   Results list the job name, node, worker, and the duration.

</td></tr><tr><td>

Critical Support Cases

</td><td>

-   Lists the total number of severity 1 and 2 support cases in the report header.
-   Provides case numbers as links, the area, priority, and state, along with tracking who opened the issue.

</td></tr></tbody>
</table>## Performance Trend Report

Drill into additional detail on selected performance metrics.

The following report options are available in regards to system performance:

-   Transaction/Report Times
-   Database response
-   Semaphore depth
-   Event queues
-   Jobs recurring and running
-   Memory
-   User session summaries

## Custom Performance Report

Generate Custom Performance report selecting a maximum of 20 metrics and a minimum of one metric from a wide range of 90 metrics available across the application. This report is almost the same as Performance Trend report, however offers you the flexibility to choose more metrics from the performance categories in the Performance page and build a dynamic report.

To configure the Custom Performance Report:

1.  Navigate to the Instance Observer Dashboard page.
2.  Select the **Reports** tab and click **On Demand Reports** from the list.
3.  Select the **Instance** for which you want to run the report.
4.  From the list of report types, select **Custom Performance Report**.
5.  Select the time frame for the report's duration in the **Date Range** field.
6.  To add metrics from all the available metrics in the application, select **All**.
7.  To add metrics from the categories available in the Performance page, select the specific category from the list.
8.  Select **Clear selection** to remove any previous selected metric from the list.

    The selected metrics from the **Available performance metrics** column appear in the **Selected performance metrics** column on the right.

9.  Select **Generate Report**.

![Custom performance report offers more metrics to measure performance.](../image/io-custom-performance-report.png)

Each metric render a different visualization, where many of them are based on time series rendering as charts, while some of them are tables where the key performance indicators are aggregated in a tabular format.

You have the flexibility to build the report in any order that you prefer. Once the report is ready, you can email it, set as CSV file, or generate a PDF.

## Database Growth Report

There are several database growth reports that are available that show how the instance database has increased over a selected date range.

**Note:** Guided customers may select a range of up to 45 days.

|Report|Description|
|------|-----------|
|Primary Database|Various metrics on how the database has either grown or decreased over the selected time frame. Total DBI size based on the sum of all tables, calculated every 4 hours.|
|Database by Size \(Including Shards\)|Various metrics on how the database has either grown or decreased over the selected, including shards. Total DBI Size align with primary shards, this is calculated every 4 hours and can be used to visualize database growth over time.|
|Top 20 Tables \(By Size\)|Lists table name, size \(GB\), 1 day growth and rate, and the 7 day growth rate.|

**Parent Topic:**[Instance Observer](../concept/io-overview.md)

