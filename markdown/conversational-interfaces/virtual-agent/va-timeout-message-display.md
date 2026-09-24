---
title: Hide or show the faulted reason message in Virtual Agent
description: Set the system properties to hide or show the faulted reason message for various Virtual Agent chat channels and pending notifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-timeout-message-display.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Virtual Agent, timeout message, agent chat, virtual agent, NASS]
breadcrumb: [Escalate to human assistance, Use, Virtual Agent, Conversational Interfaces]
---

# Hide or show the faulted reason message in Virtual Agent

Set the system properties to hide or show the faulted reason message for various Virtual Agent chat channels and pending notifications.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

By default, Virtual Agent conversations time out after two hours. For more information on adjusting timeout length, see [Closing Virtual Agent and Agent Chat conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-open-conversations.md).

You can adjust the message that users see when the conversation ends due to timeout, using the values **com.glide.cs.conversation\_faulted\_reason** for Virtual Agent, **com.glide.cs.conversation\_faulted\_reason.now\_assist\_panel** for Now Assist panel, and **com.glide.cs.conversation\_faulted\_reason.self\_service** for self-service portal chats. You can also change the timeout for a pending notification using the value **com.glide.cs.conversation\_faulted\_reason\_with\_pending\_notification**.

Setting these values to blank will use the system default message instead of showing an empty message or hiding the message entirely. You can hide or show the faulted reason message for any of the three channels, or the pending notification with the following procedure.

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Find the record for the channel whose message you want to hide or show.

    |Record|Message type|
    |------|------------|
    |**__com.glide.cs.conversation\_faulted\_reason.disabled__

**|Virtual Agent chat|
    |**__com.glide.cs.conversation\_faulted\_reason.now\_assist\_panel.disabled__**|ServiceNow Otto panel|
    |**__com.glide.cs.conversation\_faulted\_reason.self\_service.disabled__**|Self-service portal|
    |**__com.glide.cs.conversation\_faulted\_reason\_with\_pending\_notification.disabled__**|Pending notification|

3.  Set the **Value** to `True` to hide the message, or `False` to show it.

    **Note:** The default value is `False`, and the faulted reason message is also shown by default.


**Parent Topic:**[Escalate to human assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/using-va-agent-chat.md)

