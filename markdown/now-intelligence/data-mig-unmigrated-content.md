---
title: Unmigrated content and compatibility mode migrations
description: Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, filters, and configurations can't be migrated. Dashboards with this content are migrated as embedded content \(iframes\), also known as compatibility mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/data-mig-unmigrated-content.html
release: australia
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Unmigrated content and compatibility mode migrations

Most dashboard content is migrated to the new Platform Analytics experience. However, some visualizations, aspects of visualizations, filters, and configurations can't be migrated. Dashboards with this content are migrated as embedded content \(iframes\), also known as compatibility mode.

**Note:** If you have already migrated to Platform Analytics experience, the Migration Center automatically migrates any previously incompatible content that is now compatible when you upgrade releases.

## Not migrated

The only generic dashboard configuration that is not migrated is widget title alignment. Dashboards that contain unsupported content, including dynamic content blocks aren't migrated. The Core UI versions of these dashboards remain available in the dashboard library.

These filters aren't migrated:

-   Debug filter
-   Filter user preferences from dashboards
-   Cascading filters that support the Choice to Choice configuration
-   Filtered list content. For more information on List filters, see .

Visualization configurations that aren't migrated:

-   Restriction of dashboard access to specific roles.
-   Group edit rights.

    Reports that are shared to groups with edit rights only retain view rights when migrated. Open the migrated visualization in the library and share it with the group again. For more information, see [Share a data visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/share-dv-ac.md).

-   In the context of bulk migration, visualizations that are used in one or more dashboards lose their header and color configurations. \(In Core UI, these are configured at the dashboard level; in Platform Analytics experience, they are configured at the visualization level.\)

    In the context of partial migration, visualizations that are used in a single dashboard are migrated with their header and color configurations. Visualizations that are used in multiple dashboards lose their header and color configurations.


Indicator and Breakdown Scorecard elements that aren't migrated:

-   Show Distribution
-   Show Bullet chart

The Calendar year view component isn't migrated.

## Compatibility mode migrations

Migration in compatibility mode means that all of the dashboard's original artifacts are inserted into the migrated dashboard in iframes. The original content isn't changed or moved.

Dashboards with any content that is not a Performance Analytics widget, report, or interactive filter, including all custom interactive filters, custom content blocks, gauges, and gadgets, are migrated in compatibility mode, as iframes.

**Note:** Dashboards migrated in compatibility mode can experience performance issues.

## Generic configurations

Generic visualization configurations migrated in compatibility mode:

-   Sort by dot-walked fields
-   Reporting on variables and questions
-   List default drilldown view configured in Report Designer
-   [Breakdown element](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) = empty for breakdowns based on choice field
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

