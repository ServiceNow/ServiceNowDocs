---
title: Hermes Messaging Service roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/roles-by-product/roles\_hermesmessagingservice.html
release: zurich
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 1
breadcrumb: [Roles for all products]
---

# Hermes Messaging Service roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

Hermes Messaging Service administrator \[hermes\_admin\]

</td><td>

Enables users to access the Hermes Messaging Service Topic Inspector.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Kafka administrator \[kafka\_admin\]

</td><td>

Enables users to manage the integration with Apache Kafka, including topics and settings related to Kafka subscriptions.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Kafka namespace administrator \[kafka\_namespace\_admin\]

</td><td>

Enables users to manage Kafka namespace definitions.

</td><td>

None

</td><td>

None.

</td><td>

Stream Connect administrators with the kafka\_namespace\_admin role can view message data across different domains.

 For example, in a Managed Service Provider \(MSP\) instance with Kafka integrations in multiple domains, managing namespace definitions properly is important to maintain separation between domains, so don't grant this role to administrators within a single domain.

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/roles-by-product/roles-for-all-products.md)

