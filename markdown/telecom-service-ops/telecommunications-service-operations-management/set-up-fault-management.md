---
title: Configure Telecom Assurance
description: Setting up and configuring fault management enables you to monitor network devices for configuration and performance issues.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Telecommunications Service Operations Management]
---

# Configure Telecom Assurance

Setting up and configuring fault management enables you to monitor network devices for configuration and performance issues.

Configure a webhook to monitor SD-WAN network devices using Event Management. This application collects event data from your device and generates alerts.

All events are received in the ServiceNow AI Platform® dashboard and automatically mapped to alerts. Event rules evaluate each incoming event and determine whether to create an alert or link it to an existing one. You can define custom event rules, receive notifications using webhook mechanism, and integrate with external systems through the Integrations Launchpad.

-   **[Configure a webhook](../task/configure-fault-management.md)**  
Integrate with a webhook to connect to an external event source and push event information to your ServiceNow instance.
-   **[Configure an event pull connector](../task/configure-an-event-pull-connector.md)**  
Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.
-   **[../task/set-up-connector-instance-nokia-mpn.md](../task/set-up-connector-instance-nokia-mpn.md)**  


