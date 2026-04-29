---
title: Create Core UI reports from MetricBase time-series data
description: Use the MetricBase application to create time-series reports from MetricBase data.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create Core UI reports from MetricBase time-series data

Use the MetricBase application to create time-series reports from MetricBase data.

## Before you begin

You must have the MetricBase product. To get it, see [Requesting the MetricBase product](https://www.servicenow.com/docs/access?context=request-metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). For more information about MetricBase, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Roles required: report\_admin

## Procedure

1.  Navigate to `sys_reports.list` and select **New**.

2.  On the **Data** tab, enter a report name that reflects the information in the report.

3.  In the **Source type** list, select **MetricBase**.

    **Note:**

    -   The **MetricBase** menu option is available only if you have MetricBase installed on your instance.
    -   The default maximum number of series per data set is 20. You can increase the maximum value up to 100 by configuring the **glide.report.metric\_max\_series** system property. However, due to the 10,000 data points limit, increasing the number of series in a data set results in a smaller number of data points per series.
    -   The total number of data points that can be displayed per series is 10,000 / \(actual number of series in dataset \* number of data sets\). For example:
        -   1 dataset used with 20 series: 10K / \(20\*1\) = 500
        -   2 datasets used with 20 series: 10K / \(20\*2\) = 250
        -   1 dataset used with 100 series: 10K / \(100\*1\) = 100
    -   If the actual number of data points in a series exceeds the limit, the data is resampled.
    ![Create a report with MetricBase source type selected](../image/create-mb-report-source-type.png)

4.  Choose an existing MetricBase table.

5.  Click **Next**.

6.  On the **Type** tab, select the type of report to create and click **Next**.

    Only time series reports are available. For information on specific reports types, see [Report types](../reference/report-types-creation-details-rd.md). To view the updated report, click **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_k4l_khm_hp1"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Report data that you group by any of the applicable fields in the Metrics table.

</td></tr><tr><td>

Metric

</td><td>

Metrics determined in your MetricBase database. Click the plus icon \(**+**\) to add multiple metrics. For each metric, you can set one or more transforms. Click the minus icon \(**-**\) to remove a metric.

</td></tr><tr><td>

Transform

</td><td>

Data is altered.-   Select no transforms to show the raw data in your report.
-   Select one transform.
-   Select multiple transforms to create a transform chain. A transform chain applies a new transform to the results of the previous transform.
For more information, see [MetricBase transforms](../reference/metricbase-transforms.md).

</td></tr><tr><td>

Time range

</td><td>

Period of time that the report covers. Relative values are a number of minutes, hours, days, months, or years from the current time. Absolute ranges enable you to specify the start time and end time of the report.

</td></tr><tr><td>

Display data table

</td><td>

Select this option to show report data in a list below the report. The list appears on dashboards where the report is added.All report visualizations show the report data when the [glide.ui.section508](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US) system property is set to **true**. The glide.ui.section508 property overrides the **Display data table** field.

</td></tr></tbody>
</table>8.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

    See the Style options section of the report that you are creating for more information.

    -   [Area and spline report style options](../concept/c_CreateAreaAndSplineCharts.md#)
    -   [Line report style options](../concept/c_CreateLineCharts.md#)
    -   [Step line report style options](../concept/step-reports.md#)
10. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## Result

The report is created from the MetricBase source. If the report visualization is truncated, a message appears.

## What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

-   **[MetricBase transforms](../reference/metricbase-transforms.md)**  
Transforms enable you to visualize MetricBase data in different ways.

**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

