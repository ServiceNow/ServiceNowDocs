---
title: Producing and consuming messages from a Kafka client
description: Learn how to produce and consume messages to Hermes from a Kafka client.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-08-13"
reading_time_minutes: 2
breadcrumb: [Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Producing and consuming messages from a Kafka client

Learn how to produce and consume messages to Hermes from a Kafka client.

To begin exchanging messages from a Kafka client, start by creating a topic in the Hermes Kafka cluster. After you successfully create the topic, you must create a total of three processes to communicate with Hermes.

-   One process is required to produce messages to Hermes.
-   Two processes are required to consume messages from Hermes. Two processes are required because Hermes uses a pair of Kafka clusters for failover purposes. If one cluster goes down, data is produced to the other Hermes Kafka cluster.

    **Important:** You must configure two distinct consumer bootstrap addresses, one for each consumer client.


One consumer process uses ports in the 410x range and the other uses ports in the 420x range. This means you must define two distinct clients, one for each port range. Within each client configuration, you can define consumer group IDs.

## Required port ranges

Work with your network administrator to ensure that the following port ranges are open before you begin exchanging messages using Hermes:

-   Producer: 4000-4050
-   Consumer1: 4100-4150
-   Consumer2: 4200-4250

To confirm that the ports are accessible through the firewall, run the following command:

```
openssl s_client -connect <instance_name>.service-now.com:<port> -servername <instance_name>.service-now.com
```

-   Change the service-now.com domain if your instance uses a different domain name.
-   Complete the test using ports from each of the three port ranges. For example: test 4000-4003, 4100-4103, and 4200-4203.

If the command fails internally but succeeds from a client outside the network, consult your network administrator to gain access through the network firewall.

## Bootstrap addresses

Use the following port mappings to connect producers and consumers to the Kafka cluster bootstrap addresses. All Application Delivery Controllers used by Hermes follow this same convention.

**Important:** The following Hermes bootstrap address examples use ports 4000-4003, 4100-4103, and 4200-4203. However, you must open the following port ranges to ensure connectivity as additional clusters are added to the Hermes Messaging Service.

-   Producer: 4000-4050
-   Consumer1: 4100-4150
-   Consumer2: 4200-4250

Producer clients use ports ranging from 4000 to 4050. For example:

```powershell
Producers = "<instance_name>.service-now.com:4000,<instance_name>.service-now.com:4001,<instance_name>.service-now.com:4002,<instance_name>.service-now.com:4003"
```

Because Hermes uses a pair of Kafka clusters, you must configure two consumer clients with separate consumer bootstrap addresses.

**Important:** You must configure two distinct consumer bootstrap addresses, one for each consumer client.

-   The first consumer client uses ports ranging from 4100 to 4150. For example:

    ```powershell
    Consumer A = "<instance_name>.service-now.com:4100,<instance_name>.service-now.com:4101,<instance_name>.service-now.com:4102,<instance_name>.service-now.com:4103"
    ```

-   The second consumer client uses ports ranging from 4200 to 4250. For example:

    ```powershell
    Consumer B = "<instance_name>.service-now.com:4200,<instance_name>.service-now.com:4201,<instance_name>.service-now.com:4202,<instance_name>.service-now.com:4203"
    ```


When you configure producer and consumer properties for your own Kafka client, use this string pattern.

## Using the command-line interface \(CLI\)

When using the `list` command to view a list of topics, a list of current topics are returned from one or both clusters. Topics might be returned from only one cluster, depending on when the last synchronization occurred. Topics created for failover purposes are differentiated by a three-letter cluster identification prefix.

When accessing the Hermes clusters using the CLI, internal topics appear in addition to any topics you've created. For details, see [KB1705399](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705399).

You can't delete a topic from both Kafka clusters using a single command in the command-line interface \(CLI\). However, you can delete the topic from both clusters by deleting the topic record in your instance. See [Delete a topic in Hermes](../task/delete-topic-hermes.md).

