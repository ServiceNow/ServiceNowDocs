---
title: Service Mapping Lightweight Service Model
description: The Lightweight Service Model is an optimized architecture for storing and determining service topology. It maintains current service data without storing historical snapshots, reducing storage overhead and improving performance for large configuration item inventories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-lightweight-service-model.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-08-10"
reading_time_minutes: 2
keywords: [service mapping, lightweight service, service architecture, service model, service topology]
breadcrumb: [Choose the right method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping Lightweight Service Model

The Lightweight Service Model is an optimized architecture for storing and determining service topology. It maintains current service data without storing historical snapshots, reducing storage overhead and improving performance for large configuration item inventories.

## What is the Lightweight Service Model

The Lightweight Service Model is an alternative architecture for Dynamic service instances and Tag-Based application services in Service Mapping. Unlike the traditional model, which maintains a complete history of service topology snapshots, the Lightweight Service Model stores only the current state of service topology.

|Traditional model|Lightweight Service Model|
|-----------------|-------------------------|
|Stores complete history of service topology snapshots|Stores only current service topology data|
|Historical records are available for all past updates|No historical snapshots retained; timeline shows change points but not full history|
|Slower update cycles due to historical data management|Faster update cycles|
|Can query past service topology states and change history|Can query current state only, with direct access to service topology data|

## Benefits of the Lightweight Service Model

Service Mapping AI capabilities enable creating services at scale. While scaling up the mapping, the Lightweight Service Model becomes crucial for scaling up the performance.

When a service operates under the Lightweight Service Model, service topology updates are significantly faster because the system doesn't maintain historical snapshot data. In addition, storage requirements are reduced because only current service topology data is stored.

## Converting a service to Lightweight Service Model

Conversion to the Lightweight Service Model is permanent and one-way. Once you convert a service to Lightweight Service Model, this change can't be reversed. Historical snapshots that were stored under the traditional model will be deleted and can't be restored.

When you convert a service to Lightweight, the system optimizes how it stores and manages data across the service hierarchy tables. The service types that can be converted to Lightweight are Tag-Based and Dynamic.

\[Omitted image "lightweight-screenshot.png"\] Alt text: Convert to Lightweight link

Use the Lightweight Service Model related link to convert a service. For the full procedure, see [Convert a service instance to Lightweight Service Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/convert-service-instance-lightweight.md).

**Related topics**  


[Convert a service instance to Lightweight Service Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/convert-service-instance-lightweight.md)

