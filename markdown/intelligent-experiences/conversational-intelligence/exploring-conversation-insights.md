---
title: Exploring Conversation Insights
description: Learn how Conversation Insights can help you to augment conversation insights with AI-based Inferred customer satisfaction \(CSAT\) scores and factors.
locale: en-US
release: australia
product: Conversational Intelligence
classification: conversational-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Conversation Insights, Enable AI experiences]
---

# Exploring Conversation Insights

Learn how Conversation Insights can help you to augment conversation insights with AI-based Inferred customer satisfaction \(CSAT\) scores and factors.

## Conversation Insights overview

Conversation Insights is designed to deliver Inferred CSAT scores and explanatory factors for conversations in Virtual Agent and agentic workflows. It leverages AI to analyze conversations in real time, and provides actionable insights that help improve Virtual Agent and live agent interactions, and agentic workflows.

Inferred CSAT is a numerical score from 1 \(least satisfied\) to 5 \(most satisfied\). It’s predicted entirely from conversation transcripts in real time without any input from the user. In addition to the CSAT score, the model also predicts CSAT factors that contributed to the CSAT score. The following CSAT factors are associated with the Inferred CSAT score.

-   Resolution: Indicates whether the Virtual Agent or AI agent successfully resolved the user's issue without human intervention.
-   Confusion: Indicates how often the Virtual Agent or AI agent misunderstood or failed to interpret the user's intent.
-   Effort: Indicates the number of user turns or interactions required to reach a resolution.
-   Empathy: Indicates how well the Virtual Agent or AI agent acknowledged and responded to the user's emotional tone.
-   Next Steps: Captures whether the Virtual Agent or AI agent clearly communicated what the user should do next.
-   Frustration: Flags signs of user dissatisfaction or repeated failed attempts during the interaction.
-   Transfers and Escalations: Tracks how often the Virtual Agent or AI agent handed off the conversation to a human agent or another system.

Inferred CSAT scores and factors are calculated for each conversation. Conversational analytics applications can leverage the scores written to the Conversation Insights \[sn\_aci\_insights\] table to create custom dashboards and workflows. The [AI Agent Analytics dashboard](../../now-assist-ai-agents/concept/ai-agent-dashboard.md) includes visualizations with Inferred CSAT scores and factors by default.

The data retention period for the Conversation Insights \[sn\_aci\_insights\] table is two years. For more information on creating custom dashboards, see [Create a dashboard with the in-line editor](https://www.servicenow.com/docs/access?context=create-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) and [Select a table data source for a data visualization](https://www.servicenow.com/docs/access?context=select-table-data-source&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

Conversation Insights are also supported by Voice Agents, Now Assist Panel and Now Assist Virtual Agent.

To view the conversation insights for Voice Agents, go to **Assistant Designer** &gt; **Analytics** &gt; **Sentiment** dashboard.

To view the conversation insights for Now Assist Panel or Now Assist Virtual Agent, go to **Platform Analytics** &gt; **Dashboards** &gt; **AI Engagement Analytics**.

## Inferred CSAT segmented by intent

Use the additional insights introduced to report on Inferred CSAT segmented by intent. It gives better insights into why customers contact the brand and how well their needs are met. This helps companies quickly spot and fix issues with their top customer intents.

The score for Inferred CSAT segmented by intent is automatically generated when customers upgrade the Conversation Insights app. It requires a minimum sample size of 500 conversations to start and samples up to 2000 records every 15 minutes.

These metrics are available in the [AI Agent Analytics dashboard](../../now-assist-ai-agents/concept/ai-agent-dashboard.md), under the Insights tab, where you can find two new charts.

## Conversation Insights workflow

The Conversation Insights workflow illustrates how each interaction, whether handled by Virtual Agent or an AI agent, is transformed into actionable insights. You can feed the insights directly into the dashboards for analysis and decision making. The Conversation Insights workflow shows the journey from conversations to insights on dashboards.

![Infographic shows how the Conversation Insights application derives insights from conversations. For the text description, refer to the description that follows.](../image/conversation-insights-workflow-landing.svg "Conversation Insights workflow")

1.  Conversation sources
    -   Agentic AI chats
    -   Virtual Agent chats
2.  Data aggregation
    -   Agentic AI and Virtual Agent interactions are captured in the Conversation table \[sys\_cs\_conversation\].
    -   The conversation transcript, including user query, agent response, timestamps, and metadata such as the session ID and channel type are also stored in the Conversation table for processing.
3.  Insight generation
    -   The model analyzes the conversation transcript.
    -   Inferred CSAT scores are generated for CSAT factors such as Empathy, Resolution, Frustration, and so on.
4.  Insights storage
    -   Inferred CSAT scores and factors are stored in the Conversation Insights table \[sn\_aci\_insights\].
    -   The Conversation Insights table acts as a structured repository for the extracted insights.
5.  Dashboards
    -   The insights are made available to create adhoc dashboards and workflows.
    -   You can explore trends, performance metrics, and target improvements based on the Inferred CSAT scores.

## Conversation Insights benefits

|Problem|Solution|
|-------|--------|
|Traditional surveys often reflect extreme opinions and low response rates.|Inferred CSAT helps solve this problem by using AI to estimate CSAT score for conversations in real time, based on full conversation transcript. This CSAT score can help to eliminate bias and reduce the need for reliance on explicit survey feedback.|
|Post-interaction feedback delays insights resulting in lagging indicators.|CSAT scores are generated immediately after the interaction, enabling faster detection of issues and trends.|
|Lack of actionable insight behind CSAT scores.|CSAT factors like Resolution, Empathy, Effort, and so on explain user satisfaction or dissatisfaction, helping you to target improvements.|

## What to explore next

To learn more about configuring and using Conversation Insights, see:

-   [Install Conversation Insights](install-conversation-insights.md)
-   [Conversation Insights reference](conversation-insights-reference.md)

