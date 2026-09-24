---
title: Integrating Virtual Agent with Google Chat
description: Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google Chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/integrating-va-google-chat.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Virtual Agent, Self-configured, Google Chat, Channels, Integrations, Conversational Interfaces]
breadcrumb: [Configuring your Conversational Integration with Google Chat, Google Chat, Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Google Chat

Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google Chat.

## Before you begin

Ensure that you’ve installed the Google Chat plugin \[sn\_va\_google-chat\] on your ServiceNow instance before adding any integrations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

2.  In the Available Channels section, select the **Add Integration** drop-down menu on the Google Chat tile.\[Omitted image "add-google-chat-integration.png"\] Alt text: Google chat tile with integration options under drop-down menu.

    **Note:** The Google Chat tile and its **Add Integration** drop-down menu is available only after installing the Google Chat plugin \(sn\_va\_google-chat\) on your ServiceNow instance.

3.  Select the integration you want to perform, and follow the instructions.

    **Note:** If you're using the self-configured bot, do not check the **Join spaces and group conversations** box in the Enabled APIs &amp; services tab. Conversational Integration with Google Chat only supports 1-on-1 conversations.

<table id="choicetable_dwk_ccn_b1c"><thead><tr><th align="left" id="d147184e165">

Integration type

</th><th align="left" id="d147184e168">

Method

</th></tr></thead><tbody><tr><td id="d147184e174">

**Now Virtual Agent**

</td><td>

Log in to your Google Chat account when prompted. The production bot is automatically configured for your account.

</td></tr><tr><td id="d147184e183">

**Self-configured bot**

</td><td>

1.  On the Integrate Google chat with self configured bot screen, complete the information:

    |Field|Description|
    |-----|-----------|
    |Bot Name|Name for the bot.|
    |Inbound Service Account Email|Enter the inbound service account email from [Installing Conversational Integration with Google chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/installing-ci-google-chat.md).|
    |Outbound Service Account Email|Enter the outbound service account email from [Installing Conversational Integration with Google chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/installing-ci-google-chat.md).|
    |Private Key Password|The password is set when you create your key. The default is `notasecret`.|

\[Omitted image "integrate-google-chat-screen.png"\] Alt text: Integrate Google Chat with self configured bot screen.

2.  In the Attachments section, drag or select your .p12 file.
3.  Select **Submit**.
4.  Navigate to [Google Chat](https://mail.google.com/chat/u/0/#chat/home/welcome).
5.  Select **New Chat**.
6.  Enter the app name and select it.


</td></tr></tbody>
</table>
## Result

If an automated welcome message displays in the chat window, Google Chat is ready to use with Virtual Agent in your instance.

**Parent Topic:**[Configuring your Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-va-google-chat.md)

