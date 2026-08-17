---
title: Monitoring an AI system
description: Assess the quality and safety performance of a specific AI system by reviewing its scores, metric breakdowns, trends, and evaluated sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-asset-monitor.html
release: zurich
topic_type: concept
last_updated: "2026-04-10"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Monitoring an AI system

Assess the quality and safety performance of a specific AI system by reviewing its scores, metric breakdowns, trends, and evaluated sessions.

## Key benefits

-   See how a single AI system is performing without navigating between portfolio-level views and session lists.
-   Identify which metrics are pulling a quality or safety score up or down by reviewing the data sources table directly on each score card.
-   Detect regressions specific to an AI system by tracking metric trends over time.
-   Review all evaluated sessions for an AI system in one place and open any session to investigate its traces and spans.

The **Monitor** tab on the AI system asset page focuses on a single AI system. While the monitoring overview shows portfolio-wide scores and rankings, the **Monitor** tab shows scores, trends, and sessions for the selected system only. Use the **Monitor** tab when you already know which system needs attention and want to understand its performance in detail.

To start monitoring scores for an AI system, you must activate evaluation scoring for the relevant system type \(ServiceNow AI or external AI\) and then enable evaluation for the AI system from the inventory.

-   [Activate evaluation scoring for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-servicenow-ai-system.md)
-   [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md)
-   [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-enable-evaluation.md)

\[Omitted image "mon-ai-asset-monitor.png"\] Alt text: The Monitor tab showing quality and safety score cards, asset monitoring details, a trend chart, and a list of recent evaluated sessions for a single AI system.

## Required roles

The admin role is required to view the Monitor tab.

## Accessing monitoring details for an AI system

Access monitoring details for an AI system in one of the following ways:

-   Navigate to **All** &gt; **AI Control Tower** &gt; **Inventory**. Select the AI system asset and then select the **Monitor** tab.
-   Navigate to **All** &gt; **AI Control Tower** &gt; **Insights** &gt; **Monitor** and select a system name in the **AI systems ranked by score** widget.
-   Navigate to **All** &gt; **AI Control Tower** &gt; **Insights** &gt; **Monitor** &gt; **Evaluated sessions** and select the AI system name in the **AI system** column.

## Quality and safety score cards

The **Average overall quality score** and **Average overall safety score** cards display composite scores for this AI system, averaged across all evaluated sessions within the selected date range. Each score card shows a percentage, the percentage change from the prior period, and a trend chart.

The data sources table lists every metric that contributes to the composite, along with its weight and current value.

Scores are color coded for quick interpretation:

-   Red \(0 to 50%\): Low. Investigate immediately.
-   Orange \(51 to 75%\): Fair. Review recent sessions for trends.
-   Green \(76 to 100%\): Good. Meeting quality or safety targets.

## Score card side panel

Select the side panel icon on a score card to open a detailed breakdown of how the composite score is calculated.

-   See how the score is calculated by expanding the **How is this score calculated?** section, which displays a stacked bar visualization of metric contributions. Each segment's width represents the metric's weight, and its shading represents the metric's score.
-   Review the **Nuances to consider** section for notes about how the average score is derived and how different scoring formats \(binary, percentage, tiered\) affect the calculation.

For details on how scores are calculated, see [How evaluation scoring works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-how-evaluation-scoring-works.md).

## Asset monitoring details

The **Asset monitoring details** card shows the evaluation configuration that applies to this AI system.

-   **Sample rate**

    The percentage of sessions that are evaluated. The default is 100%.

-   **Data retention**

    How long evaluated session data is retained for this AI system.


## Monitor agent activity

Track how quality and safety metrics for this AI system are trending over the selected date range. The chart plots every metric with data for this AI system so you can detect regressions specific to it, confirm that recent changes improved performance, and see which metrics are shaping its overall scores.

Two line styles distinguish how each metric contributes to scoring:

-   Solid lines represent metrics that contribute to this AI system's overall quality or safety score. These metrics are configured in a metric template.
-   Dotted lines represent metrics that are being collected for this AI system but don't contribute to its overall quality or safety score. These metrics aren't configured in any metric template.

To add a dotted-line metric to your scoring formula or to adjust how much existing metrics contribute to your overall scores, see [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-metric-templates.md).

Choose which metrics to display by selecting an option from the list:

-   **__All metric categories__**

    Show every quality and safety metric that has data for this AI system. This is the default selection.

-   **__Quality metrics__**

    Show only metrics in the Quality category.

-   **__Safety metrics__**

    Show only metrics in the Safety category.


Point to a data point on the chart to see the exact score for that date.

## Recent evaluated sessions

The evaluated sessions table lists all sessions for this AI system within the selected date range. Scores are color coded for quick scanning.

Select a session name to open the session detail page and begin investigating traces and spans. For details on investigating sessions, see [Session details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-session-details.md).

-   **Name**

    Session identifier. Select the name to open the session detail page.

-   **Trace**

    Number of traces in the session.

-   **Quality score**

    Composite quality score for the session, calculated from the weighted metrics in your quality template.

-   **Safety score**

    Composite safety score for the session, calculated from the weighted metrics in your safety template.

-   **Start time**

    When the session began.

-   **End time**

    When the session ended or timed out.

-   **Total runtime tokens**

    Combined input and output tokens consumed by the AI system during this session. This reflects the cost of running the interaction, not the cost of evaluating it.


-   **[Review scores for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-review-ai-system-scores.md)**  
Determine whether a specific AI system is meeting quality and safety targets by reviewing its scores, identifying which metrics are affecting performance, and checking for regressions over time.

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

