---
title: Installing and configuring Service Exchange for Consumers
description: As a consumer, follow these steps to set up the Service Exchange for Consumers application in your own instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-exchange/service-bridge-v2-install.html
release: zurich
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Exchange for Consumers, Service Exchange]
---

# Installing and configuring Service Exchange for Consumers

As a consumer, follow these steps to set up the Service Exchange for Consumers application in your own instance.

## Pre-installation checks

**Check glide.servlet.uri property**: Ensure that the `glide.servlet.uri` property in the Glide instance is set to the correct instance URL. An issue can occur when an instance is cloned from production, but still refers to the production URL for the `glide.servlet.uri` property.

|Task|Link|
|----|----|
|Install the Service Exchange for Consumers application.|See [Install Service Exchange for Consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/install-service-bridge-v2-customer.md).|
|Add Service Exchange roles for consumers.|See [Personas for consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-customer-roles.md).|
|Register with a provider.|See [Connect to a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-register.md).|
|Activate entitlements.|See [Activate a remote record producer in Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-activate-entitlements.md).|
|Configure consumer pre-flows.|See [Service Exchange consumer pre-flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-conf-consumer-flow.md).|
|Add authorized users.|See [Add an authorized user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-create-auth-user.md).|
|Create transforms.|See [Create a transform in Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-create-transform.md).|
|Create remote tasks to sync data.|See [Create remote tasks to sync data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-remote-task-create.md).|
|Configure settings.|See [Configure settings on the consumer instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-configure-consumer-settings.md).|

