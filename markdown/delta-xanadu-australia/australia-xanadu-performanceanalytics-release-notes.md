---
title: Combined Performance Analytics release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Performance Analytics from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-performanceanalytics-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Performance Analytics release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Performance Analytics from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Performance Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Performance Analytics to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Performance Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Apply multiple levels of breakdown to an indicator](https://www.servicenow.com/docs/access?context=multi-level-breakdowns&family=yokohama&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Apply multiple levels of breakdown to an indicator](https://www.servicenow.com/docs/access?context=multi-level-breakdowns&family=zurich&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create data snapshots indicators](https://www.servicenow.com/docs/access?context=create-ds-automated-indicator&family=australia&ft:locale=en-US)**

Create data snapshots indicators and their sources rather than being able to enable data snapshots only on existing indicators. Benefit from the simplicity of data snapshots indicators, including the escape from the two-level breakdown limit. You can create either automated or formula indicators. Access control for these indicator is the same as for classic Performance Analytics indicators.

-   **[Create intraday indicators](https://www.servicenow.com/docs/access?context=create-ds-source&family=australia&ft:locale=en-US)**

Track process changes at a more granular level than daily, such as by work shift. Data snapshots indicator sources support business calendars with intraday periods, which can be as short as per minute.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Performance Analytics features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Explore native data snapshots indicators with KPI Details](https://www.servicenow.com/docs/access?context=kpi-details-targets&family=australia&ft:locale=en-US)**

KPI Details supports data snapshots indicators that you create, not only those that are enabled from classic indicators. The following features have been created for or extended to native data snapshots indicators:

    -   Subscriptions for alerts on targets and thresholds, which can be set from the targets and thresholds panels
    -   Adjustable filtering by breakdown, calendar, or time series aggregation
    -   Hierarchical breakdowns, with scores rolled up to parent elements
    -   Customizable score formatting options, such as precision and abbreviation
-   **[View data trends in data snapshots as data accumulates](https://www.servicenow.com/docs/access?context=create-ds-automated-indicator&family=australia&ft:locale=en-US)**

When you select a field by which to trend a data snapshots automated indicator, you have the option to show the trend for incomplete collection periods. This feature shows the trend as it develops for live data without having to wait for the end of the collection period. You can set this behavior either on the automated data snapshot indicator record or in a time series data visualization for a data snapshot indicator.

-   **[Collect data snapshots scores with confidence](https://www.servicenow.com/docs/access?context=tables-unlimited-breakdowns&family=australia&ft:locale=en-US)**

Data mining for data snapshots scores has the following improvements:

    -   Collect scores for tables with any volume of records.
    -   The system accurately and automatically handles data gaps when data mining is turned off.
    -   You are warned of the implications before you manually disable data mining \(score collection\).
-   **[Activate data snapshots in more cases and with better information](https://www.servicenow.com/docs/access?context=activate-unlimited-breakdowns&family=australia&ft:locale=en-US)**
    -   Activate indicators without active data collector jobs.
    -   Activate indicators regardless of underlying record volume. For example, the `INSERT_VOLUME_EXCEEDED` error no longer occurs.
    -   If the activation fails because of scripted breakdowns, the scripted breakdowns are listed in the failure message.
    -   Generic parsing errors have been rewritten into specific, categorized messages.
-   **[Data snapshots automatically installed on eligible instances](https://www.servicenow.com/docs/access?context=limitations-mlb&family=australia&ft:locale=en-US)**

If you have Australia Patch 3 or later, the Data snapshots plugin is installed automatically if you have RaptorDB Professional. If your instance is also domain separated, the Data snapshots feature is installed but disabled.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Performance Analytics features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Performance Analytics features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Performance Analytics widgets are not available on new instances. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   The Analytics Hub is not available on new instances or instances that have fully migrated to Platform Analytics. Use KPI Details instead.
-   The Performance Analytics admin console is deprecated on new instances. For upgrading customers, the console is available but does not show data from the new Platform Analytics artifacts.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Performance Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this application.

 The full features of Performance Analytics are available with a subscription. Activate the Performance Analytics plugin that matches your subscription. For details, see [Activating your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

 The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches  your subscription. For details, see Activate your Performance Analytics  subscription.

</td></tr><tr><td>

Zurich

</td><td>

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

 The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches  your subscription. For details, see Activate your Performance Analytics  subscription.

</td></tr><tr><td>

Australia

</td><td>

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

 The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches your subscription. For details, see [Activating your subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.

</td></tr><tr><td>

Zurich

</td><td>

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Performance Analytics, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

 See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

 See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

 See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

**Note:** The highlights for this release all refer to the newer Data Snapshots indicator architecture, which requires RaptorDB Professional.

-   Create new Data snapshots indicators with unlimited breakdowns. Previously you could convert only existing indicators. These indicators are supported in Data Visualizations and in KPI Details.
-   Track intraday changes with indicators such as changes between shifts. You can track changes in shifts that are still in progress, with data retrieved down to the minute level.
-   View scores as they accumulate throughout the day without having to wait for end-of-day processing.
-   When exploring a Data snapshots indicator with KPI Details, customizable score formats, apply flexible breakdowns and aggregation periods, direct alert subscriptions for targets and thresholds, and apply hierarchical roll-ups for breakdowns.

 See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

