---
title: Summarize a chat conversation by using Now Assist for HR Service Delivery \(HRSD\)
description: Summarize a Virtual Agent chat history in the Now Assist for HR Service Delivery \(HRSD\) application. You can also summarize an interaction when the chat ends. The summary includes all points of the handoff, including the Virtual Agent conversation.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Summarize a chat conversation by using Now Assist for HR Service Delivery \(HRSD\)

Summarize a Virtual Agent chat history in the Now Assist for HR Service Delivery \(HRSD\) application. You can also summarize an interaction when the chat ends. The summary includes all points of the handoff, including the Virtual Agent conversation.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

In a Virtual Agent conversation, when a requester chooses to connect to a live agent, a chat interaction appears in the inbox of an agent. You can also summarize an interaction when the chat ends. The summary includes all points of the handoff, including the Virtual Agent conversation.

**Note:**

The chat summarization admin configuration for ITSM and HR are similar. If at least one of them is enabled, you can generate a chat summary from both workspaces.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Agent Workspace for HRSD**.

2.  In Workspace, open the inbox.

3.  Accept the chat interaction.

    In the Active Chat window, a summary of the Virtual Agent conversation is generated. The summary includes the actions that were taken before the requester engaged with the live agent.

4.  Chat with the requester to get any additional details.

5.  In the Active Chat window, use the `/summarize` quick action to summarize the chat during the conversation with the requester.

6.  End the chat conversation by selecting **End Chat**.

    The chat summarization updates the **Short description** and **Chat Summary** fields when you end the chat.

7.  Review the text in the **Short description** or **Chat Summary** fields and make the necessary changes.![Review the text in theShort description orChat Summary fields and make the necessary changes.](../image/chat-summary.png)

    Because the information in these fields is automatically generated, it's a good idea to review the text and make sure that it's accurate.

8.  Select **Save**.

9.  If you think that you need further help after the initial troubleshooting before or after ending the chat, create a case from the interaction by selecting **Create HR case**.

10. When you create a case before or after ending the chat, the **Short Description** and **Description** fields of the case are updated with the interaction summary.

    **Note:** Generative AI doesn’t override an existing short description that is in the HR case template.


**Parent Topic:**[Use Now Assist for HR Service Delivery \(HRSD\)](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a Sidebar discussion by using Now Assist for HR Service Delivery \(HRSD\)](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](chat-recommendations-nahr.md)

[Generate a knowledge article from HR Agent Workspace with Now Assist](gen-kb-now-assisthr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](email-recommendation-nahr.md)

[Summarize an HR case using Now Assist for HRSD](now-assist-hrsd-summarize-case.md)

[Generate resolution notes using Now Assist for HRSD](now-assist-hrsd-res-note.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use Galileo Inside to answer HR-related questions](use-galileo-inside.md)

[Use the Now Assist panel in Agent Workspace for HR Case Management](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Detect sensitive topics by using sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-sensitivity-detection.md)

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)](analyze-sentiments-now-assist.md)

