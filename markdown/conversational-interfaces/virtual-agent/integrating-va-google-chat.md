---
title: Integrate Virtual Agent with Google chat
description: Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google chat.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [Now Virtual Agent, Self-configured, Google Chat, Channels, Integrations, Conversational Interfaces]
breadcrumb: [Configuring your Conversational Integration with Google chat, Conversational Integration with Google chat, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate Virtual Agent with Google chat

Add either the Now Virtual Agent bot or self-configured bot to your ServiceNow instance to integrate with Google chat.

## Before you begin

Install the Google chat plugin \[sn\_va\_google-chat\] on your ServiceNow instance before adding any integrations.

For more information on Now Virtual Agent integrations with Google chat, see [Exploring Conversational Integration with Google chat](../concept/exploring-ci-google-chat.md).

Role required: admin or virtual\_agent\_admin.

## About this task

**Note:** The two bot types for integrating Virtual Agent with other channels have notable differences. Use the appropriate bot for your instance.

-   The Now Virtual Agent bot is prebuilt, and is faster and easier to deploy, but is limited to one instance per tenant.
-   The self-configured bot takes more time to create and deploy, but you have full control over the bot's registration, and it's available for multiple instances per tenant.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

2.  In the Available Channels section, select the **Add Integration** drop-down menu on the Google chat tile.![Google chat tile with integration options under drop-down menu.](../images/add-google-chat-integration.png)

    **Note:** The Google chat tile and its **Add Integration** drop-down menu is available only after installing the Google chat plugin \(sn\_va\_google-chat\) on your ServiceNow instance.

3.  Sign in to your Google Chat account to complete the integration.


## Result

If an automated welcome message displays in the chat window, Google chat is ready to use with Virtual Agent in your instance.

**Parent Topic:**[Configuring your Conversational Integration with Google chat](../concept/configure-va-google-chat.md)

