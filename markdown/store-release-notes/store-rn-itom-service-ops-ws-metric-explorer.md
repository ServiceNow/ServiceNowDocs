---
title: Service Operations Workspace Metric Explorer release notes
description: Version history for the ITOM Service Operations Workspace Metric Explorer application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-ws-metric-explorer.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace Metric Explorer release notes

Version history for the ITOM Service Operations Workspace Metric Explorer application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.1.1 - June 2026**
    -   Fixed:
        -   Metric Explorer layout now displays correctly across all screen sizes.
        -   Metric Explorer tab no longer displays as blank when opened from the Metrics tab in Service Operations Workspace.
        -   Metric Explorer now displays all required components and controls on the page.
        -   Metric Explorer page no longer becomes stuck in loading mode when refreshed. Fixed async initialization issue in date range picker component.
-   **Version 27.0.0 - March 2026**

    Changed: Improved the application's accessibility

-   **Version 24.11.1 - February 2026**

    Fixed: Date range picker issue fixed

-   **Version 24.10.0 - December 2025**

    Fixed issues: Metric Explorer: Fixed an issue where viewing related metrics for CI displayed an empty graph for the last hour.

-   **Version 24.8.0 - August 2025**

    Fixed: Fixed a problem when loading specific metrics by ID.

-   **Version 24.7.3 - May 2025**
    -   Fixed:
        -   Missing feature metrics of Azure DB Metrics cloud policy
        -   Metric Explorer tab loading issue
        -   Accessibility- Missing tooltips
-   **Version 24.4.0 - February 2025**
    -   Fixed:
        -   Fixing a problem in the Date-Time picker
        -   Fixing an issue presenting alerts when selecting 'Show alerts on CI'
-   **Version 24.3.6 - December 2024**

    Fixed: Fixed the link from the Express list &gt; Preview Panel &gt; Info tab &gt; CI details popover to the Metric Explorer.

-   **Version 24.3.3 - November 2024**
    -   Changed: Accessibility improvements
    -   Fixed: Date range picker fixes
-   **Version 24.2.1 - July 2024**

    Fixed: Localization and translation issue in the Metric Explorer.

-   **Version 24.2.0 - March 2024**
    -   Fixed:
        -   Add throttling and limit the amount of series in the getMetricsPerEntryPoint API
        -   Adding a button navigating to ME when there is no metric content
-   **Version 22.5.2 - November 2023**

    Minor bug fixes.

-   **Version 22.3.0 - August 2023**
    -   Metric Explorer for Service Operations Workspace enables operators to investigate metric behavior and compare and correlate different metrics across hosts, applications and services, in order to troubleshoot issues and find their root cause.
    -   The application improves the Agent Client Collector Monitoring solution, providing operators with better visualization of metrics across CIs as well as better understanding of anomalies, alerts, and relations between metrics.
    -   With Metric Explorer, you can explore metrics related to a specific alert, or choose a CI and explore its metrics. You can compare and correlate host metrics with multiple application metrics, service entry points and more.

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

