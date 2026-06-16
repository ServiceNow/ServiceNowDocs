---
title: Data visualization core release notes
description: Version history for the Data visualization core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-dv-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [Data Visualization components release notes, ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Data visualization core release notes

Version history for the Data visualization core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.1.0 - June 2026**
    -   New:
        -   Calendar improvement: color highlighting based on field styling and source selection
        -   Breakdown relations support for Indicator scorecard
        -   Enable grouping on glide list field type
    -   Fixed:
        -   Calendar report: Collapse side panel by default
        -   Multiple filters are not applied consistently in list data visualization
        -   While creating new visualization, data is defaulted to task table, instead of selected data source table
        -   Platform Analytics Dashboard: List visualization with column level filtering does not takes the user back to the visualization
        -   Show total row count in analytics list
        -   Bubble chart is not rendering as expected in Platform Analytics when groupBy is selected for tables which support report ranges
        -   Pivot table data visualization is not drilling down on specific cells
        -   Unable to dotwalk to a field when adding it in the visualization data source
        -   Allow group by selection for all variable types
        -   "Apply date range" settings from Gauge visualizations are retained when switching to another visualization type
-   **Version 28.5.0 - June 2026**
    -   New:
        -   Calendar improvement - color highlighting based on field styling and source selection
        -   Breakdown relations support for Indicator scorecard
        -   Enable grouping on glide list field type
        -   Flat Pivot Table
    -   Fixed:
        -   An invalid location is displayed in the world map
        -   Group by doesn't load when there is a period \(.\) in the field
        -   "Apply date range" settings from Gauge visualizations are retained when switching to another visualization type
        -   List report with additional group by has empty selection label after migration
        -   Show total row count in analytics list
        -   Bubble chart is not rendering as expected in Platform Analytics when groupBy is selected for tables which support report ranges
        -   Platform Analytics Dashboard - List visualization with column level filtering does not takes the user back to the visualization
        -   Pivot table data visualization is not drilling down on specific cells
        -   When creating a new visualization, data source defaults to the Task \[task\] table, instead of selected data source table
        -   Calendar report: Collapse side panel by default
        -   Hide Export button based on the export properties
-   **Version 28.0.33 - June 2026**
    -   New: Added Total count configuration option for the Data visualization List type
    -   Fixed: Pivot table Data visualization is not drilling down on specific cells
-   **Version 28.4.5 - May 2026**
    -   Fixed an issue where a visualization configured to drill down to a list was not using the original visualization conditions at runtime.
    -   Fixed an issue where list links from the Platform Analytics Dashboard list component no longer opened with list context.
    -   Fixed an issue where group by selection was not available for all variable types.
    -   Fixed an issue where users were unable to dotwalk to a field when adding it in the visualization data source.
-   **Version 28.0.32 - May 2026**
    -   New: List visualization enhancements: Pagination support; consistent configuration, header, and exporting capabilities \(dependent on Yokohama Patch 13\).
    -   Fixed:
        -   Geomap widget does not show "0" values on initial render
        -   Allow group by selection for all variable types
        -   Single score visualizations truncates content incorrectly
        -   Scheduled Export "FileType=Excel \(.xlsx\)" generates "Error.pdf"
-   **Version 28.0.30 - May 2026**
    -   New: List visualization enhancements: Pagination support; consistent configuration, header, and exporting capabilities \(dependent on Yokohama Patch 13\).
    -   Fixed:
        -   Geomap widget does not show "0" values on initial render
        -   Allow group by selection for all variable types
        -   Single score visualizations truncates content incorrectly
        -   Scheduled Export "FileType=Excel \(.xlsx\)" generates "Error.pdf"
-   **Version 29.0.8 - April 2026**
    -   Fixed an issue where the list displayed a "No content available" message.
    -   Fixed an issue where bar charts were not visible despite data values being present.
    -   Fixed an issue where the Trend By value was not saved in the config panel for the Trend By component.
    -   Fixed an issue where clicking a reference in List visualization navigated to the parent table in Next Experience.
    -   Fixed an issue where Bubble charts were not rendering in Platform Analytics Workspace despite working correctly in Classic Reporting.
    -   Fixed an issue where longLabel was not being used for tooltips in business calendars.
    -   Fixed an issue where List reports with additional Group By had an empty selection label after migration.
-   **Version 28.4.3 - April 2026**
    -   Fixed an issue where Heatmap chart interactions did not work correctly and could apply a random filter, resulting in incorrect data being shown.
    -   Fixed an issue where bars in the Column visualization appeared wider than expected.
    -   Fixed an issue where the Bubble chart did not render in Platform Analytics Workspace even though it worked correctly in Classic Reporting.
    -   Fixed an issue where clicking a reference in the List visualization navigated users to the parent table in Next Experience instead of the expected record.
    -   \[Fixed an issue where the List visualization intermittently displayed a No content available message even when content should have been shown.
    -   Fixed an issue where clicking a Donut chart with only a single data segment did not update the List header as expected.
    -   Fixed an issue where a view disappeared while loading or when using the Copy with filters link.
-   **Version 28.0.29 - April 2026**
    -   Fixed an issue where the format values modal did not appear for metrics that included dot-walking fields, preventing users from configuring value formatting.
    -   Fixed an issue where the Single Score widget displayed an ellipsis \(...\) instead of large numeric values when the score could not be rendered within the available dimensions.
-   **Version 29.0.7 - March 2026**
    -   Exporting a dashboard to PDF did not export pivot tables.
    -   Bar chart was not visible despite data values being present.
    -   Dashboard filters were not being applied on List visualizations.
    -   Open Panel button in column filters for Analytics List was not working.
    -   Fixed an issue where exporting/downloading Donut visualizations as PNG/JPEG from Platform Analytics Workspace dashboards resulted in truncation.
    -   Analytics List component errors in UI Builder.
    -   Fixed an issue where "Show Links" did not remove URL links for some PA Dashboard elements.
    -   Fixed an issue where List visualization showed "No data available" if the glide.invalid\_query.returns\_no\_rows system property is set to true.
    -   "Show metric label" option was missing from Additional Settings.
    -   Fixed chart labels overlapping on Time Series visualizations in PAR dashboards.
    -   Fixed an issue where visualizations configured to drill down to a list were not using original visualization conditions at runtime.
    -   Fixed labels for alternative Group By after migration.
-   **Version 28.4.2 - March 2026**
    -   Fixed an issue where users with minimal roles were unable to add breakdowns to an indicator.
    -   Resolved a bug where visualizations configured to drill down to a list were not correctly applying the original visualization conditions at runtime.
    -   Fixed a failure causing trend charts to not load after upgrading to Zurich in Digital Portfolio Management \(DPM\).
-   **Version 28.0.28 - March 2026**
    -   Not able to select some specific variables in the now-dot-walk-connected component.
    -   Fixed an issue where drilldown functionality stopped working for Time Series visualizations when a Group By was applied after migration.
-   **Version 28.3.6 - February 2026**

    Fixed: Time series widget with 2nd y-axis is no longer migrated blank

-   **Version 28.3.5 - January 2026**
    -   Fixed:
        -   "Go up one level" arrow missing from drill down chart when Chart Interaction set to "Drill down to chart" and drill down chart type is a List - Simple or List
        -   The Platform Analytics filter can not apply to the PA Data Source with ^NQ condition
        -   Custom message no longer displays after upgrading to Zurich
        -   Data not showing in a column data visualization in tooltip and opens list view in wrong table
        -   Data Visualization component - Spline chart is getting cut off at the top section
-   **Version 28.0.27 - January 2026**
    -   Fixed:
        -   Legend in Pie charts now properly refreshes when sorting is modified
        -   Resolved issue where Spline charts in Data Visualization component were truncated at the top of the screen
        -   Fixed long-running Calendar reports that previously displayed all-day task details incorrectly and corrected duplicate short descriptions appearing in activity box
        -   Additional group by values now display correctly in Preview mode instead of showing "none of the values are shown"
-   **Version 28.0.25 - December 2025**

    Fixed: Avoid displaying an additional unrelated button for the AI Data Explorer

-   **Version 28.3.0 - December 2025**
    -   New: Ability to export to CSV and Excel from the data visualizations in Platform Analytics dashboards
    -   Fixed:
        -   Dashboard refresh icon doesn't work with List component
        -   Trend by field doesn't follow the same order while changing the order of the metrics data on Data Visualisations
        -   Legend and tooltip labels are having \(undefined\) values in case of duplicate labels
-   **Version 28.0.23 - November 2025**
    -   Fixed:
        -   Removal of extra button called "Enter Modal" for now assist explorer
        -   Resolved an issue where refreshing an empty Explorer tab after creating an Explorer from a data visualization in another tab resulted in a duplicate Explorer being created
-   **Version 28.2.1 - October 2025**

    Fixed:

    -   Creates new explorer in already opened empty explorer tab when an explorer is created from a data visualization
    -   Missing instruction to interact with chart for screen reader user
    -   Allow disabling exploration entry points per workspace
-   **Version 24.0.2 - August 2023**
    -   Changed:
        -   New data capabilities:
            -   Added support of forecasting for User Experience Analytics and MetricBase data sources
            -   Option to adjust forecasting settings per chart
        -   Timeseries: Added support of top X elements for Timeseries with group by for both table and indicator data sources
        -   Indicator Scoreboard:
            -   Allow to change label for manually selected indicator
            -   Easy way to re-order manually selected indicators
            -   Improved readability of previous period score
        -   Added property that allows users to refresh any data visualization on demand \(in UI Builder\)
        -   Accessibility:
            -   Improved support for screen readers
            -   Support of high contrast \(forced color\) mode
        -   Bug fixes and usability improvements.
-   **Version 23.3.2 - July 2023**

    Fixed: Bug fix.

-   **Version 23.2.4 - May 2023**
    -   New visualization type: Geomap: Allows users to visualize geographical distribution of data for a world, country, region, or state.
    -   Changed:
        -   New configuration setting to allow define alternative group by available for users to change during chart use. Available for bar, pie/donut, timeseries, heat map, bubble, and indicator scorecard visualizations.
        -   Added possibility to set group by for timeseries with multiple metrics and data sources.
        -   Improved chart responsiveness for cases with a small visualisation size Improved tick distribution for timeseries charts Indicator
    -   Scorecard:
        -   Improved readability of change and change % by better indication of direction with arrow and adding color of the change
        -   Added possibility to show all breakdown elements \(first level rows\)
    -   Bug fix and usability improvements
-   **Version 23.0.8 - March 2023**

    Bug fixes

-   **Version 23.0.5 - February 2023**
    -   New visualization types:
        -   Gauge: Shows where a single value lies across a range from minimum to maximum expected values. Set colored data ranges to help users understand progress.
        -   Bubble: Shows two ordinal fields, such as Priority and Age, as circles of different sizes along an x-y axis. Use the relative size and position of the circles to compare fields and see their relationships.
        -   Heatmap: Shows the relationship between two table fields or indicator breakdowns as a spectrum of shading between two colors. The changes in color as you move along the axes reveal patterns in the value of one or both fields or breakdowns.
    -   Changed:
        -   New setting to allow customizing message when there are no data for data visualization.
        -   Single score: Option to add icon for single score
        -   User can drill down to the total value in a donut chart
        -   Pivot table:
            -   Select multiple data sources
            -   Sort columns during consumption
            -   Configure column header truncation/wrapping

