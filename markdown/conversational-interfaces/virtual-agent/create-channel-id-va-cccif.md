---
title: Create a channel identifier for your custom chat integration
description: Create a channel identifier for your custom chat integration in the Provider Channel Identities \[sys\_cs\_provider\_application\] table.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create conversational custom chat integration, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a channel identifier for your custom chat integration

Create a channel identifier for your custom chat integration in the Provider Channel Identities \[sys\_cs\_provider\_application\] table.

## Before you begin

[Set up message authentication for your custom chat configuration](set-up-msg-auth-va-cccif.md).

If you're using [domain separation](../concept/domain-separation-virtual-agent.md), change the scope to the domain you want to use before you create the channel identifier. The domain ID will be stored in the \[sys\_cs\_provider\_application\] table and passed to the Virtual Agent server as a context parameter, which will set the domain for the user.

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the filter.

2.  On the Provider Channel Identities page, click **New**.

3.  On the form, fill in the fields.

    | | |
    |---|---|
    |Name|Name of the channel identity. For example: `VA SMS Twilio Adapter`|
    |Provider|Select the name of your provider application that you set up in a previous step. For example: `VA SMS Twilio Adapter Pro`.|
    |Default Portal|Portal in which chat links to ServiceNow records are opened by default, including links in cards used for Virtual Agent notifications and AI Search results.|
    |Message auth|Select message authentication for the channel identifier that you set up in a previous step.|
    |Inbound ID|Identifier for your bot. For example, the phone number.|
    |Short description|Description for your channel identifier.|

4.  Click **Submit**.

5.  Follow these steps again to create additional channel identifiers.


## What to do next

[Map rich controls to the channel in your custom chat integration](map-rich-controls-va-cccif.md)

**Parent Topic:**[Create a Virtual Agent conversational custom chat integration](create-adapter-for-virtual-agent.md)

