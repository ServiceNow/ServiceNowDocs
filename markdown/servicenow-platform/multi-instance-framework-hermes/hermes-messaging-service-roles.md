---
title: Hermes Messaging Service roles
description: Hermes Messaging Service is installed with these roles.Enables users to access the Hermes Messaging Service Topic Inspector.Enables users to manage the integration with Apache Kafka, including topics and settings related to Kafka subscriptions.Enables users to manage Kafka namespace definitions.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service roles

Hermes Messaging Service is installed with these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Hermes Messaging Service reference](../concept/hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components](../concept/hermes-messaging-service-components.md)

[Hermes Messaging Service security model](../concept/hermes-messaging-service-security-model.md)

[Hermes Messaging Service properties](hermes-messaging-service-properties.md)

[Hermes Messaging Service domain separation](hermes-messaging-service-domain-separation.md)

## Hermes Messaging Service administrator \[hermes\_admin\]

Enables users to access the Hermes Messaging Service Topic Inspector.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Kafka administrator \[kafka\_admin\]

Enables users to manage the integration with Apache Kafka, including topics and settings related to Kafka subscriptions.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Kafka namespace administrator \[kafka\_namespace\_admin\]

Enables users to manage Kafka namespace definitions.

### Contains Roles

List of roles contained within the role: kafka\_admin.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Stream Connect administrators with the kafka\_namespace\_admin role can view message data across different domains.

For example, in a Managed Service Provider \(MSP\) instance with Kafka integrations in multiple domains, managing namespace definitions properly is important to maintain separation between domains, so don't grant this role to administrators within a single domain.

