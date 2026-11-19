---
title: Use cases for different time series visualization types
description: Time series visualizations can emphasize the trend in the data or specific changes in the data. They can show one data source or compare several related data sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/time-series-visualization-types.html
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Use cases for different time series visualization types

Time series visualizations can emphasize the trend in the data or specific changes in the data. They can show one data source or compare several related data sources.

<table id="table_time-series"><thead><tr><th>

Visualization

</th><th>

Description and use case

</th></tr><tr><th colspan="2">

Visualizing trends in the scores of an indicator

</th></tr></thead><tbody><tr><td>

Line\[Omitted image "inline-data-vis-line.png"\] Alt text: line visualization

</td><td>

Shows how one or more values change over time by connecting a series of data points with straight lines. Use a line visualization to emphasize the trend in the data. Consider line visualizations to be the default choice for displaying a time series. If you are unsure of which visualization to use, use a line.

</td></tr><tr><td>

Spline\[Omitted image "inline-data-vis-spline.png"\] Alt text: spline visualization

</td><td>

Shows how one or more values change over time by connecting a series of data points with a fitted curve that emphasizes the trend over individual data points. Spline visualizations let you take a limited set of known data points and approximate intervening values.

</td></tr><tr><td>

Scatter\[Omitted image "inline-data-vis-trend.png"\] Alt text: scatter visualization - med

</td><td>

Shows unconnected points for values in the Y-axis against time in the X-axis. Usually the trend line is also shown. Use with a spread of data that cannot be usefully connected with a line.

</td></tr><tr><td class="sub-head" colspan="2">

Comparing scores in a data source

</td></tr><tr><td>

Column\[Omitted image "inline-data-vis-bar-column.png"\] Alt text: column visualization

</td><td>

Shows changes in data over time by displaying values as proportional vertical columns. Use either to visualize changes in one data source or to compare data sources. To compare data sources with a column visualization, either add data sources to the visualization, or place several column visualizations next to each other in a dashboard.

</td></tr><tr><td>

Step\[Omitted image "inline-data-vis-stepline.png"\] Alt text: Data visualization step line type - med

</td><td>

Emphasizes changes in a data source between discreet points in time. Use to show small incremental changes, especially when a line visualization smudges the data.

</td></tr><tr><td class="sub-head" colspan="2">

Comparing scores or trends between data sources

</td></tr><tr><td>

Area\[Omitted image "inline-data-vis-area.png"\] Alt text: area visualization

</td><td>

Resembles a line visualization, but the area between the axis and line is emphasized with colors. Use with multiple data sources to highlight the relative contribution that each data source makes to the whole.

</td></tr></tbody>
</table>**Parent Topic:**[Create time series data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-dv-time-series-ac.md)

