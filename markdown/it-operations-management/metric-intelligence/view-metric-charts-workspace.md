---
title: View metric charts in Agent Workspace
description: Agent Workspace for Metric Intelligence provides easy access to metric charts for a CI. On an alert form, you can drill down to important metric charts for the CI that is associated with the alert.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# View metric charts in Agent Workspace

Agent Workspace for Metric Intelligence provides easy access to metric charts for a CI. On an alert form, you can drill down to important metric charts for the CI that is associated with the alert.

## Before you begin

-   The CI that you want to view metric charts for, must be associated with an alert.
-   The Metric Dashboard Metadata \[sa\_metric\_dashboard\_metadata\] table must contain active chart configurations for the CI class for which you want to view metric charts.

Role required: workspace\_user and itil

## About this task

The set of metric charts, chart types, and other chart characteristics, is determined by the chart configurations in the Metric Dashboard Metadata \[sa\_metric\_dashboard\_metadata\] table, for the CI class.

## Procedure

1.  Navigate to **Agent Workspace** and click **Agent Workspace Home**.

2.  In Agent Workspace, click **List** and in the **Lists** panel, select one of the **Alerts** categorized lists such as **All Alerts** or **Top Priority**.

3.  In the alerts list view, open an alert.

    The alert must have a **Configuration item** associated with it.

4.  In the **Details** tab of the alert form, click **Metrics**.


## Result

All metric charts that are configured for the CI associated with the alert, and that are active, appear on the metric charts form in the **Metrics** tab. The calculation of the default time range for the charts is based on the times that the first and last events that generated the alert, occurred.

## What to do next

-   Modify the time range for the charts by changing **Start Time** and **End Time**. When you modify the time range, all charts are updated to reflect the new time range.
-   Click the cog wheel **Open settings** icon and change the settings for all charts:
    -   **Show bounds**: Show the bounds in the chart. Even if enabled, there are no bounds in a chart for aggregated resources.
    -   **Show legend**: Show chart legend.
-   Click **Insights Explorer** to open the Insights Explorer in a new browser tab. That Insights Explorer opens with the current CI pre-selected and with the current time range settings in Agent Workspace.

**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

