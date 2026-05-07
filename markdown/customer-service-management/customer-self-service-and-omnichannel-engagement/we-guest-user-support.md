---
title: Guest user access for Web Embeddables
description: Enable unauthenticated users to access knowledge article and catalog items on your third-party website without logging in.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Guest user access for Web Embeddables

Enable unauthenticated users to access knowledge article and catalog items on your third-party website without logging in.

## Understand the guest user support

Provide unauthenticated users with access to ServiceNow mobile Web Embeddables content on your website without requiring them to log in. Guest users can view knowledge articles and submit catalog items through direct links. They can access specific articles and catalog items that you designate as public, however, they cannot search for content or browse available items. This direct access approach gives you control over what guests can discover while providing targeted self-service.

When guests submit catalog items, the demo guest catalog item creates a case and captures their contact information.

Use access control lists \(ACLs\) to define what content guests can access and what actions they can perform. Configure which knowledge articles are public and which catalog items guests can submit. The system uses secure authentication to protect guest sessions and maintain data security throughout the interaction.

## Activate guest user support

Activate the Web Components for Guest \(sn\_guest\_component\) plugin to enable guest user support on your website. For more information on how to activate the plugin, see [Activate Web Embeddables](../task/act-web-embeddables.md). After you activate the plugin, copy the global code for your module. In your website's HTML file, paste the global code where the module is embedded. The updated global code enables guest sessions and handles authentication for visitors.

