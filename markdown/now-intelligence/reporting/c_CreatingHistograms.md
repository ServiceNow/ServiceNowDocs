---
title: Histogram reports
description: Histograms group numbers in a data set into ranges. The data used in a histogram is continuous data. Continuous data is measured whereas discrete data, which is used in bar charts, is counted.Histograms group numbers in a continuous data set into ranges.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Histogram reports

Histograms group numbers in a data set into ranges. The data used in a histogram is continuous data. Continuous data is measured whereas discrete data, which is used in bar charts, is counted.

For example, a histogram can show the pattern of P1 incidents logged over a four-week period after a product release. For the first week after the product was released, P1 incidents are low because users do not really understand the product enough to use it. In the second week, more users start working with the product and P1 issues increased. In the third week, P1 issues increase even more as more users began working with the product. In the fourth week, P1 issues stay the same as the third week. The information suggests that it is not necessary to increase support staff until the third week after a product is released.

**Note:** When accessibility is enabled, this visualization includes a report that screen readers can interpret. For more information, see [Enabling accessibility features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_SetUpSect508ComplianceFeature.md).

![Histogram Report example](../image/histo-report-ex.png "Histogram report")

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a histogram report

Histograms group numbers in a continuous data set into ranges.

### Before you begin

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d172558e171">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d172558e190">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md)

</td></tr><tr><td id="d172558e209">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d172558e234">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/metricbase/metricbase.md).

</td></tr></tbody>
</table>4.  On the **Type** tab, enter **Histogram** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

5.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_yt3_jzb_bx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Measured by

</td><td>

Select a field to report against. The values from this field appear on the X axis of the histogram and determine the width of the bars. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field.

</td></tr></tbody>
</table>6.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

7.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

