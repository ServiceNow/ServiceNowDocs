---
title: Create a Virtual Agent conversational custom chat integration
description: Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/create-adapter-for-virtual-agent.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent conversational custom chat integration

Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).

## Before you begin

Activate the [Glide Virtual Agent plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/activate-virtual-agent.md) \(com.glide.cs.chatbot\) if it's not already activated. This plugin automatically activates the Conversational Custom Chat Integration plugin \(com.glide.cs.custom.adapter\) for custom chat integrations.

Role required: admin

## About this task

To integrate chat clients with Virtual Agent, follow these configuration steps and add action scripts to Workflow Studio.

**Note:** The CCCIF uses Integration Hub. Transactions count against your Integration Hub quota.

## Procedure

1.  [Create a new channel or update an existing channel for the integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-channel-va-cccif.md).

2.  [Configure a new provider for the integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-provider-va-cccif.md).

3.  [Set up message authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/set-up-msg-auth-va-cccif.md).

4.  [Create a channel identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-channel-id-va-cccif.md).

5.  [Select rich controls for inbound \(user input\) and outbound \(bot response\) transformation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/map-rich-controls-va-cccif.md).

6.  [Create and configure a scripted REST API for your custom chat integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-rest-api-va-cccif.md).

7.  [Create the action scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-action-scripts-va-cccif.md).


