---
title: Create Core UI reports from MetricBase time-series data
description: Use the MetricBase application to create time-series reports from MetricBase data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/reporting/create-report-with-metricbase-data.html
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

You must have the MetricBase product. To get it, see Requesting the MetricBase product. For more information about MetricBase, see MetricBase.

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

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
    \[Omitted image "create-mb-report-source-type.png"\] Alt text: Create a report with MetricBase source type selected

4.  Choose an existing MetricBase table.

5.  Select **Next**.

6.  On the **Type** tab, select the type of report to create and select **Next**.

    Only time series reports are available. For information on specific reports types, see [Report types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/report-types-creation-details-rd.md). To view the updated report, select **Run**.

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

Metrics determined in your MetricBase database. Select the plus icon \(**+**\) to add multiple metrics. For each metric, you can set one or more transforms. Select the minus icon \(**-**\) to remove a metric.

</td></tr><tr><td>

Transform

</td><td>

Data is altered.-   Select no transforms to show the raw data in your report.
-   Select one transform.
-   Select multiple transforms to create a transform chain. A transform chain applies a new transform to the results of the previous transform.
For more information, see [MetricBase transforms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/metricbase-transforms.md).

</td></tr><tr><td>

Time range

</td><td>

Period of time that the report covers. Relative values are a number of minutes, hours, days, months, or years from the current time. Absolute ranges enable you to specify the start time and end time of the report.

</td></tr><tr><td>

Display data table

</td><td>

Select this option to show report data in a list below the report. The list appears on dashboards where the report is added.All report visualizations show the report data when the glide.ui.section508 system property is set to **true**. The glide.ui.section508 property overrides the **Display data table** field.

</td></tr></tbody>
</table>8.  To limit the information displayed in the report, select the filter icon \(\[Omitted image "List\_FilterIcon.png"\] Alt text: Filter icon\) and specify conditions to filter the report data.

    To learn how to construct conditions, see Condition builder.

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

    See the Style options section of the report that you're creating for more information.

    -   [Area and spline report style options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_CreateAreaAndSplineCharts.md)
    -   [Line report style options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_CreateLineCharts.md)
    -   [Step line report style options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/step-reports.md)
10. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## Result

The report is created from the MetricBase source. If the report visualization is truncated, a message appears.

## What to do next

-   Select the Report info icon \(\[Omitted image "Form\_ReferenceLookupIcon.png"\] Alt text: Info icon\) and add a description of the report.
-   Select the sharing icon \(\[Omitted image "ShareIcon.png"\] Alt text: Sharing icon\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

-   **[MetricBase transforms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/metricbase-transforms.md)**  
Transforms enable you to visualize MetricBase data in different ways.

**Parent Topic:**[Advanced Core UI reporting topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_AdvancedReporting.md)

