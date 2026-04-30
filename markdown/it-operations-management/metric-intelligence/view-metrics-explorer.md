---
title: View metric values in the Insights Explorer
description: Metric Intelligence calculates statistics for CI metric data. Insights Explorer displays these metric values as metric charts for the CIs in the CMDB. Insights Explorer lets you overlap any metrics for any CIs in a single chart to create a multi-layered view of metric values across a time range.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# View metric values in the Insights Explorer

Metric Intelligence calculates statistics for CI metric data. Insights Explorer displays these metric values as metric charts for the CIs in the CMDB. Insights Explorer lets you overlap any metrics for any CIs in a single chart to create a multi-layered view of metric values across a time range.

## Before you begin

Role required: evt\_mgmt\_user

## About this task

The Insights Explorer provides a canvas to which you can drag various metrics for CIs and create charts. You can place a single metric on the canvas, for an individual metric for a CI. For a more comprehensive chart, you can layer several metrics for a single CI or for different CIs to create a multi-metric chart. In such layered chart, each metric is distinguished by a unique color, which lets you compare metric values across CIs within a specific time range.

Insights Explorer displays metric boundaries according to the most recently configured model. Therefore, legacy anomalies from a previous build may still appear as anomalies, even though according to the current boundaries, the alert does not qualify as an anomaly.

You can also access the Insights Explorer from the following maps:

-   View metrics in a Dependency Views map
-   [View metrics from a business service map](t_EMViewDashboard.md)

![Dashboard for Metric Intelligence metrics, where you can display charts for selected CI metrics.](../image/InsightsExplorerLondon.png "Insights Explorer")

If the host name of the CI is available, it appears underneath the CI name. Host name is populated by retrieving the node information from the generated binding event as part of metric binding.

To navigate to a CI for which to display metrics:

-   Use Hottest Configuration Items \(![Hottest Configuration Items icon.](../image/hottest-config-items.png)\) to quickly access the 10 most anomalous CIs.
-   Use Configuration Items \(![Use Configuration Items icon.](../image/pinned-config-items.png)\) to create a separate custom list of any CIs from the CMDB and then add the metrics for these CIs to the canvas.
-   Use Application services \(![Use Application Services icon.](../image/business-service-cis.png)\) to create a custom list of application services that let you drill into the CIs of these services. You can then add metrics for these CIs to the canvas.
-   Use CMDB Groups \(![Use CMDB Groups icon.](../image/cmdb-group-cis.png)\) to create a custom list of CMDB Groups that let you drill into the CIs of these groups. You can then add metrics for these CIs to the canvas.

The following colors, which are based on color settings for alert severities, indicate anomaly severities:

-   **Red**

    Critical severity \(highest severity\).

-   **Orange**

    Major severity.

-   **Yellow**

    Minor severity.

-   **Blue**

    Warning severity \(lowest severity\).

-   **Green**

    Informational. No severity.


The dots at the upper left on the CI icons indicate general anomaly tracking status:

-   Grey: Metrics are being tracked for the CI, but none of those metrics have ever had an anomaly.
-   Green: Metric for CI had at least one anomaly in the past, but anomaly score is currently 0.
-   Colored: Corresponds to the last recorded severity level according to the configuration of the color band ranges.
-   No dot: There are no metrics for the CI and there is no data to drill into.

    **Note:** **Configuration Items** and **Application Services** are likely to include CIs for which there is no metric data.


Metric Intelligence does not track changes to an anomaly score if it is within the green band range.

As you create charts, a legend for each series chart automatically appears underneath the chart. For a single-metric chart, the legend has entries for the aggregations in the chart. For a multi-metric chart, the legend has entries for the metrics in the chart.

Modifications in the Insights Explorer remain during the session, and once the Insights Explorer is refreshed it returns to its initial state.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Metrics** &gt; **Insights Explorer**.

2.  Click a CI to drill down to its associated list of metrics, ordered by their most recent anomaly scores.

    For each metric, a sparkline displays metric values for the CI for the last hour. Point to the sparkline to display the metric value at each point of time.

    If [resource binding](../concept/resource-binding.md) is enabled, then the list of series being monitored for a CI also contains series that belong to a resource and metric. The naming convention for such series is '&lt;resource name&gt;/&lt;metric name&gt;'. For a series that is only bound to a CI, the naming convention is '&lt;metric name&gt;'.

3.  Drag a metric to the **Drop Metric To Create Chart** area on the canvas and point to the chart to display the exact metric value at each point of time.

    The metric chart displays data for the specified time period, according to the chart settings. By default, raw data is displayed. If the time period is longer than a week or earlier than the last week, then average data is displayed. Drag subsequent metric to the canvas as follows:

    -   In the **Drop Metric To Create Chart** area, so it is displayed individually in a new chart.
    -   Onto an existing chart, in the **Replace Chart** highlighted block to overwrite the existing chart.
    -   Onto an existing chart, in the **Add Metric** highlighted block to overlap it with the existing metrics in the chart.

        When you display multiple metrics in a single chart, the same aggregation selection applies to all the metrics, and statistics settings are not available. For example, if **Average** is selected in the **Chart Settings**, then averaged values are displayed for all the metrics in the chart.

4.  Use the **Search** box to search and filter for specific configuration items, application services, or CMDB groups that are not listed by default.

    In the SEARCH RESULTS section, click the + icon next to an item that you want to add to the ADDED ITEMS section. Or, use advanced search:

    -   Select ![Use Configuration Items icon.](../image/pinned-config-items.png) and then click ![Add CI icon.](../image/AddItem.png) **Add Configuration Item** to add any specific CIs. In the Add Configuration Items dialog box, select a **CI Class Type** such as Linux Server.
    -   Select ![Use Application Services icon.](../image/business-service-cis.png) and then click ![Add Application Service icon.](../image/AddItem.png) **Add Application Service** to add all CIs included in a specified application services. In the Add Application Services dialog box, select `Discovered Service` or `Manual Service` as the **CI Class Type** and then specify filter conditions to narrow down the search.

        **Note:** You can add an application services only if its **Operational Status** is ‘operational’.

    -   Select ![Use CMDB Groups icon.](../image/cmdb-group-cis.png) and then click ![Add CMDB Group icon.](../image/AddItem.png) **Add CMDB Group** to add all CIs included in a specified CMDB group. In the CMDB Groups dialog box specify filter conditions such as **\[GroupName\] \[starts with\] \[d\]**, to narrow down the search.
    After selecting the items that you want to add, click **Add**.

5.  Add related CIs:

    1.  Click the **Add related CIs** \(![Add related CIs icon.](../image/Insights-Explorer-Related-Items.png)\) icon next to a CI.

        The Add Related Configuration Items dialog box appears, displaying all relationships in which the selected CI is a parent or a child.

    2.  To further filter the list, you can define specific conditions that must be met.

    3.  Select the relationships from which you want to add the parent or the child CI, whichever is not the selected CI.

    4.  Click **Add**.

    The CIs from the selected relationships, which are not the selected CI, are added to the list of CIs in the Insights Explorer.

6.  Point to a legend item and click its '**X**' icon to remove the corresponding metric from the chart, or to disable the corresponding series from the **Chart Settings**.

7.  Click the cog **Settings** icon to open application settings:

    -   Enable, disable, or set the frequency for refreshing anomaly data on the Insights Explorer.
    -   Activate or deactivate the display of related lists such as All Alerts, Incidents, and Problems. For more information, see [Create or modify map indicators](https://www.servicenow.com/docs/access?context=t_CreateModifyNGBSMMapIndicators&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
8.  Click the **Chart Settings** icon to toggle the display of statistics and aggregations on the chart.

    Enabling or disabling an item to add or to remove metrics from a chart, also updates the legend of the chart to reflect the change.

<table id="table_jxg_vft_zw"><thead><tr><th>

Chart Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Bounds

</td><td>

Displays a computed upper and lower bound for the metric, based on learning of past values. The upper and lower bounds always display together.

</td></tr><tr><td>

Show Anomaly Scores

</td><td>

Displays anomaly scores on a virtual axis of 0-10. Color code is based on the score thresholds that are defined in the Anomaly Score to Event Severity Map \[sa\_metric\_anomaly\_score\_to\_event\_severity\_map\] table.

</td></tr><tr><td>

Average

</td><td>

Displays aggregated average metric values calculated in one hour intervals. Aggregated averages are displayed as follows:

-   For data that is up to 8 days old: Displays 10-minute aggregation windows.
-   For data that is up to 94 days old: Displays 10-minutes aggregation windows.
-   For older data: Displays 1-hour aggregation windows.


</td></tr><tr><td>

Minimum

</td><td>

Displays aggregated minimum metric values calculated per one hour time periods.For data that is up to 8 days old: Displays 10-minute aggregation windows.

</td></tr><tr><td>

Maximum

</td><td>

Displays aggregated maximum metric values calculated for one hour time periods.For data that is up to 8 days old: Displays 10-minute aggregation windows.

</td></tr><tr><td>

Raw

</td><td>

Displays the raw, unaggregated metric values. These values are kept only for the last 8 days.

</td></tr></tbody>
</table>
## What to do next

-   Point to the icon of a CI in the right-hand side bar to display the CI type.
-   Zoom in or out by changing the default **Last Hour** time range selection. Select one of the preset time periods to display anomaly scores for the last **6 Hours** for example, or specify a custom time period for up to 90 days back.

    To zoom in, highlight a section of a chart by pointing to the upper left corner of the section and dragging the mouse device to the lower right corner of the section. The time range of the chart changes accordingly. If there are other charts on the canvas, they are all automatically synchronized to display data for the same time range. The time range in the title bar automatically updates to reflect the new time range.

-   Right-click on a CI in the right-hand side bar and select **View Form** to open its CI form.
-   Click the map icon next to an application service listed in the **Application Services** tab, to open its application service map.
-   Click Remove \(![Remove CI icon.](../image/remove-ci.png)\) next to a CI to remove it from the Insights Explorer.
-   Click the Export icon in a chart to download it as a .png or .svg image, or as a .pdf document.

**Related topics**  


[Create an Insights Explorer view](create-metric-explorer-view.md)

