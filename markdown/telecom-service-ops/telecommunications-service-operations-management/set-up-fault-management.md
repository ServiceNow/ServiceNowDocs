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
-   **[Configure a metric pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-an-event-pull-connector.md)**  
Configure metric pull connectors to retrieve performance data from external management systems such as Meraki, Fortinet, or VeloCloud.
-   **[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)**  
Configure a mobile private network \(MPN\) pull connector instance to collect metrics, including latency KPIs, from specified KPI domains in Elastic data store. The connector publishes metrics for assurance monitoring and analytics.
-   **[Configure elastic connectors for MPN alarm collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-nokia-mpn.md)**  
Configure a connector instance to collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management.
-   **[Configure security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-security-log-collection-for-mpn.md)**  
Configure the out-of-box Health Log Analytics security log data input, an Elasticsearch collector, to collect Mobile Private Network \(MPN\) security logs and convert them into structured log records.
-   **[Override default metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/override-metric-ci-binding-tsom-sgc.md)**  
Replace the shipped logic that binds collected metrics to configuration items \(CIs\) for a Telecommunications Service Operations Management metric source. Create your own implementation of the `EventFieldMapping` extension point and wire it into an event field mapping rule.
-   **[Configure a metric aggregation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.md)**  
Configure a scheduled job to aggregate raw metrics into a calculated metric on a parent or anchor configuration item \(CI\). Aggregated metrics let you view performance data at a higher level of the network.
-   **[Create a custom metric aggregation implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-custom-metric-aggregation-implementation.md)**  
Create a custom implementation of the metric aggregation scripted extension point when the default aggregation modes don't cover a calculation you need.

