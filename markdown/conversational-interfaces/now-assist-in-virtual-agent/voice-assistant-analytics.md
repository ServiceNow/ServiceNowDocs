---
title: Voice page in assistant analytics
description: Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-10-15"
reading_time_minutes: 6
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Voice page in assistant analytics

Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.

The Voice dashboard page aggregates key metrics related to voice assistant usage and performance, including total conversations, deflection rate, conversation outcomes, satisfaction scores, response time, tool execution performance, and performance of AI agents invoked by voice assistants.

![Voice dashboard page in Assistant analytics.](../image/NAinVA-assistant-designer-analytics-voice.png "Voice dashboard page in Assistant analytics")

The visualizations on the Voice page help you with the following:

-   Monitor the volume and outcomes of voice assistant interactions to assess adoption and identify areas for improvement.
-   Track inferred customer satisfaction \(CSAT\) score and engagement metrics, helping you enhance user experience and efficiency.
-   Analyze AI agent performance and conversations deflected to optimize voice workflows and reduce reliance on live agents.

You can filter the dashboard data using the following options:

-   Filter by voice assistant: View metrics for specific voice assistants.
-   Filter by language: View metrics by conversation language, such as English, German, Spanish, and so on
-   Filter by communication channel type: View metrics by channel, such as phone, mobile app - iOS, mobile app - Android, or web browser.
-   Filter by date range: View metrics for a specific time period.

## Voice assistants

-   **Percent voice conversations deflected**

    This area of the dashboard shows the percentage of voice conversations successfully self-handled by voice assistants, measured through large language model \(LLM\) transcript analysis. This metric measures the effectiveness of voice assistants in handling user queries independently.

    ![Percent voice conversations deflected.](../image/NAinVA-assistant-designer-analytics-voice-percent-deflected.png "Percent voice conversations deflected")

-   **Total Deflected Conversations Over Time**

    This area of the dashboard shows the trend of deflected conversations with voice assistants over the selected date range. Hover over a date to view the assistant name, number of conversations deflected, and percentage of conversations deflected.

    ![Total deflected conversations over time screen.](../image/NAinVA-assistant-designer-analytics-voice-deflection-trend.png "Total deflected conversations over time")

-   **Total conversations**

    This area of the dashboard shows the total number of conversations with voice assistants in the selected date range. Use this metric to track growth in voice interactions and set benchmarks for assistant performance.

    ![Total voice conversations.](../image/NAinVA-assistant-designer-analytics-voice-total-conv.png "Total conversations")

-   **Total conversations over time**

    This area of the dashboard shows the trend of voice conversations over the selected date range. Hover over a date to view the assistant name, number of conversations handled by the assistant on that date, and the percentage of conversations handled by the assistant on that date relative to the total conversations in the selected date range.

    ![Total voice conversations.](../image/NAinVA-assistant-designer-analytics-voice-conv-trend.png "Total conversations over time")

-   **AI voice agents in use**

    This area of the dashboard shows the number of AI voice agents invoked by the assistant to handle conversations in the selected date range.

    ![Total number of AI voice agents used by the assistant](../image/NAinVA-assistant-designer-analytics-voice-agents-active.png "AI voice agents in use")

-   **AI voice agents in use over time**

    This area of the dashboard shows the trend of AI voice agents associated with the assistant actively handling conversations over the selected date range. Hover over a date to view the assistant name that contains the agents and count of agent invocations.

    ![Trend of AI voice agents invoked by the assistant](../image/NAinVA-assistant-designer-analytics-voice-agents-invocation-trend.png "AI voice agents in use over time")


## Additional conversation outcomes

-   **Conversations transferred to a live agent**

    This area of the dashboard shows the number of conversations transferred from a voice assistant to a live agent for further assistance. This metric indicates how often users require support beyond what the voice assistant can provide. Use this data to identify common escalation triggers and optimize assistant workflows to reduce unnecessary transfers.

    ![Conversations transferred to a live agent](../image/NAinVA-assistant-designer-analytics-voice-conv-live-agent.png "Conversations transferred to a live agent")

-   **Number of tickets created**

    This area of the dashboard shows the number of tickets, for example, incident and case records, created for follow up actions after a conversation. This highlights instances where user issues required formal tracking and resolution. Monitor ticket creation trends to assess assistant effectiveness and identify areas for improvement in issue resolution.

    ![Number of tickets created.](../image/NAinVA-assistant-designer-analytics-voice-tickets-created.png "Number of tickets created")

-   **Conversations disconnected**

    This area of the dashboard shows the number of conversations that ended abruptly or disconnected before engagement. Reveals potential friction points or technical issues in voice interactions. Investigate disconnected conversations to improve assistant reliability and user experience.

    ![Conversations disconnected.](../image/NAinVA-assistant-designer-analytics-voice-conv-disconnect.png "Conversations disconnected")


## Conversations and user insights

-   **Immediate live agent transfers**

    This area of the dashboard shows the number of conversations where users requested a transfer to a live agent within 30 seconds of starting the call. This metric applies to phone conversations only. Use this metric to help identify scenarios that drive near immediate escalation to a live agent.

    ![Immediate live agent transfers.](../image/NAinVA-assistant-designer-analytics-voice-immediate-transfers.png "Immediate live agent transfers")

-   **Inferred customer satisfaction \(CSAT\) score**

    This area of the dashboard shows the average inferred CSAT score for voice conversations in the selected data range, calculated through LLM transcript analysis. Scored on a 5-point scale, 1 = least satisfied and 5 = most satisfied. This metric tracks user sentiment for voice assistant interactions. Track CSAT trends to evaluate the impact of assistant updates and guide improvements in user experience.

    ![Inferred customer satisfaction (CSAT) score.](../image/NAinVA-assistant-designer-analytics-voice-inferred-csat.png "Inferred customer satisfaction (CSAT) score")

-   **Average voice conversation duration**

    This area of the dashboard shows the average duration of voice conversations excluding the time spent with a live agent after transfer, so the value reflects only the AI-handled portion of the call. This metric helps assess the efficiency of voice interactions. Use this metric to identify opportunities to streamline conversations and reduce resolution time.

    ![Average voice conversation duration.](../image/NAinVA-assistant-designer-analytics-voice-average-duration.png "Average voice conversation duration")


## Response Time

Response time is the duration between when a user finishes their question or request and when the voice assistant begins its response.

-   **50th percentile response time**

    This area of the dashboard shows the response time within which 50% of responses were completed. Only 50% of responses took longer than this time.

    ![50th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-50th-response.png "50th percentile response time")

-   **90th percentile response time**

    This area of the dashboard shows the response time within which 90% of responses were completed. Only 10% of responses took longer than this time.

    ![90th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-90th-response.png "90th percentile response time")

-   **99th percentile response time**

    This area of the dashboard shows the response time within which 99% of responses were completed. Only 1% of responses took longer than this time.

    ![99th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-99th-response.png "99th percentile response time")


## Tool insights

-   **Executions by tool type**

    This area of the dashboard shows the number of tool executions categorized by type, including scripts, flow actions, subflows, and RAG-based search. See [Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information on tool types. Use this metric to understand which tools are most frequently invoked during voice conversations and optimize tool performance.

    ![Executions by tool type.](../image/NAinVA-assistant-designer-analytics-voice-tool-executions.png "Executions by tool type")

-   **50th percentile response time**

    This area of the dashboard shows the tool execution time within which 50% of executions were completed and the other 50% of executions took longer than this time. Use this metric to understand the typical tool execution time during voice conversations.

    ![Tool 50th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-tool-50th-response.png "Tool 50th percentile response time")

-   **90th percentile response time**

    This area of the dashboard shows the tool execution time within which 90% of executions were completed. Only 10% of executions took longer than this time. Use this metric to identify slower tool executions that may impact conversation flow.

    ![Tool 90th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-tool-90th-response.png "Tool 90th percentile response time")

-   **99th percentile response time**

    This area of the dashboard shows the tool execution time within which 99% of executions were completed. Only 1% of executions took longer than this time. Use this metric to detect outlier cases where tool performance may need optimization.

    ![Tool 99th percentile response time.](../image/NAinVA-assistant-designer-analytics-voice-tool-99th-response.png "Tool 99th percentile response time")


## Use of AI agents

-   **AI voice agent summary**

    This area of the dashboard shows the performance summary of AI voice agents invoked during voice conversations, including resolution status and total conversation count per agent. Use this metric to identify successful agents and improve underperforming ones.

    ![Deflection by AI agent.](../image/NAinVA-assistant-designer-analytics-voice-number-deflect.png "AI voice agent summary")


