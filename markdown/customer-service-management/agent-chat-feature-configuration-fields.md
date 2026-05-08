---
title: Chat feature configuration form fields
description: Description of the Chat feature configuration form fields.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Engagement Messenger reference, Reference, Customer Service Management]
---

# Chat feature configuration form fields

Description of the Chat feature configuration form fields.

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title text

</td><td>

Title for the chat feature widget on the messenger home page. The default title is `Chat with an agent.`

</td></tr><tr><td>

Reference chat topic

</td><td>

The topic that enables contextual chat for case or work order.

 This field is automatically set to **EC Contextual help**.

</td></tr><tr><td>

Message for when chat is offline

</td><td>

The message that appears on a messenger when an agent is offline and Virtual Agent isn’t set up. The default message is `Our customer support is offline`.

</td></tr><tr><td>

Enabled for unauthenticated users

</td><td>

Option for enabling the Live and Virtual Agent chat feature for guest users who visit the website that hosts the messenger.

 **Note:**

Starting with the Vancouver release, the chat client was enabled by default only for authenticated users. To enable the chat client for unauthenticated users to be able to access Virtual Agent chat and Live Agent chat, you must enable the **$sn-va-web-client-app** and **sn\_va\_web\_client\_app\_embed** pages for public access. For more information, see Make UI pages public or private.

</td></tr><tr><td>

Enabled for authenticated users

</td><td>

Option for enabling the Live and Virtual Agent chat feature for users who sign in to the website that hosts the messenger.

</td></tr><tr><td class="sub-head" colspan="2">

Feature launch messaging

</td></tr><tr><td>

Feature launch message

</td><td>

Title of a chat card when it’s initiated from a chat feature.

</td></tr><tr><td>

Feature launch description

</td><td>

Description of a chat launcher that is within a feature launch message.

</td></tr><tr><td class="sub-head" colspan="2">

Global chat settings

</td></tr><tr><td>

Change the default mode for chatting

</td><td>

Determines the default mode for chatting, either synchronously \(Chat\) or asynchronously \(Messaging\).For information on how to set the default chat mode, see [Change the default chat mode for the Chat feature](../task/em-set-default-mode-of-chatting.md).

</td></tr><tr><td>

Configure advanced chat options

</td><td>

Determines the chat options for managing various conversation features.For more information, see [Chat Setup configuration form](em-advanced-chat-setup.md).

</td></tr><tr><td>

Email notifications for unread messages

</td><td>

Determines the email settings for sending email summaries for unread messages.For more information on how to enable email notifications for a specified duration, see[Configure email notifications for unread chat messages](../task/setup-email-notification-unread-message.md).

**Note:** The green color next to **Status** indicates that the email notification is enabled.

</td></tr></tbody>
</table><table id="table_tww_xgb_g4b"><tbody><tr><td>

![Engagement Messenger home page displaying a Chat with an agent widget to initiate a chat with Virtual Agent.](../image/em-agent-chat-widget.png "Agent chat widget")

</td><td>

![Widget displaying the Chat with us and Submit a case features along with their description.](../image/em-chat-launcher.png "Chat feature launcher widget")

</td></tr></tbody>
</table>