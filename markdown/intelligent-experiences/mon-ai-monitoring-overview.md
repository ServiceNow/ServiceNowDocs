---
title: Monitoring overview
description: Identify low-scoring AI systems quickly by reviewing quality and safety scores, AI-generated insights, and performance trends across your AI portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-monitoring-overview.html
release: australia
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review scores, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Monitoring overview

Identify low-scoring AI systems quickly by reviewing quality and safety scores, AI-generated insights, and performance trends across your AI portfolio.

## Key benefits

-   See the quality and safety health of your entire AI portfolio at a glance without opening individual system records.
-   Focus your attention on the AI systems and metrics that need it most using ranked lists and AI-generated insights.
-   Detect gradual regressions before they affect users by tracking metric trends over time.
-   Understand exactly how a composite score is calculated by expanding the scoring breakdown for any score card.

The monitoring overview is the starting point for assessing how your AI systems are performing in production. It brings together score cards, inventory data, AI-generated insights, and trend analysis so you can identify issues and take action from a single page.

**Note:** If you have the AI Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, the **Overview** page provides a summary for only the AI systems that you own.

\[Omitted image "mon-ai-monitor-overview.png"\] Alt text: Monitoring overview page showing the quality score, safety score, top action items, and AI systems ranked by score.

## Required roles

The AI Asset Owner or AI Steward role is required to view the monitoring overview.

## Accessing the monitoring overview

View the monitoring overview by navigating to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** &gt; **Overview**.

## Your top recommendations

AI-generated insights surface the highest-priority issues affecting your AI systems. Each recommendation includes a severity level, an outcome category \(for example, Drive AI Productivity\), and a brief description of the issue.

**Note:** Insights are generated daily based on sessions from the previous 24 hours. This delay allows the evaluation engine to collect enough sessions to produce meaningful analysis.

Each insight card provides the following actions:

-   **__View details__**

    Opens a side panel with the full analysis, including affected metrics, impact, description, and root cause.

-   **__Open__**

    Navigates to the location where you can act on the insight. For ServiceNow AI agents, this option takes you to actionable recommendations in the AI Skill Kit. For external AI systems, this option takes you to the related AI asset page in AI Control Tower.

-   **__Complete__**

    Marks the insight as resolved and removes it from the list. Use this options after you have addressed the underlying issue.

-   **__Delete__**

    Removes the insight from the list without marking it resolved. Use this option for insights that don't require action, such as duplicates or expected behavior.


Use the recommendations to prioritize which issues to investigate first. For example, an insight might report that a safety score dropped significantly during the past week and identify the specific session and metric driving the decline.

**Important:** AI-generated insights are based on automated analysis and may not reflect all contributing factors. Verify findings by reviewing session detail before taking action.

## AI systems and asset types

Two inventory widgets show the distribution of AI systems on your instance.

-   **AI systems**

    Shows the total count of AI systems by management status \(Managed and Unmanaged\). Only managed assets are evaluated.

-   **Asset types**

    Shows the distribution of AI systems by type \(for example, Agentic AI, Generative AI, and Classic AI\). Select a type to open the inventory filtered by that type. Only Agentic AI assets are evaluated.


## Quality and safety score cards

The quality and safety score cards display average overall scores for your Agentic AI systems. Each score card shows a percentage and a performance label.

Scores are color coded for quick interpretation:

-   Red \(0 to 50%\): Low. Investigate immediately.
-   Orange \(51 to 75%\): Fair. Review recent sessions for trends.
-   Green \(76 to 100%\): Good. Meeting quality or safety targets.

The safety score card populates only when external AI systems are being evaluated and have returned scored sessions. Because ServiceNow AI systems don't have safety metrics available, the safety score card remains empty until at least one external AI system has produced evaluated sessions. If the card appears empty, verify that evaluation scoring is active for your external AI systems and that trace data is being received.

View a scoring breakdown by selecting the side panel icon.

## Score card side panel

Selecting a quality or safety score card opens a side panel with a detailed breakdown of how the composite score is calculated. The panel includes tabs for **ServiceNow AI systems** and **External AI systems** so you can view the scoring breakdown for each type.

-   See how the score has changed over time by reviewing the average score and the percentage change from the prior period with a trend chart.
-   Identify which metrics are contributing to the score by reviewing the data sources table, which shows each metric's name, weight, and current score.
-   Expand the scoring formula section to see a visualization of how each metric contributes to the composite, along with explanatory notes about how the score is calculated.

Analyze which metrics are pulling a composite score up or down, and by how much. For details on how scores are calculated, see [How evaluation scoring works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-how-evaluation-scoring-works.md).

## AI systems ranked by score

View which AI systems are scoring lowest or highest. Select **Quality** or **Safety** from the list, and select **Lowest** or **Highest** to change the sort order. Select a system name to open its evaluation details.

## Monitor agent activity

Track how quality and safety metrics for your Agentic AI systems are trending over time in the Monitor agent activity chart. The chart plots every metric with data for the selected range so you can detect gradual regressions, confirm that recent changes improved performance, and see which metrics are shaping your overall scores.

Two line styles distinguish how each metric contributes to scoring:

-   Solid lines represent metrics that contribute to your overall quality or safety score. These metrics are configured in a metric template.
-   Dotted lines represent metrics that are being collected but don't contribute to your overall quality or safety score. These metrics aren't configured in any metric template.

To add a dotted-line metric to your scoring formula or to adjust how much existing metrics contribute to your overall scores, see [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).

Choose which metrics to display by selecting an option from the list:

-   **__All metric categories__**

    Show every quality and safety metric that has data for the selected date range. This is the default selection.

-   **__Quality metrics__**

    Show only metrics in the Quality category.

-   **__Safety metrics__**

    Show only metrics in the Safety category.


Point to a data point on the chart to see the exact score for that date.

## Use cases

-   **Identifying a quality regression during a weekly review**

    An AI steward opens the monitoring overview on Monday morning. The quality score card shows 68% \(orange\), down from 82% the previous week. The administrator selects the score card and sees that Task completion dropped from 88% to 54%. The AI systems ranked by score widget shows a specific incident resolution agent at the bottom of the list. The administrator selects that system, opens the lowest-scoring session, and discovers that a downstream API integration started returning timeout errors over the weekend. The administrator files an incident and monitors subsequent sessions to verify the fix.

-   **Responding to an AI-generated insight**

    The top recommendations list surfaces a critical insight: "Safety score dropped the most this week." The administrator selects **View details** and reads that the Instruction adherence metric dropped 18% for an external HR case management agent. The root cause analysis indicates the agent began straying from its approved response guidance in leave-request responses. The AI steward shares the insight with the product owner, who adjusts the agent's response guidelines.

-   **Monitoring a newly deployed agent**

    After deploying a new ServiceNow ITSM agent, the product owner opens the monitoring overview and filters to the new system using the AI systems ranked by score widget. Over the first week, the trend chart shows Tool choice accuracy starting at 62% and improving to 78% as the team adjusts the agent's tool configuration. The owner uses the scoring breakdown side panel to confirm which metrics are improving and which still need attention.


**Parent Topic:**[Reviewing quality and safety scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-reviewing-ai-system-scores.md)

