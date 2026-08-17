---
title: Telecommunications Service Operations Management reference
description: Several types of components are installed with Telecommunications Service Operations Management applications and plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Telecommunications Service Operations Management]
---

# Telecommunications Service Operations Management reference

Several types of components are installed with Telecommunications Service Operations Management applications and plugins.

-   **[Arista VeloCloud installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/arista-velocloud-installed-integrations.md)**  
Predefined system integrations use VeloCloud REST APIs to pull events into your ServiceNow instance to monitor your Arista VeloCloud devices.
-   **[Fortinet installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/fortinet-installed-integrations.md)**  
Predefined system integrations use Fortinet REST APIs to pull metric data into your ServiceNow instance to monitor your Fortinet devices.
-   **[Cisco Meraki installed integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/meraki-installed-integrations.md)**  
Predefined system integrations use Meraki REST APIs to pull metric data into your ServiceNow instance to monitor your Cisco Meraki devices. Each integration is driven by a connector instance whose metric parameter determines the data that the instance collects.
-   **[System components installed with Telecommunications API notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/alarm-management-user-roles.md)**  
Administrators can assign user roles to grant access to the API notification database tables. The following standard roles for the Topic \[sn\_api\_notif\_mgmt\_topic\] and Topic Subscription \[sn\_api\_notif\_mgmt\_subscription\] tables are included in the ServiceNow system.
-   **[System components installed with Nokia Altiplano](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/properties-installed-with-nokia-altiplano.md)**  
System properties control how the connector operates, including discovery options and performance settings.
-   **[Telecom discrepancy identification and reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/system-properties-affecting-telecom-discrepancy-identification-reconciliation.md)**  
The system properties are part of the TSOM Visibility plugin \(sn\_tsom\_core\) and control the Telecom Discrepancy Identification &amp; Reconciliation log \(TSOM CMDB Audit\). The TSOM Visibility plugin enables the TSOM Visibility applications. It contains logic shared across the Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution.
-   **[Fortinet Service Graph Connector API Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/fortinet-service-graph-connector-api-endpoints.md)**  
The Service Graph Connector for Fortinet integrates Fortinet Dashboard API data into ServiceNow AI PlatformConfiguration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
-   **[Cisco Meraki Service Graph Connector API Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/cisco-meraki-service-graph-connector-api-endpoints.md)**  
The Service Graph Connector for Meraki integrates Cisco Meraki Dashboard API data into ServiceNow AI Platform®Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
-   **[Arista VeloCloud Service Graph Connector API Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/arista-velocloud-service-graph-connector-api-endpoints.md)**  
The Service Graph Connector for Arista VeloCloud integrates VeloCloud Orchestrator API data into ServiceNow AI Platform Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
-   **[MPN Formulas table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formulas-table.md)**  
Reference for the MPN Formulas \[sn\_tsom\_em\_conns\_kpi\_definitions\] table and the automatic processing that occurs when a record is inserted or updated.
-   **[MPN latency KPIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-latency-kpis.md)**  
Reference for the latency KPIs collected by the MPN Pull Connector and the derived UE-to-switch latency metric.
-   **[MPN security log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-security-log-fields.md)**  
Reference for the structured fields produced when a raw MPN security log document is parsed.
-   **[Retrieve data from Nokia Altiplano via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/retrieving-data-nokia-altiplano-API.md)**  
Examples of Retrieving Data from Nokia Altiplano via REST API.
-   **[Page limits for Meraki pull connector endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/meraki-pull-connector-page-limits.md)**  
The Meraki pull connector paginates API requests so that all records are retrieved for large organizations. The page size is set per endpoint to match each endpoint's maximum supported value in the Meraki API v1.
-   **[Pull connector granularity constraints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/pull-connector-granularity-constraints.md)**  
Each connector type enforces minimum and maximum values for the granularity and metrics collection schedule fields on the connector instance form. The connector instance form rejects values outside the supported range.
-   **[Metric aggregation configuration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.md)**  
The configuration object passed to the metric aggregation scripted extension point defines what to aggregate, how to aggregate it, and where to publish the result. The parameters that apply depend on the aggregation mode.
-   **[Metric type IDs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/tsom-metric-type-ids.md)**  
Metric type IDs identify each time-series metric that a connector writes to the metrics database. Use these IDs to locate metrics in Insights Explorer or when you build custom dashboards and indicators.

