---
title: Filter KPI Details by breakdown elements
description: In KPI Details, you apply breakdowns and elements to the indicator in the Filters sidebar.When you filter an indicator by multiple breakdown elements, you can either view a single aggregate score of all elements or a separate score for each element. However, not all indicators support an aggregate score of multiple elements.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Examining indicators with KPI Details, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Filter KPI Details by breakdown elements

In KPI Details, you apply breakdowns and elements to the indicator in the Filters sidebar.

## Before you begin

Role required: None. However, upgraded instances may require pa\_viewer.

## About this task

You can select as many breakdowns as the indicator supports. With [breakdown matrix collection](../../performance-analytics/task/create-breakdown-mapping.md#) enabled on the indicator, you can select up to two levels of breakdown, and you can select multiple elements on the first breakdown. \(If the indicator is a formula indicator, breakdown matrix collection must be enabled on the contributing automated indicators.\) With [data snapshots](../../performance-analytics/concept/multi-level-breakdowns.md) enabled on the indicator, you can select any number of breakdowns and elements.

**Important:** Filter conditions do not persist between KPI Details page refreshes.

## Procedure

1.  In the sidebar of KPI Details, select the Filter icon. ![Filter icon highlighted on sidebar.](../image/kpi-details-filter-icon.png)

    You see a list of the breakdowns for this indicator.

2.  Expand a breakdown.

    You see a list of the elements of the breakdown.

3.  If an elements filter exists for the breakdown, you can use it to refine the list of elements.

    1.  Expand the **Refine by** list to see the available element filters.

        This image shows the "Groups I manage" and "One of my groups" elements filters, which are available for the Assignment Group breakdown in the base system.

        ![Refine by menu on KPI Details filter pane showing available element filters.](../image/kpi-details-elements-filters.png)

    2.  Select an elements filter.

        In this image, the "One of my groups" is selected. The list of elements now includes only the assignment groups to which the logged-on user belongs.

        ![One of my groups element filter applied to the Assignment Group breakdown, so only the groups with the user as a member are shown.](../image/kpi-details-elements-filters2.png)

4.  In the **Sort by** menu, sort the elements by name, by the score for the selected date, or by the change from the previous date.

    If real-time scores are turned on, only sorting by name is available.

5.  Select one or more elements.

    If the elements are sorted by score, the filter panel shows you the score for each breakdown element for the selected date. If the elements are sorted by change, the filter panel shows you the percent change since the previous collection period for the selected date. When real-time scores are turned on, no previews are available.

6.  Select a second-level breakdown.

    1.  Expand a second breakdown.

    2.  Select only one element.

7.  If you have selected multiple elements, select how to display the elements.

    By default, the aggregate score is displayed. Select **Display as separate time series** to show each element separately. You can make a selection only in cases where both aggregate and separate score displays are possible. For more information, see [Aggregate score of multiple elements](apply-brkdowns-element-kpi-details.md#).

8.  Click **Apply**


## Selecting elements to filter by

In this example, the filter sidebar has been opened. You expand the Priority breakdown and select the 1 - Critical, 2 - High, and 3 - Moderate elements. You are about to click **Apply**. You will see the values of these elements as a single aggregate, because you did not select **Display as separate time series**.

![Breakdown and element filter sidebar for KPI Details, highlighting Apply button](../image/kpi-details-filter-sidebar.png)

## Aggregate score of multiple elements

When you filter an indicator by multiple breakdown elements, you can either view a single aggregate score of all elements or a separate score for each element. However, not all indicators support an aggregate score of multiple elements.

The following indicators support an aggregate score of multiple elements:

-   Automated indicators that aggregate data as a Count, Sum, Minimum, or Maximum value

    **Note:** The word "aggregate" is used for two different things here: the aggregate view of multiple indicator scores, and the data aggregation that is set on an indicator.

-   Manual indicators
-   External indicators that do not use `SQL AVG()` or `SQL COUNT(DISTINCT...)` in their SQL statement
-   Formula indicators that have aggregate element views enabled on their indicator records. For more information, see the entry on the **Allow aggregation of multiple breakdown element scores** field on the Other tab in [Create a formula indicator](../../performance-analytics/task/t_CreateAFormulaIndicator.md).

**Note:** When you navigate to KPI Details from a Performance Analytics widget on a Workspace Experience, and this widget uses an element filter that returns more than one element, only the first element is applied.

If the indicator supports a view of multiple elements, KPI Details shows the **Display as separate time series** control in the Filters sidebar. The behavior of this control depends on which views of multiple elements are supported:

-   If an indicator supports both aggregate and separate views, you see the aggregate view by default. To show a separate line for each element of a breakdown, select **Display as separate time series**.
-   If an indicator supports only the view of multiple elements as separate lines, **Display as separate time series** is selected and the choice is inactive.

**Note:** The **Display as separate time series** control is not enabled until you select multiple elements.

### Aggregate compared to separate view of multiple elements

In this example, the Number of open incidents indicator aggregates by Count and therefore supports an aggregate view of multiple elements. Both aggregate and separate views are shown.

![Indicator with 4 elements selected, showing the aggregate view](../image/kpi-details-multi-element-aggregate.png "Aggregate view of multiple elements")

![Number of open incidents indicator with multiple elements selected and separate time series view selected](../image/kpi-details-multi-element-separate.png "Separate view of multiple elements")

The following formula indicator does not have aggregate views of multiple elements enabled. The **Display as separate time series** option is selected automatically and you cannot change it.

![The filter sidebar for a formula indicator that does not allow aggregate view of multiple elements, with multiple elements selected](../image/kpi-details-multi-element-sep-only.png "Filter sidebar of indicator that does not support aggregate view")

**Related topics**  


[Indicator breakdowns](../../performance-analytics/concept/c_CreatingBreakdowns.md)

