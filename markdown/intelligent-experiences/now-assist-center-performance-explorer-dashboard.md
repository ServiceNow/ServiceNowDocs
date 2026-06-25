---
title: Now Assist Center Performance Explorer dashboard
description: Use the Now Assist Center Performance Explorer dashboard to review and analyze the execution details of assistants and AI agents across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-performance-explorer-dashboard.html
release: australia
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 3
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI, performance]
breadcrumb: [View AI assets usage and performance, Monitor, Now Assist Center, Enable AI experiences]
---

# Now Assist Center Performance Explorer dashboard

Use the Now Assist Center Performance Explorer dashboard to review and analyze the execution details of assistants and AI agents across your organization.

## Now Assist Center Performance Explorer dashboard

The Now Assist Center Performance Explorer dashboard displays execution-level details for assistants and AI agents. Use the dashboard to investigate individual executions, analyze performance metrics, and identify patterns across your AI asset deployments.

The Performance Explorer dashboard includes two sub-tabs: **Assistants** and **Agents**. Each sub-tab displays a table of individual executions for the selected asset type.

## Assistants

The **Assistants** tab displays a list of individual assistant executions. Use the **Date**, **Assistant Name**, **Result Type Offered**, **Conversation End State**, **Deflection Outcome**, and **Deflection State** filters to narrow results. Select **Reset Filters** to clear all applied filters.

\[Omitted image "now-assist-center-performance-explorer-assistants.png"\] Alt text: Assistants tab showing a table of assistant executions with columns for Assistant Name, Executed On, Result Type Offered, Conversation End State, Inferred CSAT, Deflection Outcome, Deflection State, and Effort Score.

-   **Assistant Name**

    The name of the assistant that was executed. Select the assistant name to view the full execution record.

-   **Executed On**

    The date on which the assistant execution occurred.

-   **Result type Offered**

    The type of result that the assistant offered during the execution, such as an answer, a deflection, or a transfer.

-   **Conversation End State**

    The state of the conversation at the end of the execution, such as Open or Faulted.

-   **Inferred CSAT**

    The inferred customer satisfaction score for the execution, calculated based on conversation signals.

-   **Transfers and escalation**

    Indicates whether the conversation was transferred or escalated to a live agent during the execution.

-   **Assist**

    The number of assist actions performed by the assistant during the execution.

-   **Deflection Outcome**

    The outcome of the deflection attempt, indicating whether the conversation was successfully deflected.

-   **Deflection State**

    The state of the deflection for the execution, such as deflected or not deflected.

-   **Effort Score**

    A score reflecting the level of effort required by the user to complete the interaction, based on conversation signals.


## Agents

The **Agents** tab displays a list of individual AI agent executions. Use the **Date**, **State**, and **E2E Latency \(S\)** filters, or the **Search Agent** field, to narrow results. Select **Reset Filters** to clear all applied filters.

\[Omitted image "now-assist-center-performance-explorer-agents.png"\] Alt text: Agents tab of the Performance Explorer dashboard, showing a table of AI agent executions with latency, call, and CSAT columns.

-   **Agent Name**

    The name of the AI agent that was executed.

-   **Executed On**

    The date on which the AI agent execution occurred.

-   **State**

    The state of the AI agent execution, such as Completed or Terminated.

-   **Tool Calls**

    The total number of tool calls made by the AI agent during the execution.

-   **LLM Calls**

    The total number of large language model \(LLM\) calls made by the AI agent during the execution.

-   **E2E Latency \(S\)**

    The end-to-end latency of the execution, in seconds, measured from the start to the completion of the AI agent run.

-   **Tool Latency**

    The cumulative latency contributed by tool calls during the execution.

-   **LLM Latency**

    The cumulative latency contributed by LLM calls during the execution.

-   **Assists Consumed**

    The number of assist credits consumed by the AI agent during the execution.

-   **Inferred CSAT**

    The inferred customer satisfaction score for the execution, calculated based on interaction signals. See [Exploring Conversation Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/conversational-intelligence/exploring-conversation-insights.md) for more information.


**Parent Topic:**[View AI assets usage and performance in Now Assist Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-view-ai-usage.md)

