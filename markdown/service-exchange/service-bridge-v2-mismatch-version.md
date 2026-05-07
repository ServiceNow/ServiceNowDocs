---
title: Mismatched version support
description: Providers and consumers using different versions of the Service Exchange applications can exchange and synchronize data between their ServiceNow instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Service Exchange]
---

# Mismatched version support

Providers and consumers using different versions of the Service Exchange applications can exchange and synchronize data between their ServiceNow instances.

-   Providers can upgrade their Service Exchange application and deploy new capabilities without interrupting services to consumers who haven’t upgraded to their application.
-   Consumers who haven’t upgraded can use existing entitlements from their provider, as well as new entitlements at or below their current compatibility level. However, they can’t activate entitlements on newer compatibility levels until they upgrade to the latest version.

The following is an example scenario:

-   The provider and consumer are using Service Exchange for Providers 1.0 and Service Exchange for Consumers 1.0. The provider has created some configurations \(such as remote task definitions, remote record producers, or foundation data sync offerings\) and the consumer is using these entitlements.
-   The provider decides to upgrade to Service Exchange for Providers 2.0 but the consumer is still using the older version. In this case, the consumer can continue to use the entitlements created using the older version of Service Exchange and sync data with the provider.
-   To use the latest configuration revisions \(created with the upgraded application\), the consumer must upgrade to a version that is compatible with the provider.

**Related topics**  


[Configuring revisions](service-bridge-v2-config-revision.md)

