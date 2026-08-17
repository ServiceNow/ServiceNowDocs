---
title: ServiceNow AI Conversation evaluation
description: The ServiceNow AI Conversation evaluation dashboard displays AI response quality metrics and satisfaction scores for individual conversations. It includes detailed evaluation records with human feedback and automated scoring across quality dimensions such as intent accuracy, request completion, truthfulness, and context retention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/snow-ai-convstn-evaluation.html
release: australia
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 3
breadcrumb: [Evaluation, ServiceNow AI dashboard, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# ServiceNow AI Conversation evaluation

The ServiceNow AI Conversation evaluation dashboard displays AI response quality metrics and satisfaction scores for individual conversations. It includes detailed evaluation records with human feedback and automated scoring across quality dimensions such as intent accuracy, request completion, truthfulness, and context retention.

## Conversation evaluation overview

The ServiceNow AI Conversation evaluation dashboard displays key performance indicators \(KPIs\), trend analysis, volume metrics, and detailed evaluation records. These metrics collectively provide visibility into AI response quality and user satisfaction levels.

To view the ServiceNow AI Conversation evaluation dashboard on AI Control Tower, navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **ServiceNow AI** &gt; **Evaluation** &gt; **Conversation evaluation**.\[Omitted image "aict-snow-ai-evaluation-dashboard.png"\] Alt text: The ServiceNow AI Conversation evaluation dashboard with different widgets displaying the insights.

**Note:** You can filter the Evaluation dashboard view by:

-   **User Satisfaction**: Displays the overall satisfaction metric aggregated across all evaluation criteria.
-   **Request Completion**: Measures whether the AI response fully addresses the user's request or question.
-   **Intent Accuracy**: Assesses whether the AI correctly understood the user's underlying intent or purpose.
-   **Slot Filling**: Evaluates the AI's ability to extract and identify key information entities from conversations.
-   **Truthfulness \(Hallucination Prevention\)**: Evaluates the AI's ability to extract and identify key information entities from conversations.
-   **Context Retention**: Assesses whether the AI maintains and references relevant context from prior conversation turns.
-   **Conciseness**: Measures whether the AI response is appropriately brief and focused without unnecessary verbosity.
-   **Smoothness \(Deadlock avoidance\)**: Assesses the AI's ability to navigate conversation flow without getting stuck or repeating itself.
-   **Coherence**: Measures whether the AI response is logically consistent, well-organized, and easy to follow.

All metrics on the Value dashboard default to the last 30 days. Use the time period selector in the top-right corner to adjust the date range and view metrics for different time periods \(for example, last 7 days, last 90 days, or a custom range\).

## Average autoeEvaluation score

The Average auto-evaluation score widget displays the mean satisfaction score calculated from automated evaluation algorithms applied to AI-generated responses. The auto-evaluation score uses predefined criteria to assess whether responses meet quality standards, including relevance, accuracy, completeness, and appropriate tone.

## Average human feedback score

The Average human feedback score widget captures the mean satisfaction rating provided directly by users or evaluators who interact with AI responses. Human feedback scores are typically higher than auto-evaluation scores when the AI system is performing well. Users may appreciate factors that automated systems don't capture, such as tone, helpfulness, and contextual understanding. Significant gaps between these metrics may indicate areas where evaluation criteria need adjustment.

## Evaluation score trend

The Evaluation Score Trend line chart visualizes the trajectory of average auto-evaluation user satisfaction scores over a selected time period.

You can view the average satisfaction score on the Y-axis and the weekly periods on X-axis along with the evaluation trend with fluctuation over time.

This metric helps you determine whether your AI system performance is improving, degrading, or remaining stable, enabling data-driven decisions about optimization efforts.

## Total evaluations

The Total Evaluations bar chart shows the volume of AI response evaluations completed per week across your selected time period.

You can view the number of evaluations on the Y-axis and the weekly periods on the X-axis. A consistent evaluation volume strengthens the statistical reliability of your performance metrics. Sudden drops in evaluation volume may indicate reduced AI agent usage or fewer user interactions.

## Evaluations

The Evaluations table provides a detailed record-by-record view of all AI response evaluations within your selected date range. You can see the evaluations listed by State, Human user satisfaction score, Auto evaluation user satisfaction score, and Gap \(Human - Auto evaluation user satisfaction score\).

**Note:** For a single evaluation record, you can select to view the evaluations by **View human scores** and **Label auto evaluated scores**, where as **Label random scores** is the default view.

