---
title: Change Virtual Agent and Agent Chat system messages
description: Customize the default system messages displayed during Virtual Agent conversations and Agent Chat.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 1
keywords: [Change, Virtual Agent, Agent Chat, system, messages, customize, default]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Change Virtual Agent and Agent Chat system messages

Customize the default system messages displayed during Virtual Agent conversations and Agent Chat.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Use **System messages** in Chat Settings to change the properties that control standard chat messages displayed in your instance. If you're using Virtual Agent and Agent Chat, the **System Messages** list displays properties for both Virtual Agent and Agent Chat messages. If you're using Agent Chat only, the **System Messages** list displays only the properties relevant to Agent Chat.

**Note:** While the chat widget uses the Messages table \[sys\_ui\_message\] to configure the greeting and closing messages, third-party Conversational Integrations \(such as Microsoft Teams\) use system messages. To change them, modify these messages in System Messages as follows:

-   For greetings that call vaSystem.getTopicSelectionMessage\(\), modify the value of **com.glide.cs.topic\_picker\_msg**.
-   For closings that call vaSystem.endConversation\(\), modify the value of **com.glide.cs.conversation\_ended\_msg**.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **System messages**, select **View All**.

3.  In the System Messages list, select the property record for the message you want to change.

4.  In the **Value** field, enter the new message text and select **Save**.

    Any changes are immediately applied to the system messages displayed in your instance.


**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

