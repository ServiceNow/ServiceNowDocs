---
title: Hermes Messaging Service domain separation
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for the Hermes Messaging Service. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service domain separation

Domain separation is supported for the Hermes Messaging Service. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Overview of Hermes Messaging Service domain separation

On a domain-separated instance, you can use namespaces to configure which domains can access specific topics in the Hermes Kafka cluster. You assign topics to ServiceNow domains using the topic record's namespace.

## How domain separation works with the Hermes Messaging Service

On a domain-separated instance, a user with the kafka\_namespace\_admin role can assign namespaces to specific ServiceNow domains. When the Kafka namespace admin assigns a namespace to a particular domain, all the topics created in that namespace will have the same domain. Users can only see and interact with the topics and namespaces they have access to, based on domain visibility and access control lists \(ACLs\). Topics created with the Default Namespace are created in the global domain.

Both the Kafka Topics \[sys\_kafka\_topic\] table and the Kafka Namespaces \[sys\_kafka\_namespace\] table are domain-separated tables. Domain separation rules filter which records are available in each domain. In addition to being domain-separated, these tables can also be protected with ACLs, just like any other table.

All domain support features require the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin.

**Parent Topic:**[Hermes Messaging Service reference](../concept/hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components](../concept/hermes-messaging-service-components.md)

[Hermes Messaging Service security model](../concept/hermes-messaging-service-security-model.md)

[Hermes Messaging Service properties](hermes-messaging-service-properties.md)

[Hermes Messaging Service roles](hermes-messaging-service-roles.md#)

[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

