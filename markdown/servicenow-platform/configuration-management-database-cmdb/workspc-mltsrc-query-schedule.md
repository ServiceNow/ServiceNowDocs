---
title: Schedule a CMDB 360 query for a report
description: Set up a schedule to regularly query for CMDB 360 data. Use scheduled queries to provide CMDB 360 data to reports you create, which can provide insight into how discovery sources populate the CMDB and the reliability of those discovery sources.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB 360 experience in a workspace, CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Schedule a CMDB 360 query for a report

Set up a schedule to regularly query for CMDB 360 data. Use scheduled queries to provide CMDB 360 data to reports you create, which can provide insight into how discovery sources populate the CMDB and the reliability of those discovery sources.

## Before you begin

Ensure that you run the CMDB 360 query at least once.

To access CMDB 360 in Service Graph Workspace, you must first switch from CMDB Workspace to Service Graph Workspace. For more information, see [Service Graph Workspace store app](../concept/sg-workspace.md).

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor.

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Insights icon and in the Insights page navigation panel, select **CMDB 360**.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **CMDB 360**.
2.  On the Saved queries tile, create or access a CMDB 360 query.

    If you created a new query, you must run the query at least once before you can select **Create Schedule** on the query results page.

3.  Select **Schedule query** on the Results Layout page of the query.

    To create a schedule for the Compare attributes values query, select **Schedule query** on the Discovery Sources page.

4.  Specify a **Run** frequency and time you want to schedule the query to run.

    When you select Weekly or Monthly, you must also select a day of the week or calendar day, respectively.

5.  Select **Save**.


## What to do next

[Create a CMDB 360 report](../concept/multisource-data-report-builder.md#) to integrate CMDB 360 query results with platform [Reporting capabilities](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US). Each run of the query automatically updates the generated report.

**Related topics**  


[Create a Get Records query](workspc-mltsrc-query-get-records.md)

[Create a Find Gap query](workspc-mltsrc-query-find-gap.md)

[Create a Compare Attribute Values query](workspc-mltsrc-query-comp-attr-value.md)

