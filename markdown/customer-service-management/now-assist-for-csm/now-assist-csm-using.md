---
title: Using ServiceNow Otto for Customer Service Management \(CSM\)
description: If you have an agent role, you can summarize the customer chat conversations, summarize the case details, and generate the case resolution notes with the ServiceNow Otto for Customer Service Management \(CSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-using.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [ServiceNow Otto for CSM, Customer Service Management]
---

# Using ServiceNow Otto for Customer Service Management \(CSM\)

If you have an agent role, you can summarize the customer chat conversations, summarize the case details, and generate the case resolution notes with the ServiceNow Otto for Customer Service Management \(CSM\) application.

## Skills reuse

By default, all skills exist in the global domain. When you use ServiceNow Otto in a domain-separated environment, users are only able to access data within their domain. For example, if a user uses the summarization skill, ServiceNow Otto only uses material that exists within the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/next-experience-pickers.md).\)

Summarize your chat conversations to understand the chat context quicker:

-   Summarize the chat between the Virtual Agent and the customer when the chat is handed off to a live agent.
-   Summarize the chat between a live agent and a customer when a chat is handed off to another live agent or when an agent ends the interaction.
-   Summarize the chat at any point during the conversation using the `/summarize` quick action.

Summarize the case details to understand the case context quicker. These summaries are useful for long-running or complex cases that include multiple conversations between agents and customers.

Generate the case resolution notes to wrap up cases faster. When you're ready to propose a solution to a customer, this feature can generate resolution notes and add them to the Case form. The resolution notes also provide the context about the case resolution to other agents who might encounter similar issues.

-   **[Summarize a chat conversation by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-chat.md)**  
Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer by using the chat summarization skill in the ServiceNow Otto for Customer Service Management \(CSM\) application.
-   **[Summarize a Sidebar discussion by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/summarize-sidebar-conversations.md)**  
Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the ServiceNow Otto for Customer Service Management \(CSM\) application.
-   **[Generate a chat reply recommendation by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.md)**  
Generate a reply based on the context of the chat conversation using ServiceNow Otto icon. Chat reply recommendations can help provide agents with quick replies to common questions.
-   **[Summarize case insights by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-case.md)**  
Use ServiceNow Otto for Customer Service Management \(CSM\) to generate a consolidated view of case insights directly from the case record. The **Case Insights** section surfaces a summary of the case alongside key contextual information to help service reps understand and act on cases quickly.
-   **[Generate an email response by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/generate-email-reply-recommendations.md)**  
Generate an email response that is based on the case and email context by using the AI icon. With email response, agents can create quick emails or responses, helping minimize errors and ramp up productivity.
-   **[Generate the resolution notes for a case by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-generate-resolution.md)**  
Generate resolution notes for a case and propose the resolution to the customer by using the resolution notes generation skill in ServiceNow Otto for Customer Service Management \(CSM\). This helps you wrap up cases faster and provide resolution information to other agents who might encounter similar issues.
-   **[Generate a knowledge article with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/Now-Assist-generate-article-csm-workspace.md)**  
Generate knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment using ServiceNow Otto.
-   **[Summarize a call by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/summarize-a-call-by-using-now-assist-for-customer-service-management-csm.md)**  
Generate a summary of the call conversation between a live agent and a customer by using the call summarization skill in the ServiceNow Otto for Customer Service Management \(CSM\) application.
-   **[Using conversational search in ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/using-conversational-search-in-now-assist-panel.md)**  
Get common case-related information from the KBs within the case record by asking questions in the panel.
-   **[Using scheduling assistant via GenAI in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/using-scheduling-assistant-via-genai-in-virtual-agent.md)**  
Book, reschedule, and cancel appointments with Virtual Agent conversations using ServiceNow Otto Setup a new appointment, modify an existing one, or cancel an appointment with a streamlined and user-friendly flow.
-   **[Suggested steps generation in ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)**  
Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution in the ServiceNow Otto for Customer Service Management \(CSM\) application.
-   **[Analyze sentiments in ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.md)**  
Make informed decisions on cases and email interactions based on requester's sentiment and the reasoning behind it in the ServiceNow Otto for Customer Service Management \(CSM\) application.
-   **[Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/request-gen-ai-capabilities-csm-now-assist-panel.md)**  
Request generative AI capabilities such as chat summaries, case summaries, resolution notes, and more using the ServiceNow Otto panel.
-   **[Use sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/use-sentiment-analysis-dashboard.md)**  
Visualize and interpret customer sentiment across cases using the sentiment analysis dashboard and GenAI insight cards.
-   **[View trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/view-trending-topics-dashboard.md)**  
Identify clusters of related records and visualize their volumes and sentiment trends over time using the trending topics dashboard and GenAI-generated insights.
-   **[Generate activity stream responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/generate-a-recommendation-to-respond-to-an-activity.md)**  
Generate recommendations for work notes or comments in a case record using ServiceNow Otto and add them to enhance the quality of your interactions with the user.
-   **[Use automated quality assurance dashboard as a live agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/use-quality-assurance-dashboard-as-an-agent.md)**  
The automated quality assurance dashboard provides GenAI-generated quality insights for individual agents, including time-based filters, trend analysis, category and parameter breakdowns, with a detailed list of reviewed cases.
-   **[Use automated quality assurance dashboard as a manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/use-quality-assurance-dashboard-as-a-manager.md)**  
Access the automated quality assurance dashboard from the CSM Configurable Workspace to view detailed agent performance metrics and quality assurance scoring data.
-   **[Create a case based on service definition recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/use-service-definition-rec.md)**  
Use ServiceNow Otto to view AI-predicted service recommendations based on the context of an interaction record, such as the short description or description, and create cases based on these recommendations.
-   **[Using Troubleshooting steps identification AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/troubleshooting-steps-identification-ai-agent.md)**  
The Troubleshooting steps identification AI agent analyzes case context by comparing it with knowledge articles, similar cases, and standard operating documents. It then proposes additional troubleshooting steps.

**Parent Topic:**[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm.md)

