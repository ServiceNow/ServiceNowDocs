---
title: Create a real-time score visualization for a score widget
description: To see the current score, use a real-time score visualization in a score widget. You can also show a trend line of scores.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Score widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a real-time score visualization for a score widget

To see the current score, use a real-time score visualization in a score widget. You can also show a trend line of scores.

## Before you begin

-   The indicator for which you want the real-time scores must have the **Show real-time score** property enabled.
-   Role required: pa\_admin or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is deprecated, meaning it is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

A real-time score visualization shows the current score and both the absolute and percentage change between this score and the score at the last previous scheduled data collection. The score is calculated when a dashboard user opens a dashboard that contains the widget. This visualization is similar to a **Chart** view in an Analytics Hub. You can also show a trend line of absolute or percentage changes in scores.

For more information, see [Real-time scores](../concept/real-time-scores.md).

**Warning:**

-   Real-time scores can differ per viewer and differ from collected scores. Real-time scores are taken directly from the relevant facts tables. Therefore, the Access Control Lists \(ACL\) of those facts tables determine the real-time scores that each logged-in user sees.
-   If the widget has too many data elements, it cannot update in real time. In this case, a message appears that instructs the viewer to refresh the widget manually.

![Real-time score visualization of open incidents](../image/real-time-score.png "Real-time score visualization")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Click **New**.

3.  In the **Name** and **Subtitle** fields, give the widget a name and subtitle that reflect the information being displayed.

4.  In the **Type** field, select **Score**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

5.  In the **Visualization** field, select **Real-time score**.

6.  In the **Indicator** field, select the indicator for which you want to show scores.

7.  Fill in any of the following fields:

<table id="table_k4q_fhr_w2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown and Element

</td><td>

Only the scores that match the specified element of this breakdown are shown. Select values for both **Breakdown** and **Element**. Otherwise, only scores that are not associated with any element of the breakdown are shown. **Note:** Instead of specifying an element for the first-level breakdown, you can specify an elements filter in the **Elements Settings** tab. Use elements filters for creating personal visualizations. For more information, see [Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#).

 **Important:** If the widget is for a formula indicator, all contributing indicators in the formula must support the breakdown. Otherwise an error message instead of a value appears in the widget on a dashboard.

</td></tr><tr><td>

2nd Breakdown and Element

</td><td>

Drill down to a second level of breakdown and element, if a first-level breakdown and element have been specified. **Note:**

-   Second-level breakdowns must be enabled on the indicator record, in the **Collect breakdown matrix** tab.
-   **Follow element** must be disabled. Dashboard breakdowns count as one breakdown level of the two that are possible.


</td></tr></tbody>
</table>8.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    **Note:**

    -   If multiple elements are selected on the breakdown dashboard, only the aggregate value of the elements can be shown.
    -   Record watcher is not supported on Score widgets when multiple elements are selected on a breakdown dashboard. In this case, real time is refreshed only on page refresh.
    For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

9.  Select a template.

    |Template name|Description|
    |-------------|-----------|
    |**Template 1**|Line shows absolute change in score.|
    |**Template 2**|Line shows percentage change in score.|
    |**Template 3**|Line is not displayed.|

    Real-time score visualizations use Template 2 by default.

10. In the **Element Settings** tab, you can select an element filter instead of selecting a specific element in the **Element** field.

    Use this approach to personalize which breakdowns are shown depending on the viewer. For more information about using element filters to personalize widgets, see [Personalized visuals](../concept/personalized-visuals.md#).

11. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Real-time scores](../concept/real-time-scores.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Create an automated indicator](t_CreateAnAutomatedIndicator.md#)

