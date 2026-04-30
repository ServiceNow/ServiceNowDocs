---
title: Summarize a chat conversation by using Now Assist for Customer Service Management \(CSM\)
description: Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Now Assist for Customer Service Management \(CSM\), Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Summarize a chat conversation by using Now Assist for Customer Service Management \(CSM\)

Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

The chat summarization skill enables you to do the following actions:

-   Summarize the Virtual Agent chat history and provide a summary of the actions taken by the customer before the customer engages with a live agent.
-   Summarize the live agent and customer chat history, including the actions taken by the customer before the live agent hands off the call to another live agent and the customer engages with the new agent.
-   Summarize the chat at any point during the conversation using the `/summarize` quick action.
-   Summarize the chat between a live agent and a customer when a chat is handed off to another live agent or when an agent wraps up the conversation and ends the interaction.

**Note:** You can also generate a chat summary on demand from the Now Assist panel. For more information, see [Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-chat-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In CSM Configurable Workspace, open a chat from your inbox.

    The chat summarization skill creates an inline summary in the Active Chat window. This summary includes the customer’s issue and the actions that the customer has taken before the customer engaged with a live agent. The summary appears in the Active Chat window and is identified by the Now Assist icon \(![Now assist icon.](../../../common/image/icon-ai-sparkle.png)\) and the **AI chat summary** label.

    ![AI-generated chat summaries for an interaction.](../image/now-assist-csm-chat-summary.png "Interaction record with chat summaries")

3.  Provide feedback for the chat summary by selecting the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\) or not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\) on the summary card.

    This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

4.  Chat with the customer to get any additional details about their question or issue.

    For example, if the customer is having an issue with the hardware, you may need the hardware model number and serial number.

5.  In the Active Chat window, use the `/summarize` quick action to summarize the chat during the conversation with the customer.

    The chat summarization skill creates an additional inline summary in the Active Chat window. This quick action is helpful if you want to summarize long or detailed customer conversations.

6.  If Live Agent to Live Agent handoff is enabled, transfer a chat to another agent after accepting an incoming chat with the following steps:

    1.  Select the Transfer to Agent icon ![icon](../../../reuse/icons/product-icons/user-transfer-fill-24.svg)to transfer the interaction to another agent.

    2.  Select the name of another live agent.

    3.  The second live agent selects **Accept** to join the chat.

        Another summary of the chat is created when the conversation moves from one live agent to another live agent.

7.  End the chat conversation by selecting **End Chat**.

    The chat summarization skill updates the **Short description** and **Chat Summary** fields on the interaction record when you end the chat.

    **Note:** If a chat summary isn’t available for the interaction, the **Chat Summary** field doesn’t appear on the interaction record.

8.  Review the text in the **Short description** and **Chat Summary** fields and make any necessary corrections.

    Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

9.  Select **Save**.


## What to do next

If necessary, you can create a case from an interaction record. The system uses the information from the **Short description** and **Chat Summary** fields on the interaction record to populate the **Short description** and **Description** fields on the case record.

The system displays the Now Assist icon \(![Now assist icon.](../../../common/image/icon-ai-sparkle.png)\) next to these fields and removes the icon if the agent makes changes to the fields and saves the record.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

