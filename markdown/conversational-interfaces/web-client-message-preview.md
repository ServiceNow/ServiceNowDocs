---
title: Enable message preview on the chat widget
description: Admins can allow their end users to see a preview of any new or unread messages waiting for them when the chat window is minimized.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Message preview, chat widget, advanced work assignment, AWA, com.glide.cs.advanced-chat-popover]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Enable message preview on the chat widget

Admins can allow their end users to see a preview of any new or unread messages waiting for them when the chat window is minimized.

## Before you begin

This feature is only available after you've installed and updated the Omni-Experience Standard Feature Set to the latest version through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Set the com.glide.cs.advanced-chat-popover system property to True. This system property activates the smart chat component on the Service Portal. By default, the property is set to False. This system property is only applicable to the requester persona.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **General**.

2.  Under **Display options**, activate **Message preview**.

    A message displays confirming that the setting has been saved.


## Result

When message preview is activated, and the chat window is minimized, the end user sees a message preview badge icon ![Message preview badge icon.](../image/message-preview-icon-web-client.png) in the minimized chat window. The message preview badge icon lets the user know that there are new or unread messages, and how many. In this example, the end user has one new or unread message.

A message preview pane shows the first new or unread message next to the badge icon. The message is based the conversation. For example, if the user needed help with using the laptop, the message preview pane could be similar to the following image.

![Message preview pane with number of unread messages displaying next to preview badge icon.](../image/message-preview-icon-text.png)

The end user can either:

-   Click the message preview pane to continue the conversation in the chat, or
-   Close the message preview pane.

The badge icon appears only when there are new or unread messages. The badge icon is updated every 10 seconds, and displays the first new or unread message.

**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

