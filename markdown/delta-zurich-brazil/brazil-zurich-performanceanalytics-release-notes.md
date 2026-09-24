---
title: Combined Performance Analytics release notes for upgrades from Zurich to Brazil
description: Consolidated page of all release notes for Performance Analytics from Zurich to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-brazil/brazil-zurich-performanceanalytics-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Performance Analytics release notes for upgrades from Zurich to Brazil

Consolidated page of all release notes for Performance Analytics from Zurich to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Performance Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Performance Analytics to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Performance Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr><tr><td>

Brazil

</td><td>

Starting with the Brazil release, KPI Composer is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Performance Analytics features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Data snapshots automatically installed on eligible instances](https://www.servicenow.com/docs/access?context=limitations-mlb&family=australia&ft:locale=en-US)**

If you have Australia Patch 3 or later, the Data snapshots plugin is installed automatically if you have RaptorDB Professional. If your instance is also domain separated, the Data snapshots feature is installed but disabled.


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

</td></tr><tr><td>

Brazil

</td><td>

-   **[Use bucket groups to breakdown Data Snapshots indicators by continuous data](https://www.servicenow.com/docs/access?context=map-bucket-group-to-ds-source&family=brazil&ft:locale=en-US)**

To filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.

-   **[Use calculated fields to break down Data Snapshots indicators by date](https://www.servicenow.com/docs/access?context=create-a-calculated-field&family=brazil&ft:locale=en-US)**

Create calculated fields to show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.

-   **[Create indicators on Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=data-fabric-tables-zcc&family=brazil&ft:locale=en-US)**

Create classic automated indicators on external data via Workflow Data Fabric. Use Workflow Data Fabric tables in indicator sources just as you would any other facts tables.

-   **[Intraday scores supported on indicators with Data snapshots enabled](https://www.servicenow.com/docs/access?context=ds-score-collection-enabled-indicators&family=brazil&ft:locale=en-US)**

You can now collect intraday scores on classic indicators with Data snapshots enabled instead of only on natively created Data snapshots indicators.

-   **[Manage and troubleshoot your Data snapshots jobs more easily](https://www.servicenow.com/docs/access?context=data-snapshots-logs&family=brazil&ft:locale=en-US)**

You now are provided with new estimates and more log information:

    -   Time estimates before a job starts
    -   Progress percentages for first-day mining, changes loader, and delta mining jobs
    -   Logs include the next scheduled run timestamp after incremental job completion

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Performance Analytics features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Performance Analytics features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   The **Dashboard Visualization** tab in KPI Composer is no longer supported. Existing data visualization tabs remain.
-   The Analytics Hub has been replaced by KPI Details. Attempts to open the Analytics Hub are redirected to KPI Details.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Activation information**

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches  your subscription. For details, see Activate your Performance Analytics  subscription.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches your subscription. For details, see [Activating your subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

Complimentary Performance Analytics for Incident ManagementPerformance Analytics is active by default. You cannot create indicators or breakdowns with this complimentary application.

 The full features of Performance Analytics are available with a subscription. For details, see [Activating your subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&family=brazil&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Additional requirements**

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

 See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-zurich-brazil/rn-combined-intro.md)

