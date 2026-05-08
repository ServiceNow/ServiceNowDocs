---
title: Exploring Now Assist for Customer Service Management \(CSM\)
description: With the Now Assist for Customer Service Management \(CSM\) application, your agents can use generative AI to summarize the customer chat conversations and case details to get the context of the case. They can also generate the case resolution notes to share with the other agents and wrap up cases faster.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Now Assist for CSM, Customer Service Management]
---

# Exploring Now Assist for Customer Service Management \(CSM\)

With the Now Assist for Customer Service Management \(CSM\) application, your agents can use generative AI to summarize the customer chat conversations and case details to get the context of the case. They can also generate the case resolution notes to share with the other agents and wrap up cases faster.

Summarize a chat with Now Assist for Customer Service Management.

## Now Assist for Customer Service Management \(CSM\) overview

The following generative AI capabilities are available for an agent:

-   An interaction chat summary provides the context about the chat conversation between your agents and customers at different points of the handoff, such as when a Virtual Agent chat history is handed off to a live agent, or when one live agent hands off a chat history with a customer to another live agent.
-   A case summary enables an agent to gather the case context on long-running or complex cases. Because these cases can contain a lot of information, including the conversations with the customer or other agents, an agent can generate a summary to gain understanding faster.
-   The case resolution notes can assist an agent to help wrap up cases faster and provide the context about the case resolution to the other agents who might encounter similar issues.
-   A call summary assists an agent with obtaining the key details that were discussed during the conversations between the live agents and customers. It provides a high-level overview of the conversation in a clear format.
-   Knowledge generation can help an agent to streamline content creation. An agent can automatically generate knowledge articles by using the relevant data from the case record after proposing a resolution or closing the case. By not having to generate knowledge articles manually, this feature can save your agents valuable time and effort.
-   Sidebar summary captures discussions between agents, requesters, and experts, and can be posted to case notes for further troubleshooting.
-   Chat recommendation generates reply suggestions for agents using the Now Assist context menu.
-   Email response generates reply suggestions for agents from existing or new emails using the Now Assist context menu.
-   Sentiment analysis helps reduce escalated cases by providing agents with the most current sentiment on a case, based on customer interactions and the latest trends. It also offers insights into why the sentiment is what it is today.
-   Suggested steps generation resolves cases and boosts agent productivity by automatically outlining the next best actions for unfamiliar cases in the Recommended Actions tab.
-   Sentiment analysis on an account uses filters and sorting dashboards to track sentiment, providing valuable insights and reducing escalated cases.
-   Conversational subflows and actions in the Now Assist panel use natural language to trigger subflows or actions, improving agent productivity and allowing them to complete tasks efficiently within the panel.

-   The Portal case form guides requesters through a self-service flow using Genius Results, helping them find solutions and reducing the number of cases created.

## Now Assist for Customer Service Management \(CSM\) skills

The Now Assist for CSM application includes the generative AI skills that enable your agents to understand the chat and case context so that they can propose resolutions to the customer more quickly.

-   **Chat summarization**

    Provides an agent with a summary of a customer's Virtual Agent chat history, live agent chat history, and the interaction history. Agents can view or create the following summaries:

    -   Virtual Agent chat handoff summary: Summarizes the conversation when Virtual Agent hands off a chat to a live agent​ and displays the summary in the Active Chat window. An agent can view a summary of the actions that were taken by a customer before engaging with a live agent.
    -   Live Agent to Live Agent handoff summary: Summarizes the conversation when a live agent hands off a chat to another live agent​ and displays the summary in the Active Chat window. An agent can view a summary of the actions that were taken by a customer before hand off to another live agent.
    -   Quick action summary: Provides a summary when an agent uses the `/summarize` quick action in the Active Chat window.
    -   Chat wrap up summary: Populates the **Chat Summary** and **Short description** fields on the interaction record when a live agent wraps up a chat with a customer.

        **Note:** If a chat summary isn’t available for the interaction, the **Chat Summary** field doesn’t appear on the interaction record.

    ![AI-generated chat summaries for an interaction.](../image/now-assist-csm-chat-summary.png "Interaction record with chat summaries")

-   **Sidebar discussion summarization**

    Provides an agent with a summary of the sidebar discussions between agents, requesters, and subject matter experts. An agent can also post the summary to the case work notes for further troubleshooting before or after the chat ends.

    ![Choose participants to start a discussion.](../image/now-assist-sidebar-discussion.png "Sidebar discussion modal")

-   **Chat reply recommendation**

    Enables an agent to generate a reply recommendation from a chat using Now Assist context menu.

    The chat reply recommendation skill displays a pop-up window that an agent can use to generate a recommendation and review it before sending it as a reply.

    ![Modal that enables an agent to generate a reply recommendation from a chat.](../image/now-assist-chat-reply-recommendation.png "Now Assist context menu")

-   **Case summarization**

    Provides an agent with a summary of a customer service case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context, refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The case summarization skill generates a case summary and displays it above the activity stream. The summary includes the information that the agent enters in the following case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Email
    -   Service level agreement \(SLA\)
    ![AI-generated case summary for a case record.](../image/now-assist-csm-case-summary.png "Case record with case summary")

-   **Email response**

    Enables an agent to generate an email response from an existing or new email using Now Assist context menu.

    The email response skill displays a pop-up window that an agent can use to generate a recommendation and review it before sending it as a reply.

    ![Pop-up window that an agent can use to generate a recommendation and review it before sending it as a reply in an email.](../image/now-assist-email-reply-recommendation.png "Now Assist context menu modal")

-   **Resolution notes generation**

    Enables an agent to generate the resolution notes for a case, propose the resolution to the customer, and add the information to the case record.

    The resolution notes that generation skill displays a pop-up window that an agent can use to select a resolution code and review the resolution notes text before proposing a resolution to a customer.

    ![AI-generated resolution information for a case record.](../image/now-assist-csm-propose-solution-modal.png "Resolution notes generation pop-up window")

    **Note:** The resolution notes generation skill requires a minimum of 50 words in the case record to generate the resolution notes. If the resolution notes can't be generated, the system displays a message below the **Resolution notes** field.

-   **Knowledge generation**

    Enables an agent to generate a knowledge article from a case after proposing a resolution or closing the case.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article that is based on similar cases and review it before publishing the knowledge article draft.

    ![Al-generated knowledge article information for a case record.](../image/now-assist-kb-dialog-box.png "Knowledge article generation pop-up window")

-   **Call summarization**

    Provides an agent with a call summary when the call ends and includes the main points discussed during the call, including the issue and the actions taken. An agent can generate a call summary of the interaction to understand the case context and post the summary to the case work notes. An agent can view or create the following summaries:

    -   Chat wrap up summary: Populates the **Chat Summary** and **Short description** fields on the interaction record when a live agent wraps up a chat with a customer.

        **Note:** If a call summary isn’t available for the interaction, the **Chat Summary** field doesn't appear on the interaction record.

    -   Call summary from the Now Assist panel: Creates a summary of the conversation between the agent and customer from the Now Assist panel by selecting **Summarize conversation**.
    ![AI-generated call summary for an interaction.](../image/now-assist.csm-call-summary.png "Interaction record with call summary")


## Sentiment analysis on a case

Sentiment analysis helps reduce escalated cases by providing agents with the most current sentiment on a case, based on customer interactions and the latest trends. It also offers insights into why the sentiment is what it is today.

![The case shows that the sentiment is positive and improving](../image/sentiment-analysis-form-view-configurable-workspace.png "Sentiment analysis on a case") ![]( "Sentiment analysis on a case")

## Sentiment analysis on an account

Track the sentiment of a business-to-business account using filters and sorting dashboards to gain valuable insights and reduce escalated cases.

![Sentiment on accounts showing trends in the dashboard view](../image/sentiment-analysis-dashboard.png "Sentiment analysis on an account")

## Conversational subflows and actions in Now Assist panel

Use natural language to trigger subflows or actions, enhancing agent productivity and allowing them to complete tasks efficiently within the Now Assist panel. For more info, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../task/request-gen-ai-capabilities-csm-now-assist-panel.md).

## Now Assist in Portal case form

Guide requesters through a self-service flow using Genius Results to find solutions and reduce the number of cases created. For more info, see [Using Now Assist in portal case form](using-ai-search-with-q-a-within-the-portal-form.md).

## Suggested steps generation

Suggested steps generation may help resolve cases and boost agent productivity by outlining the next best actions for unfamiliar cases in the Recommended Actions tab.

![Suggested steps by Now Assist to resolve the issue](../image/suggested-steps.png "Suggested steps")

## Activity response generation

Use the activity response generation skill to automatically generate recommendations for resolution notes, work notes, and comments. This feature helps agents add meaningful updates to case records, improving efficiency, and interaction. For more info, see [Generate activity stream responses](../task/generate-a-recommendation-to-respond-to-an-activity.md).

## Trending topics dashboard

Get a comprehensive view of trending topics across cases along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and drill down into specific trends using customizable filters. For more info, see [View trending topics dashboard](view-trending-topics-dashboard.md). ![Dashboard showing trending topics with a table of top 10 trends and metrics, with colorful bar charts for GenAI generated insights on impacted accounts, products, assignment groups, and channels.](../image/trending-topics-dashboard.png)

## Sentiment analysis dashboard

Get a comprehensive view of customer sentiment across cases and accounts. The dashboard uses Now LLM Service insights to explain sentiment changes and lets you drill down to find root causes—helping teams take targeted actions. For more info, see [Use sentiment analysis dashboard](use-sentiment-analysis-dashboard.md). ![Dashboard showing sentiment trend line chart, sentiment breakdown by channel, and multiple bar charts for negative and positive drivers, assignment groups, escalation impact, and case counts by channel.](../image/sentiment-trends-dashboard.png)

## Now Assist panel in CSM Configurable Workspace

An agent can use the Now Assist panel in CSM Configurable Workspace. This conversational interface enables an agent to request a chat summary or case summary and generate the case resolution notes. For more information about the Now Assist panel, see Now Assist panel.

## Now Assist in AI Search

The Now Assist in AI Search application uses Now LLM Service to extract actionable Q&amp;A Genius Result answers from the knowledge articles that are found in Service Portal, Virtual Agent, Employee Center, and global searches. By using this application, an agent can improve the customer's experience by retrieving the relevant content from the knowledge base and generating concise answers. For more information, see Now Assist in AI Search.

## Now Assist in Virtual Agent

Now Assist in the Virtual Agent guided setup can reduce the time and effort needed to deploy Now Assist within Virtual Agent. Your administrators can configure features and skills as well as sources of information such as knowledge bases and catalogs. For more information, see Configure Now Assist in Virtual Agent.

With the Now Assist Multi-Turn Catalog Requests skill, your customers can engage with Virtual Agent in a conversational manner to request catalog items. A customer can request an item and then refine their search by providing additional information. For more information, see Multi-turn catalog ordering.

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it does not appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service is not exposed to any sensitive information. For more information, see Multi-turn catalog ordering.

-   **[Supporting information for Now Assist for Customer Service Management \(CSM\)](now-assist-csm-supporting-info.md)**  
Get a quick overview of the important information that is related to the Now Assist for Customer Service Management \(CSM\) application.

**Parent Topic:**[Now Assist for Customer Service Management \(CSM\)](now-assist-csm.md)

**Related topics**  


[bundle-platai.platform-now-assist-landing]

[bundle-platai.exploring-now-assist-platform]

