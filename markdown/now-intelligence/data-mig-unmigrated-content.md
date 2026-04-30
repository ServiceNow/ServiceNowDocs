---
title: Content not migrated or migrated in compatibility mode
description: Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, and filters are inserted in the migrated dashboard as embedded content \(iframes\), also known as compatibility mode. Some configurations are not migrated at all.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-02-11"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Content not migrated or migrated in compatibility mode

Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, and filters are inserted in the migrated dashboard as embedded content \(iframes\), also known as compatibility mode. Some configurations are not migrated at all.

**Note:** If you have already migrated to Platform Analytics experience, the Migration Center automatically migrates any previously incompatible content that is now compatible when you upgrade releases.

## Not migrated

Generic dashboard configurations that are not migrated:

-   Dashboard groups
-   Widget header and title colors
-   Widget title alignment

Filters that are not migrated

-   Group filter
-   Debug filter
-   Filter user preferences from dashboards
-   Cascading filters that support the Choice &gt; Choice configuration

Visualization configurations that are not migrated:

-   Export to PNG/JPEG on the chart itself from dashboard
-   Report drilldown into another report on partial migrations.

    Report drilldown into another report is supported on full migration.

-   Progress bars for Percent Complete fields in Simple list visualizations.
-   Restriction of dashboard access to specific roles.
-   Data tables under data visualizations

Indicators/Breakdown Scorecard elements that are not migrated:

-   Show Distribution
-   Show Bullet chart

Calendar component elements that are not migrated:

-   Year view
-   Highlighting based on

## Compatibility mode migrations

Migration in compatibility mode means that the original artifacts are inserted into the migrated dashboard in iframes. The original content is not changed or moved.

All custom interactive filters, custom content blocks, gauges, and gadgets are migrated in compatibility mode, as iframes.

All other content that is not a Performance Analytics widget, report, or interactive filter is migrated in compatibility mode, as iframes.

**Note:** Dashboards with visualizations or other widgets migrated in compatibility mode may experience performance issues.

Custom interactive filters are migrated in compatibility mode, but may not work on the migrated dashboard. If the custom functionality is required, roll back the dashboard back to the Core UI version.

## Generic configurations

Generic visualization configurations migrated in compatibility mode:

-   Report drilldown into another report

    Migrated in compatibility mode on partial migrations. Report drilldown into another report is supported on full migration.

-   Sort by dot-walked fields
-   Reporting on variables/questions
-   Configuration for filters applied as separate/aggregate
-   List default drilldown view configured in Report Designer
-   Business calendar \(as trend by\) for timeseries reports
-   Timeseries PA breakdown: top X elements
-   [Breakdown element](../../performance-analytics/concept/performance-analytics-glossary.md#) = empty for breakdowns based on choice field
-   Sort by Performance Analytics breakdown based on choice field order
-   Single score with compare X period back
-   Pivot scorecard support for element filter
-   Group by based on duration fields
-   Different follow filters for related indicators on the Indicator scorecard and visualizations
-   Hierarchy breakdown support on filters/data visualizations

## List scorecard configurations

List scorecard configurations migrated in compatibility mode:

-   Show Key indicators
-   Filter based on: Best Performing, Worst Performing, Improved, Deteriorated
-   Different follow filters on additional indicators

## Other scorecard configurations

Scorecard widgets with multiple widget indicators that have different time series aggregations are migrated in compatibility mode.

## Reports

Reports migrated in compatibility mode:

-   Control
-   Trendbox
-   Box
-   Pareto

    Can be migrated with the latest store update.

-   Histogram
-   Funnel
-   Pyramid
-   Geomap

## Performance Analytics widgets

Performance Analytics widgets migrated in compatibility mode:

-   Workbench
-   Text Analytics
-   Treemap
-   Previous period charts
-   Spider
-   Funnel
-   Pyramid
-   Pareto

    Can be migrated with the latest store update.

-   Relative compare

