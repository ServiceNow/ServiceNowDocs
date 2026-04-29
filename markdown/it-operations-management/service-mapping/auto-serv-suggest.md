---
title: Automated Service Suggestions
description: Automated Service Suggestions simplifies the processing of mapping application services or adding to an existing service by providing application service candidates using machine learning. Mapped services provide key information to help you make data-driven decisions, prioritize services, and respond to situations.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Automated Service Suggestions

Automated Service Suggestions simplifies the processing of mapping application services or adding to an existing service by providing application service candidates using machine learning. Mapped services provide key information to help you make data-driven decisions, prioritize services, and respond to situations.

Using machine learning \(ML\), Service Mapping quickly identifies potential application fingerprints based on discovered processes. It evaluates the relationship between these fingerprints and configuration items \(CIs\) and creates meaningful connections. These connections are used to create an application service map, a visual representation of a service.

Automated Service Suggestions further simplifies the mapping process by using the ML information to calculate entry points, efficiently identifying where to begin mapping an application service. It also generates a list of application service candidates. Each candidate includes an entry point as well as a set of previously identified resources to include in the service map. You can then select a candidate to create a new application service or to add to an existing service.

## Service Fingerprints

Service Fingerprints complements Automated Service Suggestions by identifying unique, classified components of identified application service candidates. Presenting these components facilitates the selection of the most suitable suggested application service. You can view components of an application in your actual environment, including details such as product, product category, publisher, and description. Use this information to search for specific components you want to discover or to make informed decisions about which candidates to convert into application services.

To use Service Fingerprints, you must download and install ITOM Content Service from the ServiceNow® Store and opt in to ITOM Content Service. For more information, see [ITOM Content Service](../../discovery/concept/discovery-content-services.md).

## Domain separation with Automated Service Suggestions

Automated Service Suggestions supports domain separation starting with version 1.9.0. No support is currently offered for on-premise instances. Reach out to product management for further information.

**Related topics**  


[Exploring Service Mapping](service-mapping-get-started.md)

[Service Mapping Workspace](../reference/sm-dashboard.md)

[Application service readiness dashboard in configurable workspace](../reference/readiness-dashboard-ml.md)

[Map application services based on Automated Service Suggestions](../task/map-application-suggestion.md)

