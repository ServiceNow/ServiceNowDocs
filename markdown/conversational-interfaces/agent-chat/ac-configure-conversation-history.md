---
title: Setting up conversation history
description: Enable and customize the conversation history options that are available on the conversation history screen.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Agent Chat, Conversational Interfaces]
---

# Setting up conversation history

Enable and customize the conversation history options that are available on the conversation history screen.

## Before you begin

Conversation history provides the capability to easily access historical conversations on the same channel. The agent can be more efficient by reviewing those conversations without opening multiple tabs and reviewing the transcripts. This page provides options to enable conversation history and to configure how many to display and optional filtered view for the agents.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Agent Chat** and then on the Agent Experience card, select **View Settings** next to Conversation History.

3.  To turn on conversation history, toggle on the Activate switch.

4.  In the Number of conversations to display field, enter the number of previous conversations that should display on the screen.

    The maximum number of conversations that can display is 25.

5.  To create a conversation history filter, select **New**.

6.  On the Create New Conversation History Filter screen, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Name|Name of the conversation history filter.|
    |Active|Select the check box if this filter should be applied.|
    |Description|Description of the conversation history filter.|
    |Order|Order in which the filters should be prioritized. The filter with the lowest order matching the agent's groups is used to filter the interactions.|
    |Apply to all groups|Option for making the conversation history filter available to all user groups.|

7.  Select **Set conditions** to display the Condition dialog.

8.  On the Condition dialog, build a filter for the conversation history.

    For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

9.  Select **Set**.

10. On the Create New Conversation History Filter screen, select **Submit** or **Update**.


**Parent Topic:**[Configuring Agent Chat](../concept/ci-agent-chat-configuring.md)

