---
title: Content not migrated or migrated in compatibility mode
description: Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, filters, and configurations cannot be migrated. Dashboards with this content are migrated as embedded content \(iframes\), also known as compatibility mode.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-15"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Content not migrated or migrated in compatibility mode

Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, filters, and configurations cannot be migrated. Dashboards with this content are migrated as embedded content \(iframes\), also known as compatibility mode.

**Note:** If you have already migrated to Platform Analytics experience, the Migration Center automatically migrates any previously incompatible content that is now compatible when you upgrade releases.

## Not migrated

The only generic dashboard configurations that is not migrated is widget title alignment.

Filters that are not migrated

-   Debug filter
-   Filter user preferences from dashboards
-   Cascading filters that support the Choice &gt; Choice configuration
-   Filtered list content. For more information on List filters, see [Create a filter in List](https://www.servicenow.com/docs/access?context=t_CreatingFilters&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Visualization configurations that are not migrated:

-   Restriction of dashboard access to specific roles.
-   Group edit rights.

    Reports that are shared to groups with edit rights only retain view rights when migrated. Open the migrated visualization in the library and share it with the group again. For more information, see [Share a data visualization in the Visualization Designer](../../reporting/task/share-dv-ac.md#).

-   In the context of bulk migration, visualizations that are used in one or more dashboards lose their header and color configurations. \(In Core UI, these are configured at the dashboard level; in Platform Analytics experience, they are configured at the visualization level.\)

    In the context of partial migration, visualizations that are used in a single dashboard are migrated with their header and color configurations. Visualizations that are used in multiple dashboards lose their header and color configurations.


Indicators/Breakdown Scorecard elements that are not migrated:

-   Show Distribution
-   Show Bullet chart

Calendar component elements that are not migrated:

-   Year view
-   Highlighting based on

## Compatibility mode migrations

Migration in compatibility mode means that all of the dashboard's original artifacts are inserted into the migrated dashboard in iframes. The original content is not changed or moved.

Dashboards with any content that is not a Performance Analytics widget, report, or interactive filter, including all custom interactive filters, custom content blocks, gauges, and gadgets, are migrated in compatibility mode, as iframes.

**Note:** Dashboards migrated in compatibility mode may experience performance issues.

## Generic configurations

Generic visualization configurations migrated in compatibility mode:

-   Sort by dot-walked fields
-   Reporting on variables/questions
-   List default drilldown view configured in Report Designer
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
-   Histogram
-   Funnel
-   Pyramid

## Performance Analytics widgets

Performance Analytics widgets migrated in compatibility mode:

-   Workbench
-   Text Analytics
-   Treemap
-   Previous period charts
-   Spider
-   Funnel
-   Pyramid
-   Relative compare

