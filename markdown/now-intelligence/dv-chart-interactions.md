---
title: Chart interactions in a data visualization
description: You can set what occurs when a user interacts with a chart, such as by selecting a bar column. Possibilities include navigating to a URL, opening another data visualization, and filtering all visualizations on the dashboard by the selected value.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-03-25"
reading_time_minutes: 4
keywords: [How to filter all visualizations on a dashboard by selected value, How to configure URL navigation in data visualization, drilldown]
breadcrumb: [Platform Analytics]
---

# Chart interactions in a data visualization

You can set what occurs when a user interacts with a chart, such as by selecting a bar column. Possibilities include navigating to a URL, opening another data visualization, and filtering all visualizations on the dashboard by the selected value.

Adding a Drill down to chart interaction to a data visualization 

The configuration panel of a data visualization includes a section labeled Chart interaction. In this section, you set what is called "on-click behavior." This term refers to what happens when a user interacts with a segment of the chart that represents a value. Examples include selecting a point on a time series or a segment of a pie or donut. You can also disable chart interactions for the visualization.

**Important:** You cannot configure chart interactions for data visualizations on technical dashboards or other UI Builder pages. You can turn chart interactions on or off with the **Enable drilldowns** toggle, but you cannot otherwise change them. Instead, you have to configure handlers for on-click events. For information about configuring drilldowns from data visualizations on a technical dashboard, see [Add a drilldown event to a data visualization in a technical dashboard](../../dashboards/task/add-custom-drilldown-event.md).

The following actions are available for a chart interaction:

-   **Go to data view**

    Opens a view of the data appropriate to the data type. For information about the views for each data source, see [Data views for different data sources](../../dashboards/reference/visualization-drilldown-in-config-ws.md).

    **Note:** Go to data view is the default interaction for all supported data sources. User Experience Analytics data is not supported.

-   **Go to URL**

    Opens the URL you specify. This URL can be on the instance or external to it. Where relevant, you can specify the name of the page that is opened in a tooltip. Go to URL is the default interaction for User Experience Analytics data sources.

-   **Apply as filter**

    Filters all applicable data visualizations on the dashboard by the value of the selected segment. Does not apply when the Group by field is a time duration. Available only for Horizontal and Vertical Bar and Pie/Donut visualizations, and only for table and indicator data sources. Not available on UI Builder. For more information, see [Make a data visualization act as a filter](../task/make-dv-act-as-filter.md).

-   **Drill down to chart**

    Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization. You configure this new drill-down visualization seamlessly as part of the process of configuring the chart interaction.

    **Note:** Drill down to chart has the following limitations:

    -   You cannot configure Drill down to chart in the inline dashboard editor, only in the Visualization Designer.
    -   Drill down to chart is available only for table data sources.
    -   You cannot set drill down to chart from the Calendar, Geomap, Indicator scorecard, or List visualizations. However, you can drill down from supported visualizations to any visualization that can display table data.

Different chart interactions support different data sources and data visualization types. The following table shows the matrix of support.

<table id="table_c4f_plr_d1c"><thead><tr><th>

Action

</th><th>

Supported data visualizations

</th><th>

Supported data sources

</th></tr></thead><tbody><tr><td>

Go to data view

</td><td>

All

</td><td>

All that the visualization supports except User Experience Analytics

</td></tr><tr><td>

Go to URL

</td><td>

All except Geomap and Indicator Scorecard

</td><td>

All that the visualization supports

</td></tr><tr><td>

Apply as filter \(Available only in inline dashboard editor\)

</td><td>

-   Horizontal and Vertical Bar
-   Pie and Donut

</td><td>

Table and indicator

</td></tr><tr><td>

Drill down to chart \(Available only in Visualization Designer\)

</td><td>

All except Calendar, Indicator scorecard, List, and Geomap

</td><td>

Table

</td></tr></tbody>
</table>-   **[Configure chart interactions](../../reporting/task/configure-go-data.md)**  
Select what happens when a viewer interacts with a section of the chart for a data visualization that you are editing.
-   **[Data views for different data sources](../../dashboards/reference/visualization-drilldown-in-config-ws.md)**  
When the chart interaction for a data visualization is set to Go to data, interacting with a data value on the chart opens different pages depending on the data source.

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

