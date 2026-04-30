---
title: Installing and configuring Service Exchange for Consumers
description: As a consumer, follow these steps to set up the Service Exchange for Consumers application in your own instance.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Exchange for Consumers, Service Exchange]
---

# Installing and configuring Service Exchange for Consumers

As a consumer, follow these steps to set up the Service Exchange for Consumers application in your own instance.

## Pre-installation checks

**Check glide.servlet.uri property**: Ensure that the `glide.servlet.uri` property in the Glide instance is set to the correct instance URL. An issue can occur when an instance is cloned from production, but still refers to the production URL for the `glide.servlet.uri` property.

|Task|Link|
|----|----|
|Install the Service Exchange for Consumers application.|See [Install Service Exchange for Consumers](../task/install-service-bridge-v2-customer.md).|
|Add Service Exchange roles for consumers.|See [Personas for consumers](service-bridge-v2-customer-roles.md).|
|Register with a provider.|See [Registering with a provider](../task/service-bridge-v2-register.md).|
|Activate entitlements.|See [Activate entitlements in Service Exchange](../task/service-bridge-v2-activate-entitlements.md).|
|Configure consumer pre-flows.|See [Service Exchange consumer pre-flows](../task/service-bridge-v2-conf-consumer-flow.md).|
|Add authorized users.|See [Add an authorized user](../task/service-bridge-v2-create-auth-user.md).|
|Create transforms.|See [Create a transform in Service Exchange](../task/service-bridge-v2-create-transform.md).|
|Create remote tasks to sync data.|See [Create remote tasks to sync data](../task/service-bridge-v2-remote-task-create.md).|
|Configure settings.|See [Configure settings on the consumer instance](../task/service-bridge-v2-configure-consumer-settings.md).|

