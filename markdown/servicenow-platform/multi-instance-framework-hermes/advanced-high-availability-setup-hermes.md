---
title: Advanced High Availability transfer with Hermes
description: Learn how messages are produced and consumed in Hermes during normal operation, Advanced High Availability \(AHA\) transfer, and failover scenarios.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced High Availability transfer with Hermes

Learn how messages are produced and consumed in Hermes during normal operation, Advanced High Availability \(AHA\) transfer, and failover scenarios.

ServiceNow production instances operate in geographically separate data centers. Each data center is paired with another data center to provide redundancy with failover support. One data center is designated as the active side and the other as standby. For example, your instance might be configured in the DC1 and DC2 data centers, with DC1 as the active side.

With the activation of StreamConnect, LES, or IDR, a new Hermes Kafka cluster is provisioned in both data centers. To ensure high availability and provide failover support, Hermes uses a pair of active/active Kafka clusters, one in each data center.

-   **Near cluster**

    The Hermes Kafka cluster located in the same data center as the instance is the near cluster.

-   **Far cluster**

    The cluster running in the other data center is the far cluster. The opposite is true for the other instance. Its near cluster is in its data center, and its far cluster is running in the other data center.


![Near and far Hermes Kafka clusters are relative to the instance.](../images/hermes-near-far.png "Near and far Hermes Kafka clusters")

## Normal operation

Under normal operating conditions, messages are produced by the instance or an external client to the near Hermes cluster. For example, if your instance is running in the DC1 datacenter, messages are produced to the near Hermes cluster in DC1. Messages sent from an external client are produced to the cluster using a port in the 400x range as defined in the producer bootstrap URL.

When a topic is created in Hermes, its created in both clusters. Two consumer processes are used for consuming messages from both clusters, but only a single consumer is actively consuming under normal circumstances. Each consumer must use distinct bootstrap URLs, one in the 410x range and the other in the 420x range.

## Failover process

Under the following circumstances, the cluster where messages are produced can change.

-   **Instance Advanced High Availability \(AHA\) Transfer**

    When an instance undergoes an AHA transfer, the standby instance becomes active, and the previously active instance becomes standby. In this scenario, the instance switches to using the Hermes cluster on the newly-active side.

    For example, if the instance is running in DC1 and DC2 datacenters with DC1 as the current active side, and an AHA transfer occurs, the instance switches to using the Hermes cluster in DC2.

-   **Hermes failover**

    The instance actively monitors the health of the Hermes cluster. If it detects any issues with the cluster, it enters failover mode. In this case, until the instance detects that the near Hermes cluster has recovered, it uses the Hermes cluster near the standby instance.

    For example, if the instance is running in DC1 and DC2 datacenters with DC1 as the active side, it uses the Hermes cluster in DC1. If it detects an issue with the Hermes cluster in DC1, it enters Hermes failover mode and starts producing messages to the DC2 cluster until the DC1 cluster is healthy again. After recovery, it resumes using the Hermes cluster in DC1.


When failover occurs, if consumers are lagging, both consumers can potentially consume messages until one of the consumers finishes processing. For example, if the current active side is DC1, the consumer consuming from DC1 is actively processing messages. If a problem occurs in the DC1 cluster resulting in failover to the DC2 cluster, the consumer consuming from the DC2 cluster starts processing messages. If the consumer consuming from the DC1 cluster was lagging, both consumers continue to consume messages until the DC1 consumer catches up.

## Maintaining order

If maintaining message order is required, it’s the responsibility of the consumer application to manage this. Note that the global ordering of messages is dependent on how the topic in Kafka is defined.

