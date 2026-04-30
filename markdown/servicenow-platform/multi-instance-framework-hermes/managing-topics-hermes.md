---
title: Managing topics in Hermes
description: Manage topic records in your instance and Kafka topics in the Hermes Kafka cluster using the Hermes Messaging Service.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managing topics in Hermes

Manage topic records in your instance and Kafka topics in the Hermes Kafka cluster using the Hermes Messaging Service.

## Topic records

Messages are organized and stored in Kafka topics in the Hermes Kafka cluster. Topic records are stored in the Kafka Topics \[sys\_kafka\_topic\] table in your instance. This table shows a list of topics records with a reference to each topic's namespace. Each topic record has a field for the topic's name, related namespace, and whether the topic is active.

Values in the Name column of the Kafka Topics \[sys\_kafka\_topic\] table aren't inherently unique. For example, topic records might have the same Name value when they belong to different namespaces or exist in different clusters. However, values in the Full Name column are always unique.

A scheduled job runs regularly to synchronize topic records with the topics found in Hermes. This job performs the following functions:

-   Creates topic records for any discovered topics, assigning them to the appropriate namespace based on the prefix for the topic name.
-   Synchronizes topics created from external sources, such as the Kafka command-line interface \(CLI\). For example, when a topic is created from an external source on the near cluster, the job runs and creates the topic on the far cluster as well.
-   Logs a warning message if a topic can't be matched to any namespace. If a topic can't be matched to any namespace, the topic record isn't created. There's a default, prefix-less namespace called the Default Namespace that matches all topics. The only time a topic doesn't match any namespace is when the Default Namespace has been deleted or modified.
-   Marks topics as inactive if no Kafka topic was found for them.

You can monitor and view topics in the Hermes Kafka cluster using the topic inspector. For more information, see [Monitoring topics in the Hermes Kafka cluster](monitoring-topics-hermes-kafka-cluster.md).

Kafka topics are specific to a particular instance. This means you can't migrate a topic record from the Kafka Topics \[sys\_kafka\_topic\] table to another instance using an update set. Instead, you must manually create the topic in the target instance.

## Creating topics

You can create topics in the Hermes Kafka cluster using either of the following methods:

-   Create the topic from your instance. This creates a record the Kafka Topics \[sys\_kafka\_topic\] table and creates a Kafka topic in the Hermes Kafka cluster. See [Create a topic in Hermes](../task/create-topic-instance-hermes.md).
-   Create the topic externally. For example, create the topic using the Kafka command-line interface \(CLI\).

    **Note:** To avoid syncing issues between the cluster and your instance, include the application ID when creating topics externally. For example, without the application ID, a topic created from the CLI with a name like `snc.instancename.fulfillment.topicname` is created in the default namespace instead of the `fulfillment` namespace. To ensure the topic is created in the `fulfillment` namespace, include the application ID in the name using the format `snc.instancename.fulfillment.app_id.topicname`. Replace `app_id` with the application ID of your choice.


If, for some reason, a topic can't be created in the Hermes Kafka cluster, it won't be created in the Kafka Topics \[sys\_kafka\_topic\] table either.

## Updating topics

If necessary, you can change the number of partitions in a topic. Note that you can only increase the number of partitions in a topic. For more information, see [Update a topic in Hermes](../task/update-topic-hermes.md).

After it's created, the namespace assigned to a topic record is permanent. If you create a namespace record and want to move existing topics to it, you must delete the topics and recreate them in the Hermes Kafka cluster with the new namespace prefix. If the topics weren't created through the instance, new topic records will be created and assigned to the matching namespace record after a rescan.

## Deleting topics

You can delete topics from the Hermes Kafka cluster using either of the following methods:

-   Delete the topic directly from the Kafka Topics \[sys\_kafka\_topic\] table in your instance. This method automatically deletes the topic from all the Hermes Kafka clusters in one action. See [Delete a topic in Hermes](../task/delete-topic-hermes.md)
-   Delete the topic externally. For example, delete the topic using the Kafka command-line interface \(CLI\).

    **Important:** Deleting the topic externally requires that you delete the topic from both Hermes clusters manually by specifying each set of ports \(410x and 420x\). If possible, delete the topic through the instance instead.


You can't delete a topic if it has subscriptions in Stream Connect.

## Rescanning topics

Rescanning creates topic records for any topics in the Hermes Kafka cluster that don't already have corresponding topic records. For example, if you create topics in Hermes using the CLI, you can rescan to create corresponding topic records in the Kafka Topics \[sys\_kafka\_topic\] table immediately instead of waiting for the scheduled job to create them.

-   The rescan occurs automatically every ten minutes.
-   Created topic records are assigned to existing namespaces based on prefix matching rules.

Sometimes topic records in your instance don't match what's in Hermes. This situation can happen in the following cases:

-   When the ServiceNow Integration Hub Kafka Consumer \(com.glide.hub.kafka\_consumer\) plugin is enabled after there are already topics in Hermes.
-   When topic records are deleted accidentally.
-   When namespace definitions are changed, and you want to assign existing topics to the new namespaces.

-   **[Create a topic in Hermes](../task/create-topic-instance-hermes.md)**  
Create a topic from within ServiceNow. Creating a topic from your instance adds a topic record to the Kafka Topics \[sys\_kafka\_topic\] table and adds a Kafka topic to Hermes.
-   **[Update a topic in Hermes](../task/update-topic-hermes.md)**  
Update a Kafka topic in Hermes by modifying the topic record.
-   **[Delete a topic in Hermes](../task/delete-topic-hermes.md)**  
Remove a topic and its messages by deleting it from Hermes. Deleting a topic record deletes it from your instance and from the Hermes Kafka cluster.
-   **[Rescan topics in Hermes](../task/rescan-topics-hermes.md)**  
Synchronize topic records in your instance with topics in the Hermes Kafka cluster by rescanning.

**Parent Topic:**[Managing namespaces and topics in Hermes](managing-namespaces-topics-hermes.md)

**Related topics**  


[Managing namespaces in Hermes](managing-namespaces-hermes.md)

[Monitoring topics in the Hermes Kafka cluster](monitoring-topics-hermes-kafka-cluster.md)

