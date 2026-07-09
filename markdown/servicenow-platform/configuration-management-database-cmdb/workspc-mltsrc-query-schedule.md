---
title: Schedule a CMDB 360 query for a report
description: Set up a schedule to regularly query for CMDB 360 data. Use scheduled queries to provide CMDB 360 data to reports you create, which can provide insight into how discovery sources populate the CMDB and the reliability of those discovery sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-schedule.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CMDB 360 experience in CMDB Workspace, CMDB 360/Multisource CMDB, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Schedule a CMDB 360 query for a report

Set up a schedule to regularly query for CMDB 360 data. Use scheduled queries to provide CMDB 360 data to reports you create, which can provide insight into how discovery sources populate the CMDB and the reliability of those discovery sources.

## Before you begin

Ensure that you run the CMDB 360 query at least once.

Role required: sn\_cmdb\_user and either cmdb\_ms\_admin or cmdb\_ms\_editor.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace menu bar, select **CMDB 360**.

3.  On the Saved queries tile, create or access a CMDB 360 query.

    If you created a new query, you must run the query at least once before you can click **Create Schedule** on the query results page.

4.  Select **Schedule query** on the Results Layout page of the query.

    To create a schedule for the Compare attributes values query, select **Schedule query** on the Discovery Sources page.

5.  Specify a **Run** frequency and time you want to schedule the query to run.

    When you select Weekly or Monthly, you must also select a day of the week or calendar day, respectively.

6.  Click **Save**.


## What to do next

[Create a CMDB 360 report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/multisource-data-report-builder.md) to integrate CMDB 360 query results with platform [Reporting capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/reporting-landing-page.md). Each run of the query automatically updates the generated report.

**Related topics**  


[Create a CMDB 360 Get Records query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-get-records.md)

[Create a CMDB 360 Find Gap query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-find-gap.md)

[Create a CMDB 360 Compare Attribute Values query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/workspc-mltsrc-query-comp-attr-value.md)

