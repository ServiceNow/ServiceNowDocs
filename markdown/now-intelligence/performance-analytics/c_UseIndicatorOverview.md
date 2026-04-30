---
title: Analytics Hub list of indicators
description: The Analytics Hub provides a list of indicators, their scores, and a customizable selection of other analytics. Click the name of an indicator to see more details about that indicator. The Analytics Hub replaces scorecards.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics Hub, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Analytics Hub list of indicators

The Analytics Hub provides a list of indicators, their scores, and a customizable selection of other analytics. Click the name of an indicator to see more details about that indicator. The Analytics Hub replaces scorecards.

To access the Analytics Hub list, navigate to **Performance Analytics** &gt; **Analytics Hub**.

## Indicator list controls

The list of indicators includes the following controls:

-   Click the name of an indicator to open a view of the Analytics Hub that is focused on the indicator. An extended set of analytical tools is available in this view.
-   Click the pencil icon next to an indicator to open the indicator record for editing. This icon is available only if your roles give you access to the indicator record.
-   A solid green star beside an indicator name indicates that it is a favorite. Click the star beside the indicator to mark it as a favorite.
-   A black dot beside an indicator name indicates that it is a key indicator. Mark indicators as key by selecting the **Key** check box when creating the indicator.

![List of indicators with callouts to different features](../image/ah-list-indicators.png "List of indicators")

To customize what the Analytics Hub shows, click the list settings icon \(![](../image/Cogwheel.png)\) beside the search box.

![Settings for customizing what is shown in the indicator list of the analytics hub](../image/analytics-hub-list-settings.png "Indicator list settings")

The list settings include the following sections:

-   Filter settings
-   Breakdown source and element settings
-   Column settings

## Filter settings

You can filter which indicators are shown with the following settings:

-   **Key indicators**

    Only indicators that are defined as key indicators in the indicator record are shown.

-   **With a target**

    Only indicators with a defined target are shown.

-   **Formula**

    Only formula indicators are shown.

-   **Manual**

    Only manual indicators are shown.


![Filter section of the List Settings with Formula selected](../image/ah-filter-settings.png "Filter setting to show only formula indicators")

## Breakdown source and element settings

Within the settings, you can also select a breakdown source. Only indicators that use that breakdown source are shown. After choosing the breakdown source, you can further filter the list of indicators by selecting a breakdown element. Only indicators to which that element applies are shown.

In the following example, you see how the scores change when the list is filtered on the Indicator.Priority breakdown source and then on the 1 - Critical element.

![List of all indicators.](../image/ah-list-no-breakdown-filter.png "Indicator list with no breakdown filter applied")

![Same indicator list with the Incident.Priority breakdown source selected and all indicators without that breakdown source filtered out.](../image/ah-list-breakdown-source.png "Indicator list with a breakdown source filter applied")

![Same indicator list, now showing scores only where Priority is 1 - Critical.](../image/ah-list-bkdown-source-element.png "Indicator list with a breakdown source and element filter applied")

## Column settings

Select which analytics to show in the indicator list. The indicator scores are always shown.

-   **Change**

    The change in scores, in absolute value, between the most recent and the preceding data collection.

-   **Trend**

    The trend line for scores over the course of the data collection. This trend line is a miniaturization of the trend line that can be seen when the Analytics Hub is focused on a specific indicator.

-   **Bullet chart**

    A chart comparing current score to target. This chart is shown for an indicator only if a target is set on that indicator. ![Bullet chart showing that the score meets the target of 5%](../image/analytics-hub-bullet-chart.png)

-   **Date**

    Date that the latest score was collected.

-   **Target**

    The target for the indicator, if one has been set.

-   **Gap**

    The gap between the latest score and the target. A value is shown only if a target has been set for the indicator.

-   **Frequency**

    The frequency with which scores are calculated for the indicator.

-   **Direction**

    Whether the score for the indicator should minimize, maximize, or neither.

-   **Show percentage**

    If activated, the change in score is shown as a percentage instead of as an absolute value.


## Filter by performance

You can filter the list of indicators based on the indicator performance, in addition to filtering the list in the settings. ![Analytics Hub performance filters](../image/analytics-hub-performance.png)

-   **Best:** Shows indicators that are outperforming their target \(green\), ordered by Gap % \(best performers on top\).
-   **Worst:** Shows indicators that are under performing their target \(red\), ordered by Gap % \(worst performers on top\).
-   **Improved:** Shows indicators that have improved compared to the previous data collection \(moving in the right direction\).
-   **Degraded:** Shows indicators that have degraded compared to the previous data collection \(moving in the wrong direction\).

