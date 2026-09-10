---
title: Voice page in assistant analytics
description: Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/voice-assistant-analytics.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 16
breadcrumb: [Analyzing assistants, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Voice page in assistant analytics

Monitor the performance of voice assistants from the Voice page of Assistant analytics in Assistant Designer.

The Voice page shows performance metrics for your voice assistants, organised across four tabs: **Overview**, **Performance**, **Insights**, and **Assist consumption**. Use these tabs to monitor conversation volume, resolution rates, tool execution, authentication performance, conversation quality signals, and AI agent assist usage.

\[Omitted image "aiv-voice-assistant-analytics-dashboard.png"\] Alt text: Voice assistants analytics page in Assistant Designer showing the Overview tab with four sub-tabs, filters, and performance widgets including total conversations and resolution rate.

You can filter the data on all tabs using the following options:

-   Filter by voice assistant: View metrics for specific voice assistants.
-   Filter by language: View metrics by conversation language, such as English, German, Spanish, and so on.
-   Filter by communication channel type: View metrics by channel, such as phone, mobile app - iOS, mobile app - Android, or web browser.
-   Filter by date range: View metrics for a predefined period, such as last 7 days or last 30 days, or select a custom start and end date using the date picker.

Scorecard widgets display a trend indicator below the metric value, showing the change in value compared to the equivalent previous period. The indicator includes the absolute change, the percentage change, and the comparison date range.

**Note:** Metrics marked with the **AI Inferred** tag are calculated through large language model \(LLM\) transcript analysis. Results may vary and may not be fully accurate. Review AI Inferred metrics before acting on them.

## Overview tab

The **Overview** tab shows high-level conversation volume, resolution performance, and AI voice agent activity for the selected date range.

-   **Total voice conversations**

    This area of the dashboard shows the total number of voice conversations in the selected date range. Only sessions where at least one intent was detected are included in this count. Sessions where no intent was detected are excluded. Select the chart view to see how conversation volume has changed over the selected date range. Use this metric to track growth in voice interactions and set benchmarks for assistant performance. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-total-voice-conversations.png"\] Alt text: Scorecard showing the total number of voice conversations in the selected date range, with a chart toggle to view conversation volume over time.

-   **Resolution rate \(%\)**

    This area of the dashboard shows the resolution rate for voice conversations. Only conversations with at least one detected intent are included. Conversations with no detected intent are not counted. A conversation is counted as resolved only when every intent in it was completed. If even one intent is not completed, the entire conversation is counted as unresolved. The dashboard shows a breakdown of resolved conversations in two categories:

    -   **Resolved by AI**: conversations resolved entirely by the AI voice agent, with no human involvement.
    -   **Resolved by live agent after transfer**: conversations that required a live agent to complete at least one intent.
    These two categories are mutually exclusive and together account for all resolved conversations. Select the chart view to see how the resolution rate has changed over the selected date range. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-resolution-rate.png"\] Alt text: Scorecard showing resolution rate percentage with a breakdown bar for AI-resolved and live agent-resolved shares, and a chart toggle for rate over time.

-   **Live agent transfer rate \(%\)**

    This area of the dashboard shows the percentage of conversations transferred from the voice assistant to a live agent in the selected date range. Use this metric to identify common escalation triggers and optimise assistant workflows to reduce unnecessary transfers. Select the chart view to see how the transfer rate has changed over the selected date range. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-live-agent-transfer-rate.png"\] Alt text: Scorecard showing the live agent transfer rate as a percentage of conversations transferred to a human agent, with a chart toggle to view the rate over time.

-   **Additional conversation outcomes**

    This area of the dashboard shows conversation outcomes beyond resolution and live agent transfer. Immediate outcomes refer to events occurring within the first 30 seconds of the call.

    The table includes the following columns: **Outcome**, **Conversation count**, **Conversation change**, and **Percent of total conversations**.

    Outcomes tracked include:

    -   **Immediate live transfers**: conversations where the caller requested transfer to a live agent within the first 30 seconds.
    -   **Immediate disconnects**: conversations that disconnected within the first 30 seconds.
    -   **Session expiration**: conversations that ended due to session timeout.
    -   **Ticket created**: conversations that resulted in a ticket created for follow-up. Only incidents and service requests are included.
    \[Omitted image "aiv-additional-conversation-outcomes.png"\] Alt text: Table showing four conversation outcomes beyond resolution and live agent transfer, with counts, changes, and percentage of total conversations for each outcome type.


The **Conversation mechanics** widgets show how voice conversations unfold during the selected date range.

-   **Average handle duration \(with voice assistant\)**

    This area of the dashboard shows the average duration of the AI-handled portion of voice conversations, excluding time spent with a live agent after transfer. Duration is measured using a single call duration event per call. Use this metric to identify opportunities to streamline conversations and reduce resolution time.

    \[Omitted image "aiv-average-handle-duration-with-voice-assistant.png"\] Alt text: Scorecard showing the average duration of AI-handled voice conversations in seconds, excluding time spent with a live agent after transfer.

-   **Average turns**

    This area of the dashboard shows the average number of turns taken by the voice assistant per voice conversation in the selected date range. A turn is counted each time the voice assistant speaks. Use this metric to assess how efficiently the assistant resolves user requests.

    \[Omitted image "aiv-average-turns.png"\] Alt text: Scorecard showing the average number of conversational turns between the user and the voice assistant per conversation.

-   **Average CSAT score**

    This area of the dashboard shows the average customer satisfaction \(CSAT\) score for voice conversations in the selected date range. CSAT scores are captured through your own post-conversation survey solution. Conversations with no score are excluded from the average. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-average-csat-score.png"\] Alt text: Scorecard showing the average CSAT score for voice conversations in the selected date range.

-   **AI voice agent performance**

    This area of the dashboard shows a breakdown of conversation count, resolution rate, and AI resolution rate by invoked AI agents. Use this table to identify high-performing agents and improve underperforming ones.

    The table includes the following columns:

    -   **Voice AI agent**: name of the AI voice agent.
    -   **Conversations**: total number of conversations the agent took part in.
    -   **Conversation change**: change in conversation count compared to the previous period.
    -   **Resolution rate \(%\)**: percentage of the agent's conversations where all detected intents were completed.
    -   **Resolved by AI \(%\)**: percentage of the agent's conversations that were fully resolved with no human involvement.
    **Note:** Resolution rate in this table uses the same intent-based calculation as the Resolution rate scorecard. Only conversations with at least one detected intent are included. If a call involved more than one AI agent, it appears in each agent's row.

    \[Omitted image "aiv-voice-agent-performance.png"\] Alt text: Table showing conversation count, resolution rate, and resolved by AI percentage for each AI voice agent.


## Performance tab

The **Performance** tab shows response time, authentication performance, and tool execution metrics for the selected date range.

\[Omitted image "aiv-performance-tab.png"\] Alt text: Voice assistants analytics page showing the Performance tab with sections for Response Time, Guest authentication, Guest authentication time, Tool executions, and Tool time.

**Response Time**

Time from when a user finishes speaking to when the voice assistant responds.

\[Omitted image "aiv-response-time-scorecards.png"\] Alt text: Three scorecards showing the 50th, 90th, and 99th percentile response times in seconds.

-   **Response time \(50th percentile\)**

    Response time within which 50% of voice assistant responses were completed. This is measured from when the user finishes speaking to when the voice assistant responds. Only 50% of responses took longer than this time. Select **Related records** to view the underlying records.

-   **Response time \(90th percentile\)**

    This area of the dashboard shows the response time within which 90% of voice assistant responses were completed. Only 10% of responses took longer than this time. Select **Related records** to view the underlying records.

-   **Response time \(99th percentile\)**

    This area of the dashboard shows the response time within which 99% of voice assistant responses were completed. Only 1% of responses took longer than this time. Select **Related records** to view the underlying records.


**Guest authentication**

Number of interactions with successful and failed guest authentication. Successful means the caller was authenticated at any point in the interaction. Failed means every authentication attempt was unsuccessful.

-   **Guest authentication**

    This area of the dashboard shows guest authentication outcomes as a donut chart. A daily bar chart shows how successful and failed authentication attempts trended over the selected date range. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-guest-authentication-outcomes.png"\] Alt text: Donut chart showing guest authentication outcomes with a breakdown of successful and failed attempts, alongside a daily bar chart showing authentication trends over time.


**Guest authentication time**

Time from the first voice AI identification question until the authentication API call response. Use the outcome selector to filter results by all attempts, successful, or failed.

\[Omitted image "aiv-guest-authentication-time-scorecards.png"\] Alt text: Three scorecards showing the 50th, 90th, and 99th percentile guest authentication times in seconds, with an outcome selector for Total attempts, Successful, or Failed.

-   **Guest authentication time \(50th percentile\)**

    This area of the dashboard shows the time within which 50% of guest authentication sequences were completed. Use the outcome selector to filter results by Successful, Failed, or all authentication attempts. Select **Related records** to view the underlying records.

-   **Guest authentication time \(90th percentile\)**

    This area of the dashboard shows the time within which 90% of guest authentication sequences were completed. Only 10% took longer than this time. Use the outcome selector to filter results by Successful, Failed, or all authentication attempts. Select **Related records** to view the underlying records.

-   **Guest authentication time \(99th percentile\)**

    This area of the dashboard shows the time within which 99% of guest authentication sequences were completed. Only 1% took longer than this time. Use the outcome selector to filter results by Successful, Failed, or all authentication attempts. Select **Related records** to view the underlying records.


**Tool executions**

How many times each type of tool was used.

-   **Execution count by tool type**

    This area of the dashboard shows the total number of tool executions across voice conversations, broken down by tool type. Select the chart view to see how execution counts have changed over the selected date range. Use this metric to understand which tools are most frequently invoked during voice conversations. See [Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia.md) for information on tool types.

    \[Omitted image "aiv-execution-count-by-tool-type.png"\] Alt text: Donut chart showing total tool executions broken down by tool type, with a chart toggle to view execution counts over time.


**Tool time**

Time required for the voice assistant to complete actions using tools.

\[Omitted image "aiv-tool-time-scorecards.png"\] Alt text: Three scorecards showing the 50th, 90th, and 99th percentile tool execution times in seconds.

-   **Tool execution time \(50th percentile\)**

    This area of the dashboard shows the tool execution time within which 50% of tool executions were completed. Select **Related records** to view the underlying records.

-   **Tool execution time \(90th percentile\)**

    This area of the dashboard shows the tool execution time within which 90% of tool executions were completed. Only 10% of executions took longer than this time. Select **Related records** to view the underlying records.

-   **Tool execution time \(99th percentile\)**

    This area of the dashboard shows the tool execution time within which 99% of tool executions were completed. Only 1% of executions took longer than this time. Select **Related records** to view the underlying records.

-   **Tool Performance**

    This area of the dashboard shows performance broken down by individual tool. Success % reflects the share of executions that completed without error. P50, P90, and P99 represent execution time percentiles in seconds.

    The table includes the following columns:

    -   **Type**: the tool type. Supported types are Flow actions, Scripts, Subflows, and RAG-based search.
    -   **Tool**: the name of the specific tool invoked.
    -   **Success rate**: the percentage of executions that completed without error.
    -   **P50 Time \(s\)**: median execution time in seconds.
    -   **P90 Time \(s\)**: 90th percentile execution time in seconds.
    -   **P99 Time \(s\)**: 99th percentile execution time in seconds.
    \[Omitted image "aiv-tool-performance.png"\] Alt text: Tool performance table showing success rate and execution time percentiles for each tool, grouped by tool type including Flow actions, Scripts, Subflows, and RAG-based search.


## Insights tab

The **Insights** tab shows intent tracking data and conversation quality signals measured through large language model \(LLM\) transcript analysis.

**Intents**

What customers are calling about and how each intent performs. Displayed metrics are tracked per intent, not per conversation. A single conversation can include several intents.

-   **Intent breakdown**

    This area of the dashboard shows how often each intent was detected and how well it was resolved in the selected date range. Use this table to identify intents with low resolution rates or high live agent transfer counts and focus assistant improvement efforts on those areas.

    The table includes the following columns:

    -   **Intent name**: the intent detected during the conversation. Select **View source records** to view the underlying records for a specific intent.
    -   **Detected count**: the number of times this intent was detected.
    -   **Intent resolution rate**: the percentage of detections where this intent was resolved.
    -   **% Resolved by AI**: the percentage of detections resolved by the AI agent with no human involvement. This percentage uses total detections as the denominator, not resolved detections. It is always less than or equal to the intent resolution rate for the same intent.
    -   **Live Agent Transfer**: the percentage of detections that resulted in a transfer to a live agent.
    You can search the table by intent name and sort by any column. Detections with no matching intent reference are grouped into a single row labelled **No intent detected**.

    **Note:** Resolution rate in this table is measured at the intent level. A session with two intents where only one was resolved counts as unresolved on the **Resolution rate** scorecard on the Overview tab, but contributes to the resolution rate for the completed intent in this table.

    \[Omitted image "aiv-intent-breakdown.png"\] Alt text: Intent breakdown table showing detected count, intent resolution rate, percentage resolved by AI, and live agent transfer rate for each detected intent.

-   **Percent of conversations with multiple intents \(%\)**

    This area of the dashboard shows the percentage of voice conversations in which more than one intent was detected. Use this metric to understand how often callers raise multiple issues in a single call and whether your assistant handles multi-intent conversations effectively. Select **Source records** to view the underlying records.

    \[Omitted image "aiv-percent-conversations-multiple-intents.png"\] Alt text: Scorecard showing the percentage of voice conversations in which more than one intent was detected.

-   **Percent of conversations with no intents detected \(%\)**

    This area of the dashboard shows the percentage of voice conversations in which no intent was detected. These sessions are excluded from resolution rate calculations. Use this metric to identify whether callers are reaching the assistant without a recognised intent, which may indicate gaps in intent coverage or issues with intent detection. Select **Source records** to view the underlying records.

    \[Omitted image "aiv-percent-conversations-no-intents.png"\] Alt text: Scorecard showing the percentage of voice conversations in which no intent was detected.


**Conversation insights**

Key sentiment signals from voice conversations, measured through large language model \(LLM\) transcript analysis. Metrics in this section are marked with the **AI Inferred** tag. Select the chart view on any widget to see how each signal has changed over the selected date range.

-   **User effort required with AI agents**

    This area of the dashboard tracks how much effort a user had to put in during a conversation, based on signals like transfers, wait times, and escalations. Scored as Low, Medium, or High. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-effort-required-with-ai-agents.png"\] Alt text: Donut chart showing user effort distribution across conversations with Low, Medium, and High categories, and a chart toggle to view the distribution over time.

-   **AI agent empathy**

    This area of the dashboard measures how politely and attentively the agent acknowledged the user's needs and concerns throughout the conversation. Scored as Low, Medium, or High. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-ai-agent-empathy.png"\] Alt text: Donut chart showing AI agent empathy scores across conversations with High, Medium, and Low categories, and a chart toggle to view the distribution over time.

-   **User / AI agent confusion**

    This area of the dashboard indicates whether the agent misunderstood or failed to interpret the user's intent at any point in the conversation. Scored as Yes or No. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-ai-agent-confusion.png"\] Alt text: Donut chart showing whether confusion was detected in conversations with Yes and No categories, and a chart toggle to view the distribution over time.

-   **User frustration with AI agents**

    This area of the dashboard indicates whether the user expressed frustration, through complaints, sarcasm, or dissatisfaction, during the conversation. Scored as Yes or No. This is measured through large language model \(LLM\) transcript analysis. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-user-frustration-with-ai-agents.png"\] Alt text: Donut chart showing whether user frustration was detected in conversations with Yes and No categories, and a chart toggle to view the distribution over time.


## Assist consumption tab

**Note:** The data on this tab is for informational purposes only and should not be relied upon as a definitive statement of your AI usage for billing purposes.

The **Assist consumption** tab shows AI agent assist usage metrics for the selected date range. An assist is recorded each time an AI voice agent completes an action during a conversation. Assists are categorised into three tiers based on the number of actions taken by the voice agent: Small, Medium, and Large.

-   **Total assists consumed**

    This area of the dashboard shows the total number of assists consumed by AI voice agents in the selected date range. A daily chart alongside the scorecard shows how assist consumption has changed over time. Select **Related records** to view the underlying records.

    \[Omitted image "aiv-total-assists-consumed.png"\] Alt text: Scorecard showing the total number of AI agent assists consumed in the selected date range, with a percentage change compared to the previous period.

-   **Total assists consumed over time**

    This area of the dashboard shows how the total number of assists consumed by AI voice agents has changed over the selected date range. Hover over a date to view the number of assists consumed for that date.

    \[Omitted image "aiv-total-assists-consumed-over-time.png"\] Alt text: Line chart showing the number of AI agent assists consumed over time, with dates on the horizontal axis and number of assists on the vertical axis.

-   **Total assists consumed by tier**

    This area of the dashboard shows the total assists consumed, broken down by tier: Small, Medium, and Large. Assists consumed outside these three tiers are included in the total but do not appear as a separate tier in the chart.

    \[Omitted image "aiv-total-assists-consumed-by-tier.png"\] Alt text: Donut chart showing total assists broken down into Small, Medium, and Large tiers.

-   **Assist consumption by agent**

    This area of the dashboard shows the average actions per call and total assists consumed, broken down by AI voice agent. Assist tier is based on the number of actions the voice agent took per call. Actions counted per call include tool executions and one additional action for each call that included an authentication event.

    The table includes the following columns:

    -   **AI voice agent**: name of the AI voice agent.
    -   **Average actions per call**: average number of actions the agent took per conversation.
    -   **Assists Consumed**: total number of assists consumed by the agent.
    \[Omitted image "aiv-assist-consumption-by-agent.png"\] Alt text: Table showing assist consumption per AI voice agent, with columns for average actions per call and total assists consumed.


