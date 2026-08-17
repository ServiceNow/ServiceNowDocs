---
title: Activate ServiceNow Otto Skills
description: Turn on the AI skills to automate tasks such as case summarization, wrap-up completion, and conversational knowledge search- reducing manual work and improving case resolution speed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/activate-now-assist-for-customer-service-management-csm-skills\_0.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Configure, ServiceNow Otto for CSM, Customer Service Management]
---

# Activate ServiceNow Otto Skills

Turn on the AI skills to automate tasks such as case summarization, wrap-up completion, and conversational knowledge search- reducing manual work and improving case resolution speed.

Activation configures which skills agents access, where they appear, and which roles can use them. You customize prompts and set availability conditions so AI capabilities appear only where they add value.

This video provides an overview of how you can set up skills and monitor and analyze usage via the AI Admin Hub console.

\[Omitted video\] Description: Now Assist admin console

Each skill is configured separately, and tailored to support agents across various platforms. The following AI generated skills are available to be configured for use within CSM.

|Skill|Description|
|-----|-----------|
|Chat Summarization|Generate condensed summaries of conversations between agents or Virtual Agents and highlight key points for quick reference. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-chat-summarization-in-now-assist_0.md).|
|Call Summarization|Generate summaries of agent-customer calls within the Active Chat window to capture key call details for better agent follow-up and record keeping. For more information, see [Configure call summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-call-summarization-in-now-assist_0.md).|
|Resolution Notes|Create summaries of case resolutions to help agents quickly understand resolution details and reference notes in future similar interactions. For more information, see [Configure resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-resolution-notes-generation-in-now-assist_0.md).|
|Knowledge Generation|Draft knowledge articles based on resolving case tasks for agents to review and edit before publishing. For more information, see [Configure knowledge generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-knowledge-generation-in-now-assist_0.md).|
|Chat Reply Recommendation|Help agents generate replies for chat messages based on conversation context. For more information, see [Configure chat recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-chat-reply-recommendation-in-now-assist_0.md).|
|Email Recommendation|Generate and refine efficient email responses based on conversation context. For more information, see [Configure email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-email-reply-recommendation-in-now-assist.md).|
|Sentiment Analysis|Analyze case sentiment, trends, and reasoning from case inputs, helping agents resolve cases more efficiently. For more information, see [Configure sentiment analysis case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-sentiment-analysis-in-now-assist.md).|
|Suggested steps|Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution. For more info, see [Configure Suggested Steps Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-suggested-steps-generatin-in-now-assist.md).|
|Sidebar summarization|Generate a summary of Sidebar discussions between agents, requesters, and subject matter experts quickly. For more info, see [Configure Sidebar Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-sidebar-summarization-in-now-assist.md).|
|Case summarization|Summarize the case details and display this information on the case record, helping the agents to come to speed quickly on cases. For more info, see [Configure Case Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/case-summarization-generation-in-now-assist.md).|
|Activity response generation|Automatically generate recommendations for resolution notes, work notes and comments, helping agents add informative updates to case records For more info, see[Configure activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-activity-response-generation.md).|
|Trending topics dashboard|View trending topics across cases with insights and visualizations, helping track trend progression, regional impact, and drill down into specific trends using customizable filters. For more info see, [Configure trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-trending-topics-dashboard.md).|
|Sentiment analysis dashboard|Gain a complete picture of customer sentiment across all cases. This dashboard leverages LLM-powered analysis to explain sentiment trends and their underlying drivers. Drill down into specific patterns to identify root causes and access real-time insights that enable managers to take precise, informed action. For more info, see [Use sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/use-sentiment-analysis-dashboard.md)|
|Customer summarization|Generate concise summaries of customer interactions and case history, capturing key details, decisions, and context in one view. This helps agents quickly understand the customer's situation without reading through lengthy case notes, improving first-contact resolution and personalization. The skill pulls relevant information from case records and activity streams to create a structured summary that enables agents to respond more effectively and efficiently. For more info see, [Configure Customer summarization in ServiceNow Otto for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-customer-summarization-in-now-assist-for-csm.md).|
|Special handling notes summarization|Automatically capture and organize critical handling instructions from customer records, creating a concise summary of special requirements, restrictions, or preferences that agents must know. This helps agents quickly identify important context- such as accessibility needs, communication preferences, or service constraints- without searching through scattered notes. For more info see, [Configure special handling notes summarization in ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-special-handling-notes-summarization-in-now-assist-for-csm.md).|
|AI in portal case form|Enable the customers to receive AI-powered assistance directly within the self-service portal when submitting or updating cases. Customers can get real-time suggestions, recommended solutions, or clarifying questions as they fill out case forms, improving issue description quality and reducing resolution time. For more info, see [Set up AI in the portal case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/set-up-now-assist-in-the-portal-case-form.md).|
|Service Recommendations for Interactions|Use AI to suggest relevant services, products, or solutions to agents during customer interactions based on customer history and needs. Agents receive real-time recommendations that help identify cross-sell and up sell opportunities while addressing the customer's current issue. For more info, see [Configure service recommendations for interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-service-recommendations-int.md)|
|Complaint case summarization|Automatically generate concise summaries of customer complaints, capturing the core issue, customer sentiment, and resolution details in a structured format. This helps agents and managers quickly understand complaint severity and root causes without reading through lengthy complaint notes, enabling faster escalation and resolution. For more info, see [Customer Service Management accelerate complaint case handling AI agent collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/accelerate-complaint-case-handling.md)|

## General Configuration Steps

Each skill has it’s own configuration process. However, skill activation follows the same guided setup. What configuring steps are required varies depending on the skill.

Common Configuration components:

-   **Trigger:** Allows you to configure the circumstances in which a skill is generated. For example, chat summarizations can be configured to generate when the chat handoff is done from a live agent to a live agent.
-   **Input:** Configure the data used to create the information generated by the skill. For example, resolution notes information is generated from the description, short description, work notes, and the additional comments fields of existing case notes.
-   **Availability:** customize how and when the skill capability is active and accessible. For example, email reply recommendations can be configured to be always available. You can also use the condition builder to determine whether a user can activate the skill.
-   **Access:**determine who can access this skill. By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.
-   **Display:** determine where the skill appears. For example, the call summarization skill can be configured to display on forms and workspaces or in the ServiceNow Otto panel.

Saving and activating the configuration setup process is the same across all AI generated skills.

**Finalize and Activate Setup**

1.  After selecting **Review and Activate** to examine changes, select **Done** to close the skill configuration settings.
2.  Select **Skill** to turn on the skill for agents and complete the configuration.

    **Note:** You can clone and customize the activated skills. For more info, see [Clone the ServiceNow Otto for CSM skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/clone-the-now-assist-for-csm-skills.md) and [Customizing a ServiceNow Otto for CSM skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/customizing-now-assist-skills.md)


**Select an LLM provider**: Learn how to select an LLM provider to configure all AI generated skills at once. Your choice controls the intelligence layer for the entire capability. For more info, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md)and [Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/edit-model-providers.md).

