---
title: Agent Whisper
description: Agent Whisper lets agents and chat managers have a conversation without the requester knowing.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Agent Chat, Conversational Interfaces]
---

# Agent Whisper

Agent Whisper lets agents and chat managers have a conversation without the requester knowing.

During a chat between a requester and an agent, the agent may want to privately ask a chat manager for assistance or a chat manager and an agent may want to converse without the requester knowing. Using Agent Whisper, the agent can request help and the chat manager and agent can send messages to each other without the requester knowing.

For example, if an agent is newly hired, still in training, or unsure about how to proceed with a requester's request, the agent can ask a chat manager to join the conversation to help walk the agent through the steps of the procedure privately.

Another scenario is if an agent needs to escalate a customer conversation to a chat manager. Agents can request help and chat managers can join the chat conversations publicly to communicate directly with the customer to help deescalate the situation.

You activate Agent Whisper in Agent Chat settings. For details, see [Setting up Agent Chat](../task/ac-configure-agent-chat.md).

## Using the Help quick action

Agents can ask chat managers to join chat conversations with requesters by raising the help flag. Agents can open the Quick Action menu or enter `/help` to request for help. When using the help quick action, agents can also type a brief private message explaining what they need help with. This way, when a chat manager enters the conversation, they already know what the agent needs.

Chat managers can view the conversations with help requested from different views: interactions list view, manager dashboard, and lists.

-   Interactions list view: Agents can navigate to the interactions list view and add in the help requested column to see which conversations agents have requested help in. From here, managers can click directly into the interaction record and join the conversation with the agent and requester.
-   Manager dashboard: With the Workforce Optimization for Customer Service \(com.snc.wfo.csm\) plugin installed, managers can see that the Help requested tile on the manager dashboard homepage.
-   Lists: From Conversation Monitoring &gt; Help Requested, managers can view a list of chat interactions in which agents have requested help.

    ![Help Requested selected in Conversation Monitoring options in Lists view.](../image/agent-whisper-help-list-view.png)


To learn more about Workforce Optimization for CSM, see [Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Sending and receiving messages in Private Chat

The agent and chat manager can converse without the requester knowing that they are having a conversation. Messages that only seen by the agent and chat manager are private messages. The requester does not see private messages. The agent and chat manager can toggle between the public and private messages using the **Public Chat** and **Private Chat** tabs. The **Private Chat** tab has a yellow background with "Message only visible internally" and private messages appear on the yellow background. When someone types in the **Private Chat** tab, the typing event indicator does not display. For example, when the chat manager types in the **Private Chat** tab, the agent's and requester's screen do not display the typing event indicator.

The tab that the agent types on and sends the message from determines whether a message is posted privately or publicly. If an agent starts typing a message on the **Public Chat** tab and then switches to the **Private Chat** tab, the **Private Chat** tab does not display the message. If the agent then goes back to the **Public Chat** tab, the message is still there. However, agents can see private messages regardless of whether they are on the **Private Chat** tab or the **Public Chat** tab.

<table id="table_vnt_kb3_kpb"><thead><tr><th>

Example of Public Chat

</th><th>

Example of Private Chat

</th></tr></thead><tbody><tr><td>

![Public Chat option selected in Agent Chat window.](../image/public-chat-tab-example.png)

</td><td>

![Private Chat option selected in Agent Chat](../image/private-chat-tab-example.png)

</td></tr></tbody>
</table>![Public and private messages highlighted here are displayed with differing message box colors.](../image/public-and-private-message-example.png "Example of public and private messages")

## Joining a chat conversation in Private Chat

The first time a chat manager switches from a private conversation \(on the **Private Chat** tab\) to a public conversation \(on the **Public Chat** tab\), a dialog box displays. The dialog box informs the chat manager that they are about to join the public conversation and the requester will be notified that the chat manager is joining the conversation. The chat manager can select **Yes, I'm sure** to join the public conversation or select **Cancel** to remain in the private conversation.

![Agent Chat window showing an Agent joining a conversation.](../image/agent-whisper-join-conversation.png)

## Sharing attachments in Private Chat

If agents send an attachment while on the **Private Chat** tab, the attachment is sent only to the agent and chat manager. Message Sent confirmation messages do not display for private message conversations.

## Private messages stored in internal chat transcripts

Once the conversation ends, one external transcript and one internal chat transcript are generated.

The public chat transcript does not include private messages and is accessible for the requester to download if the Download Transcript capability has been enabled.

The private chat transcript is shown on the interaction record by default and does include private messages exchanged between agents and managers. Private messages are prefixed with the word \[PRIVATE\] to clearly indicate when a message came through the Private Chat.

To learn more about downloading the chat transcript, see [Chat transcript downloads for requesters](ci-chat-transcripts.md).

![Agent Chat Details tab with chat internal transcript highlighted.](../image/agent-whisper-download-transcript.png)

## Custom report

Admins can build a custom report to track the number of help requests, see [Build a report to track the number of help requests](ci-agent-chat-reference.md#) for instructions.

