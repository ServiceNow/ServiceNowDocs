---
title: Configure callback behavior for a channel
description: Configure callback behavior for a channel using the callback parameters. You can create a separate callback configuration for each supported conversational integration channel.
locale: en-US
release: xanadu
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Omnichannel Callback, Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure callback behavior for a channel

Configure callback behavior for a channel using the callback parameters. You can create a separate callback configuration for each supported conversational integration channel.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **General**.

2.  On the Callback configuration form, swipe the **Activate** toggle switch to the right, enter the wait time threshold, and select **Save**.

    **Note:** Ensure that the application scope of your ServiceNow instance is set to global before editing the Callback configuration form.

3.  Select a channel that you want to configure callback for from the Channel drop-down list.

4.  Select a callback topic from the Callback Topic drop-down list.

    Select **Callback-Phone** for voice channels and **Callback-General** for messaging or chat channels. These default callback topics are triggered when there are no agents available to take the call or when the average wait time in the queue is over the predefined threshold. You can also use a custom callback topic based on your requirements. For more information on how to customize a callback topic, see [Customize a default callback topic](customize-callback-topic.md).

5.  Provide the **Max callback attempts**.

    After the maximum number of callback attempts is reached, the callback task is closed and no further callback attempts are made.

6.  Provide the **Callback timeout \(threshold \(in hours\)**.

    When the callback timeout is reached, no further callback attempts are made and the callback task is closed.


