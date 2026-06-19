---
title: Exploring Conversational Integration with Google Chat
description: Use the Conversational Integration with Google Chat application to connect your end users with Virtual Agent or live agents through your Google Chat account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/exploring-ci-google-chat.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Google Chat, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Exploring Conversational Integration with Google Chat

Use the Conversational Integration with Google Chat application to connect your end users with Virtual Agent or live agents through your Google Chat account.

## Conversational Integration with Google Chat overview

Enable requesters to chat with Google Chat or live agents using the Google Chat application. Use the Conversational Integration with Google Chat app, available from the ServiceNow Store, to associate your instance with Google Chat

You must have Now Assist in Virtual Agent for Google Chat activated. For more information, see 

You have two options for integrating Virtual Agent with Google Chat: the Now Virtual Agent bot and a self-configured bot.

<table><thead><tr><th>

Integration type

</th><th>

Method

</th></tr></thead><tbody><tr><td>

Now Virtual Agent

</td><td>

Log in to your Google Chat account when you're prompted. The production bot is automatically configured for your account.

</td></tr><tr><td>

Self-configured bot

</td><td>

1.  On the Integrate Google Chat with self configured bot screen, complete the information:
    -   Bot name: Enter a name for your bot.
    -   Inbound Service Account Email: Enter the inbound service account email from [Integrate Virtual Agent with Google Chat using the self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/installing-ci-google-chat.md).
    -   Outbound Service Account Email: Enter the outbound service account email from [Integrate Virtual Agent with Google Chat using the self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/installing-ci-google-chat.md).
    -   Private key password: The password is set when you create your key. The default is `notasecret`.
2.  In the Attachments section, drag or select your .p12 file.
3.  Select **Submit**.
4.  Navigate to [Google Chat](https://mail.google.com/chat/u/0/#chat/home/welcome).
5.  Select **New Chat**.
6.  Enter the app name and select it.

</td></tr></tbody>
</table>## Conversational Integration with Google Chat users

|User|Description|
|----|-----------|
|admin or virtual\_agent\_admin|Create and publish Virtual Agent conversations.|
|admin.google.com|A Google account with admin privileges is required to integrate Virtual Agent in Google.|

Follow these steps to add Conversational Integration with Google Chat:

1.  [Install Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/install-ci-google-chat.md)
2.  [Integrate Virtual Agent with Google Chat using the self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/installing-ci-google-chat.md)
3.  [Integrate Virtual Agent with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/integrating-va-google-chat.md)

**Parent Topic:**[Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/gchat-conv-integration.md)

