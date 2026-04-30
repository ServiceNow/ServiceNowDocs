---
title: Hermes Messaging Service security model
description: The Hermes Messaging Service security model relies on the following capabilities.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service security model

The Hermes Messaging Service security model relies on the following capabilities.

|Capability|Description|
|----------|-----------|
|Namespaces and data isolation|All Kafka topics are namespaced per customer. You can only view topics that belong to you and your topics aren't visible to anyone else.|
|Authentication and authorization|The Hermes Messaging Service requires certificate-based authentication using mTLS endpoint authentication with trusted identities and authorization based on identity.|
|Domain separation|Domain separation is supported with the Hermes Messaging Service. See [Hermes Messaging Service domain separation](../reference/hermes-messaging-service-domain-separation.md).|
|High-availability|Failover is provided by multiple Kafka clusters running in separate ServiceNow datacenters.|

**Parent Topic:**[Hermes Messaging Service reference](hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components](hermes-messaging-service-components.md)

[Hermes Messaging Service system properties](../reference/hermes-messaging-service-properties.md)

[Hermes Messaging Service roles](../reference/hermes-messaging-service-roles.md#)

[Hermes Messaging Service domain separation](../reference/hermes-messaging-service-domain-separation.md)

