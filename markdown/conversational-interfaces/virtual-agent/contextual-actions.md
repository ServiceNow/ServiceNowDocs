---
title: Contextual actions for custom chat integrations
description: Commands with a pre-defined behavior can be mapped to certain user-friendly keywords and passed as user input. This input is mapped to supported contextual actions for the most appropriate response in the chat.Map user inputs to base system contextual actions.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-02-07"
reading_time_minutes: 1
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Contextual actions for custom chat integrations

Commands with a pre-defined behavior can be mapped to certain user-friendly keywords and passed as user input. This input is mapped to supported contextual actions for the most appropriate response in the chat.

## Getting started with contextual actions

User inputs can be mapped to a contextual action in two ways.

-   UI-based mapping of comma-separated keywords to available contextual actions. For example: Hi, Hola - Start Conversation
-   Script-based mapping of user actions to available contextual actions. For example: User clicks "Start" menu - Start Conversation

## Available contextual actions

|Name|Description|
|----|-----------|
|Agent|Command to request transfer to a live agent|
|Bye|Command to end a conversation with a live agent or a virtual agent whenever you are outside of a topic-selection prompt|
|Help|Command to request help using the bot|
|Hi|Command to start or end a conversation|
|Logout|Command to unlink the user messaging account from ServiceNow|
|Notifications|Command to subscribe or unsubscribe from receiving notifications|
|Restart|Command to end a bot conversation that is either in progress or runs into an error, and then begin a new conversation|

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

## Contextual action mapping

Map user inputs to base system contextual actions.

### Before you begin

Role required: admin

### About this task

Use the Contextual Actions \[sys\_cs\_contextual\_action\] table to review the commands used in the chat integrations. You can add more keywords for a command. Each record for a pre-built command has this information:

<table id="table_gky_2ry_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the command.

</td></tr><tr><td>

Commands

</td><td>

Keyword for the command. You can add multiple keywords, separated by commas.

</td></tr><tr><td>

Description

</td><td>

Explanation of the command

</td></tr><tr><td>

Applicability

</td><td>

Application in which the command is used:-   Virtual Agent only
-   Agent Chat only
-   Virtual Agent and Agent Chat

</td></tr></tbody>
</table>### Procedure

1.  Navigate to **All**, and then enter `sys_cs_contextual_action.list` in the filter.

2.  Select a contextual action from the list.

3.  Add comma-separated keywords to the **command** field.

    For example: `Agent, Live Agent, Transfer to agent`.

4.  Exclude specific messaging channels from contextual actions.

    1.  Select the **Insert a new row...** text.

    2.  Select the magnifying glass.

    3.  Select the messaging channel you would like to exclude from the contextual action.

    4.  Select the green checkmark to save.

5.  Select **Update**.


### What to do next

[Create bot messages](../task/create-bot-messages.md#) specific to each channel.

