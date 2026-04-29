---
title: Direct Kafka
description: Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka. Build efficient integrations between your enterprise systems, enabling high-volume and robust integrations to exchange data between applications, and reduce data loss with the queuing mechanism if one environment is temporarily offline.Configure a Direct Kafka Cluster for your local Kafka topics.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Direct Kafka

Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka. Build efficient integrations between your enterprise systems, enabling high-volume and robust integrations to exchange data between applications, and reduce data loss with the queuing mechanism if one environment is temporarily offline.

With Direct Kafka, you can configure a custom Kafka connection to integrate Stream Connect on your on-premise instance with your local Kafka environment. This connection enables you to use Stream Connect and its features directly, without requiring the Hermes Messaging Service or a separate message replicator.

## Direct Kafka Clusters

You can define a Direct Kafka Cluster for your local Kafka environment. A Direct Kafka Cluster uses a Connection and Credential alias to connect to your local Kafka. Once connected, the list of topics in your local Kafka is synchronized with your ServiceNow instance every five minutes. The Direct Kafka Cluster form displays the topics from your local Kafka, along with their partitions and topic aliases. You can also test the connection to the local Kafka from the Direct Kafka cluster form.

The following image shows an example of a Direct Kafka Cluster. The Connection and Credential alias is entered in the **External Kafka** field. Under Related Links, there's a link to **Test Direct Kafka Connection**. In the Direct Kafka Topics section, there's a list of the local Kafka topics and their partitions and topic aliases.

![Screen shot of a Direct Kafka Cluster record.](../images/direct-kafka-cluster.png)

## Connection and Credential aliases

Direct Kafka requires a Connection and Credential alias. For details on how to set one up, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Direct Kafka also requires a Kafka connection to connect to your local Kafka environment. For details, see [Configure a Kafka connection](../tasks/configure-kafka-connection.md). When configuring the Kafka connection, there are a couple things to keep in mind.

-   The **Bootstrap servers** are required. Enter a comma-separated list in the format HOST:PORT,HOST:PORT. The list doesn't need to include all the Apache Kafka cluster servers.
-   Direct Kafka doesn’t use a MID Server. When you create the Kafka connection, make sure the **Use MID Server** check box isn’t checked. If you want to use an existing connection that uses a MID Server, you can change the check box if the connection isn’t already being used.

## Topic synchronization

After a Direct Kafka Cluster is created, local Kafka topics are added to the External Kafka Topics \[sys\_kafka\_external\_topic\] table. A scheduled job runs every five minutes to synchronize the local Kafka topics with the topics in the External Kafka Topics table.

## Create a Direct Kafka Cluster

Configure a Direct Kafka Cluster for your local Kafka topics.

### Before you begin

-   Role required: admin
-   A Direct Kafka cluster requires a Connection and Credential alias and a Kafka connection. For step-by-step instructions, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US) and [Configure a Kafka connection](../tasks/configure-kafka-connection.md).

    **Note:** Direct Kafka doesn’t use a MID Server. When you create the Kafka connection, make sure the **Use MID Server** check box isn’t checked.


### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Direct Kafka Cluster** and select **New**.

2.  Enter a name in the **Name** field and the Connection and Credential alias in the **External Kafka** field, then select **Submit**.

    You can also add the domain in the **Domain** field.

3.  From the Direct Kafka Clusters list, select the cluster you just created.

4.  Test the connection by selecting **Test Direct Kafka Connection** under Related Links.

    The Test Connection window will open, run the test, and report the results.


### Result

The topics from your local Kafka will be imported to ServiceNow and visible on the External Kafka Topics \[sys\_kafka\_external\_topic\] table. A scheduled job runs every five minutes to synchronize local Kafka topics with the topics in the External Kafka Topics table.

### What to do next

[Create topic aliases](manage-topic-alias.md#) to connect to your Direct Kafka topics.

