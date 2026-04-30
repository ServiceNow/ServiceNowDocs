---
title: Interactive Filters on dashboards
description: You can make an Interactive Filter available to users by adding the filter to a dashboard.
locale: en-US
release: zurich
product: Interactive Filters
classification: interactive-filters
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interactive Filters on dashboards

You can make an Interactive Filter available to users by adding the filter to a dashboard.

To be effective, interactive filters must be based on the same tables as the reports they filter. Reports based on the user table, for example, do not follow Interactive Filters that are based on the incident table. For more information, see [Make a report follow interactive filters](../task/t_MakeAReportASubscriber.md).

Performance Analytics widgets on the dashboard do not follow interactive filters. Separately filter those widgets on the same breakdown source by using the breakdown dashboard controls. For more information, see [Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md).

-   **[Add an interactive filter widget to a responsive dashboard](../task/t_AddIntFilterToAResponsiveDboard.md)**  
Add an interactive filter to a dashboard to filter reports on that dashboard.
-   **[Make a breakdown act as an interactive filter](../task/make-breakdown-interactive-filter.md)**  
You can configure a Performance Analytics breakdown on a dashboard to act as an interactive filter for reports on the dashboard. The dashboard must be configured as a breakdown dashboard.
-   **[Make a report follow interactive filters](../task/t_MakeAReportASubscriber.md)**  
When you add interactive filters to a dashboard, you can configure the reports on the dashboard to accept input from interactive filters. For example, you add a filter on the Incident table's Active field. Reports on the Incident table can reflect the user's choice from that filter.
-   **[Make a report act as an interactive filter](../task/t_MakeAReportAPublisher.md)**  
You can configure an existing report widget to filter other report widgets on the same dashboard.
-   **[Reset all interactive filters on a dashboard tab](../task/reset-all-filters.md)**  
Reset all applied filters on a dashboard tab to view the default value or the unfiltered data.

**Parent Topic:**[Interactive Filters](c_HomepagePublishers.md)

