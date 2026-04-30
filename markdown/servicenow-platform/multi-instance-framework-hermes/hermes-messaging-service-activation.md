---
title: Activating the Hermes Messaging Service
description: The Hermes Messaging Service is enabled when the Glide Hermes Message Queue plugin \(com.glide.hermes\) is activated.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activating the Hermes Messaging Service

The Hermes Messaging Service is enabled when the Glide Hermes Message Queue plugin \(com.glide.hermes\) is activated.

This plugin isn't activated directly. Instead, the plugin is activated by any of the following actions:

-   Activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin
-   Installation of the Log Export Service application
-   Activation of the IDR plugin \(com.glide.idr\) in Utah or higher
-   Activation of the IDR plugin \(com.glide.idr\), and then a subsequent upgrade to Utah or higher

**Note:** Stream Connect requires Workflow Data Fabric and Stream Connect subscriptions. For more information, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

**Parent Topic:**[Configuring Hermes Messaging Service](configuring-hermes-messaging-service.md)

**Related topics**  


[Set up a secure connection to the Hermes Messaging Service](../task/set-up-secure-connection-to-hermes.md)

[Revoke a Hermes certificate](../task/revoke-certificate.md)

