---
title: Using an app in DevOps Config
description: When you create an app in DevOps Config, not only is it the container for the config data of the application, but the application model you choose links DevOps Config with other ServiceNow products, including DevOps Change Velocity.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, DevOps Config, IT Service Management]
---

# Using an app in DevOps Config

When you create an app in DevOps Config, not only is it the container for the config data of the application, but the application model you choose links DevOps Config with other ServiceNow products, including DevOps Change Velocity.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Each application model has an SDLC Component of the CMDB that is the link between ServiceNow DevOps pipeline products.

![DevOps Config app model](../image/devops-config-app-model.png)

When you create an app in DevOps Config, it's synced with DevOps Change Velocity. Updates and deletions to the app made in either application are also synced.

**Note:** An SDLC-C cannot be deleted if there is a DevOps Config or DevOps Change Velocity app associated with it​.

![DevOps Config SDLC component](../image/devops-config-sdlc-component.png "Related entities and attributes")

Mapping:

-   1:1 mapping between SDLC-C and App Model​
-   1:1 mapping between DevOps Config app and SDLC-C​
-   1:1 mapping between DevOps Change Velocity and SDLC-C​

**Parent Topic:**[Exploring DevOps Config](devops-config-getting-started.md)

