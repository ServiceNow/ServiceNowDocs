---
title: Performance Analytics release notes
description: The ServiceNow Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/performance-analytics-rn.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Platform Analytics release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Performance Analytics release notes

The ServiceNow® Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced and updated in the Brazil release.

## Performance Analytics highlights for the Brazil release

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

See [Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pa-overview.md) for more information.

## Changed in this release

-   **[Use bucket groups to breakdown Data Snapshots indicators by continuous data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/map-bucket-group-to-ds-source.md)**

    To filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.

-   **[Use calculated fields to break down Data Snapshots indicators by date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-a-calculated-field.md)**

    Create calculated fields to show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.

-   **[Create indicators on Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-fabric-tables-zcc.md)**

    Create classic automated indicators on external data via Workflow Data Fabric. Use Workflow Data Fabric tables in indicator sources just as you would any other facts tables.

-   **[Intraday scores supported on indicators with Data snapshots enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/ds-score-collection-enabled-indicators.md)**

    You can now collect intraday scores on classic indicators with Data snapshots enabled instead of only on natively created Data snapshots indicators.

-   **[Manage and troubleshoot your Data snapshots jobs more easily](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/data-snapshots-logs.md)**

    You now are provided with new estimates and more log information:

    -   Time estimates before a job starts
    -   Progress percentages for first-day mining, changes loader, and delta mining jobs
    -   Logs include the next scheduled run timestamp after incremental job completion

## Deprecated features

Starting with the Brazil release, KPI Composer is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Complimentary Performance Analytics for Incident ManagementPerformance Analytics is active by default. You cannot create indicators or breakdowns with this complimentary application.

The full features of Performance Analytics are available with a subscription. For details, see [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_PremiumPerformanceAnalytics.md).

## Plugin information

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    KPI Composer \(sn\_kpi\_compose\): Planned for deprecation in D release. There is no replacement for this plugin.


## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/par-workspace.md)**

    Distribute and consume Performance Analytics indicators \(KPIs\) through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.

-   **[Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md)**

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/analytics-intel-report-rn-landing.md)

