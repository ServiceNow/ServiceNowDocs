---
title: Pivot Table component setup
description: The Pivot Table is a visualization type within the Data visualization component that lets you create multilevel pivot visualizations. These visualizations help you analyze data across multiple dimensions.Configure the behavior of the Pivot Table data visualization type with these properties.These properties configure how table data is presented on Pivot Table visualizations.These properties configure how indicator data is presented on Pivot Table visualizations.The following properties apply to pivot data visualizations that show Usage Insights data.These properties configure how Health Log Analytics data is presented on Pivot Table visualizations.These properties apply to Pivot Table visualizations for all data sources. Access them through the Format values link under Metric.Select event handlers to configure the actions \(events\) provided with the Pivot Table data visualization type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/pivot-table-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 26
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Pivot Table component setup

The Pivot Table is a visualization type within the Data visualization component that lets you create multilevel pivot visualizations. These visualizations help you analyze data across multiple dimensions.

## Before you begin

This task assumes you have selected the Pivot Table visualization type for the Data visualization component and are ready to configure the chart properties and events. For instructions on accessing and using the UI Builder toolbox, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md). For instructions on overriding styles using the Styles pane, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md).

Role required: ui\_builder\_admin, pa\_admin, or admin

## Procedure

1.  Define a label for your Pivot Table that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-vis-content-tree.png"\] Alt text: Data Visualization component with label displayed in the content tree

2.  Select the visualization, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Data visualization label you created in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  Click **Add data source** to select a table or indicator data source to base the visualization on.

    You can select multiple data sources for a Pivot Table.

4.  Add filters to the data as needed.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Pivot table visualization component properties

Configure the behavior of the Pivot Table data visualization type with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

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
</table>**Note:** Pivot table visualizations support multiple data sources, but all must be of the same type, such as table.

After selecting the data source, configure the appropriate data properties:

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

Freeze row heading \[freezeHeader\]

</td><td>

Allows users to keep header visible while scrolling to another area in the pivot.

</td></tr><tr><td>

Freeze row footer \[freezeFooter\]

</td><td>

Allows users to keep footer visible while scrolling to another area in the pivot.

</td></tr><tr><td>

Freeze first column \[freezeFirstColumn\]

</td><td>

Allows users to keep the first column visible while scrolling.

</td></tr><tr><td>

Show alternative row colors \[showAlternateRowColors\]

</td><td>

Toggle on to display background color for alternating rows. This can make reading the pivot data easier.

</td></tr><tr><td>

Show alternative column colors \[showAlternateColumnColors\]

</td><td>

Toggle on to display background color for alternating columns. This can make reading the pivot data easier.

</td></tr><tr><td>

Display row lines \[showRowDividers\]

</td><td>

Displays border row lines to show separate rows.

</td></tr><tr><td>

Display column lines \[showColumnDividers\]

</td><td>

Displays border column lines to show separate columns.

</td></tr><tr><td class="sub-head" colspan="2">

Table size settings

</td></tr><tr><td>

Truncate first column \[truncateFirstColumn\]

</td><td>

When true, limits the width of the first column. First column contents beyond this width are truncated. First column headers are not truncated. Specify this width limit in **firstColumnMaxWidth**.

</td></tr><tr><td>

First Column max width, in px \[firstColumnMaxWidth\]

</td><td>

The maximum width of the first column, beyond which its contents are truncated. This maximum width cannot be less than the width of the first column header, which is never truncated. Values lower than the header width are ignored.Only takes effect when **truncateFirstColumn** is true. Default value is 200px.

</td></tr><tr><td>

Wrap column headers \[wrapColumnHeader\]

</td><td>

Breaks header text into lines matching content width, with a minimum limit of 100px. Does not apply to first column.**wrapColumnHeader** and **truncateColumnHeader** cannot both be true.

</td></tr><tr><td>

Truncate column headers \[truncateColumnHeader\]

</td><td>

Truncates header text into lines matching content width, with a minimum limit of 100px. Does not apply to first column.**wrapColumnHeader** and **truncateColumnHeader** cannot both be true.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr id="set-color-type"><td>

Set color type \[type\]

</td><td>

Type of color scheme to apply to the component. Options include: -   Default `default`: A color from the UX Theme Properties \[sys\_ux\_theme\_property\] table. The specific colors depend on which theme variant in the UX Themes \[sys\_ux\_theme\] table is applied to the instance.
-   Single color: A single color each for the values and the cell backgrounds.

</td></tr><tr><td>

Color \[color\]

</td><td id="pivot-color-values">

Color for values in the cells. Select from the hexadecimal codes.

</td></tr><tr><td>

Background color \[backgroundColor\]

</td><td id="pivot-background-color">

Background color for the cells. Select from the hexadecimal codes.

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

</td><td id="pivot-color-rule-met">

Color for values in the cells when the condition is met. Select from the hexadecimal codes.

</td></tr><tr><td>

Background color \[backgroundColor\]

</td><td id="pivot-background-color-rule-met">

Background color for the cells when the condition is met. Select from the hexadecimal codes.

</td></tr><tr><td>

Order \[order\]

</td><td id="entry_color-rule-order">

A numerical value that determines the order in which the rules apply. The system applies rules in the order of smallest to largest.

</td></tr></tbody>
</table>### Table data properties

These properties configure how table data is presented on Pivot Table visualizations.

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

Field for &lt;table&gt; \[groupByField\]

</td><td id="d4736e1008">

The field to group by. You can group by any field in the table including list fields.For example, in a visualization of incident data grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.

**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   If there are multiple metrics, the metric label is appended to the beginning of the group-by field values in the chart labels.
-   Fields with continuous values, such as date or integer, are automatically grouped according to any report ranges defined for the data. For more information, see [Report ranges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_ReportRanges.md).

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Column

</td><td>

Fields whose values are each represented in a vertical column.

</td></tr><tr><td>

Rows \[rowGroupBy\]

</td><td>

List of the specified row group-bys.

</td></tr><tr id="group-by-field"><td>

Field for &lt;table&gt; \[groupByField\]

</td><td id="entry_group-by-field">

The field to group by. Specify one or more values for the column and for each row. If you have multiple table data sources, the column must be a field that is common to all tables. A row group-by can refer to different fields in different tables.**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   Grouping or stacking by Variables or Questions fields is not supported.

</td></tr><tr><td>

Max number of groups \[maxNumberOfGroups\]

</td><td id="entry_max-number-groups">

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the **Other** group. You can show that aggregate with the **Show others** option.By default, you can't show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Show others \[showOthers\]

</td><td id="entry_show-others">

If **Max number of groups** is set and this option is turned on, an aggregate of the groups beyond the maximum number is displayed as the **Other** group.The **Other** element is added automatically when the number of elements exceeds the limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Show row total \[showRowGrandTotal\]

</td><td>

Show the total value of elements in each row.

</td></tr><tr><td>

Show column total \[showColumnGrandTotal\]

</td><td>

Show the total value of elements at the bottom of each column.

</td></tr><tr><td>

Show parent row totals \[showSubTotals\]

</td><td>

For a hierarchy of rows, each parent row shows total of all child rows per column, depending on metric aggregation.

</td></tr><tr><td colspan="2">

**Sorting**

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td>

Criterion for sorting groups or categories

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td>

Order in which to sort groups or categories

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show 0 when no data is available \[showZero\]

</td><td id="entry_show-0-uxa">

When toggled on, shows empty \(NULL\) values as zero \(0\). True by default.

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
</table>### Indicator data properties

These properties configure how indicator data is presented on Pivot Table visualizations.

<table id="table_oqd_rvx_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for Indicator data sources

</td></tr><tr><td>

Time aggregation \[aggregateIndicator\]

</td><td id="entry_metric-time-aggregation">

Time aggregation to apply to the metric, such as 7-day running SUM or By-month AVG. Default is the same as the indicator period. For more information, see [Applying time series aggregations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/applying-time-series-aggregations.md).

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See [Formatting properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/pivot-table-component-uib-setup.md).

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Breakdown \[breakdown\]

</td><td id="entry_group-by-breakdown">

Group indicator scores by a breakdown.**Important:**

-   Scripted breakdowns are not supported in dashboard filters.
-   If there are multiple metrics, the metric label is appended to the beginning of the breakdown element values in the chart labels.
-   Only two levels of breakdown are supported in total, including data visualization and dashboard filters. This limitation does not apply if the indicator has Data snapshots enabled. For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/multi-level-breakdowns.md).

</td></tr><tr><td>

Max number of groups \[maxNumberOfGroups\]

</td><td id="entry_max-number-groups">

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the **Other** group. You can show that aggregate with the **Show others** option.By default, you can't show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td colspan="2">

**Sorting**

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td>

Criterion for sorting groups or categories

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td>

Order in which to sort groups or categories

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show 0 when no data is available \[showZero\]

</td><td id="entry_show-0-uxa">

When toggled on, shows empty \(NULL\) values as zero \(0\). True by default.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

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

The following properties apply to pivot data visualizations that show Usage Insights data.

**Important:** Pivot table visualizations are only suitable for Events data, not Users or Sessions. Only Events have a value to group by.

<table id="table_qgm_svx_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for User Experience Analytics data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See [Formatting properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/pie-donut-component-uib-setup.md).

</td></tr><tr><td class="sub-head" colspan="2">

Group by - Events only

</td></tr><tr><td>

Columns

</td><td>

Properties of the event in a Usage Insights data source, to be shown as vertical columns.

**Note:** Available only for Events metrics, in which case it is mandatory.

</td></tr><tr><td>

Rows

</td><td>

Properties of the event in a Usage Insights data source, to be shown as horizontal rows.

</td></tr><tr><td>

Event property \[eventPropertyValue\]

</td><td>

List of properties to choose from for Usage Insights Event sources that have properties. This option applies only to Events metrics.

</td></tr><tr><td>

Show row total \[showRowGrandTotal\]

</td><td>

Show the total value of elements in each row.

</td></tr><tr><td>

Show column total \[showColumnGrandTotal\]

</td><td>

Show the total value of elements at the bottom of each column.

</td></tr><tr><td>

Show parent row totals \[showSubTotals\]

</td><td>

For a hierarchy of rows, each parent row shows total of all child rows per column, depending on metric aggregation.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show 0 when no data is available \[showZero\]

</td><td id="entry_show-0-uxa">

When toggled on, shows empty \(NULL\) values as zero \(0\). True by default.

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

These properties configure how Health Log Analytics data is presented on Pivot Table visualizations.

<table id="table_oqd_rvx_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Metric for All data sources

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Select column \(max 1\)

</td><td>

The field whose values are each represented in a vertical column.Select no more than one column. If you have multiple data sources, select a column common to all of them.

</td></tr><tr><td>

Rows \[rowGroupBy\]

</td><td>

List of the specified row group-bys.

</td></tr><tr id="group-by-field"><td>

Field for &lt;table&gt; \[groupByField\]

</td><td id="entry_group-by-field">

The field to group by. Specify one or more values for the column and for each row. If you have multiple table data sources, the column must be a field that is common to all tables. A row group-by can refer to different fields in different tables.**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   Grouping or stacking by Variables or Questions fields is not supported.

</td></tr><tr><td>

Max number of groups \[maxNumberOfGroups\]

</td><td id="entry_max-number-groups">

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the **Other** group. You can show that aggregate with the **Show others** option.By default, you can't show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Show row total \[showRowGrandTotal\]

</td><td>

Show the total value of elements in each row.

</td></tr><tr><td>

Show column total \[showColumnGrandTotal\]

</td><td>

Show the total value of elements at the bottom of each column.

</td></tr><tr><td>

Show parent row totals \[showSubTotals\]

</td><td>

For a hierarchy of rows, each parent row shows total of all child rows per column, depending on metric aggregation.

</td></tr><tr><td colspan="2">

**Sorting**

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td>

Sort by name or value

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td>

Sort in ascending or descending order Default: descending

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

These properties apply to Pivot Table visualizations for all data sources. Access them through the **Format values** link under Metric.

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
</table>## Pivot table visualization component events

Select event handlers to configure the actions \(events\) provided with the Pivot Table data visualization type.

The Events tab shows the events used by the Pivot Table. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the list actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_msr_kpn_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visualization Clicked

</td><td>

Dispatched when the visualization is clicked.Payload:

-   [ItemSelectedPayload](https://developer.servicenow.com/dev.do#!/reference/now-experience/tokyo/shared-components/now-vis-pie-wrapper/uib-config%23typedefs-ClickEventPayload) – Payload of the action dispatched when the visualization is clicked.

Payload type: `{title: string, type: string, params: PayloadParams, data: PayloadData}`

-   PayloadBreakdown - Breakdowns represented as a json object.

Payload type: `{sysId: string, elements: Array.<string>}`

-   PayloadParams – Parameters of the clicked visualization.

Payload type: `{table: string, query: string, indicatorSysid: string, breakdowns: Array.<PayloadBreakdown>, domain: string, aggregate: string, scoreDate: string}`

-   PayloadData - Payload from the data point \(timestamp, element name, value, color, cssColor\) is dispatched when clicking a visualization. For example, clicking on a data point in a timeseries chart passes the timestamp and value in the payload.

Payload type: `{elements: Array.<string>, groupBy: Array.<string>, value: string, value: string, color: string, cssColor: string}`


</td></tr></tbody>
</table>