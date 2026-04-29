---
title: Examining indicators with KPI Details
description: The KPI Details feature enables you to delve into the information behind your key performance indicators. Apply forecasts, trends, targets, and thresholds. Filter by breakdown element or apply time series aggregations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [KPI Details, Platform Analytics experience, Platform Analytics]
---

# Examining indicators with KPI Details

The KPI Details feature enables you to delve into the information behind your key performance indicators. Apply forecasts, trends, targets, and thresholds. Filter by breakdown element or apply time series aggregations.

KPI Details has several sections:![KPI Details page showing the header, visualization, and sidebar sections](../image/kpi-details-whole.png)

## Header

The header contains the name of the indicator, a date selector \(default: last data collection\), and the score on that date. Data snapshots indicators are identified with a badge. The absolute and percentage differences between that score and the previously collected score are shown. If the indicator has Maximize or Minimize set, the color of the score and the score change direction arrow indicates whether the score is improving or getting worse.

The date selector uses whatever calendar the indicator uses.

If real-time scores are enabled for the indicator, select in the header whether to view them, using the clock icon ![Real-time scores icon turned off](../image/kpi-details-real-time-icon-off.png). This icon is transparent when real-time scores are disabled and solid when they are enabled ![Real time icon when real time is activated](../../dashboards/image/real-time-update-icon.png). For more information, see [Real-time scores](../../performance-analytics/concept/real-time-scores.md).

If a target is set for the selected date, the header shows the target value and the gap between the score on that date and the target, in both absolute and percentage terms. If both target and forecast are shown, as set in [Chart options in KPI Details](chart-options.md), a badge shows whether the indicator is on track or off track to meet the target by the review date.

**Warning:** Real-time scores can differ per viewer and differ from collected scores. Real-time scores are taken directly from the relevant facts tables. Therefore, the Access Control Lists \(ACL\) of those facts tables determine the real-time scores that each logged-in user sees.

## Indicator chart

The indicator chart shows:

-   The **Chart options** menu. For more information, see [Chart options in KPI Details](chart-options.md).
-   A date picker to choose the date range of the information in the chart. For Industrial Connected Workforce \(ICW\) indicators, this date range can be in shifts or production days.
-   A time series graphic representation of the indicator over time. Click on a point in the graph to see the details for that date.
-   A time series aggregation selector. For more information, see [Select time aggregation in KPI Details](../task/select-time-series-aggregation.md). \(Does not apply to Industrial Connected Workforce indicators.\)
-   The **Show records** toggle, which shows you the records associated with the indicator score on the selected date. For more information, see [Show, compare, create, and edit records in KPI Details](../concept/show-compare-edit-records.md#).

**Warning:** In some cases, when you collect second-level breakdowns, the score and the number of records do not agree. When these values do not agree, the score is correct. For more details and an example, see [KB0748969](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748969).

**Important:** Records are not listed for the "Unmatched" breakdown element when you select it in the filter.

## Sidebar

Use the sidebar controls to:

-   Filter by breakdown and element ![Filter icon](../../reporting/image/icon-filter.png).
-   View KPI Signals for the indicator \(![Icon in KPI Details sidebar to open KPI Signals, showing there is a new signal](../image/kpi-details-open-signals.png)\). See [KPI Signals](../concept/process-behavior-charts-for-kpis.md).
-   Set an indicator target or threshold\(![Target icon](../image/target-icon.png)\). See [Indicator targets and thresholds in KPI Details](../concept/kpi-details-targets.md).

## Process analysis

Besides these three sections, a **Run process analysis** button lets you launch a Process Mining analysis on the indicator. For more information, see [Process Mining](../../../administer/process-mining/concept/process-mining.md).

## More actions menu

You also have a More actions menu ![More actions menu icon](../../../common/image/icon-menu.png) that gives you access to the indicator record and scoresheet. For more information, see [Access indicator record or scoresheet from KPI Details](../task/access-indicator-record-scoresheet.md).

-   **[View contributing indicators to a formula in KPI Details](../concept/view-formula-components.md)**  
If you’re viewing a formula indicator in KPI Details, you can list the contributing indicators to that formula. Depending on the KPI Details configuration, you can open the contributing indicators in KPI Details.
-   **[Show, compare, create, and edit records in KPI Details](../concept/show-compare-edit-records.md#)**  
You can view the list of records underlying an indicator score. You can create a record, edit individual records, or compare records. You can also export the list of records.
-   **[Chart options in KPI Details](chart-options.md)**  
The KPI Details **Chart options** menu enables you to show, hide, or change aspects of an indicator visualization. Selected chart options persist per user for each indicator. Chart options are divided into analysis, time series, and chart type options.
-   **[Select time aggregation in KPI Details](../task/select-time-series-aggregation.md)**  
You can aggregate changes in indicators into discrete time intervals. A time aggregation consists of an AVG or SUM function combined with a time series, such as By quarter.
-   **[Configure trend for a native Data snapshots indicator in KPI Details](../task/configure-trend-ds-indicator.md)**  
Select a calendar and period by which to aggregate scores on the chart. You can also choose whether to include scores from incomplete periods.
-   **[Configure display properties for a Data snapshots indicator](../task/configure-display-properties-ds-indicator.md)**  
Change display properties for viewing a specific native Data snapshots indicator in KPI Details.
-   **[Filter indicator scores by breakdown elements in KPI Details](../task/apply-brkdowns-element-kpi-details.md#)**  
Apply breakdowns and elements to filter classic and Data snapshots-enabled indicators. The filter controls are in the KPI Details sidebar.
-   **[Filter native Data snapshots indicator scores in KPI Details](../task/filter-data-snapshots-indicator-scores.md)**  
Filter native Data snapshots indicators by the fields on their Data snapshots sources. For fields that refer to tables with report hierarchies, roll up scores to the parent field.
-   **[Access indicator record or scoresheet from KPI Details](../task/access-indicator-record-scoresheet.md)**  
In KPI Details, the More actions menu lets you open the record or the scoresheet of the indicator you are viewing.

**Parent Topic:**[KPI Details](../concept/kpi-details.md)

**Related topics**  


[Exploring KPI Details](../concept/exploring-kpi-details.md)

[Indicator targets and thresholds in KPI Details](../concept/kpi-details-targets.md)

[KPI Details reference](../concept/kpi-details-reference.md)

[Performance Analytics \(Indicator data sources\)](../../performance-analytics/concept/r_PALandingPage.md)

