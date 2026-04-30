---
title: Indicator targets
description: Targets are goals your organization wants to achieve. Targets show the difference between the desired score at a certain date and the actual score of an indicator.You can set target values for indicators. You can have the targets apply only to specific breakdown elements and time series. The target starts to apply at a selected date and continues to apply until you set the next target. However, you can set a review date on which to reconsider the target.A target color scheme can be used to visualize the position of the indicator score relative to its target.You can specify a target that applies separately to each subset of data for an indicator with a breakdown.You can control which users receive a notification when a target is achieved. Notifications are also sent when it appears that a target will be achieved within the next 14 days.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Targets and thresholds, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indicator targets

Targets are goals your organization wants to achieve. Targets show the difference between the desired score at a certain date and the actual score of an indicator.

You can create targets on KPI Details or its Core UI equivalent, the Analytics Hub.

A target can be personal or global. A personal target is visible only to the user that created it and appears as a light line. A global target is visible to all users and appears as a dark line. Because you cannot share a personal target, it appears only on the Analytics Hub and KPI Details. The matrix of target visibility follows:

|Platform Analytics experience feature|Equivalent Core UI feature|Global or Personal targets|View or set|
|-------------------------------------|--------------------------|--------------------------|-----------|
|[KPI Details](../../par-for-workspace/concept/kpi-details.md)|[Analytics Hub](c_UsePerformanceAnalyticsScorecards.md)|Global and personal|Set and view|
|[Time series](../../reporting/task/create-dv-time-series-ac.md) and [Single score](../../reporting/task/create-dv-sing-sc-ac.md) Platform Analytics data visualizations|[Time series Performance Analytics widgets](../reference/time-series-widgets.md)|Global|View only|
|[Dashboards in Platform Analytics](../../par-for-workspace/concept/analytics-center-dashboards.md) containing time series or single score data visualizations that show targets|[Responsive dashboards](../../dashboards/reference/dashboards-landing-page.md) containing Time series Performance Analytics widgets that show targets|Global|View only|
|[Proactive analytics insights cards](../../par-for-workspace/concept/proactive-analytics.md) on Platform Analytics dashboards, which show targets being met or breached|No equivalent|Global|View only|
|UI Builder pages containing time series or single score data visualizations that show targets|No equivalent|Global|View only|

![Analytics Hub showing global targets for an indicator](../image/target.png "Target open for editing")

**Parent Topic:**[Performance Analytics targets and thresholds](pa-targets-thresholds.md)

## Create or edit targets

You can set target values for indicators. You can have the targets apply only to specific breakdown elements and time series. The target starts to apply at a selected date and continues to apply until you set the next target. However, you can set a review date on which to reconsider the target.

### Before you begin

Role required: pa\_target\_admin to create global targets that are visible to all users. Any user who can view an indicator on the Analytics Hub or KPI Details can view targets and create personal targets. A pa\_target\_admin, pa\_power\_user, or pa\_admin can edit any global target.

### Procedure

1.  Either:

    -   Open the Analytics Hub for an indicator.
    -   If you are working in the Platform Analytics experience, open KPI Details for an indicator. For more information, see [Create a target in KPI Details](../../par-for-workspace/task/create-kpi-details-targets.md).

        **Note:** KPI Details gives you the additional option to set targets in bulk for multiple breakdown elements. For more information, see [Add targets for multiple breakdown elements in KPI Details](../../par-for-workspace/task/add-multiple-targets.md).

2.  To limit the target to a subset of the scores, select a breakdown and a breakdown element.

    You can also select a 2nd-level breakdown and element.

3.  Select a time aggregation if the target should apply only to a specific time series, such as 7-day SUM.

    For more information, see [Applying time series aggregations](applying-time-series-aggregations.md#).

4.  Click the Target icon \(![](../image/TargetIcon.png)\).

    The Targets panel opens.

5.  In the Targets panel, select either Global or Personal targets.

    You see all the existing Global or Personal targets on this indicator that apply to whichever breakdown elements or time series you selected. You can select and deselect breakdown elements or a time series interactively, and the list of targets updates.

6.  Either create a new target or edit or delete an existing target:

    -   To create a target, click the + plus sign.
    -   To edit an existing target, click it in the Targets panel.
    -   To delete an existing target in the Analytics Hub, click the delete icon. ![](../image/delete-threshold-ah.png)
7.  Enter the target value for the score, in one of the following ways:

    -   Enter an absolute value in **Target**, or
    -   Select **Set target as an improvement of the baseline**. If you select this option, the following fields become available:

<table id="table_g5y_vzl_mmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target Calculation

</td><td>

Select either a percentage improvement or a number of units of the indicator to improve by.

</td></tr><tr><td>

Direction

</td><td>

When the indicator has a defined direction, this field is read-only. If the indicator direction changes, this field changes. Targets are recalculated accordingly.If the indicator does not have a direction, you can set a direction on the target here. However, usually it is better to define a direction on the indicator. For example, the score color that indicates an improvement or a deterioration works only when a direction is defined on the indicator.

</td></tr><tr><td>

Percentage/Units of the KPI

</td><td>

Enter either the percentage or the number of units of the KPI that you want as the targeted change to the baseline.

</td></tr><tr><td>

Baseline

</td><td>

Decide whether the improvement applies against the existing target or against the average value for the date range selected in the Analytics Hub. Another target must already exist to select **Existing Target**. For more information about the date range, see [Date ranges of scores in the Analytics Hub](scorecard-overview-tab.md#).

</td></tr><tr><td>

Baseline value

</td><td>

Read-only calculated value that serves as the basis for the target.

</td></tr><tr><td>

Target

</td><td>

This value is calculated from the baseline and the target calculation. You can adjust this value, for example to change a decimal value to a whole number for a count. If you adjust the target, the Percentage/Units of the KPI are recalculated.

</td></tr></tbody>
</table>8.  Select a start date.

    You can set a date in the future.

9.  Select a review date.

    The target applies from the selected start date until the start date of the next target, if any. If you do not define a later target, the target applies indefinitely. Thus, the review date serves as a reminder to consider changing the target. Whether or not you change the target value after review, consider selecting a new, future review date.

    **Note:** Overlapping targets are not allowed. Only one target at a time can be active.

10. Click **Save**.


### Creating, reviewing, and editing a target

Here we are going to look at the more advanced target features. Let's say it's July 1 and your Number of Open Incidents varied regularly from late May until mid-June, with a gradual downward trend. Then it started going up and down wildly, but the overall trend is still downward.![Initial trend data on the indicator](../image/target-ex-initial-trend.png)

As an incident manager, you want the number of open incidents to go down. You are not sure from your scores on a good target to set. However, the numbers look reliable up to mid-June, so a 10% decrease in the average score up to that point seems reasonable. So you create a new global target for your team. You select a date range up to June 15, and you set a 10% decrease on the average for that period as your target. You decide to start the target today and evaluate it on July 15.

|Field|Value|
|-----|-----|
|Target Calculation|Percentage \(%\)|
|Percentage|10|
|Baseline|Average score for the selected date range \(only choice, because no older target was set\)|
|Target|Originally calculated as 202.5. Since the incident count can only be a whole number, you decide to round off this value to 203.|
|Start/End date|July 1/July 15|

![Animated gif of creating a target based on a 10% reduction of an average score over a date range](../image/target-ex-set-first.gif)

July 15 comes around, and your team has exceeded all expectations—Or your customers are all on holiday and not reporting incidents. In any case, the number of open incidents is far below your target.![Number of open incidents at time of target review](../image/target-ex-review.png)

You now have several options:

-   Edit the existing target. Set a new target value and a new review date, for example 160 and August 15.
-   Create another target. The old target ceases to apply on the date the new target starts. The new target could again be an improvement of the baseline. You have the option of setting the old target as the baseline for the new target.

### What to do next

Select which users receive notifications. Notifications are sent when a target is achieved or is expected to be achieved within 14 days. For more information, see [Configure which users receive a target notification](pa-targets.md#).

You can also nominate responsible users for targets in KPI Details. For more information, see [Responsibility for global indicator targets](../../par-for-workspace/concept/responsibiity-targets-kpi-details.md#).

**Related topics**  


[KPI Details](../../par-for-workspace/concept/kpi-details.md)

## Create a target color scheme

A target color scheme can be used to visualize the position of the indicator score relative to its target.

### Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

### About this task

For example, if you want to filter the number of open incidents, the scores for an increase of 25% can be shown in red, an increase of 10% in orange, and no change in yellow. Whereas, for example, a decrease by 25% can be shown in dark green. Two target color schemes are available in Performance Analytics by default: the 3-color traffic light and the 5-color traffic light.

**Note:** You can only set a color scheme for a global target, not a personal target.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **System** &gt; **Target Color Schemes**.

    You have several target color schemes provided with the base system.

2.  Click **New**.

3.  Enter a **Name** and a **Description**.

4.  Define each of the five ranges and their associated colors.

    If you do not want to use all the ranges, you can use the same range color for multiple range limits.

    You select colors from the Color Definitions \[sys\_report\_color\] table. For information about defining more colors, see [Define system colors for analytics](../../reporting/task/t_DefiningSystemColors.md).

5.  Click **Submit**.

    A **Default indicator target color scheme** can be set in **Performance Analytics** &gt; **System** &gt; **Properties**. This is used when no color scheme has been selected for an indicator [target](performance-analytics-glossary.md#).


## Add a target for all elements of a breakdown

You can specify a target that applies separately to each subset of data for an indicator with a breakdown.

### Before you begin

Role required: pa\_target\_admin or admin

### About this task

For example, you can set a target on an Incident indicator that applies separately to the scores for each assignment group.

**Note:** This functionality is available only for global targets. The **Any element** check box does not appear for personal targets.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Targets**.

2.  Select the **Indicator** you want to set the target for.

3.  Select a **Breakdown**.

    The **Any element** check box is selected by default. Do not clear this check box.

4.  Select a **Time series**.

    For example, you can measure closed incidents daily and set monthly targets for closed incidents.

5.  Select a **Color scheme** for the target.

6.  Click **Submit**.


### What to do next

Define target values for the new target.

## Configure which users receive a target notification

You can control which users receive a notification when a target is achieved. Notifications are also sent when it appears that a target will be achieved within the next 14 days.

### Before you begin

Role required: pa\_target\_admin

### About this task

This functionality applies to global targets only. For personal targets, the target owner automatically receives notifications.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Targets**.

2.  Select a target.

3.  In the **Users** related list, click **Edit**.

4.  Move the users that you want to notify from the **Collection** column to the **Users List** column.

5.  Click **Save**.


### What to do next

The notification is sent automatically when a target is reached. Users that receive a notification can unsubscribe from that notification.

**Related topics**  


[Notifications](https://servicenow.com/docs/?context=CSHelp:Notifications-Landing)

