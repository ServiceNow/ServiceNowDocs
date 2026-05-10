---
title: Create a Compare Attribute Values query
description: Create a Compare Attribute Values query from the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace to help you find CIs with mismatched attribute values between discovery sources.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CMDB 360 experience in a workspace, CMDB 360, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a Compare Attribute Values query

Create a Compare Attribute Values query from the CMDB 360 dashboard in CMDB Workspaceor in Service Graph Workspace to help you find CIs with mismatched attribute values between discovery sources.

## Before you begin

To access CMDB 360 in Service Graph Workspace, you must first switch from CMDB Workspace to Service Graph Workspace. For more information, see [Service Graph Workspace store app](../concept/sg-workspace.md).

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor.

## About this task

The query enables you to determine if there’s an issue with how a discovery source reports a CI.

The Compare Attribute Values query compares CIs from different discovery sources for mismatched values. Mismatches occur when a discovery source reports attribute values for a CI that are different from values reported by other discovery sources or the CMDB. You can use the query to identify these CIs and reconcile the attribute values, or fix any issues with the discovery sources.

## Procedure

1.  Open either workspace:

2.  -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Insights icon and in the Insights page navigation panel, select **CMDB 360**.
-   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **CMDB 360**.
3.  Select **Create Query**.

4.  Select **I want to compare attribute values between discovery sources or against the CMDB**.

5.  Select a CI class that you want to compare attribute values for.

    You can select a selected class to open the condition builder. Use the condition builder to specify conditions that must be met for each class. Use **And** or **Or** to specify multiple conditions.

6.  Select **Continue**.

7.  On the Attributes to compare form, select options:

    |Option|Description|
    |------|-----------|
    |Any attribute doesn't match|Select if you want to retrieve CIs where there's a mismatch with any specified attribute values between the discovery sources.|
    |Every attribute doesn't match|Select if you want to retrieve CIs where there's a mismatch with every specified attribute value between the discovery sources.|
    |Select attributes to compare|Specify the attributes that you want to compare for mismatched values.|

8.  Select **Continue**.

9.  Select the discovery sources that you want to compare attribute values for.

    |Field|Description|
    |-----|-----------|
    |Compare to CMDB|Select if you want to compare the specified attribute values against your CI attributes recorded in the CMDB. When you compare against the CMDB, you only need one discovery source.|
    |Select discovery sources|The discovery sources that you want to compare. Select at least two.|
    |Limit results to|Limits the query results to CIs that belong to a service or CMDB group. When you select **Application Services**, **Technical Services**, or **CMDB Groups**, a prompt appears. You can use the prompt to specify the service or group that you want the query to filter for.|

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
-   After creating a schedule, you can select **Create Report** to configure a report that you can manage using [Reporting capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/reporting-landing-page.md).
-   On the Query Results page, access a record to view further details.

