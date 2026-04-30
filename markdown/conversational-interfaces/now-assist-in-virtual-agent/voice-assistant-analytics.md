---
title: Voice page in assistant analytics
description: View how voice assistants are performing, including total calls, average call duration, conversation outcomes, and user sentiment.
locale: en-US
release: yokohama
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-10-15"
reading_time_minutes: 2
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Voice page in assistant analytics

View how voice assistants are performing, including total calls, average call duration, conversation outcomes, and user sentiment.

The Voice dashboard page aggregates key metrics related to voice assistant usage and performance, including total voice conversations, deflected conversations, conversation outcomes, satisfaction scores, and performance of AI agents invoked by voice assistants.

![Voice dashboard page in Assistant analytics.](../image/NAinVA-assistant-designer-analytics-voice.png "Voice dashboard page in Assistant analytics")

The visualizations on the Voice page help you with the following.

-   Monitor the volume and outcomes of voice assistant interactions to assess adoption and identify areas for improvement.
-   Track inferred customer satisfaction \(CSAT\) score and engagement metrics, helping you enhance user experience and efficiency.
-   Analyze AI agent performance and conversations deflected to optimize voice workflows and reduce reliance on live agents.

## Voice assistants

-   **Total voice conversations**

    This area of the dashboard shows the total number of conversations with voice assistants in the selected date range. Use this metric to track growth in voice interactions and set benchmarks for assistant performance.

    ![Total voice conversations.](../image/NAinVA-assistant-designer-analytics-voice-total-conv.png "Total voice conversations")

-   **Total voice conversations deflected**

    This area of the dashboard shows the number of voice conversations successfully self-handled by voice assistants, measured through large language model \(LLM\) transcript analysis. This metric measures the effectiveness of voice assistants in handling user queries independently.

    ![Total voice conversations deflected.](../image/NAinVA-assistant-designer-analytics-voice-total-deflect.png "Total voice conversations deflected")


## Additional conversation outcomes

-   **Conversations transferred to a live agent**

    This area of the dashboard shows the number of conversations transferred from a voice assistant to a live agent for further assistance. This metric indicates how often users require support beyond what the voice assistant can provide. Use this data to identify common escalation triggers and optimize assistant workflows to reduce unnecessary transfers.

    ![Conversations transferred to a live agent](../image/NAinVA-assistant-designer-analytics-voice-conv-live-agent.png "Conversations transferred to a live agent")

-   **Number of tickets created**

    This area of the dashboard shows the number of tickets, for example, incident and case records, created for follow up actions after a conversation. This highlights instances where user issues required formal tracking and resolution. Monitor ticket creation trends to assess assistant effectiveness and identify areas for improvement in issue resolution.

    ![Number of tickets created.](../image/NAinVA-assistant-designer-analytics-voice-tickets-created.png "Number of tickets created")

-   **Conversations disconnected**

    This area of the dashboard shows the number of conversations that ended abruptly or disconnected before completion. Reveals potential friction points or technical issues in voice interactions. Investigate disconnected conversations to improve assistant reliability and user experience.

    ![Conversations disconnected.](../image/NAinVA-assistant-designer-analytics-voice-conv-disconnect.png "Conversations disconnected")


## Conversations and user insights

-   **Inferred customer satisfaction \(CSAT\) score**

    This area of the dashboard shows the average inferred CSAT score for voice conversations in the selected data range, calculated through LLM transcript analysis. Scored on a 5-point scale, 1 = least satisfied and 5 = most satisfied. This metric tracks user sentiment for voice assistant interactions. Track CSAT trends to evaluate the impact of assistant updates and guide improvements in user experience.

    ![Inferred customer satisfaction (CSAT) score.](../image/NAinVA-assistant-designer-analytics-voice-inferred-csat.png "Inferred customer satisfaction (CSAT) score")

-   **Average voice conversation duration**

    This area of the dashboard shows the average duration of voice conversations before resolution or transfer to live agent. This metric helps assess the efficiency of voice interactions. Use this metric to identify opportunities to streamline conversations and reduce resolution time.

    ![Average voice conversation duration.](../image/NAinVA-assistant-designer-analytics-voice-average-duration.png "Average voice conversation duration")


## Use of AI agents

-   **Deflection by AI agent**

    This area of the dashboard shows the number of conversations deflected per AI agent. This metric measures the effectiveness of individual agents in resolving user issues independently.

    ![Deflection by AI agent.](../image/NAinVA-assistant-designer-analytics-voice-number-deflect.png "Deflection by AI agent")


