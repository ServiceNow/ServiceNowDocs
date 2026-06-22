---
title: Getting work from chats
description: Use the agent inbox to manage your incoming work items, such as chats, cases, incidents, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/live-agent-overview.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Finding issues to work on in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Getting work from chats

Use the agent inbox to manage your incoming work items, such as chats, cases, incidents, and more.

To open the agent inbox, select the Inbox \[Omitted image "inbox-icon-pol.png"\] Alt text: Inbox icon in the Navigation panel icon in the navigation bar. When you accept a chat, an interaction record is automatically created and captures the work done in that session.

<table id="table_tvl_cmd_1db"><thead><tr><th>

Agent responsibilities

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Monitor your inbox

</td><td>

Use designated service channels to route work items to available agents, such as incoming chat requests, case assignments, and incidents.

</td></tr><tr><td>

Start a chat session

</td><td>

Accept a chat from your inbox. You have a time limit to accept a chat before it reroutes to another agent. The chat associates to an [interaction record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/interaction-message-agent-workspace.md) that captures the conversation and work done during the session.During a chat session, you can:

-   Add attachments using the Action toolbar.
-   Transfer the chat to another agent.
-   Add another agent to the chat.
-   Perform other support tasks, such as create an incident or case.
-   Use workspace tools, such as the ribbon to glance at information or the activity stream to review related work.

</td></tr></tbody>
</table>## Agent inbox features

\[Omitted image "workspace-inbox-example.png"\] Alt text: Inbox screenshot with callouts for inbox, toolbar, active chat panel, interaction record, attachments, and buttons.

<table id="table_kjx_2yp_2db"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\(A\) Agent inbox

</td><td>

Display the queues that are assigned to you, the number of active chats in each queue, and the average wait time for chats in the queue.

</td></tr><tr><td>

\(B\) Active chat panel

</td><td>

Display your active chat session. Chat actions appear beneath the chat and allow your agents to attach a file, add an agent, transfer the chat, and more. Depending on your configuration, these may display:

-   Conversation history: messages from previous conversations appear. Only previous conversations between you and the requester appear.
-   Cross-channel conversation history: messages from all channels \(including Facebook Messenger, LINE, Slack, Twilio SMS, Microsoft Teams, WhatsApp, and Voice\) will appear.
-   Customer sentiments: feelings of the customer \(positive, neutral, negative, null \(no value assessed\)\). Customer sentiments let you identify if a user's sentiment is moving from neutral/positive to negative so you can take action to move them back to a more positive sentiment.
-   Start and end messages that include icons indicating the channel used for the conversation \(chat, phone, or messaging\):

\[Omitted image "channel-icon-examples.png"\] Alt text: Types of channels.


</td></tr><tr><td>

\(C\) Toolbar

</td><td>

Display buttons for available actions: -   [Quick actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/agent-chat/ci-agent-chat-using.md) \[Omitted image "quick-action-icon.png"\] Alt text: Quick action icon - select to display the quick action menu.
-   Transfer to queue \[Omitted image "transfer-to-queue.png"\] Alt text: Transfer to queue icon - select to transfer the conversation to the queue.
-   Transfer to agent \[Omitted image "transfer-to-agent.png"\] Alt text: Transfer to agent icon - select to transfer the conversation to an agent.
-   Attach \[Omitted image "attachment.png"\] Alt text: Attachment icon - select to add an attachment to the conversation.
-   Dynamic Translation for Agent Chat enabled \[Omitted image "Globe.png"\] Alt text: Globe icon for dynamic translation - displays if DTAC is enabled.
-   Overflow \[Omitted image "OverflowIcon.png"\] Alt text: Overflow button - select to display any additional actions.

 **Note:** Not all buttons may be available.

</td></tr><tr><td>

\(D\) Interaction record

</td><td>

Display the interaction record \(IMS\). The IMS initiates from a chat or phone call and lists the initial information about the customer and the communication. You can archive this interaction as a log of communication, or you can create an incident or a case that is based on the customer needs.

</td></tr><tr><td>

\(E\) Buttons

</td><td>

Perform an action by selecting a button: -   Create Incident
-   End Conversation
-   Save
-   End Chat
-   Assign to Me

 **Note:** Not all buttons may be available.

</td></tr><tr><td>

\(F\) Attachments panel

</td><td>

Add attachments to the interaction. For example, you can add supporting information to a customer issue. If templates are available, they appear in the template section of this panel.

</td></tr></tbody>
</table>## Ongoing messages

The Ongoing messages tab displays when you have access to at least one presence state which includes a messaging-based service channel.

\[Omitted image "clock-number.png"\] Alt text: Screen shot with ongoing messages.

Select the clock \[Omitted image "icon-clock.png"\] Alt text: Clock icon icon to display cards for ongoing messages. If the clock icon has a number in the upper right-hand corner \[Omitted image "icon-clock-number.png"\] Alt text: Clock icon, this number indicates the number of messaging conversations with unread messages. If a card has a green dot, there is a new message for that messaging conversation. The card also displays the interaction number and when the last update was made on the conversation.

