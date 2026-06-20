---
title: Combined Platform Analytics experience release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Platform Analytics experience from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-platformanalyticsexperience-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Platform Analytics experience release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Platform Analytics experience from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Platform Analytics experience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Platform Analytics experience to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

New customers: The Platform Analytics experience is automatically available on the ServiceNow AI Platform. It offers an intuitive interface to help you better understand and utilize your data.

 Upgrading customers: If you are currently using Core UI responsive dashboards, you will continue to have access without any disruption. Consider transitioning to the Platform Analytics experience to take full advantage of the new capabilities.

</td></tr><tr><td>

Yokohama

</td><td>

If you had previously migrated your analytics assets to Platform Analytics, assets that were in compatibility mode but are newly supported in Yokohama are migrated automatically.

</td></tr><tr><td>

Zurich

</td><td>

On upgrade, any homepages on your instance that have been opened are migrated to Core UI dashboards, which are visible in the dashboard library. For more information, see [Homepage deprecation](https://servicenow-staging.fluidtopics.net/access?context=homepage-deprecation-help-tool&family=zurich&ft:locale=en-US).

 Simple lists are all converted to the new List element on upgrade.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Platform Analytics experience.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Create a Process Mining project from dashboard insights](https://servicenow-staging.fluidtopics.net/access?context=pm-projects-insights-suggestions&family=xanadu&ft:locale=en-US)**

With a single click, create a Process Mining project from the list of suggestions in the Insights panel on a dashboard. Suggestions are available when an issue is identified that might be improved through Process Mining.

-   **[Control data source availability by role](https://servicenow-staging.fluidtopics.net/access?context=dv-use-data-source-acl&family=xanadu&ft:locale=en-US)**

Restrict the ability to create data visualizations for a data source to roles that you specify.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Generate data visualizations conversationally](https://servicenow-staging.fluidtopics.net/access?context=analytics-assist-landing-page&family=yokohama&ft:locale=en-US)**

Generate Platform Analytics artifacts from conversational interactions using Analytics Generation. Analytics Generation is part of the Now Assist for Creator application.

-   **[Implement filters in groups](https://servicenow-staging.fluidtopics.net/access?context=create-filter-group&family=yokohama&ft:locale=en-US)**

Create filter groups with shared apply, clear, and reset buttons. Filters in a group appear in their own container. Grouping filters reduces the number of calls and improves performance compared to cascading filters for big data use cases.

-   **[Apply multiple levels of breakdown to an indicator](https://servicenow-staging.fluidtopics.net/access?context=multi-level-breakdowns&family=yokohama&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.

-   **[Show the distribution of data in box plot data visualizations](https://servicenow-staging.fluidtopics.net/access?context=create-dv-box-plot&family=yokohama&ft:locale=en-US)**

Show the median and lower and upper quartiles of numeric data along with outliers by using box plots. You can also compare the distribution of different groups of this data.

-   **[Target suggestion cards](https://servicenow-staging.fluidtopics.net/access?context=proactive-analytics&family=yokohama&ft:locale=en-US)**

Be notified of missing target values and review dates for indicators. If you have target Insights active for your dashboard, Target suggestion cards alert you to the missing values and provide an easy way to fix them.


</td></tr><tr><td>

Zurich

</td><td>

-   **[View, share, and export table records in the List component](https://servicenow-staging.fluidtopics.net/access?context=create-dv-analytics-list&family=zurich&ft:locale=en-US)**

Take advantage of the improved list capabilities of the List element, which replaces List - Simple. The List supports pagination, export from dashboards, export to comma-separated values, and alternative group by. It also provides a consistent configuration experience with other data visualizations.

-   **[Create indicators and migrate to data snapshots in the indicator library](https://servicenow-staging.fluidtopics.net/access?context=your-kpis&family=zurich&ft:locale=en-US)**
    -   Manage indicators from the indicator library, including links to create and edit indicators.
    -   Activate data snapshots conveniently, opening up the possibilities of applying multiple levels of breakdown to your indicators. See statistics on recent views and updates in tiles.
    -   If data snapshots are activated for the instance, see how many indicators are eligible and have already had data snapshots enabled.
    -   Show columns for any field on indicator records, as well as usage information.
-   **[Drill down to application overviews for User Experience Analytics](https://servicenow-staging.fluidtopics.net/access?context=visualization-drilldown-in-config-ws&family=zurich&ft:locale=en-US)**

Navigate to individual application overviews for User Experience Analytics from data visualizations. The **Go to data view** chart interaction is now supported for User Experience Analytics data and takes the viewer to these overview pages by default.

-   **[Filter data in User Experience Analytics](https://servicenow-staging.fluidtopics.net/access?context=filter-user-list&family=zurich&ft:locale=en-US)**

Filter User Experience Analytics data on default and custom User Experience Analytics properties.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Platform Analytics experience features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Analysis cache for indicators on data visualizations](https://servicenow-staging.fluidtopics.net/access?context=data-caching-pa&family=xanadu&ft:locale=en-US)**

You can now cache indicator data as well as table data.

-   **[Prefetching cached data](https://servicenow-staging.fluidtopics.net/access?context=data-caching-pa&family=xanadu&ft:locale=en-US)**

Cached data with an expiration time of 8 hours or more is refreshed automatically within the 30 minutes before it would expire. You therefore don't have to wait for the dashboard or visualization to load new data the first time you view it for the day.

-   **[Unloading Platform Analytics dashboards to update sets simplified](https://servicenow-staging.fluidtopics.net/access?context=move-pae-db-with-update-set&family=xanadu&ft:locale=en-US)**

Unload Platform Analytics inline dashboards to update sets with one click.

-   **[Migration improvements](https://servicenow-staging.fluidtopics.net/access?context=data-migration&family=xanadu&ft:locale=en-US)**

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
-   **[Migration Center Improvements](https://servicenow-staging.fluidtopics.net/access?context=data-migration&family=xanadu&ft:locale=en-US)**
    -   If you have migrated in an earlier version, previously unsupported visualizations are migrated on upgrade.
    -   Improved migration log UX.
-   **[Platform Analytics creation rights for specific scoped apps](https://servicenow-staging.fluidtopics.net/access?context=c_DelegatedDevelopment&family=xanadu&ft:locale=en-US)**

Using the ServiceNow AI Platform delegated development capability, a non-admin user can get the rights to create Platform Analytics objects for a specific scoped app.

-   **[Insights card grouping](https://servicenow-staging.fluidtopics.net/access?context=proactive-analytics&family=xanadu&ft:locale=en-US)**

When multiple insights of the same type are generated, they are aggregated into a single card.

Trend and target or threshold insights are also shown on a single card.

-   **[Insight notifications in data visualizations](https://servicenow-staging.fluidtopics.net/access?context=proactive-analytics&family=xanadu&ft:locale=en-US)**

If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies to data visualizations on both an in-line dashboard with insights activated and a UI Builder page.

-   **[Project does not need to be specified for process mining insights](https://servicenow-staging.fluidtopics.net/access?context=proactive-analytics&family=xanadu&ft:locale=en-US)**

If you have process mining insights activated, you no longer have to specify per dashboard which process mining projects to check for insights. All relevant projects are checked automatically.

-   **[Insight notifications in data visualizations](https://servicenow-staging.fluidtopics.net/access?context=proactive-analytics&family=xanadu&ft:locale=en-US)**

If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies both to data visualizations on an in-line dashboard with insights activated and to individual data visualizations on a UI Builder page.

-   **[Auto sizing of single score visualizations](https://servicenow-staging.fluidtopics.net/access?context=create-dv-sing-sc-ac&family=xanadu&ft:locale=en-US)**

The new Auto size option for single score visualizations fits the visualization dynamically into the available space, depending on targets or other information displayed in it.

-   **[Global filters apply to advanced dashboards](https://servicenow-staging.fluidtopics.net/access?context=pass-global-filters-to-db&family=xanadu&ft:locale=en-US)**

When opened, advanced dashboards are automatically filtered by the values of the global filter passed from the source page.

-   **[Saved data visualization on dashboard can be unlinked from library](https://servicenow-staging.fluidtopics.net/access?context=editing-local-copy-saved-dv&family=xanadu&ft:locale=en-US)**

If you have a shared data visualization on a dashboard that you can edit, you can unlink the local copy on the dashboard from the library and edit it without special roles and without impacting other dashboards.

-   **[Simple list follows filters](https://servicenow-staging.fluidtopics.net/access?context=create-dv-simple-list-ac&family=xanadu&ft:locale=en-US)**

A simple list on a dashboard can follow filters on that dashboard. You can also add borders to a simple list.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Migrate more features to Platform Analytics from the Core UI](https://servicenow-staging.fluidtopics.net/access?context=data-migration&family=yokohama&ft:locale=en-US)**

Migration scripts are improved to support more features. All migration script improvements are applied automatically on upgrade to content that was previously migrated in compatibility mode.

    -   Data table configurations are migrated from the Core UI to Platform Analytics data visualizations.
    -   Dashboard groups are migrated to dashboard categories.
    -   Pareto charts are migrated.
    -   List component border changes are migrated.
    -   Follow/unfollow filter settings are migrated for Lists.
-   **[Use more Core UI features in Platform Analytics](https://servicenow-staging.fluidtopics.net/access?context=data-mig-unmigrated-content&family=yokohama&ft:locale=en-US)**

Several data visualizations have been enhanced to match the capacities in Core UI reports and widgets. The migration script supports these enhancements. Each of these enhancements has an entry in the release notes with links to the product documentation.

    -   Use the new Box plot data visualization.
    -   Configure **Follow filters** per metric on bar or time series visualizations with multiple metrics.
    -   Sort values by name, report range, and element order on time series visualizations of table data.
    -   Choose an aggregate or separate view of breakdown elements on time series visualizations of indicator data.
    -   Select dates from business calendars on time series visualizations.
-   **[Trend by Business calendars in time series data visualizations](https://servicenow-staging.fluidtopics.net/access?context=config-dv-time-series-table-data&family=yokohama&ft:locale=en-US)**

Business calendars are a **Trend by** option for table data sources on time series visualizations. \(Core UI feature gap\)

-   **[Use a Fiscal calendar in date filters](https://servicenow-staging.fluidtopics.net/access?context=create-date-filter-workspace&family=yokohama&ft:locale=en-US)**

If your instance has Fiscal calendars installed, you can choose relative data ranges from that calendar.

-   **Export [dashboards](https://servicenow-staging.fluidtopics.net/access?context=export-pae-dashboard-ppt&family=yokohama&ft:locale=en-US) and [data visualizations](https://servicenow-staging.fluidtopics.net/access?context=export-visualization-vd&family=yokohama&ft:locale=en-US) to PDF and PPT**

Export dashboards and data visualizations to PDF or Microsoft PowerPoint files at will or in [scheduled emails](https://servicenow-staging.fluidtopics.net/access?context=schedule-export-dboards-data-viz&family=yokohama&ft:locale=en-US).

-   **[Show breakdown elements separately on time series visualizations of indicators](https://servicenow-staging.fluidtopics.net/access?context=config-dv-time-series-ind-data&family=yokohama&ft:locale=en-US)**

Show multiple elements in the chart separately rather than as an aggregate value by turning on the **Show filter as separate series** option. \(Core UI feature gap\)

-   **[Lock editing on dashboards](https://servicenow-staging.fluidtopics.net/access?context=edit-db-in-ac&family=yokohama&ft:locale=en-US)**

Ensure that only one person can have a dashboard open for editing at one time through the edit lock on dashboards. If you are locked out of editing a dashboard, you see who the current editor is.

-   **[Access indicator record or scoresheet](https://servicenow-staging.fluidtopics.net/access?context=access-indicator-record-scoresheet&family=yokohama&ft:locale=en-US)**

Navigate either to the record of the indicator you are exploring or its scoresheet through KPI Details. Appropriate roles are required.

-   **[Export records that underlie an indicator from KPI Details](https://servicenow-staging.fluidtopics.net/access?context=kpid-record-list-actions&family=yokohama&ft:locale=en-US)**

With **Show records** activated in KPI Details, you can export the list of records in one of several formats, either as a local download or as an email attachment.

-   **[Hide axes for bar visualizations](https://servicenow-staging.fluidtopics.net/access?context=create-dv-bar-ac&family=yokohama&ft:locale=en-US)**

Control the display of axes on bar charts. On horizontal bar charts, you can hide the y-axis. On vertical bar charts, you can hide the x-axis.

-   **[Cache indicator scorecard data](https://servicenow-staging.fluidtopics.net/access?context=data-caching-pa&family=yokohama&ft:locale=en-US)**

Indicator scorecards now support data caching.

-   **[Group by elements more efficiently in data visualizations](https://servicenow-staging.fluidtopics.net/access?context=select-group-runtime&family=yokohama&ft:locale=en-US)**

Specify the maximum number of elements in a Group By you want to retrieve through the **Max number of groups** option. Previously, all elements from the database were retrieved and then sorted.

-   **[Prefetch dashboard layout](https://servicenow-staging.fluidtopics.net/access?context=configure-dashboard-data-broker&family=yokohama&ft:locale=en-US)**

If you have a dashboard component on a page in your own workspace, improve performance by using a preset to configure a data broker that pre-fetches static JavaScript, such as layout.

-   **[Call multiple visualizations together](https://servicenow-staging.fluidtopics.net/access?context=local-data-instance-multi-viz&family=yokohama&ft:locale=en-US)**

For a technical dashboard, if you have multiple data visualizations of the same type calling the same data source, configure a data resource to make a single call for all of them.

-   **[Improvements to time-series visualizations](https://servicenow-staging.fluidtopics.net/access?context=config-dv-time-series-table-data&family=yokohama&ft:locale=en-US)**
    -   Simplify identifying specific values on line, spline, area, or step charts through the **Show markers** option, which displays a symbol at each data point.
    -   Sort by name, report range, group bucket, and element order. \(Core UI feature gap\)
-   **[Improvements for visualizations that show multiple metrics](https://servicenow-staging.fluidtopics.net/access?context=chart-options-multi-metrics&family=yokohama&ft:locale=en-US)**
    -   In time series visualizations, provide viewers an alternative group by, where the viewer chooses the group-by value at runtime, for up to 3 data sources. \(Core UI feature gap\)
    -   Set whether individual metrics follow filter components on the page or dashboard in both bar and time series visualizations. \(Core UI feature gap\)

</td></tr><tr><td>

Zurich

</td><td>

-   **[Select whether to drill down to Platform Analytics or Core UI lists](https://servicenow-staging.fluidtopics.net/access?context=visualization-drilldown-in-config-ws&family=zurich&ft:locale=en-US)**

Decide whether data view chart interactions for data visualizations on an instance drill down to Platform Analytics or Core UI record lists. This choice applies only on the Platform Analytics experience.

-   **[View usage information in the dashboards library](https://servicenow-staging.fluidtopics.net/access?context=dashboards-for-admin-users&family=zurich&ft:locale=en-US)**

For analytics managers, the dashboard library now contains usage statistics, such as the number of dashboards not viewed in one year and the number of dashboards deactivated for more than three months.

-   **[Export data visualizations from dashboards to PNG and JPEG](https://servicenow-staging.fluidtopics.net/access?context=export-data-vis-from-dboard&family=zurich&ft:locale=en-US)**

Export individual data visualizations as a viewer to a graphic file.

-   **[Platform Analytics experience is supported even when Next Experience UI is disabled](https://servicenow-staging.fluidtopics.net/access?context=data-migration-perform&family=zurich&ft:locale=en-US)**

You can migrate to Platform Analytics even if Next Experience isn’t enabled. Core UI dashboards are embedded in iframes.

-   **[Migration Center changes](https://servicenow-staging.fluidtopics.net/access?context=data-migration&family=zurich&ft:locale=en-US)**
    -   Dashboard owners can perform partial migration on their own dashboards.
    -   Geomap migration supported.
    -   Interactive filter check box option.
    -   Header color is supported.
    -   Export to CSV from lists is supported.
-   **[Data visualizations and filters support Workflow Data Fabric tables](https://servicenow-staging.fluidtopics.net/access?context=workflow-data-fabric&family=zurich&ft:locale=en-US)**

Perform data analysis on external data fabric sources.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Platform Analytics experience features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Platform Analytics experience features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Reporting is not available on new instances. Use Platform Analytics data visualizations with table data sources instead. Users with admin and report\_admin roles will still be able to use Reporting for Service Portal.
-   Performance Analytics widgets are not available for new customers. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   Responsive dashboards are not available for new customers. Create dashboards in Platform Analytics instead.
-   Interactive filters are not available for new customers. Create filters in Platform Analytics instead.
-   The Analytics Hub is not available for new customers. Use KPI Details instead.
-   For new customers, interactive analysis is available only for Core UI lists.
-   In-form analytics are deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   The Performance Analytics admin console is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   Dependency assessment is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Platform Analytics experience.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Platform Analytics is a ServiceNow AI Platform feature that is active by default. Some data sources, such as indicators, may require a subscription.

</td></tr><tr><td>

Yokohama

</td><td>

The Platform Analytics experience is active by default. However, some additional steps might be required.

-   To use indicator data sources, you might need to activate Performance Analytics.
-   To use Process Mining with the Platform Analytics experience, you might need to activate Process Mining.

</td></tr><tr><td>

Zurich

</td><td>

Platform Analytics experience is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Platform Analytics experience we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Platform Analytics experience we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Platform Analytics experience, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

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

</td></tr><tr><td>

Yokohama

</td><td>

Dashboard overview and Filter components now support Reflow at 400% zoom.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Platform Analytics experience we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Platform Analytics experience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Modernize and simplify the consumption of analytics by activating the Platform Analytics experience.
-   Surface meaningful insights from your analytics data to empower the direct decision making of viewers.

 See [Platform Analytics experience](https://servicenow-staging.fluidtopics.net/access?context=par-workspace&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Effortlessly create bold, meaningful data graphics by and refining the results in an AI-powered conversational interface.
-   Speed up the process of turning insights into actions with dynamic new features like suggested performance targets and more powerful data filtering.
-   Share data insights more broadly with enhanced Microsoft PowerPoint support.

 See [Platform Analytics experience](https://servicenow-staging.fluidtopics.net/access?context=par-workspace&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Collaborate on data-informed decisions through an AI-assisted, interactive explorer that serves as a centralized workspace, where you can create and share data visualizations on the fly.
-   Manage Performance Analytics indicators more conveniently, with access to editing, creation, and migration from within the Platform Analytics experience.

 See [Platform Analytics experience](https://servicenow-staging.fluidtopics.net/access?context=par-workspace&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

