---
title: Configure Service Exchange for Providers
description: To set up and configure the Service Exchange for Providers application, follow these steps.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Exchange for Providers, Service Exchange]
---

# Configure Service Exchange for Providers

To set up and configure the Service Exchange for Providers application, follow these steps.

## Pre-installation checks

**Check glide.servlet.uri property**: Ensure that the `glide.servlet.uri` property in the Glide instance is set to the correct instance URL. An issue can occur when an instance is cloned from production, but still refers to the production URL for the `glide.servlet.uri` property.

|Task|Link|
|----|----|
|Install the Service Exchange for Providers application.|See [Install Service Exchange for Providers](../task/install-service-bridge-v2-provider.md).|
|Set up a new provider record.|See [Set up a Service Exchange provider record](../task/service-bridge-v2-new-provider.md).|
|Assign Service Exchange roles for providers.|See [User roles for providers](service-bridge-v2-personas.md).|
|Create catalog personas.|See [Create catalog personas](../task/service-bridge-v2-create-catalog-persona.md).|
|Create remote choice definitions.|See [Create remote choice definitions in Service Exchange for Providers](../task/service-bridge-v2-create-remote-choice-fld-defs.md)|
|Create remote catalog items.|See [Create remote catalogs in Service Exchange for providers](service-bridge-v2-remote-catalog.md).|
|Create remote task definitions.|See [Create a remote task definition in Service Exchange for Providers](../task/service-bridge-v2-create-remote-tasks-defs.md).|
|Create transforms.|See [Create a transform in Service Exchange](../task/service-bridge-v2-create-transform.md).|
|Update Authorized Users settings.|See [Update settings for authorized users](../task/service-bridge-v2-configure-settings.md)|

If you’re a consumer, see [Configure Service Exchange for Consumers](service-bridge-v2-install.md).

**Related topics**  


[Configure Service Exchange for Consumers](service-bridge-v2-install.md)

[Service Exchange](../../tmt-service-bridge/concept/tmt-service-bridge-both-landing-page.md)

