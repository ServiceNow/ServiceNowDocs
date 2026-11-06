---
title: Performance Analytics release notes
description: The ServiceNow Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals.Data snapshots indicators now support bucket groups and calculated date fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/performance-analytics-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-25"
reading_time_minutes: 2
keywords: [Performance analytics, Platform analytics, indicator, KPI, data snapshots, indicators, KPI]
breadcrumb: [Platform Analytics release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Performance Analytics release notes

The ServiceNow® Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals.

## About Performance Analytics

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

See [Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pa-overview.md) for more information.

## Activation and other requirements

-   **Activation information**

    Complimentary Performance Analytics for Incident ManagementPerformance Analytics is active by default. You cannot create indicators or breakdowns with this complimentary application.

    The full features of Performance Analytics are available with a subscription. For details, see [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_PremiumPerformanceAnalytics.md).


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/analytics-intel-report-rn-landing.md)

## Brazil Early Availability

Data snapshots indicators now support bucket groups and calculated date fields.

### What's new

-   **[Use bucket groups to break down Data Snapshots indicators by continuous data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/map-bucket-group-to-ds-source.md)**

    To filter Data snapshots scores by a numeric field on the source table, you can now map a bucket group to that field. The bucket group splits that field into value ranges.

-   **[Use calculated fields to break down Data Snapshots indicators by date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-a-calculated-field.md)**

    Create calculated fields to show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.


### What's changed

-   **[Create indicators on Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-fabric-tables-zcc.md)**

    Create classic automated indicators on external data via Workflow Data Fabric. Use Workflow Data Fabric tables in indicator sources just as you would any other facts tables.

-   **[Intraday scores supported on indicators with Data snapshots enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/ds-score-collection-enabled-indicators.md)**

    If you enable Data snapshots on an existing classic automated indicator, you can collect intraday scores on the data snapshots indicator.

-   **[Manage and troubleshoot your Data snapshots jobs more easily](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/data-snapshots-logs.md)**

    You now are provided with new estimates and more log information:

    -   Time estimates before a job starts
    -   Progress percentages for first-day mining, changes loader, and delta mining jobs
    -   Logs include the next scheduled run timestamp after incremental job completion

### What's deprecated or removed

-   **[KPI Composer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/designing-pa-solution.md)**

    KPI Composer is deprecated starting in the Brazil release. Removal is expected in the D release, and no replacement is planned. KPI Composer will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


### Plugin information

-   **Plugins planned for deprecation**

    KPI Composer \(sn\_kpi\_compose\): Planned for deprecation in D release. There is no replacement for this plugin.


