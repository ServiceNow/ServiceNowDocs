---
title: Single score report
description: Single score reports display a single value that is key to your business. Add single score reports to dashboards and configure them to update in real time.Create a single score chart to display a metric or score that is key to your business. The value updates in real time on a dashboard.Change the look of your single score report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Single score report

Single score reports display a single value that is key to your business. Add single score reports to dashboards and configure them to update in real time.

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

Single score reports which include [dynamic conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_UsingTheDynamicOperator.md) added at the report level will not show real-time updates on dashboards unless manually refreshed, or upon a page refresh. The real-time dashboard widget relies on the record watcher to know when an update has been made in order for the single score widget to auto-refresh. However, dynamic conditions aren't supported as part of the record watcher. See further explanation in [Create a real-time score visualization for a score widget](../../performance-analytics/task/create-real-time-score-widget.md).

![A single score report that has been added to a dashboard](../image/SingleScoreReport.png "Single score report that has been added to a dashboard")

**Note:** This report type cannot be run as a scheduled report.

This data visualization is supported on the mobile platform. For more information see [Single score reports for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-reporting-single-score.md) and [Mobile dashboard preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-dashboard-preview.md).

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a single score report

Create a single score chart to display a metric or score that is key to your business. The value updates in real time on a dashboard.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d233968e281">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d233968e300">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md)

</td></tr><tr><td id="d233968e319">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d233968e344">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/metricbase/metricbase.md).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Single score** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_k3f_gpm_fs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Aggregation

</td><td>

Computational method for aggregating report data. The default is **Count**, which displays the number of records selected.**Note:** A single score chart displays only the aggregate value.

 If you select **Count Distinct**, only unique records are counted. For example, you want to generate a report with a distinct number of users who have one or more of the roles in a given list of roles. Users with more than one role would be counted twice unless you use **Count Distinct**.

 If you select **Average**, **Sum**, or **Count Distinct**, a list of fields from the selected **Table** appears. You may further be able to aggregate on fields from extended tables. See [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#) Select a field to aggregate by from this list. For example, if you select a duration field, such as **Business duration** on the Incident table, the aggregated data is expressed in days, hours, and minutes.

 If you select an integer field, such as the **Priority** field, the data is expressed as a number. You may further be able to aggregate on fields from extended tables. See [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#)

</td></tr><tr><td>

Set Value Formatting

</td><td>

Enables you to configure how to show numerical values in reports, including decimal precision, rounding, minimum and maximum duration units, and abbreviations for duration units. See [Value formatting in reports](../reference/value-formatting-reports.md#).

 **Note:** Decimal precision does not work on currency fields.

</td></tr></tbody>
</table>    **Note:** Currency fields default to two decimal places. With the **Set Value Formatting** option, you can configure decimal precision for 0-4 decimal places.

8.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

10. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can share the report with users and groups, add the report to a dashboard, and publish the report to the web.

## Single score report style options

Change the look of your single score report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Display Zero

</td><td>

Check box to display the number **0** when the value of the report is zero. Clear this check box to display an error message when the value of the cell is 0. Applicable when **Aggregation** is **Count** or **Count Distinct**.

</td></tr><tr><td>

Default color

</td><td>

Color of the score in the chart.

</td></tr><tr><td>

Drilldown view

</td><td>

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See [Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/t_ConfigureTheListLayout.md) . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

</td></tr><tr><td>

Edit coloring rules

</td><td>

Click this hyperlink to configure how values are colored in the report. You can create rules to define which colors are used based on operators and values. For example, you can specify that any value greater than 5 displays in red. See [Create coloring rules for single score reports](../task/single-score-report-coloring-rules.md).

</td></tr><tr><td class="sub-head" colspan="2">

Title

</td></tr><tr><td>

Show chart title

</td><td>

When the chart title is shown for the report.-   **Never**: Never show the chart title.
-   **Report only**: Shows the chart title on reports.
-   **Always**: Shows the chart title on reports, dashboards, and landing pages.

</td></tr><tr><td>

Chart title

</td><td>

The chart title has a maximum length of 40 characters. If no title is entered, the report name is used for the title. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Size of the chart title

</td><td>

Size of the chart title in pixels. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Chart title color

</td><td>

Color of the chart title. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Title horizontal alignment

</td><td>

How the chart title is aligned horizontally. This field is available when the **Custom chart title position** option is cleared.

</td></tr><tr><td>

Title vertical alignment

</td><td>

How the chart title is aligned vertically. This field appears when **Custom chart title position** is cleared.

</td></tr></tbody>
</table>