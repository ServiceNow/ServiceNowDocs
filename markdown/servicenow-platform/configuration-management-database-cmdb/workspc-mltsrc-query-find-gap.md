---
title: Create a Find Gap query
description: Create a Find Gap query from the CMDB 360 dashboard of your CMDB Workspace or in Service Graph Workspace to help you find CIs that are not being reported by a discovery source.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CMDB 360 experience in a workspace, CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a Find Gap query

Create a Find Gap query from the CMDB 360 dashboard of your CMDB Workspaceor in Service Graph Workspace to help you find CIs that are not being reported by a discovery source.

## Before you begin

To access CMDB 360 in Service Graph Workspace, you must first switch from CMDB Workspace to Service Graph Workspace. For more information, see [Service Graph Workspace store app](../concept/sg-workspace.md).

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor

## About this task

Gaps in discovery source reporting occur when at least one discovery source reports on the CI and another doesn't, enabling you to identify discovery sources that might have an issue.

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Insights icon and in the Insights page navigation panel, select **CMDB 360**.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **CMDB 360**.
2.  Select **Create Query.**

3.  Select **I want to find gaps in data between discovery sources**.

4.  Select the CI classes that you want to check for gaps.

5.  Select **Continue**.

6.  Select non-reporting discovery sources.

    A non-reporting discovery source is a discovery source that doesn't report CIs as expected.Multiple non-reporting discovery sources have an OR condition with each other.

7.  Select one or two reporting discovery sources.

    These discovery sources report the CI as expected and act as a baseline for identifying the gap in reporting.

    You can leave the **Select reporting discovery sources for gap tracking** prompt empty to include all discovery sources in the query.

8.  Select **Continue**.

9.  On the form, select the options:

    |Field|Description|
    |-----|-----------|
    |Show unique CMDB 360 records|Select if you want to see only unique CMDB 360 records. Records for the same CIs from different discovery sources are consolidated.|
    |Show CI records by discovery source|Select if you want to see records for each CI and discovery source pair.|
    |Limit results to|Limits the query results to CIs that belong to a service or CMDB group. When you select **Application Services**, **Technical Services**, or **CMDB Groups**, a prompt appears where you can specify the service or CMDB group that you want the query to filter for.|

10. Select **Continue**.

11. Enter a name and description for your query.

12. Select **Save** .


## What to do next

Run the query at least once if you want to create a schedule.

On the CMDB 360 Query Results page:

-   If the number of results exceeds the number of results appearing on the page:
    -   Select **Load More Results​**: To show the next page of results. The number of results that appear on each result page is specified by the [glide.identification\_engine.multisource.query.batch.limit](../reference/components-multisource-cmdb.md) system property \(100 items by default\).
    -   Select **Load All Results**: To show all results, up to the limit specified by the [glide.identification\_engine.multisource.query.max.limit](../reference/components-multisource-cmdb.md) system property \(10000 by default\).
    -   Select a CMDB 360 Source link to easily access preview data of a source and see more details.
-   You can select **Create Schedule** to [set up a schedule](workspc-mltsrc-query-schedule.md) that runs your query on a regular basis. Scheduling your query enables you to use the query results in reports you create.
-   After creating a schedule, you can select **Create Report** to [configure a report](../concept/multisource-data-report-builder.md#) that you can manage using [Reporting capabilities](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
-   On the Query Results page, access a record to view further details.

