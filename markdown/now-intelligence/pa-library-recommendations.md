---
title: Platform Analytics library recommendations
description: Library recommendations help you maintain healthy analytics ecosystems. The recommendations surface problematic analytics resources for you to clean up, making it easier for analysts to find the resources they need.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Platform Analytics library recommendations

Library recommendations help you maintain healthy analytics ecosystems. The recommendations surface problematic analytics resources for you to clean up, making it easier for analysts to find the resources they need.

**Note:** The feature requires the Analytics Library Recommendations \(app-analytics-recommendations\) application from the ServiceNow® Store. This application is part of Platform Analytics Advanced and has additional license requirements.

Library recommendations are a tool to help analytics managers help analysts.

Analysts need to discover analytics resources that help them answer specific business questions—whether they're selecting initial datasets, assessing trends, exploring patterns, or monitoring performance. However, analysts might find themselves searching through thousands of such resources without any clear quality signal. Even when they find what appear to be relevant resources, they might remain unsure that they have found the best ones.

Analytics managers are supposed to help analysts by weeding out the analytics resources. However, these managers have no systematic visibility into which artifacts degrade trust or usage patterns. Cleanup is reactive \(triggered by complaints\) rather than proactive.

Library recommendations are designed to help make cleanup proactive. For each library, the analytics manager sees a set of resources that may need to be modified or deleted.

The recommendations are provided as tiles on a panel on each library page. Visibility is restricted to admin roles, such as pa\_admin for the indicator library. A scheduled job scans the library for potential issues and stores the results in a table. Activate or deactivate the job to turn the library feature on or off. When active, the job runs weekly, but you can adjust this timing.

The following pages describe the existing library recommendation types and the underlying artifacts.

-   **[Dashboard library recommendations](../reference/dashboard-library-recommendations.md)**  
Analytics managers can view information about potentially problematic dashboards.
-   **[Data visualization library recommendations](../reference/data-viz-library-recommendations.md)**  
Analytics managers can view information about potentially problematic data visualizations.
-   **[Indicator library recommendations](../reference/ind-library-recommendations.md)**  
Analytics managers can view information about potentially problematic indicators.
-   **[Installed jobs, tables, and properties for Platform Analytics library recommendations](../reference/installed-tables-jobs-and-properties.md)**  
Several types of components are installed with activation of the  plugin, including tables, properties, and scheduled jobs.

**Parent Topic:**[Platform Analytics experience](par-workspace.md)

