---
title: Create a CMDB 360 Get Records query
description: Create a Get Records query from the CMDB 360 dashboard of your Configuration Management Database \(CMDB\) Workspace to help you explore your existing CMDB 360 data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-get-records.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CMDB 360 experience in CMDB Workspace, CMDB 360/Multisource CMDB, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB 360 Get Records query

Create a Get Records query from the CMDB 360 dashboard of your Configuration Management Database \(CMDB\) Workspace to help you explore your existing CMDB 360 data.

## Before you begin

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace menu bar, select **CMDB 360**.

3.  On the Saved Queries tile, click **Create Query.**

4.  Click **I want to get CMDB 360 data**.

5.  Select the CI classes to include in the query.

    You can click a selected class to open the condition builder. Use the condition builder to specify conditions that must be met for each class. Use **And** or **Or** to specify multiple conditions.

    Select **All Classes** if you want to include all CI classes without conditions.

6.  Click **Continue**.

7.  Select discovery sources to query on.

    The query retrieves CMDB 360 data that originates from the discovery sources you specify.

    You can leave the Select discovery sources prompt empty to retrieve data for all discovery sources.

8.  Click **Continue**.

9.  On the form, select the options:

    |Field|Description|
    |-----|-----------|
    |Show unique CMDB 360 records|Select if you want to see only unique CMDB 360 records. Records for the same CIs from different discovery sources are consolidated.|
    |Show CI records by discovery source|Select if you want to see records for each CI and discovery source pair.|
    |Limit results to|Limits the query results to CIs that belong to a service or CMDB group. When you select **Application Services**, **Technical Services**, or **CMDB Groups**, a prompt appears. You can use the prompt to specify the service or group that you want the query to filter for.|

10. Click **Continue**.

11. Enter a name and description for your query.

12. Click **Save** .


## What to do next

Run the query at least once if you want to create a schedule or report.

On the CMDB 360 Query Results page:

-   If the number of results exceeds the number of results appearing on the page:
    -   Click **Load More Results​**: To show the next page of results. The number of results that appear on each result page is specified by the [glide.identification\_engine.multisource.query.batch.limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/components-multisource-cmdb.md) system property \(100 items by default\).
    -   Click **Load All Results**: To show all results, up to the limit specified by the [glide.identification\_engine.multisource.query.max.limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/components-multisource-cmdb.md) system property \(10000 by default\).
    -   Click a CMDB 360 Source link to easily access preview data of a source and see more details.
-   You can click **Create Schedule** to [set up a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-schedule.md) that runs your query on a regular basis. Scheduling your query enables you to use the query results in reports you create.
-   After creating a schedule, you can click **Create Report** to [configure a report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/multisource-data-report-builder.md) that you can manage using [Reporting capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/now-intelligence/reporting/reporting-landing-page.md).
-   On the Query Results page, access a record to view further details. For example, click a link in the Primary Record column, and then in the CI Details page, click **View CMDB 360 Data**.

