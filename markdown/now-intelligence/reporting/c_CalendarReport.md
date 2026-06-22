---
title: Calendar reports
description: Calendar reports display date-driven events on a calendar.Create a calendar report to show and highlight date-driven events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/reporting/c\_CalendarReport.html
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Calendar reports

Calendar reports display date-driven events on a calendar.

**Note:** This topic refers to Reporting in the Core UI. For instances migrated to Platform Analytics experience and new Zurich instances, see [Create a calendar report data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-dv-calendar-ac.md).

\[Omitted image "CalendarReport.png"\] Alt text: Calendar report

You can highlight calendar events by relevant criteria such as priority, status, or escalation. Events that have no end date have a duration of one hour.

## Limitations

-   You can limit the number of events that may be returned when you browse backwards in a calendar visualization. There is a limit of 30 days into the past, starting from the first day in the current Calendar view. Events that start more than 30 days before the first day visible on a calendar are not displayed. If you select **Year**, then the calendar includes events that start between December 1 of the previous year and December 31 of the current year.

    The KB article [Weekly calendar view does not display all entries](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0598360) covers scenarios in which some expected entries do not display.

    To show more or fewer days, edit the **glide.report.calendar.max\_days\_back** property. See [Reporting properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/reporting-properties.md).

    **Note:** Performance may degrade if this value is too large.

-   This report type cannot be run as a scheduled report.
-   Calendar reports on a start date field show the range of the field from the start date to the end date. Calendar reports on an end date field show only the end date.

**Parent Topic:**[Report types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/report-types-creation-details-rd.md)

## Create a calendar report

Create a calendar report to show and highlight date-driven events.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On instances with Unified Analytics enabled, and on new Zurich instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**. For more information, see [Differences between Core UI and Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d50021e289">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/c_ReportSources.md).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d50021e308">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/remote-tables/remote-tables.md)

</td></tr><tr><td id="d50021e327">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(\[Omitted image "upload-icon.png"\] Alt text: Upload icon\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d50021e352">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/metricbase/metricbase.md).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Calendar** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_wvg_5jr_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Event to display

</td><td>

The date-driven event to display on the calendar. This list contains fields that are in the date/time format in the data source or source table. Click the info icon \(\[Omitted image "icon-info.png"\] Alt text:\) for a description of the selected event.

</td></tr></tbody>
</table>8.  To limit the information displayed in the report, select the filter icon \(\[Omitted image "List\_FilterIcon.png"\] Alt text: Filter icon\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


### What to do next

**Note:** When there are more events on a date than fit in the calendar cell, a link is shown to view the additional events.

\[Omitted image "calendar-with-extra-events.png"\] Alt text: Calendar cell with two extra events, also shown expanded

If there are more than thirty events, the cell shows + many. Click this link to show all the events in a list view for that date.

-   Select the Report info icon \(\[Omitted image "Form\_ReferenceLookupIcon.png"\] Alt text: Info icon\) and add a description of the report.
-   Select the sharing icon \(\[Omitted image "ShareIcon.png"\] Alt text: Sharing icon\) to open the **Sharing** menu. On this menu, you can share the report with users and groups, add the report to a dashboard, and publish the report to the web.

