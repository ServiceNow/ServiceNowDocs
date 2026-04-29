---
title: Integrating Virtual Agent with Google chat
description: Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google chat.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [Now Virtual Agent, Self-configured, Google Chat, Channels, Integrations, Conversational Interfaces]
breadcrumb: [Conversational Integration with Google chat, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Google chat

Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google chat.

## Before you begin

Ensure that you’ve installed the Google chat plugin \[sn\_va\_google-chat\] on your ServiceNow instance before adding any integrations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

2.  In the Available Channels section, select the **Add Integration** drop-down menu on the Google chat tile.![Google chat tile with integration options under drop-down menu.](../images/add-google-chat-integration.png)

    **Note:** The Google chat tile and its **Add Integration** drop-down menu is available only after installing the Google chat plugin \(sn\_va\_google-chat\) on your ServiceNow instance.

3.  Select the integration you want to perform, and follow the instructions.

<table id="choicetable_dwk_ccn_b1c"><thead><tr><th align="left" id="d142101e159">

Integration type

</th><th align="left" id="d142101e162">

Method

</th></tr></thead><tbody><tr><td id="d142101e168">

**Now Virtual Agent**

</td><td>

Log in to your Google Chat account when you are prompted. The production bot is automatically configured for your account.

</td></tr><tr><td id="d142101e177">

**Self-configured bot**

</td><td>

1.  On the Integrate Google chat with self configured bot screen, complete the information:

    |Field|Description|
    |-----|-----------|
    |Bot Name|Name for the bot.|
    |Inbound Service Account Email|Enter the inbound service account email from [Installing Conversational Integration with Google chat](installing-ci-google-chat.md).|
    |Outbound Service Account Email|Enter the outbound service account email from [Installing Conversational Integration with Google chat](installing-ci-google-chat.md).|
    |Private Key Password|The password is set when you create your key. The default is `notasecret`.|

![Integrate Google Chat with self configured bot screen.](../images/integrate-google-chat-screen.png)

2.  In the Attachments section, drag or select your .p12 file.
3.  Select **Submit**.
4.  Navigate to [Google chat](https://mail.google.com/chat/u/0/#chat/home/welcome).
5.  Select **New Chat**.
6.  Enter the app name and select it.


</td></tr></tbody>
</table>
## Result

If an automated welcome message displays in the chat window, Google chat is ready to use with Virtual Agent in your instance.

**Parent Topic:**[Conversational Integration with Google chat](../concept/gchat-conv-integration.md)

