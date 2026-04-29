---
title: Filter native Data snapshots indicator scores in KPI Details
description: Filter native Data snapshots indicators by the fields on their Data snapshots sources. For fields that refer to tables with report hierarchies, roll up scores to the parent field.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Examining indicators, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Filter native Data snapshots indicator scores in KPI Details

Filter native Data snapshots indicators by the fields on their Data snapshots sources. For fields that refer to tables with report hierarchies, roll up scores to the parent field.

## Before you begin

Role required: None. However, upgraded instances may require pa\_viewer.

## Procedure

1.  Open KPI Details for a native Data snapshots indicator, as described in [View KPI Details](../../performance-analytics/task/view-kpi-details.md).

2.  In the sidebar of KPI Details, select the Filter icon. ![Filter icon highlighted on sidebar.](../image/kpi-details-filter-icon.png)

    You see a list of the currently available fields that can filter this indicator.

3.  Change which fields can filter the indicator.

    1.  Select ![Configure icon.](../../../common/image/Form_PersonalizeFormIcon.png) **Configure** at the beginning of the Filters panel.

        ![The Configure button at the beginning of the Filters panel.](../image/kpid-ds-configure-filters.png)

    2.  Select and deselect fields that you can filter by.

    3.  Press **OK**.

4.  Expand a field to filter by to reveal its values.

5.  If the field refers to a table with a record hierarchy, you can roll up values in that hierarchy.

    1.  Turn on **Is in hierarchy**.

    2.  If more than one hierarchy can apply, select the hierarchy.

    3.  Select a parent value.

        The values of all child elements are rolled up to that parent.

    Example: The Functional Location.Location filter follows the Location record hierarchy. In this hierarchy, the Packing Area - Amsterdam value has two children, Packaging Machine - Amsterdam and Packing Line - Amsterdam. With **Is in hierarchy** turned off, Packing Area - Amsterdam shows only its own count of 9 records, excluding the record counts of its children.

    ![Filters in a hierarchy with Is in hierarchy turned off.](../image/kpid-filter-ds-hierarchy-off.png)

    With **Is in hierarchy** turned on, Packing Area - Amsterdam shows a count of 22 records: its own 9 records, plus the 7 Packaging Machine - Amsterdam and the 6 Packing Line - Amsterdam records.

    ![Filters in a hierarchy with Is in hierarchy turned on.](../image/kpid-filter-ds-hierarchy-on.png)

6.  In the **Sort by** menu, sort the elements by name, by the score for the selected date, or by the change from the previous date.

    If real-time scores are turned on, only sorting by name is available.

7.  Select one or more field values.

    If the values are sorted by score, the filter panel shows you the score for each field value for the selected date. If the elements are sorted by change, the filter panel shows you the percent change since the previous collection period for the selected date. Sort by name shows the values in alphabetical order.

8.  If you have selected multiple elements, select how to display the elements.

    By default, the aggregate score is displayed. Select **Display as separate time series** to show each element separately. You can make a selection only in cases where both aggregate and separate score displays are possible. For more information, see [Aggregate score of multiple elements](apply-brkdowns-element-kpi-details.md#).

9.  Click **Apply**


**Parent Topic:**[Examining indicators with KPI Details](../reference/kpi-details-components.md)

**Related topics**  


[View contributing indicators to a formula in KPI Details](../concept/view-formula-components.md)

[Show, compare, create, and edit records in KPI Details](../concept/show-compare-edit-records.md#)

[Chart options in KPI Details](../reference/chart-options.md)

[Select time aggregation in KPI Details](select-time-series-aggregation.md)

[Configure trend for a native Data snapshots indicator in KPI Details](configure-trend-ds-indicator.md)

[Configure display properties for a Data snapshots indicator](configure-display-properties-ds-indicator.md)

[Filter indicator scores by breakdown elements in KPI Details](apply-brkdowns-element-kpi-details.md#)

[Access indicator record or scoresheet from KPI Details](access-indicator-record-scoresheet.md)

