---
title: Stream Connect roles
description: Assign roles to specify what different users can see and do.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Integration Hub, Workflow Data Fabric]
---

# Stream Connect roles

Assign roles to specify what different users can see and do.

## Roles

For more information about managing and assigning roles, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_u4x_zmk_qhc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Roles inherited

</th></tr></thead><tbody><tr><td>

Kafka\_admin

</td><td>

Manage integration with Kafka, including topics and settings related to kafka subscriptions.

</td><td>

-   sn\_help\_setup\_player
-   pd\_author
-   hermes\_viewer
-   pd\_operator
-   stream\_connect\_alert\_viewer
-   canvas\_user
-   view\_changer
-   fd\_read\_flows

</td></tr><tr><td>

kafka\_namespace\_admin

</td><td>

Manage Kafka namespace definitions. In an MSP instance with Kafka integrations in multiple domains, managing namespace definitions properly is important to maintain separation between domains, so it is recommended that this role not be granted to administrators within a single domain.

</td><td>

kafka\_admin

</td></tr><tr><td>

stream\_connect\_admin

</td><td>

Management role for setting related to subscriptions, topics etc.

</td><td>

-   message\_replication\_admin
-   stream\_connect\_api
-   kafka\_admin
-   stream\_connect\_viewer
-   kafka\_namespace\_admin
-   connection\_admin

</td></tr><tr><td>

stream\_connect\_alert\_viewer

</td><td>

Read-only access to all stream connect alert records and logs.

</td><td>

None

</td></tr><tr><td>

stream\_connect\_api

</td><td>

Role with full access to invoke Stream Connect scriptable APIs

</td><td>

None

</td></tr><tr><td>

stream\_connect\_readonly\_api

</td><td>

Role required to invoke read-only scriptable API calls related to Stream Connect

</td><td>

None

</td></tr><tr><td>

stream\_connect\_viewer

</td><td>

Role with read-only access to Stream Connect configuration and runtime statistics.

</td><td>

-   message\_replication\_user
-   hermes\_viewer
-   stream\_connect\_readonly\_api
-   stream\_connect\_alert\_viewer

</td></tr></tbody>
</table>**Parent Topic:**[Integration Hub reference](../concept/integration-hub-reference.md)

