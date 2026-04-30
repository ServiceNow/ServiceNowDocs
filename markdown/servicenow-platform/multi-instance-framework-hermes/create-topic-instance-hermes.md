---
title: Create a topic in Hermes
description: Create a topic from within ServiceNow. Creating a topic from your instance adds a topic record to the Kafka Topics \[sys\_kafka\_topic\] table and adds a Kafka topic to Hermes.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing topics in Hermes, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a topic in Hermes

Create a topic from within ServiceNow. Creating a topic from your instance adds a topic record to the Kafka Topics \[sys\_kafka\_topic\] table and adds a Kafka topic to Hermes.

## Before you begin

Role required: kafka\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Topics**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_iyn_bm2_3zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the topic.The string that you enter is combined with the application ID and namespace to create the full Kafka topic name.

**Note:** Don't include the `snc.<instance_name>` prefix with the topic name.

</td></tr><tr><td>

Application ID

</td><td>

Application associated with the topic. Default is Stream Connect.

</td></tr><tr><td>

Namespace

</td><td>

Namespace associated with the topic.

 You can either select a namespace created by the Kafka namespace administrator or select the Default Namespace if separate namespaces aren't configured for your instance.

 In ServiceNow, all Kafka topics link to a namespace. Namespaces are used to organize topics and, on a domain-separated instance, for domain separation. When a namespace is assigned to a particular domain, all the topics created in that namespace have the same domain.

</td></tr><tr><td>

Partitions

</td><td>

Number of partitions to create for the topic.

 -   Minimum value: 1
-   Maximum value: 32
-   Default value: 1


</td></tr><tr><td>

Active

</td><td>

Option to activate the topic.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The topic appears in both the Kafka Topics \[sys\_kafka\_topic\] table and in Hermes. If, for some reason, a topic can't be created in Hermes, it won't be created in the Kafka Topics \[sys\_kafka\_topic\] table either.

**Parent Topic:**[Managing topics in Hermes](../concept/managing-topics-hermes.md)

