---
title: Create a namespace in Hermes
description: Organize your Kafka topics by creating a namespace.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing namespaces in Hermes, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a namespace in Hermes

Organize your Kafka topics by creating a namespace.

## Before you begin

Role required: hermes\_admin or kafka\_namespace\_admin

## About this task

Use namespaces to organize Kafka topics in logical ways. For example:

-   Create namespace records for each Kafka cluster that replicates messages to Hermes.
-   Create namespace records for each domain in a domain-separated instance. For more information, see [Hermes Messaging Service domain separation](../reference/hermes-messaging-service-domain-separation.md).

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Namespaces**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_lds_3pz_3zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the namespace.

</td></tr><tr><td>

Topic Prefix

</td><td>

Prefix assigned to all topics in this namespace.Topics are assigned to namespaces based on the topic prefix. A scheduled job checks for new topics in Hermes. When it finds one, it creates a topic record and links the topic to the namespace.

**Warning:** To avoid conflicts between the app ID and the namespace that could result in unexpected behavior, don't specify a topic prefix beginning with `sn_` when creating a namespace record.

</td></tr><tr><td>

Allowed Application Scopes

</td><td>

List of application scopes that have access to this namespace.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A namespace record is created in the Kafka Namespace \[sys\_kafka\_namespace\] table. Topics created in or replicated to Hermes are assigned to the namespace based on the topic prefix.

## What to do next

-   Organize topics yourself by creating one or more topic records and linking them to this namespace. See [Create a topic in Hermes](create-topic-instance-hermes.md).
-   Manage access to Kafka topics in the Hermes Kafka cluster by configuring Access Control Lists \(ACLs\) for this namespace in the certificate generator. See [Set up a secure connection to the Hermes Messaging Service](set-up-secure-connection-to-hermes.md).

**Parent Topic:**[Managing namespaces in Hermes](../concept/managing-namespaces-hermes.md)

