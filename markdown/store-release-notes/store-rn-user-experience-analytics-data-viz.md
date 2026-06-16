---
title: Usage Insights in Data Visualizations release notes
description: Version history for the Usage Insights in Data Visualizations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-user-experience-analytics-data-viz.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Usage Insights in Data Visualizations release notes

Version history for the Usage Insights in Data Visualizations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.2.2 - June 2026**
    -   Support for AI Native Experience channel
    -   Support for conversation analytics
-   **Version 6.1.12 - March 2026**

    Usage Insights funnel capabilities are now available as part of PA Dashboard visualization experiences. Funnels created in Usage Insights can now be configured and displayed directly within Platform Analytics inline dashboards, enabling a unified view of conversion analytics in PA Dashboards. Existing funnels can be selected through the PA dashboard configuration and identical metrics and conversion rates are ensured across both surfaces. Access controls defined in Usage Insights are respected, and clear messages are displayed if a funnel is unavailable or access has been revoked.

-   **Version 5.1.2 - February 2026**
    -   Enhancements in data viz: Support global date range filter to all UIX \( Usage Insights\) vizualizations including Funnels.
    -   Funnel fix: uxa funnel saves relative dates as absolute, so relative dates period is not being calculated correctly
-   **Version 5.0.8 - August 2025**
    -   Fixed:
        -   Hardcoded string in Page analytics "Date range"
        -   Inline dashboard drilldown for Events/Pages score cards to UXA dashboard - dummy advanced filter is displayed
        -   After setting groupby value, label for the panel is wrong \(id is taken by mistake\)
        -   Drill Down - Events and page details page show dummy condition builder filters on UXA after drill down
-   **Version 4.0.22 - July 2025 \(Yokohama\)**

    Fix for the following: UXA Pages does not load if the system property glide.sys.date\_format has any other format like dd-MMM-yyyy.

-   **Version 4.0.17 - March 2025**

    Fixed: UX Analytics metrics with score card data will display previous period and change arrows.

-   **Version 4.0.16 - February 2025**
    -   Changed: Make sure that all existing dashboards/data viz based on UXA are still working after update to ClickHouse, our new data warehouse \(Y\)
    -   Fixed:
        -   Users with analytics\_viewer role will be able to create data visualizations based on UXA data source
        -   Data source will not be available for charts that require more than 1 dimension/group by
    -   Removed: Child app drop down on data source selection stage
-   **Version 3.1.4 - August 2024**

    Bug fix.

-   **Version 3.1.3 - Mary 2024**

    Import User Experience Analytics data through the UI Builder and Performance Analytics Data Visualization components, helping to provide an alternative method to visualize data for analysis.


