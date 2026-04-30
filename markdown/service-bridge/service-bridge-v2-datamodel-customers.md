---
title: Service Exchange for Consumers data model
description: The Service Exchange for Consumers data model provides insight into how the tables that are used in the Service Exchange for Consumers application relate to each other.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model, Reference, Service Exchange]
---

# Service Exchange for Consumers data model

The Service Exchange for Consumers data model provides insight into how the tables that are used in the Service Exchange for Consumers application relate to each other.

The Service Exchange for Consumers data model uses a combination of the following types of tables to store data:

-   Service Exchange for Consumers application tables.
-   Customer Service Management application tables.
-   ServiceNow AI Platform standard tables.

The following table lists the Access Control Rights \(ACR\) for specific Service Exchange for Consumer tables.

<table id="table_umg_zc4_gzb"><thead><tr><th>

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

Authorized User

 \[sn\_sb\_con\_authorized\_user\]

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

Consumer

 \[sn\_sb\_con\_consumer\]

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

 \[sn\_sb\_con\_entitlement\]

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

Inbound Field

 \[sn\_sb\_con\_inbound\_field\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Outbound Field

 \[sn\_sb\_con\_outbound\_field\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Persona

 \[sn\_sb\_con\_persona\]

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

Provider Connection

 \[sn\_sb\_con\_provider\_connection\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

</td><td>

admin

</td><td>

None

</td></tr><tr><td>

Provider Task

 \[sn\_sb\_con\_provider\_task\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_requestor

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_requestor

</td><td>

admin

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_requestor

</td></tr><tr><td>

Remote Choice Cache

 \[sn\_sb\_con\_remote\_choice\_cache\]

</td><td>

admin

</td><td>

admin

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Remote Record Producer

 \[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_requestor

</td><td>

None

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td></tr><tr><td>

Remote Task

 \[sn\_sb\_con\_remote\_task\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_remote\_task\_

 creator

</td></tr><tr><td>

Remote Task Definition

 \[sn\_sb\_con\_remote\_task\_def\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td></tr><tr><td>

Variable

 \[sn\_sb\_con\_remote\_task\_variable\]

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

Service Exchange Settings

 \[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Remote Choice

 \[sn\_sb\_con\_st\_remote\_choice\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_requestor

</td><td>

None

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Transform

 \[sn\_sb\_con\_transform\]

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

</td></tr></tbody>
</table>**Parent Topic:**[Service Exchange data model](service-bridge-v2-data-model.md)

