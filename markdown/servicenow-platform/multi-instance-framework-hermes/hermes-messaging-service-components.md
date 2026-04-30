---
title: Hermes Messaging Service components
description: The Hermes Messaging Service architecture is built on the following components.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service components

The Hermes Messaging Service architecture is built on the following components.

|Component|Description|
|---------|-----------|
|Hermes Message Queue|A dedicated multi-tenant message queue in the ServiceNow Hermes Kafka cluster for managing the flow of data to and from the instance. The message queue uses certificate-based authentication that supports bi-directional traffic. The Hermes Message Queue is available to ServiceNow applications via the Hermes Glide API.|
|Hermes Gateway|Part of the ServiceNow datacenter that enables you to connect to a ServiceNow endpoint to read and write data to the Hermes Message Queue.|
|Hermes Glide connector|Connector that integrates instance functionality \(for example, flows, data export, and data replication\) with the Hermes Message Queue via the API.|

**Parent Topic:**[Hermes Messaging Service reference](hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service security model](hermes-messaging-service-security-model.md)

[Hermes Messaging Service system properties](../reference/hermes-messaging-service-properties.md)

[Hermes Messaging Service roles](../reference/hermes-messaging-service-roles.md#)

[Hermes Messaging Service domain separation](../reference/hermes-messaging-service-domain-separation.md)

