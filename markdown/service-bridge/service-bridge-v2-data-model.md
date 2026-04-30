---
title: Service Exchange data model
description: The Service Exchange applications data model provides insight into how the tables that are used in Service Exchange relate to each other.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Exchange reference, Service Exchange]
---

# Service Exchange data model

The Service Exchange applications data model provides insight into how the tables that are used in Service Exchange relate to each other.

The data model uses a combination of the following types of tables to store data:

-   Service Exchange application tables.
-   ServiceNow AI Platform standard tables.

The following diagram provides an overview of the data model for Service Exchange.

![Diagram shows the Service Exchange data model](../image/service-bridge-v2-data-model-full.jpg "Service Exchange data model")

The following table lists the Access Control Rights \(ACR\) for specific Service Exchange base table.

<table id="table_kgs_tm3_gzb"><thead><tr><th>

Table

</th><th>

Read

</th><th>

Write

</th><th>

Delete

</th><th>

Create

</th></tr></thead><tbody><tr><td>

Authorized user

 \[sn\_sb\_authorized\_user\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td></tr><tr><td>

Connection

 \[sn\_sb\_connection\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

</td><td>

admin

</td><td>

admin

</td></tr><tr><td>

Entitlement

 \[sn\_sb\_entitlement\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Provider Task

 \[sn\_sb\_provider\_task\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb.requestor

</td><td>

admin

 sn\_sb.admin

 sn\_sb.requestor

</td><td>

admin

</td><td>

admin

 sn\_sb.admin

 sn\_sb.requestor

</td></tr><tr><td>

Remote Record Producer

 \[sn\_sb\_remote\_record\_producer\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

</td><td>

admin

</td><td>

admin

</td></tr><tr><td>

Remote Task

 \[sn\_sb\_remote\_task\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_creator

</td><td>

None

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Scratchpad

 \[sn\_sb\_scratchpad\]

</td><td>

admin

</td><td>

None

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Transform

 \[sn\_sb\_transform\]

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Transform Line

 \[sn\_sb\_transform\_line\]

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td><td>

None

</td><td>

None

</td></tr></tbody>
</table>