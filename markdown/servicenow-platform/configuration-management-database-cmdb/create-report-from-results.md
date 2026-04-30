---
title: Create a basic report
description: After running a query in the CMDB Query Builder, you can create a basic report that is scoped to the query execution.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create report, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a basic report

After running a query in the CMDB Query Builder, you can create a basic report that is scoped to the query execution.

## Before you begin

The [Core UI plugin](https://www.servicenow.com/docs/access?context=t_ActivateUI16&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) \(com.glide.ui.ui16\) must be activated.

Role required:

-   View report: cmdb\_query\_builder or cmdb\_query\_builder\_read
-   Create report: cmdb\_query\_builder or cmdb\_query\_builder\_read, and report\_user

In a base system, the cmdb\_query\_builder role is contained in the itil and asset roles.

## Procedure

1.  Navigate to **All** &gt; **Configuration** and click **CMDB Query Builder**.

2.  Build a query.

3.  In the query results pane, click **Load More Results** or **Load All Results** to load all the results that you want to include in the basic report.

4.  In the query results pane, click the column context menu and select **Bar Chart** or **Pie Chart**.


## Result

The Reports application creates a basic report, which is scoped to the query results that are currently loaded and is static.

**Related topics**  


[Reporting](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

[Build a CMDB query using the CMDB Query Builder](use-cmdb-query-builder.md)

[Build a Service Mapping query using the CMDB Query Builder](build-service-mapping-query.md)

[Run a partial CMDB query](run-partial-cmdb-query.md)

