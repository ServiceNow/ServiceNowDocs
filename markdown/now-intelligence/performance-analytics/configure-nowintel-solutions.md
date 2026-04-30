---
title: Configure Platform Analytics Solutions
description: Platform Analytics Solutions come configured with the expectation that you keep your ServiceNow AI Platform data in a standard set of tables and fields. If you are using different fields, configure the Solutions to point to the correct locations.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Analytics solutions, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configure Platform Analytics Solutions

Platform Analytics Solutions come configured with the expectation that you keep your ServiceNow AI Platform data in a standard set of tables and fields. If you are using different fields, configure the Solutions to point to the correct locations.

**Tip:** You may find it convenient to use the Performance Analytics admin console as the starting point for configuring Platform Analytics Solutions. From the admin console, you can perform the following actions:

-   Activate the Solution from the plugins list or through a guided setup, if one is available. \(You cannot activate Solutions that are only available on the ServiceNow Store from the admin console.\)
-   Check whether Performance Analytics is fully activated on this instance.
-   Run diagnostics.
-   Look up KPIs to configure.
-   Use Dependency Assessment to find the related [indicators](performance-analytics-glossary.md#), [breakdowns](performance-analytics-glossary.md#), and sources for your Solution.

For more information, see [Performance Analytics Admin Console](pa-admin-console.md).

## Run diagnostics

After you install any Platform Analytics Solutions, run all diagnostics on all records, as described in [Execute diagnostics for all records](self-diagnostics.md#). These diagnostics can catch many mismatches between the configuration of your Platform Analytics Solutions and your tables.

## Domain separation and 'Run As' user

By default, System Administrator is the **Run As** user for data collection jobs in the Platform Analytics Solutions. Verify that this user exists on the instance, and whether this user has the appropriate level of access. An inappropriate **Run As** user can cause errors or limit the data that is collected. If you have Domain Separation enabled, ensure you set an appropriate **Run As** user in each domain.

1.  [Review the indicator sources](../task/review-indicator-sources.md)  
Determine which fields contain the data you are looking for in each application you are enabling for Performance Analytics.
2.  [Update Performance Analytics scripts](../task/update-pa-scripts.md)  
Platform Analytics Solutions include Performance Analytics scripts to perform calculations on records. These scripts use the time stamp fields from the indicator sources. If you change the time field stamps in an indicator source, also modify the related scripts.
3.  [Review the breakdown sources](../task/review-breakdown-sources.md)  
Breakdown sources represent the elements that you use to examine a KPI in more detail. Modify the breakdown source to limit the element list to only those items that are meaningful for the data analysis.

**Parent Topic:**[Platform Analytics solutions](../../dashboards/concept/content-packs-in-form-analytics-published.md)

