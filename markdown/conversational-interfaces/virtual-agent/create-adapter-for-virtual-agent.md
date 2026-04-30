---
title: Create a Virtual Agent conversational custom chat integration configuration
description: Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent conversational custom chat integration configuration

Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).

## Before you begin

Activate the [Glide Virtual Agent plugin](activate-virtual-agent.md) \(com.glide.cs.chatbot\) if it's not already activated. This plugin automatically activates the Conversational Custom Chat Integration plugin \(com.glide.cs.custom.adapter\) for custom chat integrations.

Role required: admin

## About this task

To integrate chat clients with Virtual Agent, follow these configuration steps and add action scripts to Workflow Studio.

**Note:** The CCCIF uses Integration Hub. Transactions count against your Integration Hub quota.

## Procedure

1.  [Create a new channel or update an existing channel for the integration](create-channel-va-cccif.md).

2.  [Configure a new provider for the integration](create-provider-va-cccif.md).

3.  [Set up message authentication](set-up-msg-auth-va-cccif.md).

4.  [Create a channel identifier](create-channel-id-va-cccif.md).

5.  [Select rich controls for inbound \(user input\) and outbound \(bot response\) transformation](map-rich-controls-va-cccif.md).

6.  [Create and configure a scripted REST API for your custom chat integration](configure-rest-api-va-cccif.md).

7.  [Create the action scripts](create-action-scripts-va-cccif.md).


