---
title: Bar visualization component setup
description: Present data as vertical or horizontal bars or Pareto charts. In general, use horizontal bars to graph nominal data, use vertical bars to graph ordinal data, and use Pareto bars to show the most important dimensions of complex data. Bars are a type of Data visualization component.Configure the data and presentation of bar visualizations with these properties.The following properties apply to bar data visualizations that show table data.The following properties apply to Bar data visualizations that show indicator data.The following properties apply to Bar data visualizations that show Usage Insights data.These properties configure how Health Log Analytics data is presented on bar visualizations.Select event handlers to configure the actions \(events\) provided with the Data visualization component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/bar-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 40
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Bar visualization component setup

Present data as vertical or horizontal bars or Pareto charts. In general, use horizontal bars to graph nominal data, use vertical bars to graph ordinal data, and use Pareto bars to show the most important dimensions of complex data. Bars are a type of Data visualization component.

## Before you begin

This task assumes you have placed the Data visualization on the stage and are ready to configure the Bar visualization properties and events. For instructions on accessing and using the UI Builder toolbox, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

Role required: admin or ui\_builder\_admin.

## Procedure

1.  Define a label for your Data visualization that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-vis-content-tree.png"\] Alt text: Data visualization component with label displayed in the content tree

2.  Select the Bar visualization, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Data visualization label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

3.  Select the Horizontal, Vertical Bar, or Pareto Bar **Data Visualization Type**.

    The available data sources and properties change depending on the selected chart type.

    **Note:** Pareto bar visualizations only accept one data source, one metric and one groupby. You cannot select **Sort by**since Pareto bar visualizations default by descending.

4.  Click **Add data source** to select a data source to base a visualization on.

5.  Add filters to the data as needed.

6.  Click **Add this source** to add your selected data source.

7.  Enter static input in the input fields by typing in the content or selecting it from a drop-down list.

    See the sections on each Data visualization type to see configurations options available based on the selected data source.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Bar visualization component properties

Configure the data and presentation of bar visualizations with these properties.

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
</table><table id="table_c3v_mxv_yqb"><thead><tr><th>

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
</table>**Note:** Bar visualizations support multiple data sources, but they must all be the same type, such as table.

After selecting the data source, configure the appropriate data properties:

-   Table data properties
-   Indicator data properties
-   Usage Insights data properties
-   Health Log Analytics data properties

To find the tables for each of these properties, search for each table title on this page in your browser search function.

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
</table><table id="table_qff_hb2_grb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Display settings**

</td></tr><tr><td>

Height \[height\]

</td><td id="entry_height">

The height of the chart.

</td></tr><tr><td>

Show only one data point in tooltip \[showClosestSeriesOnHover\]

</td><td id="entry_show-only-one-tooltip">

When turned on, the tooltip shows only the data point being hovered over. When turned off, the tooltip shows all data points.Default: Off, except when zoom is 400%, which automatically turns it on.

</td></tr><tr><td>

Show data table \[showDataTable\]

</td><td id="entry_show-data-table">

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td class="sub-head" colspan="2">

**Chart variation**

</td></tr><tr><td>

Chart variation \[chartVariation\]

</td><td id="entry_chart-variation">

Style of bars. Options include:-   Stacked `stacked`: Group by fields are stacked on top of each other.
-   Side-by-side `grouped`: Group by fields are side-by-side.
-   Normalized `normalized`: Group by fields are stacked and stretched to fill the chart.

This property applies only when more than one **Group by** is applied.

</td></tr><tr><td class="sub-head" colspan="2">

**Y axis**

</td></tr><tr><td>

Show grid \[bar: showYGrid\] \[time series: yAxisShowGrid\]

</td><td id="entry_show-grid">

Adds grid lines to the chart.

</td></tr><tr><td>

Hide y axis \[yAxisHidden\]

</td><td id="entry_hide-axis">

Option to hide the vertical axis.If you have the latest Data Visualizations application from the ServiceNow Store, you can hide the y-axis on any bar chart. Otherwise, you can't hide it on horizontal bar charts.

</td></tr><tr><td>

Axis title \[yAxisTitle\]

</td><td id="entry_axis-title">

Title to display on the vertical axis of the visualization.

</td></tr><tr><td>

Axis range - from \[yAxisFrom\]

</td><td id="entry_axis-range-from">

Starting point for the range of values for the vertical axis of the visualization.This property applies only to vertical bar charts.

</td></tr><tr><td>

Axis range - to \[yAxisTo\]

</td><td id="entry_axis-range-to">

End point for the range of values for the vertical axis of the visualization.This property applies only to vertical bar charts.

</td></tr><tr><td>

Axis style \[yAxisStyle\]

</td><td id="entry_axis-style">

Style of the Y axis. -   Clean `clean`: Adds a straight line to the Y axis.
-   No tick lines `noTicks`: Option to remove all marks from the Y axis.
-   Standard `default`: Adds a line and tick marks to the Y axis.

</td></tr><tr><td>

Wrap labels \[yAxisWrapLabels\]

</td><td id="entry_wrap-labels">

Wraps long labels in the vertical axis. This property applies to the Y axis only to horizontal and Pareto bar charts.

</td></tr><tr><td>

Max label size, px \[yAxisMaxLabelSize\]

</td><td id="entry_max-label-size">

Maximum label size for the vertical axis, in pixels. This property applies to the Y axis only to horizontal and Pareto bar charts.

</td></tr><tr><td>

Truncation type \[yAxisTruncationType\]

</td><td id="entry_truncation-type">

Determines where to truncate long labels. Options include:-   Start `start`
-   Middle `middle`
-   End `end`

This property applies only to the Y axis and only on horizontal bar charts.

</td></tr><tr><td class="sub-head" colspan="2">

**X axis**

</td></tr><tr><td>

X axis title \[xAxisTitle\]

</td><td id="entry_x-axis-title">

Title to display on the horizontal axis of the visualization.

</td></tr><tr><td>

Hide axis \[xAxisHidden\]

</td><td id="entry_hide-y-axis">

Option to hide the horizontal axis. If you have the latest Data Visualizations application from the ServiceNow Store, you can hide the x-axis on horizontal or vertical bar charts. Otherwise, you can't hide it on horizontal bar charts.

</td></tr><tr><td>

Axis range - from \[xAxisFrom\]

</td><td id="entry_x-axis-from">

Starting point for the range of values for the horizontal axis of the visualization.This property applies only to horizontal bar charts.

</td></tr><tr><td>

Axis range - to \[xAxisTo\]

</td><td id="entry_x-axis-to">

End point for the range of values for the horizontal axis of the visualization.This property applies only to horizontal bar charts.

</td></tr><tr><td>

Axis position \[xAxisPosition\]

</td><td id="entry_x-axis-position">

Where to position the horizontal axis. Options include:-   Top `top`
-   Bottom `bottom`

 This property applies only to horizontal bar charts.

</td></tr><tr><td>

Axis style \[xAxisStyle\]

</td><td id="entry_x-axis-style">

Style of the X axis. Options include:-   Clean `clean`: Adds a straight line to the X axis.
-   No tick lines `noTicks`: Option to remove all marks from the X axis.
-   Standard `default`: Adds a line and tick marks to the X axis.

 This property applies only when **Show grid** is true.

</td></tr><tr><td>

Wrap labels \[xAxisWrapLabels\]

</td><td id="entry_wrap-x-labels">

Wraps long labels in the horizontal axis.This property applies only to vertical and Pareto bar charts.

</td></tr><tr><td>

Max label size, px \[xAxisMaxLabelSize\]

</td><td id="entry_max-x-label-size">

Maximum label size for the horizontal axis, in pixels.This property applies only to vertical and Pareto bar charts.

</td></tr><tr><td>

Truncation type \[xAxisTruncationType\]

</td><td id="entry_x-truncation-type">

Determines where to truncate long labels. Options include:-   Start `start`
-   Middle `middle`
-   End `end`

</td></tr><tr><td class="sub-head" colspan="2">

**Legend**

</td></tr><tr><td>

Show legend \[showRegister\]

</td><td id="entry_show-legend">

Option to display the legend. Activated automatically at 400% zoom.

</td></tr><tr><td>

Show legend value \[showRegisterValue\]

</td><td id="entry_show-legend-value">

Option to display the value corresponding to the area of the chart you hover on. The value displays as a tooltip and in the chart legend.

</td></tr><tr><td>

Legend position \[registerPosition\]

</td><td id="entry_legend-position">

Legend location relative to the chart: Above, Below, Right, or Left

</td></tr><tr><td class="sub-head" colspan="2">

Data label

</td></tr><tr><td>

Show data labels \[showDataLabels\]

</td><td id="entry_show-data-labels">

Option to display the score for each data point.

</td></tr><tr><td>

Data label position \[dataLabelPosition\]

</td><td id="entry_data-label-position">

Location of data labels: at the top, middle, or bottom of the bars.**Note:** Only available when **Show data labels** is true.

</td></tr><tr><td>

Show overlapping labels \[showOverlappingLabels\]

</td><td id="entry_show-overlapping-labels">

Option to display values that overlap.**Note:** Only available when **Show data labels** is true.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr id="set-color-type"><td>

Set color type \[type\]For Pareto bar charts, only Default and Single color are available.

</td><td>

Type of color scheme to apply to the component. Options include: -   Default `default`: A color from the UX Theme Properties \[sys\_ux\_theme\_property\] table. The specific colors depend on which theme variant in the UX Themes \[sys\_ux\_theme\] table is applied to the instance.
-   Color palette `palette`: List of color palettes to select from predefined system palettes in the Chart Color Scheme \[pa\_chart\_color\_schemes\] table. For grouped or stacked data, the colors apply in order from highest value to lowest. For multiple data sources, palette colors apply in the order of data sources. For example, the first color of a palette applies to the first data source, and the second palette color applies to the second source. All visualizations that use the same color palette show the same colors, regardless of what data they display.
-   Single color/Colors per metric `singleColor`: Select a single color in the **Set value color** field. You can select the color from a set of icons, from a list of colors including their icons, or by searching for the color name or hexadecimal value. The colors are taken from the Color Definition \[sys\_report\_color\] table.

If the visualization has more than one metric, you see the Colors per metric option instead. This option lets you select a single color \[singleColor\] for each metric.

-   Fixed element color `chartColor`: Use a specific color from the Chart Colors table \[sys\_report\_chart\_color\] for each element. All data visualizations that use fixed element colors show the same element, such as critical incidents in the Global scope, in the same color. This option is available if a maximum of one data source or metric is added, and a Group by is defined.

</td></tr><tr><td>

Palette \[palette\]

</td><td id="entry_palette">

Color palette to apply to the component. **Note:** Only available when **Set color type** is **Color palette**.

</td></tr><tr><td>

Color \[color\]

</td><td id="entry_single-color">

Single color to apply to the component. **Note:** Only available when **Set color type** is **Single color**.

</td></tr></tbody>
</table>### Table data properties

The following properties apply to bar data visualizations that show table data.

<table id="table_data-props-table"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

MetricYou can add multiple metrics.

If you have multiple metrics, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-multi-metrics.md).

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

Opens the formatting values dialog. See the Formatting Properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Field for &lt;table&gt; \[groupByField\]

</td><td id="entry_group-by-field">

The field to group by. You can group by any field in the table including list fields.For example, in a visualization of incident data grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.

**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   If there are multiple metrics, the metric label is appended to the beginning of the group-by field values in the chart labels.
-   Fields with continuous values, such as date or integer, are automatically grouped according to any report ranges defined for the data. For more information, see [Report ranges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_ReportRanges.md).

</td></tr><tr><td>

Max number of groups \[maxNumberOfGroups\]

</td><td id="entry_max-number-groups">

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the **Other** group. You can show that aggregate with the **Show others** option.By default, you can't show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Show others \[showOthers\]

</td><td id="entry_show-others">

If **Max number of groups** is set and this option is turned on, an aggregate of the groups beyond the maximum number is displayed as the **Other** group.The **Other** element is added automatically when the number of elements exceeds the limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Hide elements with values of 0 \[hideZeroValues\]

</td><td id="entry_hide-0-values">

When toggled on, elements with a value of NULL or 0, such as rows or data points, aren't displayed. This control is not available when the metric is COUNT.

</td></tr><tr><td>

Add alternative group by \[additionalGroupByConfig\]

</td><td>

A JSON array of name/label pairs of items to group by. Item type depends on data source. In runtime, the viewer of the data visualization has the ability to select which of these objects to group by or stack by. The viewer toggles the visibility of the group by item selector in the visualization's More actions menu.**Important:**

-   Alternative group-bys support only up to three metrics on one visualization.
-   Alternative group-by does not support data binding on the data source

</td></tr><tr><td>

Selector visible by default \[showAdditionalGroupBySelector\]

</td><td>

When turned on, the viewer sees the alternative group by item selector by default. In any case, the viewer toggles the selector visibility in the More actions menu. This property only takes effect if at least one alternative group by item has been added.

 Default: false

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td id="entry_sort-by">

Sorting options of the main and alternative groups set in **Group by**. Options include:-   Name: Sorts the values alphabetically by field or element name.
-   Value: Sorts the values numerically or by count.
-   Element order: Sorts the groups according to the value of the Sequence field. Available when grouping by records on the Choice \[sys\_choice\] table, either directly or through a breakdown.
-   Group bucket: Sorts the elements by bucket group, when applicable. Only available for indicator data sources and when the breakdown used for the **Group by** is based on a bucket group.
-   Report range: Sorts the table field values by range. Only available for table data sources and when the table field used for the **Group by** has a report range associated with it.

**Note:**

-   The choices of what to sort by are based on the main, default **Group by**, if one is defined. This sorting applies to any alternative group-bys if possible. If the sorting criterion selected for the main group-by can't apply to an alternative group-by, sorting defaults to Value. For example, sorting by Element order when the alternative group-by is not on the Choice table.
-   If no main **Group by** has been set, but alternative group-bys are defined, you can sort only by Name or Value.
-   Sorting is not available for Pareto bar visualizations. Pareto charts are always sorted by value in descending order.

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td id="entry_sort-by-order">

The direction of the group-by sorting. Options include:-   Ascending `asc`
-   Descending `desc`

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Follow filter per metric \[filterPerMetric\]

</td><td id="entry_filter-per-metric">

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on. For more information, see [Following filters per metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-bars-multi-metrics.md).

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Drill down label \[drilldownLabel\]

</td><td>

Text visible at the tooltip to help user understand what will happen on click.

</td></tr><tr><td>

Show selected data point \[enableClickAndStay\]

</td><td>

When enabled, the data point that has been selected is shown visually. Enables configuring an event handler associated with the data point such as acting as filter.

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

The following properties apply to Bar data visualizations that show indicator data.

<table id="table_oqd_rvx_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

MetricYou can add multiple metrics.

If you have multiple metrics, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-multi-metrics.md).

</td></tr><tr><td>

Time aggregation \[aggregateIndicator\]

</td><td id="entry_metric-time-aggregation">

Time aggregation to apply to the metric, such as 7-day running SUM or By-month AVG. Default is the same as the indicator period. For more information, see [Applying time series aggregations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/applying-time-series-aggregations.md).

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting Properties table.

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

</td></tr><tr><td>

Add alternative group by \[additionalGroupByConfig\]

</td><td>

A JSON array of name/label pairs of items to group by. Item type depends on data source. In runtime, the viewer of the data visualization has the ability to select which of these objects to group by or stack by. The viewer toggles the visibility of the group by item selector in the visualization's More actions menu.**Important:**

-   Alternative group-bys support only up to three metrics on one visualization.
-   Alternative group-by does not support data binding on the data source

</td></tr><tr><td>

Selector visible by default \[showAdditionalGroupBySelector\]

</td><td>

When turned on, the viewer sees the alternative group by item selector by default. In any case, the viewer toggles the selector visibility in the More actions menu. This property only takes effect if at least one alternative group by item has been added.

 Default: false

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td id="entry_sort-by">

Sorting options of the main and alternative groups set in **Group by**. Options include:-   Name: Sorts the values alphabetically by field or element name.
-   Value: Sorts the values numerically or by count.
-   Element order: Sorts the groups according to the value of the Sequence field. Available when grouping by records on the Choice \[sys\_choice\] table, either directly or through a breakdown.
-   Group bucket: Sorts the elements by bucket group, when applicable. Only available for indicator data sources and when the breakdown used for the **Group by** is based on a bucket group.
-   Report range: Sorts the table field values by range. Only available for table data sources and when the table field used for the **Group by** has a report range associated with it.

**Note:**

-   The choices of what to sort by are based on the main, default **Group by**, if one is defined. This sorting applies to any alternative group-bys if possible. If the sorting criterion selected for the main group-by can't apply to an alternative group-by, sorting defaults to Value. For example, sorting by Element order when the alternative group-by is not on the Choice table.
-   If no main **Group by** has been set, but alternative group-bys are defined, you can sort only by Name or Value.
-   Sorting is not available for Pareto bar visualizations. Pareto charts are always sorted by value in descending order.

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td id="entry_sort-by-order">

The direction of the group-by sorting. Options include:-   Ascending `asc`
-   Descending `desc`

</td></tr><tr><td class="sub-head" colspan="2">

Date range

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

Follow filter per metric \[filterPerMetric\]

</td><td id="entry_filter-per-metric">

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on. For more information, see [Following filters per metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-bars-multi-metrics.md).

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Drill down label \[drilldownLabel\]

</td><td>

Text visible at the tooltip to help user understand what will happen on click.

</td></tr><tr><td>

Show selected data point \[enableClickAndStay\]

</td><td>

When enabled, the data point that has been selected is shown visually. Enables configuring an event handler associated with the data point such as acting as filter.

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

The following properties apply to Bar data visualizations that show Usage Insights data.

**Important:** Bar visualizations are only suitable for Events data, not Users or Sessions. Only Events have a value to group by.

<table id="table_qgm_svx_k5b"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

MetricYou can add multiple metrics.

If you have multiple metrics, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-multi-metrics.md).

</td></tr><tr><td>

Label \[label\]

</td><td id="entry_label">

Label of the metric. By default it is the same as the name of the data source.**Note:** If you have multiple metrics on the same data source, consider giving them custom labels. If you are defining group-by fields or breakdowns, this is particularly important. Chart labels in this case show both the metric label and the group-by value, so the metrics need different labels.

</td></tr><tr><td>

Format values

</td><td>

Opens the formatting values dialog. See the Formatting Properties table.

</td></tr><tr><td class="sub-head" colspan="2">

Group by - Events only

</td></tr><tr><td>

Event property \[eventPropertyValue\]

</td><td>

List of properties to choose from for Usage Insights Event sources that have properties.

 This property applies only to Events metrics, in which case it is mandatory.

</td></tr><tr><td>

Add alternative group by \[additionalGroupByConfig\]

</td><td>

A JSON array of name/label pairs of items to group by. Item type depends on data source. In runtime, the viewer of the data visualization has the ability to select which of these objects to group by or stack by. The viewer toggles the visibility of the group by item selector in the visualization's More actions menu.**Important:**

-   Alternative group-bys support only up to three metrics on one visualization.
-   Alternative group-by does not support data binding on the data source

</td></tr><tr><td>

Selector visible by default \[showAdditionalGroupBySelector\]

</td><td>

When turned on, the viewer sees the alternative group by item selector by default. In any case, the viewer toggles the selector visibility in the More actions menu. This property only takes effect if at least one alternative group by item has been added.

 Default: false

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td id="entry_sort-by">

Sorting options of the main and alternative groups set in **Group by**. Options include:-   Name: Sorts the values alphabetically by field or element name.
-   Value: Sorts the values numerically or by count.
-   Element order: Sorts the groups according to the value of the Sequence field. Available when grouping by records on the Choice \[sys\_choice\] table, either directly or through a breakdown.
-   Group bucket: Sorts the elements by bucket group, when applicable. Only available for indicator data sources and when the breakdown used for the **Group by** is based on a bucket group.
-   Report range: Sorts the table field values by range. Only available for table data sources and when the table field used for the **Group by** has a report range associated with it.

**Note:**

-   The choices of what to sort by are based on the main, default **Group by**, if one is defined. This sorting applies to any alternative group-bys if possible. If the sorting criterion selected for the main group-by can't apply to an alternative group-by, sorting defaults to Value. For example, sorting by Element order when the alternative group-by is not on the Choice table.
-   If no main **Group by** has been set, but alternative group-bys are defined, you can sort only by Name or Value.
-   Sorting is not available for Pareto bar visualizations. Pareto charts are always sorted by value in descending order.

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td id="entry_sort-by-order">

The direction of the group-by sorting. Options include:-   Ascending `asc`
-   Descending `desc`

</td></tr><tr><td class="sub-head" colspan="2">

Date range

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

Data update

</td></tr><tr><td>

Follow filters \[followFilters\]

</td><td id="entry_follow-filters">

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Follow filter per metric \[filterPerMetric\]

</td><td id="entry_filter-per-metric">

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on. For more information, see [Following filters per metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-bars-multi-metrics.md).

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown \[enableDrilldown\]

</td><td id="entry_enable-drilldown">

Option to redirect a user to underlying information when they click a value or section. Destination depends on how event handler is configured or how Chart Interactions are configured on the Visualization Designer or inline dashboard editor. Turn off to prevent redirection.

</td></tr><tr><td>

Drill down label \[drilldownLabel\]

</td><td>

Text visible at the tooltip to help user understand what will happen on click.

</td></tr><tr><td>

Show selected data point \[enableClickAndStay\]

</td><td>

When enabled, the data point that has been selected is shown visually. Enables configuring an event handler associated with the data point such as acting as filter.

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

These properties configure how Health Log Analytics data is presented on bar visualizations.

<table id="table_data-props-indicator"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

MetricYou can add multiple metrics.

If you have multiple metrics, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-multi-metrics.md).

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

Field for grouping

 \[groupByField\]

</td><td>

A selection of Health Log Analytics fields you can group the data by.

</td></tr><tr><td>

Max number of groups \[maxNumberOfGroups\]

</td><td id="entry_max-number-groups">

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the **Other** group. You can show that aggregate with the **Show others** option.By default, you can't show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by \[sortBy\]

</td><td id="entry_sort-by">

Sorting options of the main and alternative groups set in **Group by**. Options include:-   Name: Sorts the values alphabetically by field or element name.
-   Value: Sorts the values numerically or by count.
-   Element order: Sorts the groups according to the value of the Sequence field. Available when grouping by records on the Choice \[sys\_choice\] table, either directly or through a breakdown.
-   Group bucket: Sorts the elements by bucket group, when applicable. Only available for indicator data sources and when the breakdown used for the **Group by** is based on a bucket group.
-   Report range: Sorts the table field values by range. Only available for table data sources and when the table field used for the **Group by** has a report range associated with it.

**Note:**

-   The choices of what to sort by are based on the main, default **Group by**, if one is defined. This sorting applies to any alternative group-bys if possible. If the sorting criterion selected for the main group-by can't apply to an alternative group-by, sorting defaults to Value. For example, sorting by Element order when the alternative group-by is not on the Choice table.
-   If no main **Group by** has been set, but alternative group-bys are defined, you can sort only by Name or Value.
-   Sorting is not available for Pareto bar visualizations. Pareto charts are always sorted by value in descending order.

</td></tr><tr><td>

Sort by order \[sortByOrder\]

</td><td id="entry_sort-by-order">

The direction of the group-by sorting. Options include:-   Ascending `asc`
-   Descending `desc`

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

Follow filter per metric \[filterPerMetric\]

</td><td id="entry_filter-per-metric">

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on. For more information, see [Following filters per metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/chart-options-bars-multi-metrics.md).

</td></tr><tr><td>

Show filter icon \[showFilterIcon\]

</td><td id="entry_show-filter-icon">

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Enable drilldown\[enableDrilldown\]

</td><td>

Enables the viewer to open the Health Log Analytics log viewer by interacting with the chart, such as by clicking on a value.

</td></tr><tr><td>

Drill down label \[drilldownLabel\]

</td><td>

Text visible at the tooltip to help user understand what will happen on click.

</td></tr><tr><td>

Show selected data point \[enableClickAndStay\]

</td><td>

When enabled, the data point that has been selected is shown visually. Enables configuring an event handler associated with the data point such as acting as filter.

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
</table>## Bar visualization component events

Select event handlers to configure the actions \(events\) provided with the Data visualization component.

Event handlers work with data resources to link the list actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers. For information about event handlers, see [event handlers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

<table id="table_msr_kpn_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visualization Clicked

</td><td>

Dispatched when the visualization is clicked.Payload:

-   [ItemSelectedPayload](https://developer.servicenow.com/dev.do#!/reference/now-experience/tokyo/shared-components/now-vis-bar-wrapper/uib-config%23typedefs-ClickEventPayload): Payload of the action dispatched when the visualization is clicked.

Payload type: `{title: string, type: string, params: PayloadParams, data: PayloadData}`

-   PayloadBreakdown: Breakdowns represented as a json object.

Payload type: `{sysId: string, elements: Array.<string>}`

-   PayloadParams: Parameters of the clicked visualization.

Payload type: `{table: string, query: string, indicatorSysid: string, breakdowns: Array.<PayloadBreakdown>, domain: string, aggregate: string, scoreDate: string}`

-   PayloadData - Payload from the data point \(timestamp, element name, value, color, cssColor\) is dispatched when clicking a visualization. For example, clicking on a data point in a timeseries chart passes the timestamp and value in the payload.

Payload type: `{elements: Array.<string>, groupBy: Array.<string>, value: string, value: string, color: string, cssColor: string}`


-   Pareto.ClickEventPayload: `{title: string, type: string, nativeEvent: object, params: Pareto.PayloadParams, data: Pareto.PayloadData}`

-   Pareto.PayloadParams: Parameters of the clicked visualization.

Payload type: `{dataSourceType: string, table: string, query: string, indicatorSysid: string, breakdowns:<Pareto.PayloadBreakdown>, domain: string, aggregate: string, scoreDate: string}`

-   Pareto.PayloadData - Payload data of the clicked area. `{value: string, groupBy: string, elements: string}`

Pareto.PayloadBreakdown - Breakdowns represented as a json object.`{sysId: string,elements: string}`


</td></tr></tbody>
</table>