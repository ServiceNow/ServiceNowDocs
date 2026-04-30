---
title: Exploring Now Assist for HR Service Delivery \(HRSD\)
description: With the Now Assist for HR Service Delivery \(HRSD\) application, your agents can summarize the customer chat conversations and case details to get the context of the case, generate the case resolution notes, and wrap up cases faster.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Exploring Now Assist for HR Service Delivery \(HRSD\)

With the Now Assist for HR Service Delivery \(HRSD\) application, your agents can summarize the customer chat conversations and case details to get the context of the case, generate the case resolution notes, and wrap up cases faster.

## Now Assist for HR Service Delivery \(HRSD\) Overview

The following generative AI capabilities are available for an agent:

-   A case summary provides an agent with a concise summary of a case. It ​enables an agent to get the context by gathering information about an issue and taking actions more quickly​. It ​also enables an agent to refresh and post the summary to the work notes.
-   The case resolution notes can help an agent to wrap up cases faster and provide the context about the case resolution to the other agents who might encounter similar cases.
-   An interaction chat history provides the context about the chat conversation between the agents and requesters at different points of the handoff, such as when the Virtual Agent conversation chat history is handed off to a live agent.

The following generative AI capabilities are available for employees or administrators:

-   Get direct and actionable responses on customer-specific content by using generative AI in search.
-   Enhance self-service by using the new Now LLM Service powered Virtual Agent experience with a simplified set-up experience.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Now Assist for HR Service Delivery \(HRSD\) Skills

The Now Assist for HRSD application includes the generative AI skills and features that enable your agents to understand the chat and case context so that they can propose resolutions to the requester more quickly.

-   **Chat summarization**

    Provides an agent with a chat summary of all points of the handoff, including the Virtual Agent conversation and the live agent conversation:

    -   Quick action summary: Provides a concise summary of the interactions with the quick actions that the agent took.
    -   Virtual Agent handoff summary: Summarizes the chat when Virtual Agent hands off the chat to a live agent​.
    -   Live Agent to Live Agent handoff summary: Summarizes the conversation when a live agent hands off a chat to another live agent and displays the summary in the Active Chat window. An agent can view a summary of the actions that were taken by a customer before hand off to another live agent.
    -   Chat wrap up summary: Accelerates the wrap-up time by populating the full chat summary when a conversation ends.
    -   Chat wrap up short description: Accelerates the wrap-up time by populating the short description that summarizes the requester issues when the conversation ends​.
    For information on activating the chat summarization skill, see [Configure chat summarization and chat reply recommendation skills in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=configure-chat-summarization-in-the-now-assist-admin-console&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For information on how to use the skill on Agent Workspace for HR Case Management, see [Summarize a chat conversation by using Now Assist for HR Service Delivery \(HRSD\)](../task/now-assist-hrsd-chat.md).

    The following example shows an AI-generated chat summary.

    ![AI-generated chat summary that is shown to the agent in Workspace. For the text description of the workflow, refer to the following list.](../image/summary-chat.png "AI-generated chat summary")

    -   1: The agent accepts the chat with the requester and gets any additional details.
    -   2: The agent provides the details and ends the conversation.
    -   3: The chat summarization skill automatically updates the short description in the **Short description** field.
    -   4: The chat summarization skill automatically updates the chat summary in the **Chat Summary** field.
-   **Case summarization**

    Provides an agent with a concise summary of a case, including the issue, actions that were taken, SLA, attachment summary and resolution information, depending on the state of the case. An agent can view a case summary to understand the case context, refresh the summary, and post the summary to the case work notes.

    For information on activating the case summarization skill, see [Configure case or incident summarization in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=configure-case-or-incident-summarization-in-the-now-assist-admin-console&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For information on how to use the skill on Agent Workspace for HR Case Management or Core UI, see [Summarize an HR case using Now Assist for HRSD](../task/now-assist-hrsd-summarize-case.md).

    The following example shows an AI-generated case summary.

    ![HR case summary that is generated by Now Assist in the Workspace.](../image/case-summarization2.png "AI-generated case summary on Agent Workspace for HR Case Management")

-   **Resolution notes generation**

    Automatically generates the resolution notes for an agent when the state of a case is changed to Closed Complete. An agent can accept the AI-generated notes or edit the notes before saving it to the case.

    For information on activating the resolution notes skill, see [Configure Now Assist for HR Service Delivery \(HRSD\)](../task/configure-now-assist-hr.md). For information on how to use the skill on Agent Workspace for HR Case Management, see [Generate resolution notes using Now Assist for HRSD](../task/now-assist-hrsd-res-note.md).

    The following example shows the AI-generated resolution notes.

    ![Add resolution notes dialog box with generated resolution notes that read "Provided link to Career Level Guide for Solution Consulting."](../image/gen-resolution-note2.png "AI-generated resolution notes")

-   **Knowledge generation**

    Enables an agent to generate a knowledge article from a case after proposing a resolution or closing the case.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article and review it before publishing the knowledge article draft.


## Redirection for sensitive topics

Certain subjects, such as workplace safety or employee compensation, might not be suited for generative AI conversations. Now Assist for HR Service Delivery \(HRSD\) includes out-of-the-box filters to detect sensitive topics.

The admin activates the filters or creates custom filters to enable the Virtual agent to detect if these kinds of subjects are included in the conversation and offer the following redirection options:

-   **Live agent**

    The employee is redirected to the relevant chat queue to connect with a live agent.

-   **Case**

    The employee can open a case, which is assigned to the respective HR service.

-   **Proceed, this is not sensitive**

    In situations where the LLM incorrectly identifies a phrase as a sensitive topic, employees can opt to continue the interaction with the Virtual Agent.


![Options for detected sensitive topics](../image/sensitivity-detection.png)

For more information on the out-of-the-box filters and how they are mapped to chat queues and HR case services, see [Sensitivity detection filters mapping](../reference/reference-sd-info-values.md).

For information on setting up sensitivity detection, see [Configure sensitivity detection](../task/config-na-sd-filters.md).

## Now Assist panel in the Agent Workspace for HR Case Management

The Now Assist panel provides agents with a conversational interface that they can use to request the chat and case summaries on demand.

For more information about the Now Assist panel, see [Use the Now Assist panel in Agent Workspace for HR Case Management](../task/now-assist-panel-hr.md). ![Now Assist panel menu in Workspace.](../image/now-assist-icon.png)

## Now Assist AI Helper – Galileo Inside

Enable users to access HR articles and industry research from Galileo by The Josh Bersin Company in the Now Assist panel or Now Assist Virtual Agent.

HR professionals, managers, and employees can submit queries on topics including company-specific policies or industry-wide best practices. Now Assist AI Helper – Galileo Inside generates responses based on the KB articles on the customer instance, as well as articles and documents in the Galileo library.

![Galileo Inside responses contain in-text citations and source URLs](../image/galileo-now-assist.png)

Galileo Inside uses Retrieval-Augmented Generation \(RAG\) to generate responses to user queries based on relevant articles and research, delivering accurate domain-specific information in real time.

A one-time configuration provides continuous access to the Galileo library with monthly updates to ensure users have the latest information. For more information, see [Configure Now Assist AI Helper – Galileo Inside](../task/configuring-galileo-inside.md).

