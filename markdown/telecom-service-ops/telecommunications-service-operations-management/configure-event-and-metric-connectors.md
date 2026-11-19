---
title: Configure event and metric connectors
description: Configure the connectors that collect events, alarms, and performance metrics from external sources and forward them to Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-event-and-metric-connectors.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure event and metric connectors

Configure the connectors that collect events, alarms, and performance metrics from external sources and forward them to Event Management.

Use a webhook to receive events that external systems push to your instance, or configure pull connectors to retrieve events and metrics on a schedule. You can also control how collected metrics are bound to configuration items \(CIs\) and aggregated.

-   **[Configure a webhook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-fault-management.md)**  
Integrate with a webhook to connect to an external event source and push event information to your ServiceNow instance.
-   **[Configure a metric pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-an-event-pull-connector.md)**  
Configure metric pull connectors to retrieve performance data from external management systems such as Meraki, Fortinet, or VeloCloud.
-   **[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)**  
Configure a mobile private network \(MPN\) pull connector instance to collect metrics, including latency KPIs, from specified KPI domains in Elastic data store. The connector publishes metrics for assurance monitoring and analytics.
-   **[Configure elastic connectors for MPN alarm collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-nokia-mpn.md)**  
Configure a connector instance to collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management.
-   **[Configure security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-security-log-collection-for-mpn.md)**  
Configure the out-of-box Health Log Analytics security log data input, an Elasticsearch collector, to collect Mobile Private Network \(MPN\) security logs and convert them into structured log records.
-   **[Configure an anomaly alert for an MPN data input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-anomaly-alert-for-new-mpn-data-input.md)**  
Configure a log anomaly alert for a Mobile Private Network \(MPN\) data input that generated its own source type.
-   **[Configure elastic connectors for MPN health status collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-rag-status-collection.md)**  
Configure a connector instance to collect health status data from an MPN Elastic index, and optionally customize the rules used to calculate that status.
-   **[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-equinix.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-equinix.md)**  

-   **[Override default metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/override-metric-ci-binding-tsom-sgc.md)**  
Replace the shipped logic that binds collected metrics to configuration items \(CIs\) for a Telecommunications Service Operations Management metric source. Create your own implementation of the `EventFieldMapping` extension point and wire it into an event field mapping rule.
-   **[Configure a metric aggregation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.md)**  
Configure a scheduled job to aggregate raw metrics into a calculated metric on a parent or anchor configuration item \(CI\). Aggregated metrics let you view performance data at a higher level of the network.
-   **[Create a custom metric aggregation implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/create-custom-metric-aggregation-implementation.md)**  
Create a custom implementation of the metric aggregation scripted extension point when the default aggregation modes don't cover a calculation you need.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

