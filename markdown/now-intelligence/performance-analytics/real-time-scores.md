---
title: Real-time scores
description: You can view some Performance Analytics scores in real-time instead of from the most recent data collection job. If real-time scores are enabled, you can view them in KPI Details and in some data visualizations.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Real-time scores

You can view some Performance Analytics scores in real-time instead of from the most recent data collection job. If real-time scores are enabled, you can view them in KPI Details and in some data visualizations.

Usually, the most recent score that a visualization can show is the one from the most recent successfully run [data collection job](performance-analytics-glossary.md#). However, some visualizations can show indicator scores in real-time, for some indicators.

You can show real-time scores for an indicator that meets the following criteria:

-   The indicator is an [automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/glossary/now-platform-glossary.md).
-   It is configured to show real-time scores.
-   The aggregate function for the indicator does not use a script.
-   The indicator source does not use a [database view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/glossary/now-platform-glossary.md).
-   None of the breakdowns that are applied to the indicator use a scripted breakdown source.

The following visualizations can show scores in real time:

-   The Analytics Hub
-   Platform Analytics data visualizations that support real time update, such as Single score.
-   KPI Details
-   Performance Analytics score widgets with the Real-time visualization
-   Workbench widgets, for the main indicator

**Warning:** Real-time scores can differ per viewer and differ from collected scores. Real-time scores are taken directly from the relevant facts tables. Therefore, the Access Control Lists \(ACL\) of those facts tables determine the real-time scores that each logged-in user sees.

**Important:** The Analytics Hub does not update real-time scores automatically. To see the most up-to-date scores on the Analytics Hub, refresh the browser page. Widgets and KPI Details do update automatically.

**Parent Topic:**[Configure Performance Analytics fundamentals](c_PAWidgetsAndDashboards.md)

**Related topics**  


[Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#)

[Analytics Hub for a specific indicator](view-scorecard.md)

[Create a real-time score visualization for a score widget](../task/create-real-time-score-widget.md)

[Single score report](../../reporting/concept/c_SingleScoreCharts.md#)

[Monitor a workflow with a workbench process widget](c_MonitorWorkflowWorkbenchWidget.md#)

