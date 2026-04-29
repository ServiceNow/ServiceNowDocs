---
title: Configure event subscription and Webhook URL
description: Configure the event subscription and the Webhook URL.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Sidebar and Slack, Sidebar and Slack, Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Configure event subscription and Webhook URL

Configure the event subscription and the Webhook URL.

## Before you begin

Role required: admin

## Procedure

1.  Open the Slack app from step one.

2.  Select **Event Subscriptions**.

3.  In the Request URL field, enter the request URL.

    For example, enter `https://{instancename}/api/sn_oe_sfs/collaboration_slack_event_processor/chats`.

4.  Select **Subscribe to events on behalf of users**.

5.  Add these events:

    |Event Name|Description|Required Scope|
    |----------|-----------|--------------|
    |member\_joined\_channel|A user joined a public channel, private channel, or MPDM.|channels:read or groups:read or mpim:read|
    |member\_left\_channel|A user left a public or private channel.|channels:read or groups:read|
    |message.channels|A message was posted to a channel.|channels:history|
    |message.groups|A message was posted to a private channel.|groups:history|
    |message.im|A message was posted in a direct message channel.|im:history|


