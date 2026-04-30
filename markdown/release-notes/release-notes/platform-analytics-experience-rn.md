---
title: Platform Analytics experience release notes
description: The ServiceNow Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
---

# Platform Analytics experience release notes

The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Xanadu release.

## Platform Analytics highlights for the Xanadu release

-   Modernize and simplify the consumption of analytics by activating the Platform Analytics experience.
-   Surface meaningful insights from your analytics data to empower the direct decision making of viewers.

See [Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for more information.

## Important information for upgrading Platform Analytics to Xanadu

New customers: The Platform Analytics experience is automatically available on the ServiceNow AI Platform. It offers an intuitive interface to help you better understand and utilize your data.

Upgrading customers: If you are currently using Core UI responsive dashboards, you will continue to have access without any disruption. Consider transitioning to the Platform Analytics experience to take full advantage of the new capabilities.

## New in the Xanadu release

-   **[Create a Process Mining project from dashboard insights](https://www.servicenow.com/docs/access?context=pm-projects-insights-suggestions&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    With a single click, create a Process Mining project from the list of suggestions in the Insights panel on a dashboard. Suggestions are available when an issue is identified that might be improved through Process Mining.

-   **[Control data source availability by role](https://www.servicenow.com/docs/access?context=dv-use-data-source-acl&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Restrict the ability to create data visualizations for a data source to roles that you specify.


## UI changes

-   **[Color icons for selecting a color](https://www.servicenow.com/docs/access?context=colors-dv&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    While configuring a data visualization, when you want to select a single color for the chart, you can now select from a set of color icons instead of only the color list. If you instead select from the list of colors, each list item has an icon of that color. You can choose a single color for any data visualization type except gauge and pie or donut.

-   **Performance Analytics not in navigation after migration**

    On new instances and after migrating to Platform Analytics on upgraded instances, Performance Analytics does not appear in the navigation menu. Instead, all Performance Analytics functionality is listed under Platform Analytics Administration.

-   **Clarification of terms KPI and indicator**

    Throughout the product, the term KPI to refer to a Performance Analytics indicator has been replaced with the term "indicator," for consistency. However, the feature names KPI Composer, KPI Details, and KPI Signals remain unchanged.


## Changed in this release

-   **[Analysis cache for indicators on data visualizations](https://www.servicenow.com/docs/access?context=data-caching-pa&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    You can now cache indicator data as well as table data.

-   **[Prefetching cached data](https://www.servicenow.com/docs/access?context=data-caching-pa&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Cached data with an expiration time of 8 hours or more is refreshed automatically within the 30 minutes before it would expire. You therefore don't have to wait for the dashboard or visualization to load new data the first time you view it for the day.

-   **[Unloading Platform Analytics dashboards to update sets simplified](https://www.servicenow.com/docs/access?context=move-pae-db-with-update-set&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Unload Platform Analytics inline dashboards to update sets with one click.

-   **[Migration improvements](https://www.servicenow.com/docs/access?context=data-migration&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Migration to the Platform Analytics Experience has added full migration of the following items in the Xanadu release:

    -   V1 Pivot reports and pivot reports with multiple columns
    -   Indicator scorecards with custom order and label names
    -   Top X elements for Performance Analytics widgets for time series breakdowns​
    -   Custom URL on-click behavior
    -   Act as filter capability
    -   Unconfigured reports, Performance Analytics widgets, and interactive filters: These objects are migrated to empty data visualizations and filter elements.
    -   Cascading filters
    -   Dashboard background colors
    -   Chart interactions: drilling down from chart to chart
-   **[Migration Center Improvements](https://www.servicenow.com/docs/access?context=data-migration&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**
    -   If you have migrated in an earlier version, previously unsupported visualizations are migrated on upgrade.
    -   Improved migration log UX.
-   **[Platform Analytics creation rights for specific scoped apps](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Using the ServiceNow AI Platform delegated development capability, a non-admin user can get the rights to create Platform Analytics objects for a specific scoped app.

-   **[Insights card grouping](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    When multiple insights of the same type are generated, they are aggregated into a single card.

    Trend and target or threshold insights are also shown on a single card.

-   **[Insight notifications in data visualizations](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies to data visualizations on both an in-line dashboard with insights activated and a UI Builder page.

-   **[Project does not need to be specified for process mining insights](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    If you have process mining insights activated, you no longer have to specify per dashboard which process mining projects to check for insights. All relevant projects are checked automatically.

-   **[Insight notifications in data visualizations](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies both to data visualizations on an in-line dashboard with insights activated and to individual data visualizations on a UI Builder page.

-   **[Auto sizing of single score visualizations](https://www.servicenow.com/docs/access?context=create-dv-sing-sc-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    The new Auto size option for single score visualizations fits the visualization dynamically into the available space, depending on targets or other information displayed in it.

-   **[Global filters apply to advanced dashboards](https://www.servicenow.com/docs/access?context=pass-global-filters-to-db&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    When opened, advanced dashboards are automatically filtered by the values of the global filter passed from the source page.

-   **[Saved data visualization on dashboard can be unlinked from library](https://www.servicenow.com/docs/access?context=editing-local-copy-saved-dv&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    If you have a shared data visualization on a dashboard that you can edit, you can unlink the local copy on the dashboard from the library and edit it without special roles and without impacting other dashboards.

-   **[Simple list follows filters](https://www.servicenow.com/docs/access?context=create-dv-simple-list-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    A simple list on a dashboard can follow filters on that dashboard. You can also add borders to a simple list.


## Deprecations

-   Reporting is not available on new instances. Use Platform Analytics data visualizations with table data sources instead. Users with admin and report\_admin roles will still be able to use Reporting for Service Portal.
-   Performance Analytics widgets are not available for new customers. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   Responsive dashboards are not available for new customers. Create dashboards in Platform Analytics instead.
-   Interactive filters are not available for new customers. Create filters in Platform Analytics instead.
-   The Analytics Hub is not available for new customers. Use KPI Details instead.
-   For new customers, interactive analysis is available only for Core UI lists.
-   In-form analytics are deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   The Performance Analytics admin console is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   Dependency assessment is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.

## Activation information

Platform Analytics is a ServiceNow AI Platform feature that is active by default. Some data sources, such as indicators, may require a subscription.

## Accessibility information

Reflow is supported for low-vision users. The following changes were made to provide this support:

-   The view mode of the Platform Analytics dashboard editor and the Visualization designer support reflow.
-   All charts: At 400% zoom, if the legend is originally in any position other than the top or the bottom, it is moved to the bottom.
-   Bubble chart: XY zoom is enabled by default during reflow at 400% zoom.
-   Donut and pie charts: Range labels are shown as legends by default at 400% zoom.
-   Gauge chart: Range labels can be shown as a legend instead. At 400% zoom, this option is enabled automatically.
-   GeoMap: Zoom controls are persistent during reflow at 200%+ zoom.
-   Pivot Table: Row headers and footers and the first column unfreeze by default during reflow at 400% zoom.
-   Time Series and bar charts: New configuration option to show the specific data point in the tooltip instead of all data points. A single data point is shown by default during reflow at 400% zoom. Also, these charts do not show points with no data.
-   Date filters: During reflow, the date picker is not available in the configuration panel. Instead, you can select the start and end date and time from the Select a date range menu. Also, all components are stacked vertically.
-   Multi-select filters: Checkbox groups with a horizontal layout reflow to a vertical layout when zoomed.
-   True/false filters: Popovers and the Clear, Cancel, and Apply buttons are removed during reflow at 400% zoom.

Other accessibility changes include:

-   Data tables can be shown for all relevant visualizations, to aid screen readers. These data tables break down the proportion of values by percentage.
-   All charts: The “More options” menu now includes the chart title.
-   Indicator Scorecard: Keyboard navigation to expand and collapse rows and speech output are now supported.

## Related ServiceNow applications and features

-   **[Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    The ServiceNow® Performance Analytics application is an in-platform process optimization solution. It enables organizations to set, track, and analyze progress toward goals. Performance Analytics provides the indicator data sources which Platform Analytics data visualizations can display.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.

-   **[User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    This application provides dashboard views for monitoring usage analytics of your Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. User Experience Analytics provides a data source which data visualizations can display.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

