---
title: Configure Telecom Assurance
description: Setting up and configuring fault management enables you to monitor network devices for configuration and performance issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.html
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

-   **[Configuring Telecommunications API notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configuring-telecommunications-api-notifications.md)**  
Configure the Telecommunications API notification in the ServiceNow instance.
-   **[Configure a webhook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-fault-management.md)**  
Integrate with a webhook to connect to an external event source and push event information to your ServiceNow instance.
-   **[Configure an event pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-an-event-pull-connector.md)**  
Configure event pull connectors that require a script, connector definition, and connector instance to pull events from external management systems. These connectors automate the data retrieval process, promoting the seamless integration of external events into your system for efficient monitoring and management.
-   **[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)**  
Configure a mobile private network \(MPN\) pull connector instance to collect metrics from specified KPI domains in Elastic data store and publish them for assurance monitoring and analytics.
-   **[Configure elastic connectors for MPN alarm collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-nokia-mpn.md)**  
Configure a connector instance to collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management.
-   **[Override default metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/override-metric-ci-binding-tsom-sgc.md)**  
Replace the shipped logic that binds collected metrics to configuration items \(CIs\) for a Telecommunications Service Operations Management metric source by creating your own implementation of the `EventFieldMapping` extension point and wiring it into an event field mapping rule.

