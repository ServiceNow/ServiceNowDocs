---
title: Create a dynamic report
description: After running a saved query in the CMDB Query Builder, create a dynamic report that continuously updates to show the latest query results. You can use a dynamic report as any other report created using Reporting and you can add it to Performance Analytics dashboards.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create report, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a dynamic report

After running a saved query in the CMDB Query Builder, create a dynamic report that continuously updates to show the latest query results. You can use a dynamic report as any other report created using Reporting and you can add it to Performance Analytics dashboards.

## Before you begin

Ensure that the query that you want to create a dynamic report for is a saved query, and that there is a specified schedule for the query. Also, run the saved query and ensure that all query results are visible.

Role required:

-   To create: cmdb\_query\_builder and report\_user
-   To view: Reporting role requirements might apply, see [Administering reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_AdminsteringReports.md) for Reporting role requirements.

## About this task

The **Create Report** button in CMDB Query Builder which is used to create a dynamic report, is activated only if:

-   The query is saved
-   The query has a schedule
-   The entire set of query results is present after a query run

The initial dynamic report that you create, is based on the results from the initial run of the saved query. Then, on every subsequent run of the saved query, the associated report automatically updates with the latest query results.

However, if you change the query definition itself, the query and the report are no longer in sync and you must create a new report.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  In the **Saved Queries** tab, select the saved query for which you want to create a report.

    Ensure that the query has a specified schedule.

3.  Select **Run** and ensure that all query results appear.

    Click **Load All Results** if available, to load all results. The **Create Report** button is enabled only if all query results are showing.

4.  Click **Create Report**.

    If the CMDB Query Builder displays the query results in a new tab, then after the new tab opens with the query results, return to the CMDB Query Builder window.

5.  In the Report Designer, click **Next** or **Back** to view and configure the new report in the **Data**, **Type**, **Configure**, and **Style** tabs.

    The report is pre-populated with the CMDB query results and a few other report details.

    -   **Report name** is set to the name of the saved query.
    -   **Source type** is set to **Data source**.
    -   **Data source** is set to the table in which the query results are stored.
    -   **Query Sys ID** is the ID of the latest run of the query.
    For more details about Reporting and about configuring a report in the Report Designer, see [Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/reporting-landing-page.md), [Creating reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/report-types-creation-details-rd.md).

6.  Click **Save** or **Run**.


## Result

CMDB Query Builder creates a report source which you can attach to a report and use with dashboards. For more details about report sources, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_ReportSources.md).

## What to do next

Use either of the following steps to view the new report source. The name of the new report source is set to the name of the CMDB query it was created from, and cannot be changed.

-   In Query Builder, click **Saved Queries**. In the Saved Queries window, click the **Query Information** icon in the tile of the saved query. Scroll to the bottom of the information list and then click the link under **Report source**.
-   Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Report Sources** and locate the new report source.

