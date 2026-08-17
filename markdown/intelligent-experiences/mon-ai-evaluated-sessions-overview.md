---
title: Evaluated sessions
description: View all evaluated AI sessions across your portfolio, compare quality and safety scores by AI system, and identify the sessions that need investigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-evaluated-sessions-overview.html
release: australia
topic_type: concept
last_updated: "2026-04-08"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigate sessions, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Evaluated sessions

View all evaluated AI sessions across your portfolio, compare quality and safety scores by AI system, and identify the sessions that need investigation.

## Key benefits

-   Compare quality and safety scores across AI systems to identify which systems are declining or performing well.
-   Find low-scoring sessions quickly by sorting and filtering the session list.
-   View score trends by AI system over weeks or months to detect patterns.
-   Open any session directly to investigate its traces and spans.

\[Omitted image "mon-ai-evaluated-sessions.png"\] Alt text: The evaluated sessions page showing the AI systems comparison chart and the sessions table.

## Required roles

The AI Asset Owner or AI Steward role is required to view evaluated sessions.

## Accessing evaluated sessions

View evaluated sessions by navigating to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** and selecting the **Evaluated sessions** tab.

## AI systems with evaluated sessions

Compare quality and safety scores across your AI systems using the bar chart. Each AI system displays a pair of bars representing its quality and safety scores.

-   Group scores by **Months**, **Weeks**, or **Days** to adjust the time granularity.

    For example, after deploying an update to an AI system, group the chart by **Days** to see whether the update improved scores without affecting other systems.

-   Select **Largest score decline** or **Top performers** from the list to change how AI systems are sorted in the chart.

## Evaluated sessions list

Find the sessions that need attention by reviewing the evaluated sessions table. Scores are color coded for quick scanning: red \(0 to 50%\), orange \(51 to 75%\), green \(76 to 100%\).

-   **Name**

    Session identifier. Select the name to open the session detail page and begin investigating traces and spans. See [Investigate a low-scoring session](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-investigate-session-task.md).

-   **Traces**

    Number of traces in the session. A session with many traces represents a longer, multi-turn interaction. Low scores on sessions with few traces can indicate a fundamental issue, while low scores on sessions with many traces may point to degradation over the course of the conversation.

-   **AI system**

    The AI system associated with the session. Select the name to view aggregated quality and safety scores across all evaluated sessions for that system.

-   **Quality score**

    Composite quality score for the session, calculated from the weighted metrics in your quality template. Sort by this column to surface the lowest-scoring sessions first.

-   **Safety score**

    Composite safety score for the session, calculated from the weighted metrics in your safety template. A red safety score warrants immediate investigation.

-   **Start time**

    When the session began. Use this to correlate low scores with known events such as deployments, configuration changes, or outages.

-   **End time**

    When the session ended or timed out.

-   **Total runtime tokens**

    Combined input and output tokens consumed by the AI system during this session. This reflects the cost of running the interaction, not the cost of evaluating it. Unusually high token counts can indicate inefficient agent behavior such as excessive retries or overly verbose responses.


**Parent Topic:**[Investigating low-scoring sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-investigating-low-scoring-sessions.md)

