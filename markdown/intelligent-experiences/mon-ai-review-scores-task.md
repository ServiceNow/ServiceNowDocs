---
title: Review scores across your AI portfolio
description: Assess the quality and safety of your AI systems by reviewing scores, identifying low-scoring systems, and learning which metrics are affecting each score.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-review-scores-task.html
release: australia
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review scores, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Review scores across your AI portfolio

Assess the quality and safety of your AI systems by reviewing scores, identifying low-scoring systems, and learning which metrics are affecting each score.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor**.

2.  Check for critical issues that need immediate attention by reviewing **Your top recommendations**.

    1.  Review each insight card for its severity level and outcome category.

    2.  Select **View details** to open the full analysis in a side panel, including affected metrics, impact, description, and root cause.

3.  Assess overall quality performance by reviewing the **Quality** score card.

    The score card displays a composite weighted average as a percentage. For example, a Quality score of 88% labeled Good \(green\) indicates that your AI systems are meeting quality targets overall.

4.  Assess overall safety performance by reviewing the **Safety** score card.

    The Safety score card displays a composite weighted average as a percentage. For example, a Safety score of 70% labeled Fair \(orange\) indicates that one or more safety metrics need attention.

5.  Understand which metrics are affecting a score by selecting the score card to open the scoring breakdown.

    1.  Select the **ServiceNow AI systems** or **External AI systems** tab to view the breakdown for a specific AI system type.

    2.  Review each metric's name, weight, current score, and change over time.

    3.  Expand the scoring formula section to see a stacked bar visualization of how each metric contributes to the composite score.

    For example, if the Quality score is 68%, the side panel might show that Task completion \(weight 25%\) scored 54% while Answer completeness \(weight 40%\) scored 91%. The low Task completion score is pulling down the composite.

6.  Identify which AI systems need attention by reviewing the **AI systems ranked by score** widget.

    1.  Select **Quality** or **Safety** from the list to choose which score to rank by.

    2.  Select **Lowest** or **Highest** to change the sort order.

    3.  Select a system name to view its evaluation details.

    For example, sorting by Lowest quality might reveal that an incident resolution agent is scoring 52% while all other systems are over 80%. This tells you where to focus your investigation.

7.  Check for regressions over time by reviewing the **Monitor agent activity** trend chart.

    1.  Choose which metrics to display by selecting **All metric categories**, **Quality metrics**, or **Safety metrics** from the list.

    2.  Adjust the time window using the date range picker.

    3.  Point to a data point on the chart to see the exact score for that date.

    Solid lines represent metrics that contribute to your overall quality or safety score. Dotted lines represent metrics that are collected but don't contribute to those scores.

    For example, a gradual decline in Tool choice accuracy from 85% to 62% over three weeks indicates a quality regression across your AI portfolio that warrants investigation.

    To add a dotted-line metric to your scoring formula, see [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).


**Parent Topic:**[Reviewing quality and safety scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-reviewing-ai-system-scores.md)

