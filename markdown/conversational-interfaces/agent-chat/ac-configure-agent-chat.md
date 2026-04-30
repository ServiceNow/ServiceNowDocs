---
title: Setting up Agent Chat
description: Configure Agent Chat to enable live agents to chat with customers and manage various conversation features for agents and end users. Through Agent Chat, agents interact with end users, create incident or case records, or transfer chats to another agent or queue.
locale: en-US
release: zurich
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Setup, Agent Chat, live agents]
breadcrumb: [Configuring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Setting up Agent Chat

Configure Agent Chat to enable live agents to chat with customers and manage various conversation features for agents and end users. Through Agent Chat, agents interact with end users, create incident or case records, or transfer chats to another agent or queue.

## Before you begin

Configure the following before starting this task:

-   Install the Agent Chat plugin \(com.glide.interaction.awa\).
-   If you want to use the Profanity Filter, activate the Profanity Filter plugin \(sn\_va\_profanity\).
-   In Advanced Work Assignment:
    -   Configure [service channels](../../advanced-work-assignment/concept/awa-service-channels.md).
    -   Define [work item queues](../../advanced-work-assignment/reference/awa-queues.md).
    -   Set up [work assignments](../../advanced-work-assignment/concept/awa-assignment.md).
-   [Update your Live Feed profile](https://www.servicenow.com/docs/access?context=t_UpdateYourProfile&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) to display agent names and avatars in the chat client.
-   [Configure Agent Chat in Service Portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

Role required: workspace\_admin

**Note:** You must be in the global view to edit the settings.

## About this task

Use Agent Chat settings to do the following:

-   Activate or deactivate:
    -   Agent Chat \(enabled by default\).
    -   Display of agent names and avatars the chat window.
    -   Display of the agent name in the header.
    -   Chat transcript downloads.
    -   Display of estimated wait time for live chat support \(transfer from the virtual agent to a live agent\).
    -   Agent Whisper, which enables supervisors to message agents privately when agents are interacting with an end user. For new instances, Agent Whisper is enabled by default.
    -   Emojis.
    -   Conversation history.
    -   Conversational autopilot client system messages.
-   Set the system messages that are displayed when a live agent transfer occurs.
-   Manage Quick Action controls.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.

2.  Select the **Agent Chat** tile.

    The Agent Chat settings screen titled "Customize how your users chat with live agents" appears.

    **Note:** Agent Chat is automatically activated when the Agent Chat plugin is installed. If you're not using Agent Chat, slide the toggle switch to deactivate it and select **Save**.

3.  Activate Agent Chat by enabling the **Activate** option.

4.  Configure the options.

<table id="table_mc1_wc1_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent names and avatars

</td><td>

Slide the toggle switch to activate or deactivate the display of the agent names and avatars in the Agent Chat client when a live agent enters, transfers, or exits a chat. Agents set their names and pictures in their Live Feed profiles.

 -   If activated, the **Agent name in header** is automatically activated and displays the agent name at the top of the chat client.
-   If deactivated, agent identities remain anonymous. No names or avatars are displayed in the chat window.


</td></tr><tr><td>

Agent name in header

</td><td>

Slide the toggle switch to activate or deactivate the display of the agent name in the header of the chat window. This option is active by default.

 This field appears if **Agent names and avatars** is active.

</td></tr><tr><td>

Transcripts

</td><td>

Slide the toggle switch to activate or deactivate the ability for requesters to download a transcript of the conversation they had with an agent.

</td></tr></tbody>
</table><table id="table_bf1_1d1_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Live chat wait status

</td><td>

Select whether to display the estimated wait time for live agent support in the chat menu for chat widgets. If you're using the Conversational Integration with Microsoft Teams, the wait time displays in a card that shows the approximate wait time to chat with an agent.

-   The wait time is the estimated time, in minutes, for the transfer from the virtual agent to a live agent.
-   The wait time updates once per minute. Wait time is based on the Queue Average Wait Time minus the waiting time.


</td></tr><tr><td>

Agent Transfer Message

</td><td>

Enter the message that users see when they are transferred to a live agent or another queue. For example: "Please stand by while I connect you to a live agent."

 **Note:** You can define only one transfer message and it is displayed for all queues in your instance. The Agent Transfer message does not support HTML, only plain text.

</td></tr><tr><td>

"No agent available" message

</td><td>

Enter the message that users see when a live agent is not available. For example: "No agents are available at the moment. Please try again later."

 **Note:** You can define only one agent availability message and it is displayed for all queues in your instance.

</td></tr></tbody>
</table><table id="table_rcd_3d1_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Whisper

</td><td>

Slide the toggle switch to activate or deactivate Agent Whisper, which enables supervisors to message agents privately when agents are interacting with a requester.

 **Note:** If you deactivate Agent Whisper, you must manually deactivate the /help quick action.

</td></tr><tr><td>

Emojis

</td><td>

Slide the toggle switch to activate or deactivate emojis.

</td></tr><tr><td>

Conversation Autopilot

</td><td>

Slide the toggle switch to activate or deactivate notifications related to Conversation Autopilot, which enables agents to use autopilot quick actions to invoke Virtual Agent topics.

</td></tr><tr><td>

Dynamic language translation

</td><td>

Slide the toggle switch to activate or deactivate the dynamic translation of end user's messages.

</td></tr><tr><td>

Profanity detection

</td><td>

Select **View all** to display the Profanity Filter settings screen. This option only displays if the Profanity Filter plugin has been installed. For more information, see [Configuring the Profanity Filter settings](ac-configure-profanity-settings.md).

</td></tr><tr><td>

Conversation History

</td><td>

Select **View all** to display the Conversation History screen.

 Set maximum number of past conversation to display in the conversation window and apply filters to only show what is most relevant to agents based on channel type, assignment group, and more.

 For details on configuring the Conversation History options, see [Setting up conversation history](ac-configure-conversation-history.md).

</td></tr></tbody>
</table><table id="table_c35_jd1_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Quick action configurations

</td><td>

Select **View all** to display the Quick Action Toolbar Controls screen.

 For details on configuring the toolbar controls, see [Setting up quick action toolbar controls](../concept/ci-quick-actions-overview.md#).

</td></tr></tbody>
</table>5.  Select **Save**.


**Parent Topic:**[Configuring Agent Chat](../concept/ci-agent-chat-configuring.md)

