---
title: Proactive analytics insights on dashboards
description: Proactive analytics automates the extraction of insights from your Performance Analytics indicators. Receive notifications on your Platform Analytics dashboards of potentially interesting changes and events in your processes.
locale: en-US
release: australia
product: Proactive Analytics
classification: proactive-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Dashboards, Platform Analytics experience, Platform Analytics]
---

# Proactive analytics insights on dashboards

Proactive analytics automates the extraction of insights from your Performance Analytics indicators. Receive notifications on your Platform Analytics dashboards of potentially interesting changes and events in your processes.

**Note:**

-   Proactive insights are a utility for use with Performance Analytics [indicators](../../performance-analytics/concept/performance-analytics-glossary.md#) on Platform Analytics dashboards. To benefit from this feature, you need to have indicators set up. These can be indicators you created yourself or indicators that are included in Platform Analytics Solutions. For more information, see [Performance Analytics \(Indicator data sources\)](../../performance-analytics/concept/r_PALandingPage.md).
-   You must have an active subscription to Performance Analytics to have Proactive analytics. For more information, see [Activating your Performance Analytics subscription](../../performance-analytics/concept/c_PremiumPerformanceAnalytics.md#).
-   To activate or deactivate Proactive analytics and select which types of insight cards to show, open the dashboard settings. For more information, see [Configure Platform Analytics dashboard settings](../../dashboards/task/configure-ac-db-settings.md).

    ![Insights settings on a dashboard.](../image/db-insights-settings.png)

-   Proactive analytics are available only on Platform Analytics dashboards, including technical dashboards. They are not available on [responsive dashboards](../../dashboards/reference/dashboards-landing-page.md), including responsive dashboards that have been migrated to Platform Analytics in compatibility mode.

## Types of insights/analytics

Proactive analytics consists of insight cards on your Platform Analytics dashboards. The system checks your indicators daily and generates insights cards for the following events:

-   **Trends**

    If an indicator is set to maximize or minimize but is trending in the opposite direction, an insight card is generated.

-   **Indicator target or threshold event**

    An insight card is created for the following events:

    -   The target on a Performance Analytics indicator \(KPI\) is missed.
    -   The target on an indicator is likely to be missed \(**Predictive target**\).
    -   The [threshold](../../performance-analytics/concept/performance-analytics-glossary.md#) of an indicator is breached. If the breach is an all-time high or low, this fact is mentioned.
    -   The threshold of an indicator is likely to be breached \(**Predictive threshold**\).
    If you turn on target insights but targets are not set for all indicators that are shown on your dashboard, or not all targets have a review date, a Target Suggestion card is generated. The card has links for each indicator.

    ![Suggestion insight to set a target.](../image/insight-target-suggestion.png)

    Selecting a link opens a modal for setting the target value and review date for that indicator. The system suggests values for you.

    ![Set target modal opened from suggestion insight, showing value and review data suggested by system.](../image/insight-set-target.png)

    For information about setting targets and thresholds on an indicator, see [Performance Analytics targets and thresholds](../../performance-analytics/concept/pa-targets-thresholds.md). You can also set targets and thresholds in a [KPI Details](kpi-details.md) page.

-   **Process mining**

    If you are using Process Mining, an insight card can be generated for any potential bottleneck in the process flows related to the indicator. These insights are intended to help IT process owners. You can also receive suggestions for Process Mining projects to create, and such projects will also generate insights. For more information, see [Creating Process Mining projects from Proactive Analytics suggestions](pm-projects-insights-suggestions.md#).

    **Note:**

    -   The sn\_process\_optimization\_analyst role is necessary to see these insights.
    -   Process mining insights are included in the DA Process Mining Insights plugin.
-   **KPI Signals event**

    A signal as defined in [KPI Signals](process-behavior-charts-for-kpis.md) is generated. KPI Signals uses standard statistical Process Behavior Charts to identify significant changes in processes. The following signals generate Insights cards:

    -   Outlier: A score beyond the three standard deviation \(3-sigma\) upper or lower limit.
    -   Short run: Four consecutive scores all greater than or all less than the average value, with three of the scores outside two standard deviations.
    -   Long run: Seven consecutive scores all greater than or all less than the average value.
    -   "Anti-signal": Informational message that the indicator has been stable for a long time.
    **Important:** KPI Signals must be configured for an indicator to generate KPI Signals events for that indicator. For more information, see [Signal, no signal, and anti-signal](signal-no-signal-anti-signal.md) and [Activate KPI Signals monitoring for an indicator \(KPI\)](../task/activate-signals-monitor.md).

-   **Key contributor guidance**

    A key contributor is a [breakdown](../../performance-analytics/concept/performance-analytics-glossary.md#) on a Performance Analytics indicator that the system identifies as having a particular impact. The system uses KPI Signals to make this determination, but you do not have to activate KPI Signals for the indicators. The system uses its own KPI Signals configuration.

    **Warning:** Be careful when you modify a Performance Analytics [data collection job](../../performance-analytics/concept/performance-analytics-glossary.md#) after the system has started to identify key contributors. You might alter the KPI Signals baseline or the evaluation interval or both. Consequently, you can have inconsistencies in the insights. If you notice such inconsistencies, identify the UUID for the affected indicator-breakdown combination. Then delete the corresponding record from the PA Correlation Analyzer State \[pa\_correlation\_analyzer\_state\] table. For more information, see [KPI Details UUIDs](kpi-details-uuids.md).

-   **Custom insights**

    Some dashboards that are included with Platform Analytics Solutions or other applications might have custom insights. For information about such insights, see the documentation for the relevant Platform Analytics Solution or application.


## Viewing insights cards on dashboards

To see the insights cards, select the **Insights** button next to the **Edit** button. If there are new insights to view, the button is marked by an orange circle.

![The dashboard view insights button.](../image/proactive-analytics-view.png)

A panel opens displaying insights cards. These cards have a lifespan of 30 days. You can scroll through the cards. Insights of the same type are grouped onto a single card.

![The Dashboard Insights panel showing insights cards. These cards show indicators that have missed their targets.](../image/proactive-analytics-insights-pane.png)

Each card shows the type of event that has occurred and the event details. Each card also has a button that opens the appropriate page for follow-up, depending on the insight type:

|Insight type|Page opened|
|------------|-----------|
|Target or threshold|KPI Details|
|Signal|KPI Details with KPI Signals pane open|
|Key contributor|KPI Details \(you have to set the filter on the key contributor manually\)|
|Process Mining finding|Analyst Workbench|

## Insights notifications in data visualizations

If **Show notifications on visualizations** is toggled on for a dashboard, visualizations on that dashboard will have a notification icon if there are any insights related to the indicators shown in that visualization. You can open the Insights pane from the More actions menu on that visualization.

![Data visualization showing an insight notification and an action under More Actions to open the Insights and suggestions panel.](../image/db-insight-on-dv.png)

## Grouped insights cards

Multiple insights of the same type are aggregated into a single card. If more insights of the type are generated before the card expires \(14 days\), they are added to the existing card. If a dashboard shows both trend and either target or threshold insights, the trend is shown on any target or threshold insight cards. No separate trend cards are generated in this case.

## Limitations and requirements

The Australia version of Proactive analytics applies only to Performance Analytics indicators.

Target and threshold events are shown only when a target or threshold has been set on the indicator. For more information, see [Performance Analytics targets and thresholds](../../performance-analytics/concept/pa-targets-thresholds.md).

KPI Signals events are shown only for indicators with KPI Signals activated. For more information, see [Activate KPI Signals monitoring for an indicator \(KPI\)](../task/activate-signals-monitor.md).

Key contributor guidance is provided only for Performance Analytics indicators with a daily frequency.

While key contributor events are also based on KPI Signals, they do not require KPI Signals to be activated on the indicator.

**Related topics**  


[Create a flow with a Proactive Analytics trigger](https://www.servicenow.com/docs/access?context=create-flow-proactive-analytics&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Indicator targets and thresholds in KPI Details](kpi-details-targets.md)

