---
title: Using the Scratchpad for Service Exchange tasks
description: The Scratchpad feature facilitates exchange of additional data between provider and consumer instances while performing Service Exchange tasks.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Using the Scratchpad for Service Exchange tasks

The Scratchpad feature facilitates exchange of additional data between provider and consumer instances while performing Service Exchange tasks.

Both providers and consumers can add, update, and remove information to and from the Scratchpad table. Using server side scripts, name-value pairs are associated with Provider Tasks and Remote tasks and this data is automatically synced between the instances. Shared data must be associated with a Provider or a Remote Task, and is automatically synced if the associated task is active.

The PSBScratchpadUtil API allows providers to share extra information that is outside of any other Service Exchange service, with their consumers. See [PSBScratchpadUtil - Scoped](https://www.servicenow.com/docs/access?context=PSBScratchpadUtilScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) for more details.

The CSBScratchpadUtil API allows consumers to share extra information that is outside of any Service Exchange service with their providers. See [CSBScratchpadUtil - Scoped](https://www.servicenow.com/docs/access?context=CSBScratchpadUtilScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) for more details.

**Note:**

-   If the associated task is deactivated or deleted, the scratchpad data is deleted after 3 days. This setting can be modified using the `sn_sb.scratchpad.autodelete.days` property.
-   Each task can have a maximum of 50 scratchpad entries.
-   Data in the scratchpad cannot exceed 4000 characters.

The following diagram shows how the scratchpad data is synced between the instances.

![Shows data transfer and sync between the provider and the consumer instances](../image/service-bridge-v2-scratchpad.jpg)

**Example Scratchpad use case:** This example shows how data in the Scratchpad is synced between the consumer and provider instances.

-   A consumer orders a laptop from the local catalog. The local catalog in this case is a [Remote Record Producer](service-bridge-v2-remote-record.md).
-   This request is immediately forwarded the provider and appears as a Provider Task on the provider's instance.
-   The provider then selects a laptop from the inventory, sets it up and adds relevant information like the serial number, model, configuration to the Scratchpad which is automatically sent to the consumer.
-   On the consumer's instance, the Scratchpad data is retrieved and updated on the local database.
-   The laptop is then assigned to the consumer.

![Sample Scratchpad use case showing the flow of data between consumer and provider instances.](../image/service-bridge-v2-scratchpad-example.jpg)

