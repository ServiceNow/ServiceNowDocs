---
title: Time series data visualization example
description: Time series visualizations show the changes in data over time. This example starts with a single indicator data source and adds more complexity.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 5
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Time series data visualization example

Time series visualizations show the changes in data over time. This example starts with a single indicator data source and adds more complexity.

In this example you start wanting to show the change in the number of open incidents over time. Then you want to show the trend, and then the number of open incidents broken down by priority. Finally you want to compare the number of open incidents against the number of new incidents.

1.  First you search for **Data Visualizations** in the Unified Navigation and select **Create data visualization**
2.  In the empty new data visualization, you select **Add data source**.

    ![The Add Data Source button in the middle of a new data visualization.](../image/ts-add-data-source.png)

3.  You want to use the indicator Number of open incidents. Fortunately, this indicator has been used before and is listed under the Suggested data sources, saving you the trouble of searching for it. You can tell that Number of open incidents is an indicator data source because of the little column-and-trend icon next to it.

    ![The Number of Open Incidents indicator in the Add Data Source modal.](../image/ts-select-indicator.png)

4.  You return to the visualization and see that the Line type has been selected by default. Line is the most common type of time series, and a time series is the usual visualization for an indicator. You also have an open Configuration panel for this data visualization, next to the line visualization. The visualization changes in real time as you configure it.

    ![The new line visualization for the Number of open incidents.](../image/ts-new-line-chart.png)

5.  The data presentation doesn't look so great, because you only created the indicator on January 11. Fortunately, the Configuration panel has a Date range section where you can trim the dates that are shown. In this case, you select **Show maximum range**, and it shows all the dates for which there are data, but only those dates.

    ![Setting the date range.](../image/ts-set-date-range.png)

6.  You would also like to see what more information you can give about this data, so you expand the **Additional settings** section. For indicators, these settings are the same as the KPI Details chart options. For more information, see [Chart options in KPI Details](../reference/chart-options.md) under the KPI Details documentation. If you have the necessary roles, you can set [targets](../../performance-analytics/concept/performance-analytics-glossary.md#) and [thresholds](../../performance-analytics/concept/performance-analytics-glossary.md#) for an indicator in KPI Details.

    ![Additional settings for a time series with a single data source and no Group By value.](../image/ts-additional-settings.png)

7.  You decide to show the data trend, to give the viewer an idea of where the indicators were heading before the Christmas break.

    ![Line visualization showing trend.](../image/ts-line-trend.png)

8.  Now you have a new task, which is to duplicate this data visualization but split up the number of incidents into groups according to their priority. You group data on a time series visualization in the **Group by** section of the Configuration panel. So you expand that section and discover that there is already a Priority breakdown for the Number of open incidents indicator. You select that breakdown.

    ![Setting the indicator scores to be grouped by Priority.](../image/ts-group-by-priority.png)

9.  You get a separate line for every **Group by** value. Here you see that you can no longer show the trend. If you expand the **Additional settings** section in the Configuration panel again, you see that no extra information besides the forecast can be shown now that you have set a **Group by** value.

    ![Line visualization with Group by values.](../image/ts-line-chart-priority.png)

10. Now you have an additional requirement, which is to display the Number of new incidents indicator in the same visualization, for comparison. To show this indicator, you expand the **Data** section in the Configuration panel and select **+ Add data source** under Data sources.

    ![Adding an additional data source.](../image/ts-add-extra-data-source.png)

11. Then you search for the Number of new incidents indicator and add it.

    ![Selecting the Number of new incidents indicator.](../image/ts-add-2nd-indicator.png)

    The result is a new line in your visualization for the Number of new incidents.

    ![Line visualization with 2 data sources, one of which is broken down by group.](../image/ts-line-chart-2-sources.png)

12. You find this difficult to read and aren't sure that this is the best visualization to use. After reading [Use cases for different time series visualization types](../../reporting/reference/time-series-visualization-types.md), you decide to change the visualization to a column display.

    ![Changing visualization type to column.](../image/ts-change-type-column.png)

13. This is certainly an improvement, but you think you could do better still.

    ![Column visualization with two data sources.](../image/ts-column-2-sources.png)

14. Fortunately, you can set different visualization types for different metrics. You go to the Metrics tiles and expand the menu under the visualization type icon for Number of new incidents. Here you choose the Line visualization again. You can only do this if you have more than one metric.

    ![Selecting visualization type for a second metric.](../image/ts-change-chart-2-metrics.png)

15. You also have the option to set different Y-axes for Number of open incidents and Number of new incidents, through the More options menu on each Metric tile. However, the scales for the two data sources are not different enough for this to help.

    ![Option to add a second Y axis for the Number of new incidents.](../image/ts-add-y-axis.png)

16. The visualization is still a little busy, but a viewer can point their cursor to a column and see the breakdown of scores for that date.

    ![Data details on a selected column](../image/ts-column-details.png)

17. The last thing you do is to make the legends more readable. Right now the entries are truncated before a viewer could see what each priority actually is. So you try expanding the legend item width to 300px.

    ![Expanded visualization legend item width.](../image/ts-widen-legend.png)

18. That's it! You save the visualization, which is ready for you to add to dashboards. If you have the right roles, you can save the visualization in the Data Visualizations library for other dashboard designers to use.

    ![Option to add a saved data visualization to a dashboard from the Visualization Designer.](../image/ts-add-to-dashboard.png)

    ![Your new data visualization on a dashboard.](../image/ts-on-dashboard.png)


**Parent Topic:**[Create time series data visualizations](../../reporting/task/create-dv-time-series-ac.md)

