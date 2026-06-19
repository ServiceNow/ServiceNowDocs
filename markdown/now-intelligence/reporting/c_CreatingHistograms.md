---
title: Histogram reports
description: Histograms group numbers in a data set into ranges. The data used in a histogram is continuous data. Continuous data is measured whereas discrete data, which is used in bar charts, is counted.Histograms group numbers in a continuous data set into ranges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/reporting/c\_CreatingHistograms.html
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Histogram reports

Histograms group numbers in a data set into ranges. The data used in a histogram is continuous data. Continuous data is measured whereas discrete data, which is used in bar charts, is counted.

For example, a histogram can show the pattern of P1 incidents logged over a four-week period after a product release. For the first week after the product was released, P1 incidents are low because users do not really understand the product enough to use it. In the second week, more users start working with the product and P1 issues increased. In the third week, P1 issues increase even more as more users began working with the product. In the fourth week, P1 issues stay the same as the third week. The information suggests that it is not necessary to increase support staff until the third week after a product is released.

**Note:** When accessibility is enabled, this visualization includes a report that screen readers can interpret. For more information, see Enabling accessibility features.

\[Omitted image "histo-report-ex.png"\] Alt text: Histogram Report example

**Parent Topic:**[Report types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/report-types-creation-details-rd.md)

## Create a histogram report

Histograms group numbers in a continuous data set into ranges.

### Before you begin

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On instances with Unified Analytics enabled, and on new Zurich instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**. For more information, see [Differences between Core UI and Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d49397e238">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/c_ReportSources.md).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d49397e257">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see Retrieving external data using remote tables and scripts

</td></tr><tr><td id="d49397e276">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(\[Omitted image "upload-icon.png"\] Alt text: Upload icon\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d49397e301">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see MetricBase.

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Histogram** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_yt3_jzb_bx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Measured by

</td><td>

Select a field to report against. The values from this field appear on the X axis of the histogram and determine the width of the bars. Select the info icon \(\[Omitted image "icon-info.png"\] Alt text: Info icon\) for a description of the selected field.

</td></tr></tbody>
</table>8.  To limit the information displayed in the report, select the filter icon \(\[Omitted image "List\_FilterIcon.png"\] Alt text: Filter icon\) and specify conditions to filter the report data.

    To learn how to construct conditions, see Condition builder.

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


### What to do next

-   Select the Report info icon \(\[Omitted image "Form\_ReferenceLookupIcon.png"\] Alt text: Info icon\) and add a description of the report.
-   Select the sharing icon \(\[Omitted image "ShareIcon.png"\] Alt text: Sharing icon\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

