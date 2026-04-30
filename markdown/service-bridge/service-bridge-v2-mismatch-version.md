---
title: Service Exchange mismatched version support
description: Providers and consumers using different versions of the Service Exchange applications can exchange and synchronize data between their ServiceNow instances.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Service Exchange, Service Exchange]
---

# Service Exchange mismatched version support

Providers and consumers using different versions of the Service Exchange applications can exchange and synchronize data between their ServiceNow instances.

-   Providers can upgrade their Service Exchange application and deploy new capabilities without interrupting services to consumers who haven’t upgraded to their application.
-   Consumers who haven’t upgraded can use existing entitlements from their provider but can’t request new entitlements unless they upgrade to the latest version.

The following is an example scenario:

-   The provider and consumer are using Service Exchange for Providers 1.0 and Service Exchange for Consumers 1.0. The provider has created some configurations \(such as remote task definitions, remote record producers, or foundation data sync offerings\) and the consumer is using these entitlements.
-   The provider decides to upgrade to Service Exchange for Providers 2.0 but the consumer is still using the older version. In this case, the consumer can continue to use the entitlements created using the older version of Service Exchange and sync data with the provider.
-   To use the latest configuration revisions \(created with the upgraded application\), the consumer must upgrade to a version that is compatible with the provider.

For details on a supporting feature, see [Service Exchange configuration revisions](service-bridge-v2-config-revision.md).

