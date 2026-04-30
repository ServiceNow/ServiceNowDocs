---
title: Service Exchange configuration revisions
description: As a provider, you can update the configurations of remote record producers, remote task definitions, foundation data sync offerings, and create new versions that can be entitled to consumers.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Service Exchange, Service Exchange]
---

# Service Exchange configuration revisions

As a provider, you can update the configurations of remote record producers, remote task definitions, foundation data sync offerings, and create new versions that can be entitled to consumers.

You can deploy new versions of entitlements with updated functionality to compatible consumers without impacting consumers who haven’t upgraded their Service Exchange applications. You can upgrade your Service Exchange applications to adopt new features even if your consumers haven’t upgraded to the latest version.

You can create multiple configuration revisions, but only the latest published revision is active and available as a new entitlement. Your consumers can either choose to activate the new entitlement or continue to use the older revision until it's archived or retired. If the consumers want to use the new revision, they must upgrade their Service Exchange application to the same version that is running on the provider's instance. Once the new revision is activated on the consumer's instance, the earlier revision is longer available and moves to an inactive state.

You can create configuration revisions for the following:

-   Remote record producers
-   Remote task definitions

See [Create configuration revisions](service-bridge-v2-create-config-rev.md) for details.

