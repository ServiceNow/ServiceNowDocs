---
title: Create a CMDB 360 Find Gap query
description: Create a Find Gap query from the CMDB 360 dashboard of your CMDB Workspace to help you find CIs that are not being reported by a discovery source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-find-gap.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CMDB 360 experience in CMDB Workspace, CMDB 360/Multisource CMDB, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB 360 Find Gap query

Create a Find Gap query from the CMDB 360 dashboard of your CMDB Workspace to help you find CIs that are not being reported by a discovery source.

## Before you begin

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor

## About this task

Gaps in discovery source reporting occur when at least one discovery source reports on the CI and another doesn't, enabling you to identify discovery sources that might have an issue.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace menu bar, select **CMDB 360**.

3.  Click **Create Query.**

4.  Click **I want to find gaps in data between discovery sources**.

5.  Select the CI classes that you want to check for gaps.

6.  Click **Continue**.

7.  Select non-reporting discovery sources.

    A non-reporting discovery source is a discovery source that doesn't report CIs as expected.Multiple non-reporting discovery sources have an OR condition with each other.

8.  Select one or two reporting discovery sources.

    These discovery sources report the CI as expected and act as a baseline for identifying the gap in reporting.

    You can leave the **Select reporting discovery sources for gap tracking** prompt empty to include all discovery sources in the query.

9.  Click **Continue**.

10. On the form, select the options:

    |Field|Description|
    |-----|-----------|
    |Show unique CMDB 360 records|Select if you want to see only unique CMDB 360 records. Records for the same CIs from different discovery sources are consolidated.|
    |Show CI records by discovery source|Select if you want to see records for each CI and discovery source pair.|
    |Limit results to|Limits the query results to CIs that belong to a service or CMDB group. When you select **Application Services**, **Technical Services**, or **CMDB Groups**, a prompt appears where you can specify the service or CMDB group that you want the query to filter for.|

11. Click **Continue**.

12. Enter a name and description for your query.

13. Click **Save** .


## What to do next

Run the query at least once if you want to create a schedule.

On the CMDB 360 Query Results page:

-   If the number of results exceeds the number of results appearing on the page:
    -   Click **Load More Results​**: To show the next page of results. The number of results that appear on each result page is specified by the [glide.identification\_engine.multisource.query.batch.limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/components-multisource-cmdb.md) system property \(100 items by default\).
    -   Click **Load All Results**: To show all results, up to the limit specified by the [glide.identification\_engine.multisource.query.max.limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/components-multisource-cmdb.md) system property \(10000 by default\).
    -   Click a CMDB 360 Source link to easily access preview data of a source and see more details.
-   You can click **Create Schedule** to [set up a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-schedule.md) that runs your query on a regular basis. Scheduling your query enables you to use the query results in reports you create.
-   After creating a schedule, you can click **Create Report** to [configure a report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/multisource-data-report-builder.md) that you can manage using Reporting capabilities.
-   On the Query Results page, access a record to view further details.

