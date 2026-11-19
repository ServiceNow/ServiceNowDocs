---
title: Single score component setup
description: The Single score component is a visualization type within Data visualization that lets you create single score visualizations.Select the data source for the Single score Data visualization with these properties.These properties configure how table data is presented on Single Score visualizations.These properties configure how indicator data is presented on Single Score visualizations.These properties configure how Usage Insights data is presented on Single Score visualizations.These properties configure how Health Log Analytics data is presented on single score visualizations.These properties apply to Single Score visualizations for all data sources. Access them through the Format values link under Metric.Select event handlers to configure the actions \(events\) provided with the Single score component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/single-score-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 27
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Single score component setup

The Single score component is a visualization type within Data visualization that lets you create single score visualizations.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Data visualization that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-vis-content-tree.png"\] Alt text: Data Visualization component with label displayed in the content tree

2.  Select the Data visualization, using one of these methods:

    -   Click anywhere within the component.
    -   Select the data visualization label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  Select the Single Score **Data Visualization Type**.

    The available data sources and properties change depending on the selected chart type.

4.  Click **Add data source** to select a table, indicator, or \(if enabled\) Usage Insights data source to base a visualization on.

    Alternatively, you can define the data manually in JSON or use a local data instance.

5.  Add filters to the data as needed.

6.  Click **Add this source** to add your selected data source.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Single Score visualization component properties

Select the data source for the Single score Data visualization with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
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

Score size \[scoreSize\]

</td><td id="entry_score-size">

Sets the size of the score. Options include: -   XS `xs`
-   S `sm`
-   M `md`
-   L `lg`
-   XL `xl`
-   XXL `xxl`
-   Auto `auto`: Size adjusts automatically between the preceding sizes depending on the viewport size and the space available after all details have been added in the **Additional settings**.

</td></tr><tr><td>

Score icon \[scoreIcon\]

</td><td id="entry_score-icon">

Select one of the icons provided with the design system to precede the score. Optional.

**Note:** See [https://developer.servicenow.com/dev.do\#!/reference/next-experience/xanadu/now-components/now-icon/gallery](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-icon/gallery) for more information.

</td></tr><tr><td>

Icon style \[iconStyle\]

</td><td id="entry_icon-style">

Select "With background" to apply color to the background of the icon. Select "No background" to apply color to the icon itself.

</td></tr><tr><td>

Sparkline style \[sparklineStyle\]

</td><td id="entry_sparkline-style">

Style of sparkline chart. Options include:-   Area `area`: Option to display the sparkline as a line with the area between its points and the horizontal axis colored in.
-   Line `line`: Option to display the sparkline as a line.

This property applies only with indicator data sources and when **Show sparkline** is true.

</td></tr><tr><td>

Metric label position \[headingPosition\]

</td><td id="entry_metric-label-position">

Position for the metric label. Options include:-   Above score `top`
-   Below score `bottom`

This property applies only with table data sources and when **Show metric label** is true.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr id="set-color-type"><td>

Set color type \[type\]

</td><td>

Type of color scheme to apply to the component. Options include: -   Default `default`: A color from the UX Theme Properties \[sys\_ux\_theme\_property\] table. The specific colors depend on which theme variant in the UX Themes \[sys\_ux\_theme\] table is applied to the instance.
-   Single color/Colors per metric `singleColor`: Select a single color in the **Set value color** field. You can select the color from a set of icons, from a list of colors including their icons, or by searching for the color name or hexadecimal value. The colors are taken from the Color Definition \[sys\_report\_color\] table.

If the visualization has more than one metric, you see the Colors per metric option instead. This option lets you select a single color \[singleColor\] for each metric.


</td></tr><tr><td>

Color \[color\]

</td><td id="entry_single-color">

Single color to apply to the component. **Note:** Only available when **Set color type** is **Single color**.

</td></tr><tr><td>

Color rules \[rules\]

</td><td id="entry_color-rules">

Define dynamic colors based on rules. For example, you can set a metric to display in blue if the metric's value is less than 100. For more information, see [Create coloring rules for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/colors-dv.md).

</td></tr><tr><td>

Add rule

</td><td id="entry_add-color-rule">

Open a dialog to add a color rule. See the properties in the **Color rule** section below to add a color rule.

</td></tr><tr><td class="sub-head" colspan="2">

Color rule

</td></tr><tr><td>

Operator \[operator\]

</td><td id="entry_color-rule-operator">

Operator used when evaluating values, such as **greater than** or **between**. For example, to style values of less than 5, select **lower than** and specify **Value** as 5.

</td></tr><tr><td>

Value 1, Value 2 \[value1, value2\] \("between" operator\)Value \[value\] \(all other operators\)

</td><td id="entry_color-rule-value">

The value to apply to the operator. For example, if greater than 50, set the metric to red. For the "between" operator, select two values. The specified color is used to display values between these values.

</td></tr><tr><td>

Color \[color\]

</td><td id="entry_color-rule-color">

Font color to apply to values that match this rule.

</td></tr><tr><td>

Order \[order\]

</td><td id="entry_color-rule-order">

A numerical value that determines the order in which the rules apply. The system applies rules in the order of smallest to largest.

</td></tr></tbody>
</table>### Table data properties

These properties configure how table data is presented on Single Score visualizations.

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

Show metric label \[showMetricLabel\]

</td><td id="entry_show-metric-label">

Option to show the metric label. In donut charts, the value is not shown if it can't fit the donut.

</td></tr><tr><td>

Show score update time \[showScoreUpdateTime\]

</td><td id="entry_show-score-update-time">

Option to display the time of the last update.

</td></tr><tr><td>

Use relative score time \[useRelativeScoreTime\]

</td><td>

Option to display the time of the last update relative to the current time. Available when **Show score update time** is on.

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

These properties configure how indicator data is presented on Single Score visualizations.

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

Additional settings for Indicator data sources

</td></tr><tr><td>

Show metric label \[showMetricLabel\]

</td><td id="entry_show-metric-label">

Option to show the metric label. In donut charts, the value is not shown if it can't fit the donut.

</td></tr><tr><td>

Show change \[showChange\]

</td><td id="entry_show-change">

Option to show the change compared to the previous score or period.

</td></tr><tr><td>

Show change % \[showChangePercentage\]

</td><td id="entry_show-change-pct">

Option to show the percent change compared to the previous score or period. This property applies only when **Show change** is turned on.

</td></tr><tr><td>

Show change from \[showChangeFrom\]

</td><td>

If **Apply date range** and **Show change** are turned on, sets whether to show the change from the previous score, the aggregate of the previous period, or the score at the start of the previous period.

</td></tr><tr><td>

Show target \[showTarget\]

</td><td id="entry_show-target">

Option to display the target value.Not available when **Compare period over period** is turned on.

</td></tr><tr><td>

Show gap % \[showGapPercentage\]

</td><td id="entry_show-gap-pct">

Option to show the percentage between the current value and the target value. This property applies only when **Show change** is turned on.

</td></tr><tr><td>

Show sparkline \[showSparkline\]

</td><td id="entry_show-sparkline">

Option to show a line graph representing the change over time.

</td></tr><tr><td>

Show score date \[showScoreDate\]

</td><td id="entry_show-score-date">

Option to show the date when the score was collected.This property applies only when **Real time update** is false.

</td></tr><tr><td>

Show score update time \[showScoreUpdateTime\]

</td><td id="entry_show-score-update-time-ind">

Option to display the time of the last update.This property applies only when **Real time update** is true.

</td></tr><tr><td>

Use relative score time \[useRelativeScoreTime\]

</td><td>

Option to display the time of the last update relative to the current time. Available when **Show score update time** is on.

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
</table>### User Analytics Experience data properties

These properties configure how Usage Insights data is presented on Single Score visualizations.

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

Date range options for Usage Insights data sources

</td></tr><tr><td>

Show data for selected period as \[scoreType\]

</td><td id="entry_show-data-period-as">

Available when **Apply date range** is selected.The indicator aggregation logic for how scores from the selected period are shown, such as Latest score, Sum, or Average.

</td></tr><tr><td>

Show maximum range \[showMaximumRange\]

</td><td id="entry_show-max-range">

Option to show the maximum range of available dates.

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

Additional settings—User Experience Analytics data sources

</td></tr><tr><td>

Show metric label \[showMetricLabel\]

</td><td id="entry_show-metric-label">

Option to show the metric label. In donut charts, the value is not shown if it can't fit the donut.

</td></tr><tr><td>

Show 0 when no data is available \[showZero\]

</td><td id="entry_show-0">

When toggled on, shows empty \(NULL\) values as zero \(0\). True by default. When true, you can't set a custom message when there is no data.

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
</table>### Health Log Analytics data properties

These properties configure how Health Log Analytics data is presented on single score visualizations.

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

Opens the formatting values dialog. See the Formatting properties table.

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

These properties apply to Single Score visualizations for all data sources. Access them through the **Format values** link under Metric.

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

</td></tr><tr><td>

Show original number in tooltips \[numberInTooltipsEnabled\]

</td><td id="entry_show-orig-number-tooltip">

Option to include a tooltip to show the unformatted number when pointed to. **Note:** Only available when **Use custom formatting** and **Enable abbreviation** are true.

</td></tr></tbody>
</table>## Single Score visualization component events

Select event handlers to configure the actions \(events\) provided with the Single score component.

The Events tab shows the events used by the Single score component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Single score actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

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

-   PayloadBreakdown - Breakdowns represented as a json object.

Payload type: `{sysId: string, elements: Array.<string>}`

-   PayloadParams – Parameters of the clicked visualization.

Payload type: `{table: string, query: string, indicatorSysid: string, breakdowns: Array.<PayloadBreakdown>, domain: string, aggregate: string, scoreDate: string}`

-   PayloadData - Payload from the data point \(timestamp, element name, value, color, cssColor\) is dispatched when clicking a visualization. For example, clicking on a data point in a timeseries chart passes the timestamp and value in the payload.

Payload type: `{change: string, elements: Array.<string>, value: string, color: string, cssColor: string}`


</td></tr></tbody>
</table>