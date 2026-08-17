---
title: Review scores for an AI system
description: Determine whether a specific AI system is meeting quality and safety targets by reviewing its scores, identifying which metrics are affecting performance, and checking for regressions over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-review-ai-system-scores.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Monitoring an AI system, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Review scores for an AI system

Determine whether a specific AI system is meeting quality and safety targets by reviewing its scores, identifying which metrics are affecting performance, and checking for regressions over time.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## About this task

When a specific AI system needs attention, determine which metrics are affecting its scores and whether performance is trending in the right direction. Review the **Monitor** tab on the AI system asset record after spotting a low-scoring system on the monitoring overview, receiving an AI-generated insight about a specific system, or being assigned a task related to an underperforming asset.

## Procedure

1.  Navigate to the **Monitor** tab for the AI system that you want to review in one of the following ways:

    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**. Select the AI system asset and then select the **Monitor** tab.
    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** and select a system name in the **AI systems ranked by score** widget.
    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** &gt; **Evaluated sessions** and select the AI system name in the **AI system** column.
2.  Set the date range for the data you want to review.

    Select the date range picker and choose a time period. The default is **Last 30 days**.

    All score cards, trends, and session data on the page update to reflect the selected range.

3.  Assess overall quality performance by reviewing the **Average overall quality score** card.

    For example, if the quality score is 88%, the data sources table might show that Task completion \(weight 40%\) scored 88% while Answer completeness \(weight 35%\) scored 86%. A low score on a heavily weighted metric has a larger impact on the composite.

4.  Assess overall safety performance by reviewing the **Average overall safety score** card.

    For example, if the Instruction adherence score is lower than Secrets detection or Sexism detection, the agent may be handling sensitive data and language correctly but still straying from its approved response guidance. Reviewing the traces where Instruction adherence dipped lowest will show which specific exchanges the judge flagged and why.

5.  View the full scoring formula by selecting the side panel icon on a score card.

    1.  View a stacked bar visualization of how each metric contributes to the composite score in the **How is this score calculated?** section.

    2.  Learn how the average score is derived and how different scoring formats affect the calculation in the **Nuances to consider** section.

6.  Check the evaluation configuration by reviewing the **Asset monitoring details** card.

    The card shows the sample rate and data retention period for this AI system. If the sample rate is less than 100%, scores are based on a subset of sessions.

7.  Check for regressions over time by reviewing the **Monitor agent activity** trend chart.

    1.  Choose which metrics to display by selecting **All metric categories**, **Quality metrics**, or **Safety metrics** from the list.

    2.  Point to a data point on the chart to see the exact score for that date.

    Solid lines represent metrics that contribute to this AI system's overall quality or safety score. Dotted lines represent metrics that are collected but don't contribute to those scores.

    For example, a gradual decline in Task completion from 90% to 72% over three weeks indicates a quality regression for this AI system that warrants session-level investigation.

    To add a dotted-line metric to your scoring formula, see [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).

8.  Identify sessions that need investigation by reviewing the **Recent evaluated sessions** table.

    1.  Sort sessions by **Quality score** or **Safety score** to surface the lowest-scoring sessions.

    2.  Select a session name to open the session detail page and begin investigating its traces and spans.

    For example, a session with a red safety score \(below 50%\) warrants immediate investigation. For details on investigating sessions, see [Investigate a low-scoring session](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-investigate-session-task.md).


**Parent Topic:**[Monitoring an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-asset-monitor.md)

