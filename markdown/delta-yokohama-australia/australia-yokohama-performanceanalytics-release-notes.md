---
title: Combined Performance Analytics release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Performance Analytics from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-performanceanalytics-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Performance Analytics release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Performance Analytics from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Performance Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Performance Analytics to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   The **Dashboard Visualization** tab in KPI Composer is no longer supported. Existing data visualization tabs remain.
-   The Analytics Hub has been replaced by KPI Details. Attempts to open the Analytics Hub are redirected to KPI Details.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Performance Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches  your subscription. For details, see Activate your Performance Analytics  subscription.


</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Performance Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Additional requirements**

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.


</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

