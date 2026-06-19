---
title: Voice page in assistant analytics
description: Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/voice-assistant-analytics.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-06-06"
reading_time_minutes: 14
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Voice page in assistant analytics

Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.

The Voice page shows performance metrics for your voice assistants, organised across four tabs: **Overview**, **Performance**, **Insights**, and **Assist consumption**. Use these tabs to monitor conversation volume, resolution rates, tool execution, authentication performance, conversation quality signals, and AI agent assist usage.

\[Omitted image "aiv-voice-assistant-analytics-dashboard.png"\] Alt text: Voice assistants analytics page in Assistant Designer showing the Overview tab with four sub-tabs, filters, and performance widgets including total conversations and resolution rate.

You can filter the data on all tabs using the following options:

-   Filter by voice assistant: View metrics for specific voice assistants.
-   Filter by language: View metrics by conversation language, such as English, German, Spanish, and so on.
-   Filter by communication channel type: View metrics by channel, such as phone, mobile app - iOS, mobile app - Android, or web browser.
-   Filter by date range: View metrics for a specific time period.

Scorecard widgets display a trend indicator below the metric value, showing the change in value compared to the equivalent previous period. The indicator includes the absolute change, the percentage change, and the comparison date range.

**Note:** Metrics marked with the **AI Inferred** tag are calculated through large language model \(LLM\) transcript analysis. Results may vary and may not be fully accurate. Review AI Inferred metrics before acting on them.

## Overview tab

The **Overview** tab shows high-level conversation volume, resolution performance, and AI voice agent activity for the selected date range.

-   **Total voice conversations**

    This area of the dashboard shows the total number of conversations with voice assistants in the selected date range. Use this metric to track growth in voice interactions and set benchmarks for assistant performance. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-total-voice-conversations.png"\] Alt text: Scorecard showing the total number of voice conversations with the assistant in the selected date range.

-   **Total voice conversations over time**

    This area of the dashboard shows how conversation volume has changed over the selected date range. Use this chart to identify patterns such as peaks and dips in usage and correlate them with changes to your assistant configuration. Hover over a date to view the total number of conversations for that date.

    \[Omitted image "aiv-total-voice-conversations-over-time.png"\] Alt text: Line chart showing how conversation volume changed over time, with dates on the horizontal axis and total conversation count on the vertical axis.

-   **Resolution rate \(AI Inferred\)**

    This area of the dashboard shows the percentage of conversations resolved by the voice AI, with no human follow-up needed. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-resolution-rate.png"\] Alt text: Scorecard showing the AI-inferred resolution rate as a percentage of conversations resolved by the voice AI without human follow-up.

-   **Resolution rate over time \(AI Inferred\)**

    This area of the dashboard shows how the resolution rate has changed over the selected date range. Use this chart to track the impact of assistant updates and configuration changes on resolution performance. Hover over a date to view the resolution rate percentage for that date.

    \[Omitted image "aiv-resolution-rate-over-time.png"\] Alt text: Line chart showing how the AI-inferred resolution rate changed over time, with resolution rate percentage on the vertical axis.

-   **Live agent transfer rate**

    This area of the dashboard shows the percentage of conversations transferred from the voice assistant to a live agent in the selected date range. Use this metric to identify common escalation triggers and optimise assistant workflows to reduce unnecessary transfers. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-live-agent-transfer-rate.png"\] Alt text: Scorecard showing the percentage of conversations transferred from the voice assistant to a live agent in the selected date range.

-   **Live agent transfer rate over time**

    This area of the dashboard shows how the live agent transfer rate has changed over the selected date range. Use this chart to identify periods of increased escalation and correlate them with conversation patterns or assistant configuration changes. Hover over a date to view the transfer rate percentage for that date.

    \[Omitted image "aiv-live-agent-transfer-rate-over-time.png"\] Alt text: Line chart showing how the live agent transfer rate changed over time, with transfer rate percentage on the vertical axis.

-   **Average handle duration \(with voice assistant\)**

    This area of the dashboard shows the average duration of the AI-handled portion of voice conversations, excluding time spent with a live agent after transfer. Use this metric to identify opportunities to streamline conversations and reduce resolution time.

    \[Omitted image "aiv-average-handle-duration-with-voice-assistant.png"\] Alt text: Scorecard showing the average duration of AI-handled voice conversations in seconds, excluding time spent with a live agent after transfer.

-   **Average handle duration \(with voice assistant\) over time**

    This area of the dashboard shows how the average handle duration has changed over the selected date range. Use this chart to track whether workflow optimisations are reducing the time the voice assistant spends handling conversations. Hover over a date to view the average handle duration in seconds for that date.

    \[Omitted image "aiv-average-handle-duration-with-voice-assistant-over-time.png"\] Alt text: Line chart showing how the average handle duration changed over time, with handle time in seconds on the vertical axis.

-   **Average turns**

    This area of the dashboard shows the average number of turns taken by the voice assistant per voice conversation in the selected date range. Use this metric to assess how efficiently the assistant resolves user requests.

    \[Omitted image "aiv-average-turns.png"\] Alt text: Scorecard showing the average number of conversational turns between the user and the voice assistant per conversation.

-   **Average turns over time**

    This area of the dashboard shows how the average number of conversational turns has changed over the selected date range. Use this chart to identify whether conversations are becoming more or less efficient over time. Hover over a date to view the average turn count for that date.

    \[Omitted image "aiv-average-turns-over-time.png"\] Alt text: Line chart showing how the average number of conversational turns per conversation changed over time.

-   **Average CSAT score**

    This area of the dashboard shows the average customer satisfaction \(CSAT\) score for voice conversations in the selected date range. CSAT scores are captured through your own post-conversation survey solution. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-average-csat-score.png"\] Alt text: Scorecard showing an average CSAT score of 3.0 out of 5 for voice conversations in the selected date range, with a 100% increase compared to the previous period.

-   **Average CSAT score over time**

    This area of the dashboard shows how the average CSAT score has changed over the selected date range. Use this chart to evaluate the impact of assistant updates on user satisfaction over time. Hover over a date to view the average CSAT score for that date.

    \[Omitted image "ai-average-csat-score-over-time.png"\] Alt text: Line chart showing how the average CSAT score changed over the selected date range, with CSAT score on the vertical axis ranging from 0 to 4 and time on the horizontal axis.

-   **AI voice agent performance**

    This area of the dashboard shows the conversation count and resolution rate for each AI voice agent invoked during conversations. The resolution rate column is AI Inferred. Use this table to identify high-performing agents and improve underperforming ones.

    The table includes the following columns:

    -   **Voice AI agent** — name of the AI voice agent.
    -   **Conversations** — total number of conversations handled by the agent.
    -   **Conversation change** — change in conversation count compared to the previous period.
    -   **Resolution rate \(%\)** — percentage of conversations resolved by the agent, measured through LLM transcript analysis \(AI Inferred\).
    \[Omitted image "aiv-voice-agent-performance.png"\] Alt text: Table showing conversation count and AI-inferred resolution rate for each AI voice agent, with columns for conversations, conversation change, and resolution rate percentage.


## Performance tab

The **Performance** tab shows tool execution metrics, authentication performance, and response time data.

-   **Execution count by tool type**

    This area of the dashboard shows the number of tool executions categorised by type, including flow actions and RAG-based search, for the selected date range. Use this metric to understand which tools are most frequently invoked during voice conversations. See  for information on tool types.

    \[Omitted image "aiv-execution-count-by-tool-type.png"\] Alt text: Donut chart showing 22 total tool executions. Flow Action accounts for 91% \(20 executions\) and Search Retriever accounts for 9% \(2 executions\).

-   **Tool execution time \(50th percentile\)**

    This area of the dashboard shows the tool execution time within which 50% of tool executions were completed. Tool time is the time required for the voice agent to complete actions using tools. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-tool-execution-time-50th-percentile.png"\] Alt text: Scorecard showing a tool execution time of 1.9 seconds at the 50th percentile, meaning half of all tool executions completed within this time.

-   **Tool execution time \(90th percentile\)**

    This area of the dashboard shows the tool execution time within which 90% of tool executions were completed. Only 10% of executions took longer than this time. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-tool-execution-time-90th-percentile.png"\] Alt text: Scorecard showing a tool execution time of 8.1 seconds at the 90th percentile. Only 10% of tool executions took longer than this time.

-   **Tool execution time \(99th percentile\)**

    This area of the dashboard shows the tool execution time within which 99% of tool executions were completed. Only 1% of executions took longer than this time. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-tool-execution-time-99th-percentile.png"\] Alt text: Scorecard showing a tool execution time of 22.9 seconds at the 99th percentile. Only 1% of tool executions took longer than this time.

-   **Tool Performance**

    This area of the dashboard shows performance broken down by individual tool. Success rate reflects the share of executions that completed without error. P50, P90, and P99 columns represent execution time percentiles in seconds.

    The table includes the following columns:

    -   **Type** — the tool type, such as Flow actions or RAG-based search.
    -   **Tool** — the name of the specific tool invoked.
    -   **Success rate** — the percentage of executions that completed without error.
    -   **P50 Time \(s\)** — median execution time in seconds.
    -   **P90 Time \(s\)** — 90th percentile execution time in seconds.
    -   **P99 Time \(s\)** — 99th percentile execution time in seconds.
    \[Omitted image "aiv-tool-performance.png"\] Alt text: Tool performance breakdown

-   **Guest authentication time \(50th percentile\)**

    This area of the dashboard shows the time within which 50% of guest authentication sequences were completed, measured from the first voice AI identification question until the authentication API call response. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-guest-authentication-time-50th-percentile.png"\] Alt text: Scorecard showing a guest authentication time of 20.6 seconds at the 50th percentile, meaning half of all guest authentication sequences completed within this time.

-   **Guest authentication time \(90th percentile\)**

    This area of the dashboard shows the time within which 90% of guest authentication sequences were completed. Only 10% took longer than this time. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-guest-authentication-time-90th-percentile.png"\] Alt text: Scorecard showing a guest authentication time of 25.5 seconds at the 90th percentile. Only 10% of guest authentication sequences took longer than this time.

-   **Guest authentication time \(99th percentile\)**

    This area of the dashboard shows the time within which 99% of guest authentication sequences were completed. Only 1% took longer than this time. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-guest-authentication-time-99th-percentile.png"\] Alt text: Scorecard showing a guest authentication time of 42.4 seconds at the 99th percentile. Only 1% of authentication sequences took longer than this time.

-   **Guest Authentication Outcomes**

    This area of the dashboard shows the number of interactions by authentication outcome. Successful means the caller was authenticated at any point during the interaction. Failed means every authentication attempt was unsuccessful.

    \[Omitted image "aiv-guest-authentication-outcomes.png"\] Alt text: Donut chart showing guest authentication outcomes for 13 total attempts. Success accounts for 100% \(13 attempts\) and Failed accounts for 0%, indicating all authentication attempts succeeded in this period.

-   **50th percentile response time**

    This area of the dashboard shows the response time within which 50% of voice assistant responses were completed, measured from when the user finishes speaking to when the voice assistant responds. Only 50% of responses took longer than this time.

    \[Omitted image "aiv-50th-percentile-response-time.png"\] Alt text: Scorecard showing a voice assistant response time of 1.3 seconds at the 50th percentile, measured from when the user finishes speaking to when the voice assistant responds.

-   **90th percentile response time**

    This area of the dashboard shows the response time within which 90% of voice assistant responses were completed. Only 10% of responses took longer than this time.

    \[Omitted image "aiv-90th-percentile-response-time.png"\] Alt text: Scorecard showing a voice assistant response time of 2.7 seconds at the 90th percentile. Only 10% of voice assistant responses took longer than this time.

-   **99th percentile response time**

    This area of the dashboard shows the response time within which 99% of voice assistant responses were completed. Only 1% of responses took longer than this time.

    \[Omitted image "aiv-99th-percentile-response-time.png"\] Alt text: Scorecard showing a voice assistant response time of 5.1 seconds at the 99th percentile. Only 1% of responses took longer than this time.


## Insights tab

The **Insights** tab shows conversation outcome data and key sentiment signals measured through large language model \(LLM\) transcript analysis.

-   **Additional conversation outcomes**

    This area of the dashboard shows conversation outcomes beyond resolution and live agent transfer. Immediate outcomes refer to events occurring within the first 30 seconds of the call.

    The table includes the following columns: **Outcome**, **Conversation count**, **Conversation change**, and **Percent of total conversations**.

    Outcomes tracked include:

    -   **Immediate live transfers** — conversations where the caller requested transfer to a live agent within the first 30 seconds.
    -   **Immediate disconnects** — conversations that disconnected within the first 30 seconds.
    -   **Session expiration** — conversations that ended due to session timeout.
    -   **Ticket created** — conversations that resulted in a ticket, such as an incident or case record, created for follow-up.
    \[Omitted image "aiv-additional-conversation-outcomes.png"\] Alt text: Table showing four conversation outcomes beyond resolution and live agent transfer, with counts, changes, and percentage of total conversations for each outcome type.

-   **User effort required with AI agents**

    This area of the dashboard tracks how much effort a user had to put in during a conversation, based on signals like transfers, wait times, and escalations. Scored as Low, Medium, or High. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-effort-required-with-ai-agents.png"\] Alt text: Donut chart showing user effort distribution across 33 conversations. Low effort accounts for 64%, medium effort for 30%, and high effort for 6%.

-   **AI agent empathy**

    This area of the dashboard measures how politely and attentively the agent acknowledged the user's needs and concerns throughout the conversation. Scored as Low, Medium, or High. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-ai-agent-empathy.png"\] Alt text: Donut chart showing AI agent empathy scores across 33 conversations. Medium empathy accounts for 97% and low empathy for 3%.

-   **User / AI agent confusion**

    This area of the dashboard indicates whether the user and agent misunderstood each other at any point in the conversation. Scored as Yes or No. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-ai-agent-confusion.png"\] Alt text: Donut chart showing confusion detection across 33 conversations. No confusion was detected in 91% of conversations and confusion was detected in 9%.

-   **User frustration with AI agents**

    This area of the dashboard indicates whether the user expressed frustration, through complaints, sarcasm, or dissatisfaction, during the conversation. Scored as Yes or No. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-frustration-with-ai-agents.png"\] Alt text: Donut chart showing user frustration detection across 33 conversations. No frustration was detected in 100% of conversations in this period.


## Assist consumption tab

**Note:** The data on this tab is for informational purposes only and should not be relied upon as a definitive statement of your Now Assist usage for billing purposes.

The **Assist consumption** tab shows AI agent assist usage metrics for the selected date range. An assist is recorded each time an AI voice agent completes an action during a conversation. Assists are categorised into three tiers based on the number of actions taken by the voice agent: Small, Medium, and Large.

-   **Total assists consumed**

    This area of the dashboard shows the total number of assists consumed by AI voice agents in the selected date range. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-total-assists-consumed.png"\] Alt text: Scorecard showing 225 total AI agent assists consumed in the selected date range, with a 100% increase compared to the previous period.

-   **Total assists consumed over time**

    This area of the dashboard shows how the total number of assists consumed by AI voice agents has changed over the selected date range. Hover over a date to view the number of assists consumed for that date.

    \[Omitted image "aiv-total-assists-consumed-over-time.png"\] Alt text: Line chart showing the number of AI agent assists consumed over time, with dates on the horizontal axis and number of assists on the vertical axis.

-   **Total assists consumed by tier**

    This area of the dashboard shows the total assists consumed, broken down by tier: Small, Medium, and Large.

    \[Omitted image "aiv-total-assists-consumed-by-tier.png"\] Alt text: Donut chart showing 225 total assists broken down by tier. Small tier accounts for 56%, medium tier for 44%, and large tier for 0%.

-   **Assist consumption by agent**

    This area of the dashboard shows the average actions per call and total assists consumed, broken down by AI voice agent. Assist tier \(small, medium, large\) is based on the number of actions taken by the voice agent.

    The table includes the following columns:

    -   **AI voice agent** — name of the AI voice agent.
    -   **Average actions per call** — average number of actions the agent took per conversation.
    -   **Assists Consumed** — total number of assists consumed by the agent.
    \[Omitted image "aiv-assist-consumption-by-agent.png"\] Alt text: Table showing assist consumption per AI voice agent, with columns for average actions per call and total assists consumed. Two agents are listed.


