---
title: Gauge visualization component setup
description: The Gauge visualization is a visualization type within the Data visualization component that lets you create gauge visualizations. A gauge can be a useful alternative to a Single score visualization if you have a fixed maximum value that you want to indicate progress towards.Configure the behavior of a Gauge visualization with these properties.The following properties apply to Gauge data visualizations that show table data.The following properties apply to Gauge data visualizations that show indicator data.The following properties apply to Gauge data visualizations that show Usage Insights data.These properties configure how Health Log Analytics data is presented on gauge visualizations.The following properties are available for formatting all Gauge visualizations. Access them from the Format values link under Metric.Select event handlers to configure the actions \(events\) provided with the Gauge visualization component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/gauge-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 23
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Gauge visualization component setup

The Gauge visualization is a visualization type within the Data visualization component that lets you create gauge visualizations. A gauge can be a useful alternative to a Single score visualization if you have a fixed maximum value that you want to indicate progress towards.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: For UI Builder: admin or ui\_builder\_admin. For Visualization Designer in runtime: any internal role

## Procedure

1.  Define a label for your Data visualization that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-vis-content-tree.png"\] Alt text: Data Visualization component with label displayed in the content tree

2.  Select the Data visualization, using one of these methods:

    -   Click anywhere within the component.
    -   Select the data visualization label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

3.  Select the gauge **Data Visualization Type**.

    The available data sources and properties change depending on the selected chart type.

4.  Click **Add data source** to select a table or indicator data source to base a visualization on.

5.  Add filters to the data as needed.

6.  Click **Add this source** to add your selected data source.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Gauge visualization component properties

Configure the behavior of a Gauge visualization with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="id_rmw_jbq_frb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show header \[showHeader\]

</td><td id="entry_show-header">

The visualization header, including title and icons.

</td></tr><tr><td>

Show header separator \[showHeaderSeparator\]

</td><td id="entry_show-header-separator">

Option to display a line separating the header from the rest of the component.

</td></tr><tr><td>

Chart title \[headerTitle\]

</td><td id="entry_chart-title">

Title of the visualization.

</td></tr><tr><td>

Description \[description\]

</td><td id="entry_description">

A short overview about the visualization that the end user sees. Descriptions help users find the visualization.

</td></tr><tr><td>

Wrap title \[wrapTitle\]

</td><td id="entry_wrap-title">

Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.

</td></tr><tr><td>

Show border \[showBorder\]

</td><td id="entry_show-border">

Option to display a line around the component.

</td></tr><tr><td>

Show refresh option

</td><td id="entry_show-refresh-option">

Option to show or hide the refresh option from data visualizations. If cache is enabled on a dashboard, the Refresh option is hidden.

</td></tr><tr><td>

Bare \[bareBorder\]

</td><td id="entry_bare">

Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.

</td></tr></tbody>
</table><table id="table_om5_qxv_yqb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define data manually \[showDataPassthrough\]

</td><td>

Option to pass data/values directly to the chart using JSON instead of using standard data sources.

</td></tr><tr><td>

Data \[dataPassthrough\]

</td><td>

JSON field for manually passing data. Replaces the **Data sources** property when **Define data manually** is toggled on.

 You can also bind a local data instance to this field. The local data resource instance must be based on one of the data resources of the Data visualization core application. Use a different local data resource instance for each type of data visualization on your page. Configure each local data resource instance to fit the visualization type. The data binding must end in `.output.result`.

 \[Omitted image "data-viz-data-source-binding.png"\] Alt text: Local data binding instance bound to data visualization.

 For more information, see [Dynamically expose data in UI Builder pages \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/data-resources.md) and [Use a local data instance with a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/dv-local-data-instance.md).

</td></tr><tr><td>

Data sources \[dataSources\]

</td><td>

The data source that the visualization is based on. Select from the following:-   Table: The current state of your data, as it is stored in an underlying database table. You can define conditions to filter the table entries or select from sets of predefined conditions on the table. These predefined conditions are also called [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_ReportSources.md). If you define custom conditions, you can use questions or service catalog variables that are defined for the table.
-   Indicator: Key performance indicators \(KPIs\) for tracking changes in your data over time. Use an indicator data source to show trends and help forecast future events. For more information, see [Performance Analytics indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_Indicators.md).

Data visualizations do not support benchmarking indicators \(Benchmarking indicator = true\).

You can select breakdowns and breakdown elements to filter the indicators. The operators "is one of" and "is \(dynamic\)" are available if the indicator and breakdown support multi-element aggregation. For more information, see [Conditional filters and operators for indicators and breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/condition-operators-ind-bkdowns.md#section_breakdown-operators).

The ability to create data visualizations of indicators can be role-restricted on your instance in the **par\_vis\_config.data\_source.can\_select\_indicator** property.

-   Usage Insights: Usage metrics of your Next Experience web applications and others. For more information, see [Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/user-exp-analytics-landing.md).

To include Usage Insights data sources in your visualizations, install the Usage Insights in PAR Integration application from the ServiceNow store. The available metrics depend on the visualization type. For more information about using these data sources, see [Usage Insights data sources for visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/uxa-data-sources.md).

-   Health Log Analytics: Analysis of log data from multiple sources to identify potential issues. Plugins for the application include dashboards and data visualizations, and the data visualizations are available in the library for reuse. For more information, see [Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-landing-page.md).

Data visualizations for Health Log Analytics can be created or edited only in the UI Builder.


</td></tr></tbody>
</table>After selecting the data source, configure the appropriate data properties:

-   Table data properties
-   Indicator data properties
-   Usage Insights data properties
-   Health Log Analytics data properties

To find the tables for each of these properties, search for each table title on this page in your browser search function.

<table id="table_rx2_1cw_yqb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Display settings**

</td></tr><tr><td>

Gauge arc angle \[gaugeArcAngle\]

</td><td id="entry_gauge-arc-angle">

Choice of sizes for the gauge, in degrees.

</td></tr><tr><td>

Value label size \[value\]

</td><td id="entry_value-label-size">

Characters that represent dynamic sizes: small \(S\), medium \(M\), or large \(L\). The actual size of the type changes in proportion to the size of the chart.

</td></tr><tr><td>

Inner radius \[innerRadius\]

</td><td id="entry_dial-inner-radius">

Decimal number to set the ratio of inner radius to outer radius of the dial chart. Allowed value from 0.7 to 0.95.

</td></tr><tr><td>

Show data table \[showDataTable\]

</td><td id="entry_show-data-table">

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td>

Height \[height\]

</td><td id="entry_height">

The height of the chart.

</td></tr><tr><td class="sub-head" colspan="2">

Ranges

</td></tr><tr><td>

Min value \[minValue\]

</td><td id="entry_dial-min-value">

Start value of the dial or gauge scale. If not specified, it is set automatically.

</td></tr><tr><td>

Max value \[maxValue\]

</td><td id="entry_dial-max-value">

End value of the dial or gauge scale. If not specified, it is set automatically.

</td></tr><tr><td>

Configure ranges \[ranges=\{numberOfRanges:\{id, label\}, rangeColorScheme:\{id, label\}, data:\{range\_1...range\_n\}\}\]

</td><td>

Specifics for a number of ranges to divide the gauge into, default 3. You select the number of ranges, the start and end values of each range, the labels, and the color spectrum.

</td></tr><tr><td class="sub-head" colspan="2">

**Legend**

</td></tr><tr><td>

Show legend \[showRegister\]

</td><td id="entry_show-legend">

Option to display the legend. Activated automatically at 400% zoom.

</td></tr><tr><td>

Legend position \[registerPosition\]

</td><td id="entry_legend-position">

Legend location relative to the chart: Above, Below, Right, or Left

</td></tr><tr><td>

Legend orientation \[registerOrientation\]

</td><td id="entry_legend-orientation">

Options for how to display the register.-   Horizontal `horizontal`: Option to display the legend horizontally.
-   Vertical `vertical`: Option to display the legend vertically up to five lines.

 This property applies only when **Legend position** is Below.

</td></tr><tr><td>

Horizontal alignment \[legendHorizontalAlignment\]

</td><td id="entry_legend-horizontal-position">

Horizontal alignment of elements in the legend: Start, Center, or End

</td></tr><tr><td>

Max legend item width, px \[legendMaxItemWidth\]

</td><td id="entry_max-legend-width">

Number of pixels after which the item in the legend is truncated.

</td></tr><tr><td class="sub-head" colspan="2">

Labels

</td></tr><tr><td>

Score label \[scoreLabel\]

</td><td>

The label of the score in the center of the gauge:

-   No label \(None\)
-   The same label as the visualization metric \(Metric label\)
-   The label that you set for the range that the score falls into, in Configure ranges \(Range label\)

 Labels are disabled and replaced by legends at 400% zoom.

</td></tr><tr><td>

Show range limit \[showRangeLimit\]

</td><td>

When true, the limits that you configured for the ranges are shown. If you did not configure any ranges, the default min and max values are shown.

</td></tr><tr><td>

Show range labels \[showRangeLabels\]

</td><td>

When true, any labels you configured for ranges are shown. This property is available only if you configured ranges and specified labels for them.

</td></tr></tbody>
</table>### Table data properties for Gauge visualizations

The following properties apply to Gauge data visualizations that show table data.

<table id="table_data-props-table"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for Table data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Select an aggregation \[aggregateFunction\]

</td><td id="entry_select-aggregate">

Computational method for aggregating data. The default is **Count**, which displays the number of records selected.**Note:** If you select **Count Distinct**, only unique records are counted. For example, you want to generate a report with a distinct number of users who have one or more of the roles in a given list of roles. Users with more than one role would be counted twice unless you use **Count Distinct**.

</td></tr><tr><td>

Field \[aggregateField\]

</td><td id="entry_metric-field">

Field to apply the metric to, for **Average**, **Sum**, or **Count Distinct** aggregations. You may further be able to aggregate on fields from extended tables.The data is shown in a format that matches the field type. For example, if you select an integer field, such as the **Priority** field, the data is expressed as a number. If you select a duration field, such as **Business duration** on the Incident table, the aggregated data is expressed in days, hours, and minutes.

If function fields were created in Report Designer for the table, they are available in the dropdown list. For more information, see [Report on function fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/function-fields-reporting.md).

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings for Table data sources

</td></tr><tr><td>

Show 0 when no data is available \[showZero\]

</td><td id="entry_show-0">

When toggled on, shows empty \(NULL\) values as zero \(0\). True by default. When true, you can't set a custom message when there is no data.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Refresh after being away for X min. \[backgroundRefreshInterval\]

</td><td id="entry_refresh-after-being-away">

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td>

Refresh requested \[refreshRequest\]

</td><td>

A string that can be passed down to trigger a data refresh. Refresh will be triggered only if the new value of this property is different than the previous one.

</td></tr><tr><td>

Real time update \[enableRealTimeUpdate\]

</td><td id="entry_real-time-update">

Option to update score in real time. If you enable both real-time update and data caching, real-time update overrides data caching.**Note:**

-   When a condition is dot-walked to another table, high traffic on the table suspends real-time data updates.
-   For tables, real-time updating supports only COUNT data aggregations.
-   Real-time updating is not supported on single score, dial, and gauge visualizations based on remote tables or Workflow Data Fabric tables.

</td></tr><tr><td>

Use data cache \[useDataCache\]

</td><td>

If activated, user queries are cached. This cached data is used on page refreshes instead of the database being queried. The load time for the data visualization is thereby shortened.The user can get current data on demand by using the manually refreshing the data visualization with the **Refresh** button.

Turning on **Real time update**, if that is available for this data visualization, overrides the use of data caching. Setting a value for **Refresh after being away for X min** or **Refresh requested** also disables data caching.

Default: false

</td></tr><tr><td>

Show cache time \[showCacheTime\]

</td><td>

When true, shows an icon that indicates that returned data are from the cache. On hover, the user sees how old the data is. Applies only when useDataCache is true.Default: true \(only when useCacheData is true\)

</td></tr><tr><td>

Cache expiration time \(h\) \[cacheExpirationTime\]

</td><td>

Number denoting the lifespan of cached data in hours. When the lifespan is exceeded, a page refresh results in the cached data being updated through a database query.A value for **Refresh after being away for X min** or **Refresh requested** can result in the data cache being updated before its expiration time.

Default: 0

</td></tr><tr><td class="sub-head" colspan="2">

No data messageThis section is available only when **Show zero** is false. Otherwise, the no data message is 0.

</td></tr><tr><td>

Set custom message when no data \[enableCustomEmptyState\]

</td><td id="entry_enable-custom-empty-state">

Option to configure a custom message that displays when no data is returned.

</td></tr><tr><td>

Illustration \[emptyStateIllustration\]

</td><td id="entry_empty-state-illustration">

An illustration to include in the message.

</td></tr><tr><td>

Heading \[emptyStateHeading\]

</td><td id="entry_empty-state-heading">

Header text of the message that describes why no data was returned.

</td></tr><tr><td>

Content \[emptyStateContent\]

</td><td id="entry_empty-state-content">

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment \[emptyStateAlignment\]

</td><td id="entry_empty-state-alignment">

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>### Indicator data properties

The following properties apply to Gauge data visualizations that show indicator data.

<table id="table_data-props-indicator"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for Indicator data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Time aggregation \[aggregateIndicator\]

</td><td id="entry_metric-time-aggregation">

Time aggregation to apply to the metric, such as 7-day running SUM or By-month AVG. Default is the same as the indicator period. For more information, see [Applying time series aggregations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/applying-time-series-aggregations.md).

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting properties table.

</td></tr><tr><td colspan="2">

Date range options

</td></tr><tr><td>

Apply date range \[applyDateRange\]

</td><td id="entry_apply-date-range">

When turned on, this option allows date filters on the dashboard or UIB page to apply to this visualization. The date range can also be configured in the visualization, but date filters override visualization settings.

</td></tr><tr><td>

Show data for selected period as \[scoreType\]

</td><td id="entry_show-data-period-as">

Available when **Apply date range** is selected.The indicator aggregation logic for how scores from the selected period are shown, such as Latest score, Sum, or Average.

</td></tr><tr><td>

Set absolute period \[showAbsolutePeriod\]

</td><td id="entry_set-abs-period">

Option to set absolute start and end date.Available when **Apply date range** is selected.

</td></tr><tr><td>

Period start \[startTime\]

</td><td id="entry_period-start">

Start date for the absolute period.This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period end \[endTime\]

</td><td id="entry_period-end">

End date for the absolute period.This property applies only when **Set absolute period** is true.

Select **Use current date for period end** to automatically update the end date to the current date. \(Not available if the start date is in the future.\)

</td></tr><tr><td>

Number of periods \[numberOfPeriods\]

</td><td id="entry_number-periods">

Number of date periods to display. This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period \[period\]

</td><td id="entry_period-interval">

Time interval for each date period. -   Days `D`
-   Weeks `W`
-   Months `M`
-   Quarters `Q`
-   Years `Y`

 The available periods depend on the time aggregation. A period can't be shorter than the time aggregation unit. If you change the time aggregation to a longer unit than the selected period, the period changes to the shortest period that is still available.

 This property applies only when **Set absolute period** is false.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Refresh after being away for X min. \[backgroundRefreshInterval\]

</td><td id="entry_refresh-after-being-away">

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td>

Refresh requested \[refreshRequest\]

</td><td>

A string that can be passed down to trigger a data refresh. Refresh will be triggered only if the new value of this property is different than the previous one.

</td></tr><tr><td>

Real time update \[enableRealTimeUpdate\]

</td><td id="entry_real-time-update-ind">

Option to update score in real time.**Note:**

-   This setting is available for automated, non-scripted indicators with a non-scripted breakdown mapping.
-   Real-time score updating does not support MIN, MAX, or COUNT DISTINCT aggregations.

</td></tr><tr><td>

Use data cache \[useDataCache\]

</td><td>

If activated, user queries are cached. This cached data is used on page refreshes instead of the database being queried. The load time for the data visualization is thereby shortened.The user can get current data on demand by using the manually refreshing the data visualization with the **Refresh** button.

Turning on **Real time update**, if that is available for this data visualization, overrides the use of data caching. Setting a value for **Refresh after being away for X min** or **Refresh requested** also disables data caching.

Default: false

</td></tr><tr><td>

Show cache time \[showCacheTime\]

</td><td>

When true, shows an icon that indicates that returned data are from the cache. On hover, the user sees how old the data is. Applies only when useDataCache is true.Default: true \(only when useCacheData is true\)

</td></tr><tr><td>

Cache expiration time \(h\) \[cacheExpirationTime\]

</td><td>

Number denoting the lifespan of cached data in hours. When the lifespan is exceeded, a page refresh results in the cached data being updated through a database query.A value for **Refresh after being away for X min** or **Refresh requested** can result in the data cache being updated before its expiration time.

Default: 0

</td></tr><tr><td class="sub-head" colspan="2">

No data message

</td></tr><tr><td>

Set custom message when no data \[enableCustomEmptyState\]

</td><td id="entry_enable-custom-empty-state">

Option to configure a custom message that displays when no data is returned.

</td></tr><tr><td>

Illustration \[emptyStateIllustration\]

</td><td id="entry_empty-state-illustration">

An illustration to include in the message.

</td></tr><tr><td>

Heading \[emptyStateHeading\]

</td><td id="entry_empty-state-heading">

Header text of the message that describes why no data was returned.

</td></tr><tr><td>

Content \[emptyStateContent\]

</td><td id="entry_empty-state-content">

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment \[emptyStateAlignment\]

</td><td id="entry_empty-state-alignment">

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>### User Experience Analytics data properties

The following properties apply to Gauge data visualizations that show Usage Insights data.

<table id="table_it1_rtn_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric properties for Usage Insights data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Data update options—Usage Insights data sources

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Refresh after being away for X min. \[backgroundRefreshInterval\]

</td><td id="entry_refresh-after-being-away">

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td>

Refresh requested \[refreshRequest\]

</td><td>

A string that can be passed down to trigger a data refresh. Refresh will be triggered only if the new value of this property is different than the previous one.

</td></tr><tr><td class="sub-head" colspan="2">

No data message

</td></tr><tr><td>

Set custom message when no data \[enableCustomEmptyState\]

</td><td id="entry_enable-custom-empty-state">

Option to configure a custom message that displays when no data is returned.

</td></tr><tr><td>

Illustration \[emptyStateIllustration\]

</td><td id="entry_empty-state-illustration">

An illustration to include in the message.

</td></tr><tr><td>

Heading \[emptyStateHeading\]

</td><td id="entry_empty-state-heading">

Header text of the message that describes why no data was returned.

</td></tr><tr><td>

Content \[emptyStateContent\]

</td><td id="entry_empty-state-content">

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment \[emptyStateAlignment\]

</td><td id="entry_empty-state-alignment">

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>### Health Log Analytics data properties

These properties configure how Health Log Analytics data is presented on gauge visualizations.

<table id="table_data-props-indicator"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for Indicator data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting Properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Date range

</td></tr><tr><td>

Set absolute period \[showAbsolutePeriod\]

</td><td id="entry_set-abs-period">

Option to set absolute start and end date.Available when **Apply date range** is selected.

</td></tr><tr><td>

Period start \[startTime\]

</td><td id="entry_period-start">

Start date for the absolute period.This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period end \[endTime\]

</td><td id="entry_period-end">

End date for the absolute period.This property applies only when **Set absolute period** is true.

Select **Use current date for period end** to automatically update the end date to the current date. \(Not available if the start date is in the future.\)

</td></tr><tr><td>

Number of periods \[numberOfPeriods\]

</td><td id="entry_number-periods">

Number of date periods to display. This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period \[period\]

</td><td id="entry_period-interval">

Time interval for each date period. -   Days `D`
-   Weeks `W`
-   Months `M`
-   Quarters `Q`
-   Years `Y`

 The available periods depend on the time aggregation. A period can't be shorter than the time aggregation unit. If you change the time aggregation to a longer unit than the selected period, the period changes to the shortest period that is still available.

 This property applies only when **Set absolute period** is false.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown\[enableDrilldown\]

</td><td>

Enables the viewer to open the Health Log Analytics log viewer by interacting with the chart, such as by clicking on a value.

</td></tr><tr><td>

Refresh after being away for X min. \[backgroundRefreshInterval\]

</td><td id="entry_refresh-after-being-away">

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td>

Refresh requested \[refreshRequest\]

</td><td>

A string that can be passed down to trigger a data refresh. Refresh will be triggered only if the new value of this property is different than the previous one.

</td></tr></tbody>
</table>### Formatting properties

The following properties are available for formatting all Gauge visualizations. Access them from the **Format values** link under Metric.

<table id="table_formatting"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use custom formatting \[customFormat\]

</td><td id="entry_custom-format">

Option to use custom formatting on the component.

</td></tr><tr><td>

Decimal precision \[decimalPrecision\]

</td><td id="entry_decimal-precision">

Number of decimal places to show in the metric.**Note:** Only available when **Use custom formatting** is true

</td></tr><tr><td>

Rounding \[rounding\]

</td><td id="entry_rounding">

Type of rounding to use to reach the number of decimals in the **Decimal precision** field. Options include:-   Up `UP`
-   Down `DOWN`
-   Ceiling `CEILING`
-   Floor `FLOOR`
-   Half up `HALF_UP`
-   Half down `HALF_DOWN`
-   Half even `HALF_EVEN`

 **Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Use the thousands group separator \[thousandSeparatorEnabled\]

</td><td id="entry_1000s-separator">

Option to use a comma to separate groups of thousands.**Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Enable abbreviation \[abbreviationEnabled\]

</td><td id="entry-enable-abbreviation">

Option to use an alphabetical abbreviation. For example, M to represent million. **Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Example

</td><td id="entry_example">

Example of the final value to show in the component. **Note:** Only available when **Use custom formatting** is true

</td></tr></tbody>
</table>## Gauge visualization component events

Select event handlers to configure the actions \(events\) provided with the Gauge visualization component.

The Events tab shows the events used by the Gauge visualization component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Gauge visualization actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_msr_kpn_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visualization Clicked

</td><td>

Dispatched when the visualization is clicked.Payload:

-   [ItemSelectedPayload](https://developer.servicenow.com/dev.do#!/reference/now-experience/tokyo/shared-components/now-vis-score-wrapper/uib-config%23typedefs-ClickEventPayload) – Payload of the action dispatched when the visualization is clicked.

Payload type: `{title: string, type: string, params: PayloadParams, data: PayloadData}`

-   PayloadBreakdown - Breakdowns represented as a json object. Payload type: `{sysId: string, elements: Array.<string>}`
-   PayloadParams – Parameters of the clicked visualization.

Payload type: `{table: string, query: string, indicatorSysid: string, breakdowns: Array.<PayloadBreakdown>, domain: string, aggregate: string, scoreDate: string}`

-   PayloadData - Payload from the data point \(timestamp, element name, value, color, cssColor\) is dispatched when clicking a visualization. For example, clicking on a data point in a timeseries chart passes the timestamp and value in the payload.

Payload type: `{elements: Array.<string>, value: string, color: string, cssColor: string}`


</td></tr></tbody>
</table>