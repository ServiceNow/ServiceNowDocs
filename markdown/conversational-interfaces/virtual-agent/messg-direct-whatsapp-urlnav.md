---
title: Set the URL navigation for WhatsApp chat
description: When agents share links in their WhatsApp chat conversations, customize the portal that those links point to. For example, you can configure links to point to your brand’s portal, or to the ServiceNow portal.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set the URL navigation for WhatsApp chat

When agents share links in their WhatsApp chat conversations, customize the portal that those links point to. For example, you can configure links to point to your brand’s portal, or to the ServiceNow portal.

## Before you begin

Install the Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application on your ServiceNow instance.

Activate the Consumer Service Portal plugin \(`com.glide.service-portal.consumer-portal`\).

Role required: admin

## Procedure

1.  In the navigation filter of your ServiceNow instance, enter `sys_cs_provider_application_list.do` and select **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the channel you’re using. Enter `WhatsApp`.|
    |Provider|Name of the provider. Enter `WhatsApp`.|
    |Default Portal|Portal to be used in the mapping. Select a portal from the list of portals.|
    |Message Auth|Message auth that you created.|
    |Inbound ID|Your WhatsApp phone ID. Enter the unique ID assigned to your WhatsApp phone number.|

3.  Select **Submit**.


## What to do next

For more information on setting up URL navigation, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).

**Parent Topic:**[Configure Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp-configure.md)

