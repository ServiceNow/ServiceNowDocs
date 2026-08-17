---
title: ServiceNow AI Impact
description: The ServiceNow AI Impact evaluation dashboard displays business outcomes and operational results from AI conversations. Metrics include issue resolution rate, time saved, cost reduction, and other KPIs demonstrating AI business value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/snow-ai-impact-evaluation.html
release: zurich
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 2
breadcrumb: [Evaluation, ServiceNow AI dashboard, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# ServiceNow AI Impact

The ServiceNow AI Impact evaluation dashboard displays business outcomes and operational results from AI conversations. Metrics include issue resolution rate, time saved, cost reduction, and other KPIs demonstrating AI business value.

## Impact evaluation overview

The ServiceNow AI Impact evaluation dashboard displays impact evaluation metrics, accessible through the Insights interface in ServiceNow AI.

\[Omitted image "aict-snow-ai-impact-eval.png"\] Alt text: The ServiceNow AI Impact evaluation dashboard with different widgets displaying the insights.

## Total conversations

The Total conversations widget displays the cumulative count of all conversations initiated within the selected time range. This metric represents the overall volume of interactions with ServiceNow AI across your organization.

## Estimated qualified conversations

The Estimated qualified conversations widget displays the count of conversations that meet qualification criteria for impact evaluation. This represents conversations eligible for efficiency, savings, and performance analysis.

## Estimated time savings \(hrs\)

The Estimated time savings \(hrs\) widget displays the cumulative time saved \(in hours\) through ServiceNow AI conversations within the selected time range. This metric is calculated based on estimated efficiency gains compared to manual task completion.

## Estimated VA efficiency \(%\)

The Estimated VA efficiency \(%\) widget displays the average efficiency percentage of virtual assistant conversations. This metric represents how effectively AI interactions resolved or assisted with user requests, expressed as a percentage.

## Average efficiency of conversations

The Average efficiency of conversations widget displays the mean efficiency rating across all conversations in the selected period. A circular progress indicator shows the percentage, with supporting metrics including:

-   Total conversation count
-   Hours saved per conversation

You can filter this metric by the following conversation sizes to view efficiency for specific conversation types:

-   Small size conversation
-   Medium size conversation
-   Large size conversation

## Estimated cost savings calculation

The Estimated cost savings calculation widget displays cost savings derived from time savings, calculated using the following configurable parameters:

-   **Hours saved**

    The total hours saved by AI conversations.

-   **Hourly rate**

    The cost per hour applied to the calculation \(default: USD currency\).

-   **Currency**

    The currency denomination for cost calculations.


The widget displays the calculated estimated cost savings figure in the specified currency. You can edit cost parameters by selecting **Edit** on the widget.

## User acceptance score

The User acceptance score widget displays an average auto-evaluation user satisfaction score trend over the selected time range. The score is represented as a line chart showing satisfaction ratings across multiple weeks, indicating user acceptance trends for ServiceNow AI conversations.

## Conversation performance

The Conversation performance section displays conversation efficiency metrics segmented by content type. The section includes the following elements:

-   **Type**

    Allows filtering by the following categorizations:

    -   By conversation size
    -   By content type
-   **Knowledge**

    Display performance data for conversations using Knowledge.

-   **Catalog**

    Display performance data for conversations using Catalog content sources.


Performance metrics are visualized as two area charts showing efficiency trends across the selected time period:

-   **Conversation efficiency**

    The Conversation efficiency chart displays efficiency percentages over time, represented as a filled area chart. The chart shows efficiency performance from the earliest date in the selected range through the most recent date, visualizing efficiency trends across weeks

-   **Time saved with conversation**

    The Time saved with conversation chart displays the trend of hours saved through AI conversations over the selected time range. The metric is visualized as a line chart showing cumulative time savings across weeks, with peaks indicating periods of higher time savings contribution.


