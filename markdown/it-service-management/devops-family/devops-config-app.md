---
title: Using an app in DevOps Config
description: When you create an app in DevOps Config, not only is it the container for the config data of the application, but the application model you choose links DevOps Config with other ServiceNow products, including DevOps Change Velocity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/devops-config-app.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring DevOps Config, DevOps Config, IT Service Management]
---

# Using an app in DevOps Config

When you create an app in DevOps Config, not only is it the container for the config data of the application, but the application model you choose links DevOps Config with other ServiceNow products, including DevOps Change Velocity.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Each application model has an SDLC Component of the CMDB that is the link between ServiceNow DevOps pipeline products.

\[Omitted image "devops-config-app-model.png"\] Alt text: DevOps Config app model

When you create an app in DevOps Config, it's synced with DevOps Change Velocity. Updates and deletions to the app made in either application are also synced.

**Note:** An SDLC-C cannot be deleted if there is a DevOps Config or DevOps Change Velocity app associated with it​.

\[Omitted image "devops-config-sdlc-component.png"\] Alt text: DevOps Config SDLC component

Mapping:

-   1:1 mapping between SDLC-C and App Model​
-   1:1 mapping between DevOps Config app and SDLC-C​
-   1:1 mapping between DevOps Change Velocity and SDLC-C​

**Parent Topic:**[Exploring DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-getting-started.md)

