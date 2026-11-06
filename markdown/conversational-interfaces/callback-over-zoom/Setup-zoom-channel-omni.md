---
title: Configure the Zoom channel for callbacks
description: Allow agents to call users back over Zoom by enabling the Zoom channel and specifying the host email address.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/callback-over-zoom/Setup-zoom-channel-omni.html
release: australia
product: Callback over Zoom
classification: callback-over-zoom
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Setting up Zoom extension for Omnichannel Callback, Zoom extension for Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Configure the Zoom channel for callbacks

Allow agents to call users back over Zoom by enabling the Zoom channel and specifying the host email address.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.

2.  In the Messaging Channels list, select the **Zoom** channel.

3.  If a message at the top of the form prompts you to switch the application scope to edit the record, select **here** in the message.

4.  In the Channel Properties section, configure the channel properties.

    -   Set the **enabled** property to `true`.

    -   In the **host\_email** property, enter the email address of the Zoom account that hosts the meetings.

5.  Select **Update**.


