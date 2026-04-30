---
title: Service Exchange for Providers data model
description: The Service Exchange for Providers data model provides insight into how the tables that are used in the Service Exchange for Providers application relate to each other.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Exchange data model, Service Exchange reference, Service Exchange]
---

# Service Exchange for Providers data model

The Service Exchange for Providers data model provides insight into how the tables that are used in the Service Exchange for Providers application relate to each other.

The Service Exchange for Providers application data model uses a combination of the following types of tables to store data:

-   Service Exchange of Providers application tables.
-   Customer Service Management application tables.
-   ServiceNow AI Platform standard tables.

The following diagram provides an overview of the data model for Service Exchange for Providers application.

![Diagram shows the Service Exchange for Providers data model.](../image/service-bridge-v2-data-model-provider.jpg "Service Exchange for Providers data model")

The following table lists the Access Control Rights \(ACR\) for specific Service Exchange for Provider tables.

<table id="table_fgp_3q3_gzb"><thead><tr><th>

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

 \[sn\_sb\_pro\_authorized\_user\]

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

Consumer Connection

 \[sn\_sb\_pro\_consumer\_connection\]

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

 \[sn\_sb\_pro\_entitlement\]

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

 \[sn\_sb\_pro\_inbound\_field\]

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

Outbound Field

 \[sn\_sb\_pro\_outbound\_field\]

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

Persona

 \[sn\_sb\_pro\_persona\]

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

Provider

 \[sn\_sb\_pro\_provider\]

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

Provider Task

 \[sn\_sb\_pro\_provider\_task\]

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

Registration

 \[sn\_sb\_pro\_registration\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb\_pro\_consumer

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

Remote Choice

 Definition

 \[sn\_sb\_pro\_remote\_choice\_definition\]

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

Remote Record

 Producer

 \[sn\_sb\_con\_remote\_record\_producer\]

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

Consumer Criteria

 \[sn\_sn\_pro\_remote\_record\_producer\_consumer\_criteria\]

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

Remote Service

 \[sn\_sb\_pro\_remote\_service\]

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

 \[sn\_sb\_con\_remote\_task\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td></tr><tr><td>

Remote Task

 Definition

 \[sn\_sb\_con\_remote\_task\_def\]

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

</td><td>

admin

 sn\_sb.admin

 sn\_sb.remote\_task\_

 creator

</td></tr><tr><td>

Consumer Criteria

 \[sn\_sv\_pro\_remote\_task\_def\_consumer\_criteria\]

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

Variable

 \[sn\_sb\_con\_remote\_task\_variable\]

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

Service Exchange

 Settings

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

