---
title: Show, compare, create, and edit records in KPI Details
description: You can view the list of records underlying an indicator score. You can create a record, edit individual records, or compare records. You can also export the list of records.If you have activated Show records, you can edit one of the records from inside KPI Details.You can compare indicator scores and underlying records for any two periods. List the records that have been moved out, shared, or moved in between these periods.If you show underlying records on KPI Details, you can refresh or export the list, select the columns to view, or create a new record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Examining indicators, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Show, compare, create, and edit records in KPI Details

You can view the list of records underlying an indicator score. You can create a record, edit individual records, or compare records. You can also export the list of records.

The scores for automated indicators are based on values collected from table records. If you are looking at an automated indicator in KPI Details, toggle **Show records** to see a list of the records underlying the indicator score. You see the records behind the score for whichever date you have selected.

![Indicator with a list of underlying records for the selected date](../../../help-center/platform-analytics-workspace/image/kpid-show-records.png)

**Note:**

-   Records are not available for [formula indicators](../../performance-analytics/concept/performance-analytics-glossary.md#), such as indicators that calculate percentages or averages.
-   The list view of shown records follows one of these settings, in order of priority:
    1.  The value of the **Records list view** config property in the UI Builder, if set
    2.  The value in the **List View** field on the indicator source, if set
    3.  The Default view

## View or edit a record

If you have activated **Show records**, you can edit one of the records from inside KPI Details.

Depending on how the KPI Details component is configured, you can edit a listed record in one of the following ways:

-   In the Quick view pane. To open the Quick view for a record, click the Information icon \(![](../../performance-analytics/image/InfoIcon.png)\) next to the record's list entry. You can view the activity on the record or edit the record. Click **Update** when you are done.![Quick edit pane on KPI Details.](../image/kpi-details-quick-edit.png)

    The Quick view pane is available only if it has been turned on in UI Builder.

-   In a separate tab for the record. To open the record in a new tab, click the value in the first column of its list entry.

    ![Clickable record number in list of records on KPI Details.](../image/kpi-details-click-record-number.png)


## Compare records

You can compare indicator scores and underlying records for any two periods. List the records that have been moved out, shared, or moved in between these periods.

Select **Compare records** above the visualization to open the record comparison view.

![Compare Records button](../image/kpid-compare-records.png)

**Note:** Data snapshots indicators do not support record comparison.

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

## Record list actions on KPI Details

If you show underlying records on KPI Details, you can refresh or export the list, select the columns to view, or create a new record.

The records list on KPI Details has a set of buttons and icons for actions on the list:

![The actions for a record list in KPI Details.](../image/kpi-details-record-list-actions.png)

-   The Refresh action ![Refresh icon](../image/icon-refresh-nextexp.png) simply refreshes the list.
-   The Records - List Actions ![Settings icon](../../dashboards/image/icon-cogwheel-ac.png) control lets you select which columns to show in the list. The Reset widths option that is also listed when you select this icon is not enabled for KPI Details.
-   The **Edit** button is not enabled for KPI Details. For technical reasons, a different mechanism is provided for editing individual records. For more information, see [View or edit a record](show-compare-edit-records.md#).
-   The **Export** button opens a dialog where you can export the list of records either as a local file or as an email attachment, in one of the following formats:
    -   Microsoft Excel
    -   CSV
    -   JSON
    -   PDF
-   The **New** button opens a blank form on the record table.

