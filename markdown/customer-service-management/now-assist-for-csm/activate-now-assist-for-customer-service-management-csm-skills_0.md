---
title: Activate Now Assist Skills
description: Enable Now Assist generative AI skills to provide AI-driven capabilities such as summarization, response suggestions, and sentiment analysis.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Activate Now Assist Skills

Enable Now Assist generative AI skills to provide AI-driven capabilities such as summarization, response suggestions, and sentiment analysis.

This video provides an overview of how you can set up skills and monitor and analyze usage via the Now Assist Admin console.

Now Assist admin console 

Each skill is configured separately, and tailored to support agents across various platforms. The following Now Assist skills are available to be configured for use within CSM.

|Skill|Description|
|-----|-----------|
|Chat Summarization|Generate condensed summaries of conversations between agents or Virtual Agents and highlight key points for quick reference. For more information, see [Configure chat summarization](../task/configure-chat-summarization-in-now-assist_0.md).|
|Call Summarization|Generate summaries of agent-customer calls within the Active Chat window to capture key call details for better agent follow-up and record keeping. For more information, see [Configure call summarization](../task/configure-call-summarization-in-now-assist_0.md).|
|Resolution Notes|Create summaries of case resolutions to help agents quickly understand resolution details and reference notes in future similar interactions. For more information, see [Configure resolution notes generation](../task/configure-resolution-notes-generation-in-now-assist_0.md#).|
|Knowledge Generation|Draft knowledge articles based on resolving case tasks for agents to review and edit before publishing. For more information, see [Configure knowledge generation](../task/configure-knowledge-generation-in-now-assist_0.md).|
|Chat Recommendation|Help agents generate replies for chat messages based on conversation context. For more information, see [Configure chat recommendation](../task/configure-chat-reply-recommendation-in-now-assist_0.md).|
|Email Recommendation|Generate and refine efficient email responses based on conversation context. For more information, see [Configure email recommendation](../task/configure-email-reply-recommendation-in-now-assist.md).|
|Sentiment Analysis|Analyze case sentiment, trends, and reasoning from case inputs, helping agents resolve cases more efficiently. For more information, see [Configure sentiment analysis case](../task/configure-sentiment-analysis-in-now-assist.md).|
|Suggested steps|Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution. For more info, see [Configure Suggested Steps Generation](../task/configure-suggested-steps-generatin-in-now-assist.md#).|
|Sidebar summarization|Generate a summary of Sidebar discussions between agents, requesters, and subject matter experts quickly. For more info, see [Configure Sidebar Summarization](../task/configure-sidebar-summarization-in-now-assist.md).|
|Case summarization|Summarize the case details and display this information on the case record, helping the agents to come to speed quickly on cases. For more info, see [Configure Case Summarization](../task/case-summarization-generation-in-now-assist.md).|
|Activity response generation|Automatically generate recommendations for resolution notes, work notes and comments, helping agents add informative updates to case records For more info, see[Configure activity response generation](../task/configure-activity-response-generation.md).|
|Trending topics dashboard|View trending topics across cases with insights and visualizations, helping track trend progression, regional impact, and drill down into specific trends using customizable filters. For more info see, [Configure trending topics dashboard](../task/configure-trending-topics-dashboard.md).|
|Sentiment analysis dashboard|Gain a complete picture of customer sentiment across all cases. This dashboard leverages LLM-powered analysis to explain sentiment trends and their underlying drivers. Drill down into specific patterns to identify root causes and access real-time insights that enable managers to take precise, informed action. For more info, see [Use sentiment analysis dashboard](use-sentiment-analysis-dashboard.md)|

## General Configuration Steps

Each skill has it’s own configuration process. However, skill activation follows the same guided setup. What configuring steps are required varies depending on the skill.

Common Configuration components:

-   **Trigger:** Allows you to configure the circumstances in which a skill is generated. For example, chat summarizations can be configured to generate when the chat handoff is done from a live agent to a live agent.
-   **Input:** Configure the data used to create the information generated by the skill. For example, resolution notes information is generated from the description, short description, work notes, and the additional comments fields of existing case notes.
-   **Availability:** customize how and when the skill capability is active and accessible. For example, email reply recommendations can be configured to be always available, or defined using the condition builder to determine whether or not a user can activate the skill.
-   **Access:**determine who can access this skill. By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.
-   **Display:** determine where the skill appears. For example, the call summarization skill can be configured to display on forms and workspaces or in the Now Assist panel.

Saving and activating the configuration setup process is the same across all Now Assist skills.

**Finalize and Activate Setup**

1.  After selecting **Review and Activate** to examine changes, select **Done** to close the skill configuration settings.
2.  Select **Skill** to turn on the skill for agents and complete the configuration.

