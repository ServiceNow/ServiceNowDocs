---
title: Summarize a chat conversation using Now Assist for Public Sector Digital Services \(PSDS\)
description: Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer using the chat summarization skill in Now Assist for Public Sector Digital Services \(PSDS\).
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Summarize a chat conversation using Now Assist for Public Sector Digital Services \(PSDS\)

Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer using the chat summarization skill in Now Assist for Public Sector Digital Services \(PSDS\).

## About this task

Agents can utilize chat summarization, powered by Now LLM, to gain contextual understanding of support issues throughout a chat's lifecycle, even if it involves virtual agent interactions, transfers to live agents, or multiple hand-offs between agents.

In a Virtual Agent conversation, when a requester chooses to connect to a live agent, a chat interaction appears in your inbox. When you accept the interaction, a summary of the Virtual Agent conversation is generated. You can request more details from the requester to resolve the issue.

You can also summarize the chat interaction when the chat ends or when an incident is created for further troubleshooting before or after the chat ends. The summary includes all points of the handoff, including the Virtual Agent conversation, and provides a context of the interaction to you and the other agents who might want to refer to it.

The chat summarization skill enables you to do the following actions:

-   Summarize the Virtual Agent chat history and provide a summary of the actions taken by the customer before the customer engages with a live agent.
-   Summarize the live agent and customer chat history, including the actions taken by the customer before the live agent hands off the call to another live agent and the customer engages with the new agent.
-   Summarize the chat at any point during the conversation using the `/summarize` quick action.
-   Summarize the chat between a live agent and a customer when a chat is handed off to another live agent or when an agent wraps up the conversation and ends the interaction.

**Note:** You can also generate a chat summary on demand from the Now Assist panel. For more information, see .

The chat summarization skill updates the Short description and Chat Summary fields on the interaction record once the chat is ended.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM Configurable Workspace**.

2.  In CSM Configurable Workspace, open a chat from your inbox.

    The chat summarization skill automatically creates an inline summary in the Active Chat window. This summary includes the constituent’s issue, the interaction with the Virtual Agent, and any actions the constituent has taken before engaging with a live agent. This summary appears in the Active Chat window and is identified by the Now Assist icon \(![Now assist icon.](../../../common/image/icon-ai-sparkle.png)\) and the **AI chat summary** label.

    ![AI-generated chat summaries for an interaction.](../image/chat-handoff-na-psds.png)

3.  Provide feedback for the chat summary by selecting the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\) or not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\) on the summary card.

    This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

4.  Chat with the customer to get any additional details about their question or issue.

    For example, if an applicant is applying for a benefit program, you may need to collect additional information from what they provided the Virtual Agent.

5.  In the Active Chat window, use the `/summarize` quick action to summarize the chat during the conversation with the customer.

    The chat summarization skill creates an additional inline summary in the Active Chat window. This is helpful if you want to summarize long or detailed customer conversations.

6.  If Live Agent to Live Agent handoff is enabled, transfer a chat to another agent after accepting an incoming chat with the following steps:

    1.  Select the Transfer to Agent icon ![Transfer to agent icon](../../../reuse/icons/product-icons/user-transfer-fill-24.svg)to transfer the interaction to another agent.

    2.  Select the name of another live agent.

    3.  The second live agent selects **Accept** to join the chat.

        Another summary of the chat is created when the conversation moves from one live agent to another live agent.

7.  End the chat conversation by selecting **End Chat**.

    The chat summarization skill updates the **Short description** and **Chat Summary** fields on the interaction record once the chat is ended.

    **Note:** If a chat summary isn’t available for the interaction, the **Chat Summary** field does not appear on the interaction record.

8.  Review the text in the **Short description** and **Chat Summary** fields to ensure accuracy, and make any necessary corrections.

9.  Select **Save**.


