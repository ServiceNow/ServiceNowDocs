---
title: PAR CoreUI Migration Scripts release notes
description: Version history for the PAR CoreUI Migration Scripts application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-air-par-coreui-migration-scripts.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# PAR CoreUI Migration Scripts release notes

Version history for the PAR CoreUI Migration Scripts application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.5 - May 2026**
    -   Fixed:
        -   Multipivot migration should set wrap header configuration to true by default.
        -   After migration, widget settings \(as header title alignment, title color, follow filters\) are lost.
-   **Version 3.0.12 - May 2026**
    -   Fixed:
        -   Multipivot migration should set wrap header configuration to true by default.
        -   After migration, widget settings \(as header title alignment, title color, follow filters\) are lost.
-   **Version 2.0.13 - May 2026**

    Fixed: After migration, widget settings \(as header title alignment, title color, follow filters\) are lost.

-   **Version 4.0.4 - April 2026**

    Fixed: The migrated visualizations do not have the owner field set correctly

-   **Version 3.0.11 - April 2026**
    -   Fixed:
        -   The migrated visualizations do not have the owner field set correctly
        -   Filter conditions defined in Core UI Reports on the data source are not carried over to the Platform Analytics Dashboard during migration
        -   The aggregation configuration is not migrated for the Speedometer/Dial visualization
        -   Core UI Reports with multiple datasets are migrated with the legend in the wrong order
-   **Version 2.0.12 - April 2026**

    Fixed: Spline visualization with the metric label for one of the data sources does not migrate as expected

-   **Version 4.0.3 - March 2026**
    -   Fixed:
        -   Static content with hidden title is migrated with the title visible
        -   Aggregation is not migrated for the Speedometer/Dial
        -   Bar series report custom duration formatting is not migrated
        -   "Add sort" option is not migrated correctly for the charts
        -   ITIL users can not open the report designer page for any of the reports that were shared with them
        -   The migration banner not hidden from the Migration Center
        -   Duplicates observed in the "Stack by" dropdown on data visualizations after migration to Pllatform Analytics experience
        -   Trend visualization columns are overlapping after the migration
        -   Duplicate API calls in Migration Center
        -   Unmigrated 'disableRanges' property in Bar chart causes "unsaved changes" alert when the visualization is opened
-   **Version 3.0.10 - February 2026**
    -   Fixed:
        -   Trend visualization columns are overlapping after the migration
        -   Invalid configuration. Required field: aggregateField in Dashboards after switching to the Next Experience UI
-   **Version 2.0.11 - January 2026**

    Fixed: Fix empty decimal precision in Core UI pie report migration- Timeseries Report with multidata set is giving "Invalid value for groupBy field: null" after migration- Bulk migration redirects to "Start Moving" page despite migration invoked sys\_property being true

-   **Version 2.0.8 - October 2025**
    -   Fixed:
        -   Unsupported widget titles, widget names are getting changed during migration as per the Portal Page preferences
        -   Migration Center info content is not readable when Polaris is off
        -   Time series widgets are migrated as vertical bars instead of columns.
-   **Version 3.0.8 - September 2025**
    -   Fixed:
        -   PA widgets, with multiple widget indicators, with different time series have incorrect values
        -   The Show date range selector is not migrated
        -   Timeseries Report with multidata set is giving "Invalid value for groupBy field: null" after migration
        -   Bulk migration redirects to "Start Moving" page despite migration invoked sys\_property being true
-   **Version 3.0.6 - August 2025**
    -   Fixed:
        -   Report/dashboard admins can access the Migration Center review pages
        -   Migrated gauge chart is not loading data source until edit
        -   During dashboard migration to platform analytics, widgets that have Header disabled migrate as though enabled
        -   Drilldown of timeseries line chart is not migrated
        -   iFramed widgets are not working after the migration when using drilldown
        -   Heatmap does not maintain the same axis element order and the chart color after the migration
        -   Chart to chart drildown is not working after the migration
-   **Version 2.0.7 - July 2025**
    -   Fixed:
        -   Titles of migrated compatibility widgets are not translating in Next Experience UI
        -   Unsupported widget titles, widget's names are getting changed during migration as per the Portal Page preferences
        -   Time series - display Settings: Duplicate values are appearing along the Y-axis
        -   PA widget that has multiple indicator widgets are stacked and not side by side
        -   During dashboard migration, widgets that have Header disabled migrate as though enabled
-   **Version 2.0.6 - June 2025**
    -   Fixed:
        -   Migration Center homepage is not responsive based on browser size
        -   Cascading filters configurations are not correctly migrated
        -   Chart title is missing after the migration
        -   Intermittent issue with them back button on a compatibility mode component
        -   Donut visualization: drill down does not redirect to the List view
-   **Version 1.5.3 - April 2025**

    Fixed:

    -   Respect value formatting on migration
    -   Dashboard tabs are migrating with incorrect names
    -   Trend line is incorrectly toggled on after migration
    -   Breakdown filters are not migrated correctly
-   **Version 2.0.4 - February 2025**
    -   Fixed:
        -   Migration Center Activate button is disabled when "com.glide.par.coreui.migration.enabled" is set to false
        -   Support of the migration of multiple datasets timeseries reports
        -   Support of the migration of chart-to-chart drill downs reports
        -   Migration Center does not load the artifacts number and list automatically while the migration is running
        -   Supports of drill down of the widgets Filters in compatibility mode in Platform Analytics dashboard
    -   Changed: Legacy widget is renamed to "Compatibility mode widget"
-   **Version 1.3.11 - December 2024**
    -   Fixed:
        -   Improved confirmation message on Migration Center
        -   Avoid reloading of compatibility mode components in Dashboards when changing the layout
-   **Version 1.1.1 - December 2024**

    Fixed: Updated confirmation modal on Migration Center.

-   **Version 1.4.5 - November 2024**

    Fixed: Enable confirmation message when starting the full migration and the activation of the Platform Analytics experience.

-   **Version 1.4.2 - August 2024**
    -   New: Supports migration of Pareto charts
    -   Fixed:
        -   Follow elements on PA widgets is considered on migration to Follow filters setting
        -   Additional group by on List visualization are migrated as additional visible columns
        -   Maintain the same order for Time series widgets with multiple additional indicators
        -   Updated documentation links and date on Migration Center info page
        -   Improve the install process and alert message when plugins are out of date
-   **Version 1.3.6 - May 2024**
    -   New: The migration script is updated to support the migration of:
        -   Report Pivot chart v1
        -   Report Pivot chart with multiple columns
        -   Unconfigured Reports, PA widgets, and Interactive filters
        -   PA widget Indicator scorecard custom order and label names
        -   PA widgets breakdown "Show Top X" configuration
        -   Chart interactions: custom URL drill-downs
        -   Chart interactions: act as filter.
-   **Version 1.1.1 - February 2024**

    Migration script to migrate Core UI responsive dashboards, reports, PA widgets, and interactive filters to the Platform Analytics experience and see the results. System Administrator will be able to start the move to Platform Analytics and collaborate with Analytics admins on reviewing the migration results.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

