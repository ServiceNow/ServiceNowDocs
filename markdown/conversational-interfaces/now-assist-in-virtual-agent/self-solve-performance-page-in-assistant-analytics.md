---
title: Self-Solve Performance page in Assistant analytics
description: Analyze self-solve and deflection metrics to measure how effectively assistants help users resolve issues without live agent intervention.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-01-06"
reading_time_minutes: 5
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Self-Solve Performance page in Assistant analytics

Analyze self-solve and deflection metrics to measure how effectively assistants help users resolve issues without live agent intervention.

The Self-Solve Performance dashboard page aggregates metrics related to self-solved events \(instances where assistants resolved user queries\), deflection rates, live agent transfers, and user effort. These metrics enable you to monitor resolution success, track deflection trends over time, and analyze the distribution of deflection outcomes. The insights from these metrics support targeted improvements to assistant behavior and help reduce the need for live agent support.

![A dashboard with score cards for key self-solve metrics, line charts tracking deflection rate and effort scores over time, and pie charts showing outcome and deflection type distributions](../image/NAinVA-assistant-designer-analytics-self-solve-performance.png "Self-Solve Performance dashboard page in Assistant analytics")

The visualizations on the Self-Solve Performance page help you with the following.

-   Monitor self-solve deflection rates to identify how often users resolve issues without live agent assistance.
-   Track deflection trends over time to evaluate the impact of assistant updates and optimizations.
-   Analyze user effort scores and deflection outcome distributions to guide improvements in user experience.

-   **Total Deflection Events**

    This area of the dashboard shows the total number of user queries in the selected date range that have the potential of being deflected. Use this metric to understand the overall volume of queries where deflection was attempted.

    ![A single score card displaying the count of events with potential for deflection. Includes a sparkline showing the trend and comparison to the previous period.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-total-events.png "Total Deflection Events")

-   **Total Deflections**

    This area of the dashboard shows the number of user queries successfully deflected by the assistant. This count indicates the number of interactions where deflection outcome was Resolved. The deflection can be attributed to AI agent, skill, topic execution or a positive feedback provided by the user.

    ![A single score card displaying the count of successfully resolved self-solve events. Includes a sparkline showing the trend and comparison to the previous period.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-total-self-solved-events.png "Total Deflections")

-   **Total Live Agent Transfers**

    This area of the dashboard shows the number of conversations transferred to a live agent during the selected period. The percentage change from the previous period helps you track whether transfers are increasing or decreasing over time. Use this metric to identify opportunities to improve assistant capabilities and reduce the need for human intervention.

    ![A single score card displaying the count of conversations transferred to live agents. Includes a sparkline showing the trend and percentage change from the previous period.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-total-live-agent-transfers.png "Total Live Agent Transfers")

-   **Deflection Rate**

    This area of the dashboard shows the overall percentage of interactions where users were successfully deflected from contacting a live agent. This is calculated using: \(\(Total number of self-solved events\)/\(Total number of events\)\) x 100.

    A higher deflection rate indicates that the assistant is effectively helping users find solutions independently. Use this metric to benchmark assistant performance and track improvements over time.

    ![A single score card displaying the average deflection rate as a percentage. Includes a sparkline showing the trend across the selected date range.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-deflection-rate.png "Deflection Rate")

-   **Deflection Rate Over Time**

    This area of the dashboard tracks the deflection rate as a trend line across the selected date range. Hover over the trend line to view the deflection rate on a given day. This chart helps you identify periods of improvement or decline in deflection performance and correlate changes with assistant updates or external factors.

    ![A line chart with the x-axis showing dates and the y-axis showing deflection rate percentage from 0% to 100%. A single trend line tracks deflection rate changes over time.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-deflection-rate-over-time.png "Deflection Rate Over Time")

-   **Deflection Outcome Distribution**

    This area of the dashboard shows the distribution of outcomes for deflection attempts. The chart displays breakdown of Resolved, Response Provided, No Response Provided events, helping you understand how often deflection attempts lead to successful resolution.

    -   Resolved: conversations where at least one AI asset, for example, AI agent, skill, topic was executed or a positive feedback was provided by the user
    -   Response Provided: conversations involving small talk or where the assistant provided a synthesized response with no further action from the user
    -   No Response Provided: conversations where no response was provided by the assistant
    -   Not Resolved: conversations where negative feedback was provided by the user or the query was escalated to a live agent
    ![A pie chart showing the proportion of self-solve outcomes. Each segment represents a different outcome category with its percentage of the total.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-self-solved-outcome-distribution.png "Deflection Outcome Distribution")

    Select a segment in the pie chart to drill down to the Deflection Details page and view conversations associated with that outcome. See [Deflection details page in Assistant analytics](deflection-details-page.md) for more information.

-   **Deflection Types Offered**

    This area of the dashboard shows the distribution of AI assets offered as deflection methods to users. For example, catalog item, synthesized response, knowledge article, and so on. Use this chart to understand which deflection methods are being employed and evaluate their relative usage.

    ![A pie chart showing the distribution of deflection methods offered to users. Each segment represents a deflection type with its percentage of the total.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-deflection-types-offered.png "Deflection Types Offered")

    Select a segment in the pie chart to drill down to the Deflection Details page and view conversations associated with that deflection type. See [Deflection details page in Assistant analytics](deflection-details-page.md) for more information.

-   **Effort Score**

    This area of the dashboard tracks user effort levels across conversations in the selected date range. Effort is categorized as High, Medium, or Low, indicating how much time and energy users needed to invest during the conversation to resolve their issues. Lower effort scores suggest a smoother self-service experience. Use this chart to help identify trends in user effort over time and prioritize improvements that reduce friction in the self-solve process. Effort score is based on the inferred Effort CSAT \(customer satisfaction\) factor. See Conversation Insights for more information.

    ![A multi-series line chart tracking High, Medium, and Low effort levels over time. The x-axis shows dates; the y-axis shows conversation count.](../image/NAinVA-assistant-designer-analytics-self-solve-performance-effort-score.png "Effort Score")


