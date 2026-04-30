---
title: Configure Amazon Polly as default voice tone for text to speech
description: You can configure Amazon Polly as the default voice by overriding the default voice tone for text to speech.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Notify with Twilio, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Amazon Polly as default voice tone for text to speech

You can configure Amazon Polly as the default voice by overriding the default voice tone for text to speech.

## Before you begin

Role required: notify\_admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **Twilio Direct Additional Properties**.

    ![Twilio Direct additional properties](../image/twilio-direct-add-properties.png)

2.  In the Twilio Direct driver property field, enter the preferred voice tone.

    For example: "`Polly.Joanne`". The ServiceNow® instance passes Polly.Joanne value to the Twilio service and renders the voice in Joanne’s tone.

    If you have a new San Diego or a higher version instance, the voice property will not be defined by default and the voice settings at Twilio will be considered. For more information on Amazon Polly voice, see [Twilio Text-to-speech](https://www.twilio.com/docs/voice/twiml/say/text-speech#amazon-polly). However, if you are upgrading to San Diego or a higher release version, the default voice property will be "alice".

    **Note:** If you are defining the property in your ServiceNow® instance, the Twilio voice settings are overridden.


**Parent Topic:**[Configure Notify with Twilio](t_ConfigureNotifyWithTwilio.md)

