---
title: Show, compare, and edit records in KPI Details
description: You can view the list of records underlying an indicator score. You can edit individual records or compare records.If you have activated Show records, you can edit one of the records from inside the Analytics Center.You can compare indicator scores and underlying records for any two periods. List the records that have been moved out, shared, or moved in between these periods.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Examining indicators with KPI Details, KPI Details, Platform Analytics]
---

# Show, compare, and edit records in KPI Details

You can view the list of records underlying an indicator score. You can edit individual records or compare records.

The scores for automated indicators are based on values collected from table records. If you are looking at an automated indicator in KPI Details, toggle **Show records** to see a list of the records underlying the indicator score. You see the records behind the score for whichever date you have selected.

![Indicator with a list of underlying records for the selected date](../../../help-center/platform-analytics-workspace/image/kpid-show-records.png)

**Note:** Records are not available for [formula indicators](../../performance-analytics/concept/performance-analytics-glossary.md#), such as indicators that calculate percentages or averages.

**Parent Topic:**[Examining indicators with KPI Details](../reference/kpi-details-components.md)

**Related topics**  


[View contributing indicators to a formula in KPI Details](view-formula-components.md)

[Chart options in KPI Details](../reference/chart-options.md)

[Select time aggregation in KPI Details](../task/select-time-series-aggregation.md)

[Filter KPI Details by breakdown elements](../task/apply-brkdowns-element-kpi-details.md#)

## View or edit a record

If you have activated **Show records**, you can edit one of the records from inside the Analytics Center.

Depending on how the KPI Details component is configured, you can edit a listed record in one of the following ways:

-   In the Quick view pane. To open the Quick view for a record, click the Information icon \(![](../../performance-analytics/image/InfoIcon.png)\) next to the record's list entry. You can view the activity on the record or edit the record. Click **Update** when you are done.![Quick edit pane on KPI Details.](../image/kpi-details-quick-edit.png)

    The Quick view pane is available only if it has been turned on in UI Builder.

-   In a separate tab for the record. To open the record in a new tab, click the value in the first column of its list entry.

    ![Clickable record number in list of records on KPI Details.](../image/kpi-details-click-record-number.png)


## Compare records

You can compare indicator scores and underlying records for any two periods. List the records that have been moved out, shared, or moved in between these periods.

Click **Compare records** above the chart to open the record comparison view.

![Compare Records button](../image/kpid-compare-records.png)

Select the periods to compare either by typing in the dates or by using a calendar. Dates are in a \[Jan-Dec\] DD YYYY format. The period on the left must be the same or earlier than the period on the right. If you try to select a later period on the left or an earlier period on the right, both scores switch to the period you just selected.

Between the two scores, you see the number of records that have been moved out, shared, or moved in between these periods. Each of these values is a button. Select a value to list the corresponding records.

You can compare records filtered on up to two [breakdowns](../../performance-analytics/concept/performance-analytics-glossary.md#), each with one element. You cannot compare records filtered on multiple level elements.

You can compare records from a past period with real-time scores. When real-time scores are turned on, by default you compare the score from the last collected period to the real-time score.

**Important:** Record comparison is available only for automated indicators that have record collection turned on. Also, if you apply a time aggregation, you can compare only scores, not records.

### Comparing records

In this example, the number of open incident records on February 1, 2023 is compared with that on February 28. You see the following changes:

|February 01|February 28|
|-----------|-----------|
|54 records|40 records|
|Change of 0% since January 01|19 fewer records \(-32.2%\) since February 27|

-   Moved out \(Removed between the dates\): 22
-   Shared \(Present on both dates\): 32
-   Moved in \(Added between the dates\): 8

![Comparing records](../image/kpid-compare-record-details.png)

