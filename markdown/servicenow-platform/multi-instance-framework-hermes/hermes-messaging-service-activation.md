---
title: Activating the Hermes Messaging Service
description: The Hermes Messaging Service is not a standalone plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-activation.html
release: brazil
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activating the Hermes Messaging Service

The Hermes Messaging Service is not a standalone plugin.

This plugin is activated as a dependency when any of the following actions are performed:

-   Activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin
-   Installation of the Log Export Service application
-   Activation of the IDR plugin \(com.glide.idr\) in Utah or higher
-   Activation of the IDR plugin \(com.glide.idr\), and then a subsequent upgrade to Utah or higher
-   Installation of the Digital End-User Experience \(DEX\) application

For more information, see the [KB1213485](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1213485) article in the Now Support Knowledge Base.

**Note:** Stream Connect requires Workflow Data Fabric and Stream Connect subscriptions. For more information, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

**Parent Topic:**[Configuring Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/multi-instance-framework-hermes/configuring-hermes-messaging-service.md)

**Related topics**  


[Set up a secure connection to the Hermes Messaging Service]()

[Revoke a Hermes certificate]()

[Restricting access to Hermes]()

[Enable encryption at rest for a Hermes topic]()

