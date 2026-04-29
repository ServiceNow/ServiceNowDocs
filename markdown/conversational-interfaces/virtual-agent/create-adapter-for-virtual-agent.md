---
title: Create a Virtual Agent conversational custom chat integration
description: Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent conversational custom chat integration

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


-   **[Create a new channel for your custom chat integration](create-channel-va-cccif.md)**  
Create a new channel or update an existing channel for your custom chat integration. Channels are defined in the Messaging Channels \[sys\_cs\_channel\] table.
-   **[Configure a provider for your custom chat integration](create-provider-va-cccif.md)**  
Create a new provider for your custom chat integration. Providers are defined in the Connections \[sys\_cs\_provider\] table.
-   **[Set up message authentication for your custom chat configuration](set-up-msg-auth-va-cccif.md)**  
Create a Hash Message Verification record and Message Auth record to set up message authentication for your custom chat integration. This is configured in the Hash Message Verifications \[hash\_message\_verification\] table.
-   **[Create a channel identifier for your custom chat integration](create-channel-id-va-cccif.md)**  
Create a channel identifier for your custom chat integration in the Provider Channel Identities \[sys\_cs\_provider\_application\] table.
-   **[Map rich controls to the channel in your custom chat integration](map-rich-controls-va-cccif.md)**  
Create records for rich controls in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.
-   **[Create and configure a scripted REST API for your custom chat integration](configure-rest-api-va-cccif.md)**  
Create a scripted REST API, add a scripted REST resource, set security and content negotiation, and set REST API rate limits.
-   **[Create the action scripts for your custom chat integration](create-action-scripts-va-cccif.md)**  
Set up the transforms that your custom chat integration needs to communicate through the chat process.

**Parent Topic:**[Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md)

