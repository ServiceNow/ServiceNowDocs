---
title: Indicator targets and thresholds in KPI Details
description: Targets are goals your organization wants to achieve. They show the difference between the desired and actual scores of an indicator on a certain date. Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/kpi-details-targets.html
release: australia
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 6
breadcrumb: [KPI Details, Platform Analytics experience, Platform Analytics]
---

# Indicator targets and thresholds in KPI Details

Targets are goals your organization wants to achieve. They show the difference between the desired and actual scores of an indicator on a certain date. Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.

## Indicator targets

A target can be personal \(for yourself\) or global \(for everyone\). A personal target is visible only to the user that created it and appears as a light line. A global target is visible to all users and appears as a dark line. Because you cannot share a personal target, it appears only in KPI Details. Global targets can also appear in time series and single score data visualizations. Dashboards can alert viewers to events related to targets through [proactive analytics insights cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/proactive-analytics/proactive-analytics.md).

To view targets, select the target icon \[Omitted image "target-icon.png"\] Alt text: Target icon in the side panel. You have two choices to make:

-   View the targets that are for everyone \(global\) or just for you \(personal\).
-   Select the Configure icon \[Omitted image "Form\_PersonalizeFormIcon.png"\] Alt text: Configure icon. and choose what combination of past, current, or future targets to view.

    \[Omitted image "kpid-select-targets-view.png"\] Alt text: Selecting which targets to view on the Targets panel.


## Indicator thresholds

When a threshold is triggered, the instance generates an email notification. This message is associated with the indicator and the message is directly available via KPI Details.

A threshold can be personal or global. A personal threshold is visible only to the user that created it. It appears as a light grey dotted line. A global threshold is visible to all users and appears as a dark grey dotted line. Because you cannot share a personal threshold, it appears only in KPI Details. Global thresholds can also appear in time series data visualizations. Dashboards can alert viewers to events related to thresholds through [proactive analytics insights cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/proactive-analytics/proactive-analytics.md).

## KPI Details with current target

In the following example, one target has been set on the indicator. That target was set on 1 October, with a review date of 6 November. On 31 October, the score was 169. The gap on 15 March is calculated as `Target value - Score on selected date`. The gap is therefore 51, or 23.2%.

\[Omitted image "kpi-details-showing-target.png"\] Alt text: KPI Details for Number of open incidents &gt; Category: Network, showing target and that indicator is on track to be less than the target

The card for the target in the Targets panel shows a different gap value. This gap is equal to `Target value - Forecast score on the review date`. If you enable **Forecast** in the Chart Options, you can see how this gap is calculated more clearly. In the following example, you see that the forecast score for the review date is 29 and the target is 30. The gap on the tile accordingly is one.

\[Omitted image "kpi-details-review-date-gap.png"\] Alt text: KPI Details with Forecast on and the review date chosen in the chart, showing that the score is expected to beat the target by 2.

An icon displays the status as On track, Off track, or Too early to track. This icon appears on both the chart and the Targets panel. The status is based on the predicted gap between target and score on the review date. Because the projected score is better than the target, the On track icon is displayed. Had it been worse than the target, the Off track icon would be displayed. If there hadn't been enough data to predict whether the target would be met, the Too early to track icon would be displayed.

## KPI Details with past target

When a target reaches its review date, it becomes known whether it has been met. The On Track, Off track, and Too early to track icons no longer apply. Instead, either a Met or a Not met icon is displayed. In the following example, the indicator met its target on the review date by a margin of two. On the card, the Gap information is replaced by the final score on the review date. This score is visible regardless of which date is chosen on the chart. The chart still displays the gap between the score and the target on the selected date.

\[Omitted image "kpi-details-met-target.png"\] Alt text: KPI Details showing target that has been met.

## Past and current targets

When a target reaches its review date, it is no longer active. Usually you want a new target to take effect. When you add a new target, the expired targets are still visible, both in the chart and on cards. Here, a new target is added to the indicator after the target from the previous example has expired. This target is based on a 10% improvement to the previous target, as described in [Create a target in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-kpi-details-targets.md). The chart shows information about whichever target is in effect on the selected date.

\[Omitted image "kpi-details-old-new-targets.png"\] Alt text: KPI Details showing both an active and an expired target.

-   **[Create a target in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-kpi-details-targets.md)**  
You can set target values for indicators that apply only to specific breakdown elements and time series aggregations. The target starts to apply at a selected date and continues to apply until you set the next target. You can set a date on which you expect to reach the target, and set a new target then.
-   **[Edit multiple targets in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-multiple-targets.md)**  
Retroactively change one or more existing targets from their start date instead of ending them and starting new targets from a later date. You can edit multiple targets to have the same value, the same change in value, or the same date.
-   **[Subscribe users to Data snapshots indicator target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/subscribe-users-to-ds-target.md)**  
If you have targets set on a native Data snapshots indicator, you can specify users to receive emails about that target. Your instance must be configured to send emails.
-   **[Create, modify, or delete a threshold in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-mod-pers-tar-thresh-kpi-details.md)**  
Add, modify, or delete personal thresholds. With the required roles, you can also add, modify, and delete thresholds for all users.
-   **[Add a target to multiple breakdown elements in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-multiple-targets.md)**  
Select multiple breakdown elements in the KPI Details target configuration panel. Add the same target to each element. This target can be an improvement on a baseline instead of an absolute value.
-   **[Responsibility for indicator targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/responsibiity-targets-kpi-details.md)**  
A user can be responsible for targets on one or more Performance Analytics indicator/breakdown combinations \(KPIs\). Responsible users are expected to track progress towards the targets and can change the targets on their KPIs.

**Parent Topic:**[KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/kpi-details.md)

**Related topics**  


[Exploring KPI Details]()

[Examining indicators with KPI Details]()

[KPI Details reference]()

[Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Performance Analytics targets and thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-targets-thresholds.md)

