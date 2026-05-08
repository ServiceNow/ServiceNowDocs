---
title: Analytics Hub for a specific indicator
description: Use the Analytics Hub to analyze indicator data deeply, such as by aggregating data, comparing scores, or viewing changes over time.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Analytics Hub, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Analytics Hub for a specific indicator

Use the Analytics Hub to analyze indicator data deeply, such as by aggregating data, comparing scores, or viewing changes over time.

To access the Analytics Hub for an indicator, select any of these methods:

-   Navigate to **Performance Analytics** &gt; **Analytics Hub**, then select an indicator.
-   Click the **Explore indicator** related link on the relevant Indicator record.
-   From a responsive dashboard, select any value in a Performance Analytics widget.

    **Note:**

    -   From a Platform Analytics dashboard, selecting a value in indicator data accesses KPI Details instead of the Analytics Hub. This is default behavior; a data visualization can be configured with different drilldown behavior.
    -   When the indicator scores in a breakdown dashboard are aggregated on multiple elements, the Analytics Hub is aggregated on the same elements. For more information, see [Viewing aggregate scores for multiple elements](scorecard-overview-tab.md#).
    -   Time series aggregations are validated on the Analytics Hub and in KPI Details but not in widgets. Therefore, you might navigate from a working widget to the Analytics Hub and get a warning that the indicator has an invalid aggregation.

## Limitation

The Analytics Hub is not optimized for mobile screen sizes. You can access the Analytics Hub on a tablet using the standard web interface.

## Adding Targets, Thresholds, Comments, and Improvement Initiatives

All tabs in the Analytics Hub have a toolbar at the top with the following actions:

-   [Targets](pa-targets.md#)
-   [Thresholds](pa-threshold.md#)
-   Add a comment
-   Information
-   Create Improvement Initiative \(Requires the Continual Improvement Management application\)

A tooltip identifies each icon in the toolbar.

![The toolbar of the Analytics Hub](../image/detailed-scorecard-toolbar.png)

The toolbar always has the rightmost four icons from the screenshot. Clicking one of these icons opens a pane where you can view or create a target, threshold, or comment. You can also view the basic information about the indicator from this pane.

**Note:** Targets, thresholds, and comments are not supported on the Analytics Hub when indicator scores are aggregated on multiple elements.

For a formula indicator, this basic information includes the formula. In the Info panel you can also expand a list of the daily scores for the indicator. To see the scores for each component indicator in a formula indicator, click on the indicator name in the formula. Doing so refocuses the Analytics Hub on that indicator.

![Information tab for a formula indicator](../image/ah-formula-scores-in-info.png)

If you have the Continual Improvement Management application and the sn\_cim.improvement\_requester role, you can create an improvement initiative. Click the **Create Improvement Initiative** icon \(![Create improvement initiative icon](../image/scorecard-cim-icon.png)\) to open an Improvement Initiative form. This form is automatically populated with details of the indicator and Analytics Hub. To see the initiative start and finish dates on the timeline, click the improvement initiative icon in the chart options on the **Overview** tab.

If you have the Process Mining application and a Process Mining role, you can open the indicator in a Process Mining dashboard. Click the **Go to****Process Mining** icon \(![Process mining icon](../image/analytics-hub-process-op-icon.png)\).

## Editing indicators and scores, exporting to PDF or CSV, and generating graphics

Every indicator on the Analytics Hub has a context menu.

![Open Analytics Hub context menu](../image/detailed-scorecard-hamburger.png)

The options in this menu depend on the type of indicator and whether it has scores.

|Option|Where present|
|------|-------------|
|[Edit indicator](../task/t_CreateAnAutomatedIndicator.md#)|All indicators|
|[Edit scores](../task/t_ManuallyAddingScoresForIndicators.md)|Automated indicators with scores|
|Add to/Remove from favorites|All indicators|
|Export to PDF|All indicators with scores|
|Export scores to CSV|All indicators with scores|
|Save chart as PNG/JPEG|All indicators with scores|
|[Launch dependency assessment](impact-analysis.md)|All indicators|

Click the context menu a second time to close it without making a choice.

## Different tabs on the Analytics Hub

The Analytics Hub for a specific indicator has the Overview and Compare tabs, which are described in [View scores and statistics](scorecard-overview-tab.md#) and [Compare scores](scorecard-compare-tab.md), respectively.

**Related topics**  


[Performance Analytics indicators](c_Indicators.md)

[Performance Analytics targets and thresholds](pa-targets-thresholds.md)

[Dependency Assessment](impact-analysis.md)

[bundle-itsm.cim-landing-page]

