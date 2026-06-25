---
title: Hermes Messaging Service security model
description: The Hermes Messaging Service security model relies on the following capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-security-model.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service security model

The Hermes Messaging Service security model relies on the following capabilities.

|Capability|Description|
|----------|-----------|
|Namespaces and data isolation|All Kafka topics are namespaced per customer. You can only view topics that belong to you and your topics aren't visible to anyone else.|
|Authentication and authorization|The Hermes Messaging Service requires certificate-based authentication using mTLS endpoint authentication with trusted identities and authorization based on identity.|
|Domain separation|Domain separation is supported with the Hermes Messaging Service. See [Hermes Messaging Service domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-domain-separation.md).|
|High-availability|Failover is provided by multiple Kafka clusters running in separate ServiceNow datacenters.|

**Parent Topic:**[Hermes Messaging Service reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components]()

[Hermes Messaging Service system properties]()

[Hermes background jobs]()

[Hermes Messaging Service roles]()

[Hermes Messaging Service domain separation]()

