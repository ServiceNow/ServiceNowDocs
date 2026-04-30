---
title: Performance Analytics release notes
description: The ServiceNow Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Performance Analytics release notes

The ServiceNow® Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced and updated in the Xanadu release.

## Performance Analytics highlights for the Xanadu release

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for more information.

## UI changes

-   **Performance Analytics not in navigation after migration**

    On new instances and after migrating to Platform Analytics on upgraded instances, Performance Analytics does not appear in the navigation menu. Instead, all Performance Analytics functionality is listed under Platform Analytics Administration.

-   **[Publish to Analytics Hub checkbox](https://www.servicenow.com/docs/access?context=t_CreateAnAutomatedIndicator&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    On indicator forms, the **Publish to Analytics Hub** checkbox has been renamed **Save to library** because this option controls publication not only to the Core UI Analytics Hub but also to the list of KPIs in the Platform Analytics library and to KPI Details.

    **Note:** This change was also made because Analytics Hub is being deprecated.

-   **Clarification of terms KPI and indicator**

    Throughout the product, the term KPI to refer to a Performance Analytics indicator has been replaced with the term "indicator," for consistency. However, the feature names KPI Composer, KPI Details, and KPI Signals remain unchanged.


## Deprecations

-   Performance Analytics widgets are not available on new instances. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   The Analytics Hub is not available on new instances or instances that have fully migrated to Platform Analytics. Use KPI Details instead.
-   The Performance Analytics admin console is deprecated on new instances. For upgrading customers, the console is available but does not show data from the new Platform Analytics artifacts.

## Activation information

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this application.

The full features of Performance Analytics are available with a subscription. Activate the Performance Analytics plugin that matches your subscription. For details, see [Activating your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Distribute and consume Performance Analytics indicators \(KPIs\) through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

