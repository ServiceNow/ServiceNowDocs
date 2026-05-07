---
title: Service Exchange authorized users and personas
description: The Authorized Users feature enables a provider to categorize remote catalog items by user personas so that only authorized users with these personas can access the catalog items. It also allows consumer admins to associate these personas to users in their instances to allow access.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remote catalogs, Explore, Service Exchange]
---

# Service Exchange authorized users and personas

The Authorized Users feature enables a provider to categorize remote catalog items by user personas so that only authorized users with these personas can access the catalog items. It also allows consumer admins to associate these personas to users in their instances to allow access.

When a provider and a consumer initially register the Service Exchange application, the active contacts on the consumer's account in the provider's ServiceNow instance are automatically added to the Authorized Users table and synced with the consumer's ServiceNow instance.

Enables the provider to subdivide services by user personas giving the consumers an easy way to define access in their instance to the provider’s services. By using the Authorized Users feature, you can identify the specific users between the provider and consumer instances to manage the consumer requests for the provider's services. You can then assign personas to the authorized users so that you can control the access to remote catalog items.

-   Both providers and consumers can create Authorized Users.
-   The providers manage the approval state for an Authorized User. By default, the approval state is set **Approved**.
-   Consumers manage the active state for an Authorized User.
-   Providers can set the maximum number of authorized users for each connection. This requires all consumers to maintain a list of active authorized users of less than or equal to the limit set by the provider. If the value is not set, consumers can have as many active authorized users as they want.

To learn more, see [Add an authorized user](../task/service-bridge-v2-create-auth-user.md).

