---
title: Configure trend for a native Data snapshots indicator in KPI Details
description: Select a calendar and period by which to aggregate scores on the chart. You can also choose whether to include scores from incomplete periods.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Examining indicators, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Configure trend for a native Data snapshots indicator in KPI Details

Select a calendar and period by which to aggregate scores on the chart. You can also choose whether to include scores from incomplete periods.

## Before you begin

Role required: None. However, upgraded instances may require pa\_viewer.

## About this task

**Important:** Only native Data snapshots indicators have this feature. Classic indicators, including ones with Data snapshots enabled, have a time aggregation instead. For more information, see [Select time aggregation in KPI Details](select-time-series-aggregation.md).

## Procedure

1.  Open KPI Details for a native Data snapshots indicator, as described in [View KPI Details](../../performance-analytics/task/view-kpi-details.md).

2.  Expand the Trend by menu, which has a label matching the currently selected aggregation period.

    ![The control for expanding the trend by menu](../image/kpid-open-trend-by.png)

3.  Note the read-only **Date field**.

    This field shows the optional date field from the Trend by section on the automated indicator record. When specified, it narrows the scores to changes per field value instead of an aggregate total. For example, if you trend by the Actual End field on a Resolved Incidents indicator, you show the number of incidents whose state changed to Resolved each day. If you don't specify a Trend by field on the indicator, you instead see the cumulative total of Resolved incidents each day.

    **Important:**

    A date field can be specified only for automated indicators. For a formula indicator, you can show only an aggregate total for the selected time period.

4.  Select a calendar.

    The calendar you select doesn’t have to be the same as the calendar selected on the indicator record. You’re selecting the calendar only to organize the scores, not collect them. Your selection determines which aggregation periods are available.

5.  Select the **Aggregation period**.

    The period you select doesn’t have to match the calendar frequency on the indicator record. You’re only organizing the display of scores.

6.  Turn on **Include incomplete periods**.

7.  Press **Apply**.


**Parent Topic:**[Examining indicators with KPI Details](../reference/kpi-details-components.md)

**Related topics**  


[View contributing indicators to a formula in KPI Details](../concept/view-formula-components.md)

[Show, compare, create, and edit records in KPI Details](../concept/show-compare-edit-records.md#)

[Chart options in KPI Details](../reference/chart-options.md)

[Select time aggregation in KPI Details](select-time-series-aggregation.md)

[Configure display properties for a Data snapshots indicator](configure-display-properties-ds-indicator.md)

[Filter indicator scores by breakdown elements in KPI Details](apply-brkdowns-element-kpi-details.md#)

[Filter native Data snapshots indicator scores in KPI Details](filter-data-snapshots-indicator-scores.md)

[Access indicator record or scoresheet from KPI Details](access-indicator-record-scoresheet.md)

