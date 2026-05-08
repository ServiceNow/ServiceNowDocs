---
title: Using Now Assist for Customer Service Management \(CSM\)
description: If you have an agent role, you can summarize the customer chat conversations, summarize the case details, and generate the case resolution notes with the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Now Assist for CSM, Customer Service Management]
---

# Using Now Assist for Customer Service Management \(CSM\)

If you have an agent role, you can summarize the customer chat conversations, summarize the case details, and generate the case resolution notes with the Now Assist for Customer Service Management \(CSM\) application.

## Skills reuse

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data within their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists within the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see Domain separation in the Now Assist Admin console. \(Note that global domain is not the same as global scope. For more information, see Exploring Next Experience pickers.\)

Summarize your chat conversations to understand the chat context quicker:

-   Summarize the chat between the Virtual Agent and the customer when the chat is handed off to a live agent.
-   Summarize the chat between a live agent and a customer when a chat is handed off to another live agent or when an agent wraps up the conversation and ends the interaction.
-   Summarize the chat at any point during the conversation using the `/summarize` quick action.

Summarize the case details to understand the case context quicker. These summaries are useful for long-running or complex cases that include multiple conversations between agents and customers.

Generate the case resolution notes to wrap up cases faster. When you're ready to propose a solution to a customer, this feature can generate resolution notes and add them to the Case form. The resolution notes also provide the context about the case resolution to other agents who might encounter similar issues.

-   **[Summarize a chat conversation by using Now Assist for Customer Service Management \(CSM\)](../task/now-assist-csm-summarize-chat.md)**  
Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Summarize a Sidebar discussion by using Now Assist for Customer Service Management \(CSM\)](../task/summarize-sidebar-conversations.md)**  
Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Generate a chat reply recommendation by using Now Assist for Customer Service Management \(CSM\)](../task/generate-chat-reply-recommendations.md)**  
Generate a reply based on the context of the chat conversation using Now Assist icon. Chat reply recommendations can help provide agents with quick replies to common questions.
-   **[Summarize a case by using Now Assist for Customer Service Management \(CSM\)](../task/now-assist-csm-summarize-case.md)**  
Generate a summary from the fields that you selected on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Generate an email response by using Now Assist for Customer Service Management \(CSM\)](../task/generate-email-reply-recommendations.md)**  
Generate an email response that is based on the case and email context by using the Now Assist icon. With email response, agents can create quick emails or responses, helping minimize errors and ramp up productivity.
-   **[Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)](../task/now-assist-csm-generate-resolution.md#)**  
Generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.
-   **[Generate a knowledge article from the CSM Configurable Workspace and classic environment with Now Assist](../../knowledge-management/task/Now-Assist-generate-article-csm-workspace.md)**  
Generate the knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment with Now Assist.
-   **[Summarize a call by using Now Assist for Customer Service Management \(CSM\)](../task/summarize-a-call-by-using-now-assist-for-customer-service-management-csm.md)**  
Generate a summary of the call conversation between a live agent and a customer by using the call summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Using conversational search in Now Assist panel](using-conversational-search-in-now-assist-panel.md)**  
Get common case-related information from the KBs within the case record by asking questions in the Now Assist panel.
-   **[Using scheduling assistant via GenAI in Virtual Agent](using-scheduling-assistant-via-genai-in-virtual-agent.md)**  
Book, reschedule, and cancel appointments with Virtual Agent conversations using Now Assist. Set up a new appointment, modify an existing one, or cancel an appointment with a streamlined and user-friendly flow.
-   **[Suggested steps generation in Now Assist for Customer Service Management \(CSM\)](../task/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)**  
Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Analyze sentiments in Now Assist for Customer Service Management \(CSM\)](../task/analyze-sentiments-in-now-assist-for-csm.md)**  
Make informed decisions on cases based on requester's sentiment and the reasoning behind it in the Now Assist for Customer Service Management \(CSM\) application.
-   **[Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../task/request-gen-ai-capabilities-csm-now-assist-panel.md)**  
Request the contextual generative AI capabilities, such as a chat summary, case summary, case resolution notes, call summary, or knowledge article generation in the CSMCustomer Service Management application by using the conversational interface in the Now Assist panel.
-   **[Use sentiment analysis dashboard](use-sentiment-analysis-dashboard.md)**  
Visualize and interpret customer sentiment across cases using the sentiment analysis dashboard and GenAI insight cards.
-   **[View trending topics dashboard](view-trending-topics-dashboard.md)**  
Identify clusters of related records and visualize their volumes and sentiment trends over time using the trending topics dashboard and GenAI-generated insights.
-   **[Generate activity stream responses](../task/generate-a-recommendation-to-respond-to-an-activity.md)**  
Generate recommendations for work notes or comments in a case record using Now Assist and add them to enhance the quality of your interactions with the user.
-   **[Use automated quality assurance dashboard as a live agent](use-quality-assurance-dashboard-as-an-agent.md)**  
The automated quality assurance dashboard provides GenAI-generated quality insights for individual agents, including time-based filters, trend analysis, category and parameter breakdowns, with a detailed list of reviewed cases.
-   **[Use automated quality assurance dashboard as a manager](../task/use-quality-assurance-dashboard-as-a-manager.md)**  
Access the automated quality assurance dashboard from the CSM Configurable Workspace to view detailed agent performance metrics and quality assurance scoring data.
-   **[Create a case based on service definition recommendations](../task/use-service-definition-rec.md)**  
Use Now Assist to view AI-predicted service recommendations based on the context of an interaction record, such as the short description or description, and create cases based on these recommendations.
-   **[Using Troubleshooting steps identification AI agent](troubleshooting-steps-identification-ai-agent.md)**  
The Troubleshooting steps identification AI agent fetches the context from a case, identifies the missing context by comparing it with knowledge articles, similar cases, and standard operating documents, and then proposes additional troubleshooting steps.

**Parent Topic:**[Now Assist for Customer Service Management \(CSM\)](now-assist-csm.md)

