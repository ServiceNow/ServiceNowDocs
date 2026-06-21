---
title: Integrating Virtual Agent with Google Chat
description: Add the Virtual Agent bot to your ServiceNow instance to integrate with Google Chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/conversational-interfaces/virtual-agent/integrating-va-google-chat.html
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-06-27"
reading_time_minutes: 1
breadcrumb: [Conversational Integration with Google Chat, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Google Chat

Add the Virtual Agent bot to your ServiceNow instance to integrate with Google Chat.

## Before you begin

Ensure that you’ve installed the Google Chat plugin \[sn\_va\_google-chat\] on your ServiceNow instance before adding any integrations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

2.  In the Available Channels section, select **Add Integration** on the Google Chat tile.\[Omitted image "add-google-chat-integration.png"\] Alt text: Google chat tile.

    **Note:** **Add Integrations** is available only after installing the Google Chat plugin \(sn\_va\_google-chat\) on your ServiceNow instance.

3.  On the Integrate Google Chat with self configured bot screen, complete the information:

    \[Omitted image "integrate-google-chat-screen.png"\] Alt text: Integrate Google Chat with self configured bot screen.

    |Field|Description|
    |-----|-----------|
    |Bot Name|Name for the bot.|
    |Inbound Service Account Email|Enter the inbound service account email from [Installing Conversational Integration with Google chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/installing-ci-google-chat.md).|
    |Outbound Service Account Email|Enter the outbound service account email from [Installing Conversational Integration with Google chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/installing-ci-google-chat.md).|
    |Private Key Password| |

4.  In the Attachments section, drag or select your .p12 file.

5.  Select **Submit**.

6.  Navigate to [Google Chat](https://mail.google.com/chat/u/0/#chat/home/welcome).

7.  Select **New Chat**.

8.  Enter the app name and select it.

    If an automated welcome message displays in the chat window, you are all set to use Google Chat with Virtual Agent.


**Parent Topic:**[Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/gchat-conv-integration.md)

