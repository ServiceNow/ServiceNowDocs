---
title: Check the status of and connection to the Hermes Kafka cluster
description: Check the status of and test the connection to the Hermes Kafka cluster by sending and receiving test messages.
locale: en-US
release: xanadu
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Check the status of and connection to the Hermes Kafka cluster

Check the status of and test the connection to the Hermes Kafka cluster by sending and receiving test messages.

## Before you begin

Role required: hermes\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Diagnostics**.

    The dashboard loads and Hermes diagnostic tests are run automatically verifying instance public key infrastructure \(PKI\) configuration, external port status, and Glide Hermes Message Queue plugin \(com.glide.hermes\) activation.

    If any of the tests fail, contact Customer Service and Support.

2.  View the producer and consumer bootstrap addresses that you can use to connect to Hermes in the Setup Information section.

    Use these port mappings to connect producer and consumer clients to the Kafka cluster bootstrap addresses, as described in [Exchanging data using Hermes](../concept/exchanging-data-hermes-messaging-service.md).

    **Note:** When configuring consumer clients, you must configure two clients using ports in separate ranges: one in 4100-4150 and another in 4200-4250.

3.  Verify that the instance can act as an issuer in an x.509 trust hierarchy.

    1.  Expand the **Instance PKI** container.

    2.  View the configuration status.

    3.  View additional instance PKI details on the Key Management Framework Health page by selecting **View more**.

    The instance PKI configuration status is displayed. If the configuration is valid, you can secure connections to Hermes by following the steps in [Set up a secure connection to the Hermes Messaging Service](set-up-secure-connection-to-hermes.md). If the configuration is invalid, contact Customer Service and Support.

4.  Confirm availability of the external ports used to connect to the Hermes Kafka cluster.

    1.  Expand the **Bootstrap Connectivity** container.

    2.  Select **Run Test**.

    In the range of ports required for Hermes, the following ports are checked:

    -   4000, 4001, 4002, 4003 producer client ports
    -   4100, 4102, 4102, and 4103 consumer client ports
    -   4200, 4201, 4202, and 4203 consumer client ports
    If the ports aren't open, contact Customer Service and Support.

5.  Confirm that the instance is able to send messages to and receive messages from the Hermes Kafka cluster.

    1.  Expand the **Instance Connectivity** container.

    2.  Select the set of clusters that you want to connect to in the **Hermes Service** drop-down list.

    3.  Select **Run Test**.

    Test Message Send and Test Message Receive results are displayed including the elapsed time, datacenter, and bootstrap information for each operation. If the tests fail, contact Customer Service and Support.

6.  Verify the timestamp of the most recent message from a topic in the Hermes Kafka cluster.

    1.  Expand the **View Topics** container.

    2.  Select the set of clusters that you want to connect to in the **Hermes Service** drop-down list.

    3.  Select **Get Topic List**.

    4.  View the timestamp for an external topic's last known message by selecting the topic name in the **External Topics** column.

    5.  View the timestamp for an internal topic's last known message by selecting the topic name in the **Internal Topics** column.

    The message's timestamp is displayed. To view full details for a topic, use the Hermes Topic Inspector. See [Monitoring topics in the Hermes Kafka cluster](../concept/monitoring-topics-hermes-kafka-cluster.md).


**Parent Topic:**[Hermes Messaging Service administration](../concept/hermes-messaging-service-administration.md)

**Related topics**  


[Monitoring data usage in Hermes](../concept/monitoring-data-usage-hermes.md)

[Tracking message usage in Hermes](../concept/tracking-hermes-messaging-service-usage.md)

[Cloning with Hermes Messaging Service enabled](../concept/cloning-with-hermes-messaging-service.md)

[View Hermes Messaging Service log messages](view-hermes-log-messages.md)

