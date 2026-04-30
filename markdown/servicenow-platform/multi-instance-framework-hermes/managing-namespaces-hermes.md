---
title: Managing namespaces in Hermes
description: Group Kafka topics together for simplified topic management and access control specification using namespaces.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managing namespaces in Hermes

Group Kafka topics together for simplified topic management and access control specification using namespaces.

In ServiceNow, all Kafka topics link to a namespace. You can use namespaces to organize topics in logical ways. For example, you can group topics together based on their Kafka cluster. You can also use namespaces to configure which domains can access which topics on a domain-separated instance. You assign topics to ServiceNow domains using the topic's namespace.

## Namespace records

Namespace records are stored in the Kafka Namespaces \[sys\_kafka\_namespace\] table. This table shows a list of namespace records with each namespace's related topic prefix. An administrator with the kafka\_namespace\_admin role creates namespace records in the Kafka Namespaces \[sys\_kafka\_namespace\] table.

## Namespaces and topic prefixes

A topic is assigned to a namespace based on the topic name's prefix. A scheduled job regularly checks Hermes for new topics. When it finds one, it creates a ServiceNow topic record for the topic and links the topic to a namespace. The prefix assigned to the topic is the basis for its namespace assignment in ServiceNow.

This image shows an example of using the Kafka cluster name prefix to organize topics into different namespaces in ServiceNow.

![Overview of how topic prefixes in Kafka are related to namespaces in ServiceNow.](../images/hermes-namespace-topic-structure.png "Kafka prefixes and topic namespaces")

In this example:

1.  An instance administrator with the kafka\_namespace\_admin role creates namespace records for the Log Analysis group, the Fulfillment group, and another subsidiary in the ServiceNow instance.
2.  The instance administrator works with the Kafka administrator to replicate topics to Hermes using the Kafka cluster name as the namespace prefix.
3.  The Kafka cluster for the fulfillment group has a topic named `material_orders`. The topic is replicated to Hermes using `fulfillment` as the namespace prefix. A new topic is created in Hermes called `fulfillment.material_orders`.
4.  A scheduled job finds the `fulfillment.material_orders` topic in Hermes, creates a topic record, and assigns the record to the Fulfillment namespace to match its prefix.

## Prefix matching rules

Topic name prefixes are matched to namespaces according to the following rules.

-   The namespace is selected based on the longest matching namespace prefix. If there's a matching namespace, the topic record is assigned to that namespace and that namespace's domain.
-   If there isn't a longer namespace prefix that matches, the zero-length prefix of the Default Namespace will match. The topic record is assigned to the Default Namespace in the global domain.
-   If the Default Namespace has been deleted or modified, so there’s no matching namespace at all, then no topic record is created.

## Namespace design considerations

Plan how want to organize your namespaces and topics before you start creating them. Once you add a topic to a namespace, you can't delete the namespace without deleting the topics that are associated with it.

-   **Have a namespace for each domain on a domain-separated instance**

    Create one namespace per ServiceNow domain.

-   **Use namespaces to organize topics by domain and Kafka installation**

    Use namespaces to separate both topics that belong in separate ServiceNow domains and topics from separate Kafka installations.

-   **After you've configured your namespaces, consider deleting or deactivating the Default Namespace**

    Keeping the Default Namespace could lead to configuration issues, such as a mismatched topic prefix. This mismatch could result in a topic that should have been created in one domain being created in the global domain.

    You can enforce tighter constraints on where topics are created by deleting the Default Namespace. For example, if you decide that all topics must have a prefix that matches a namespace, deleting the Default Namespace ensures that topics without a matching prefix aren't created.


For details on using domain separation with namespaces in Hermes, see [Hermes Messaging Service domain separation](../reference/hermes-messaging-service-domain-separation.md).

-   **[Create a namespace in Hermes](../task/create-namespace-hermes.md)**  
Organize your Kafka topics by creating a namespace.
-   **[Delete a namespace in Hermes](../task/delete-namespace-hermes.md)**  
Prevent topics from being added to a namespace by deleting the namespace in Hermes.

**Parent Topic:**[Managing namespaces and topics in Hermes](managing-namespaces-topics-hermes.md)

**Related topics**  


[Managing topics in Hermes](managing-topics-hermes.md)

[Monitoring topics in the Hermes Kafka cluster](monitoring-topics-hermes-kafka-cluster.md)

