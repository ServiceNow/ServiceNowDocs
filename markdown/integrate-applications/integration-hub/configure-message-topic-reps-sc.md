---
title: Create message and Kafka topic replications in Stream Connect
description: Set up message and topic replications to replicate data between your Apache Kafka environment and ServiceNow.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Message replication, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create message and Kafka topic replications in Stream Connect

Set up message and topic replications to replicate data between your Apache Kafka environment and ServiceNow.

## Before you begin

-   Role required: message\_replication\_admin
-   This feature requires a subscription. For more information, see [Using Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md).
-   Verify the Hermes Messaging Service and Instance PKI Certificate Generator are working.
    -   [Check the status of and connection to the Hermes Kafka cluster](https://www.servicenow.com/docs/access?context=run-hermes-messaging-service-diagnostics&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   Check the [Key Management Framework Health](https://www.servicenow.com/docs/access?context=kmf_diagnostics&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) to verify that all three items in the Instance PKI section are operational.
-   Configure and start a MID Server or MID Server cluster. For more information, see [Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    The MID Server must be able to access Hermes endpoints through the firewall. Work with your network administrator to make sure that the following port ranges are open.

    -   Producer: 4000–4050
    -   Consumer1: 4100–4150
    -   Consumer2: 4200–4250
    If you're using a MID Server cluster, it must have a cluster type of **Load Balance**. The **Failover** cluster type is not supported.

-   Stream Connect Message Replication uses a Connection &amp; Credential alias to connect to your local Kafka. [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) with a **Connection type** of **Kafka**. A Connection &amp; Credential alias requires a [Kafka Connection](configure-kafka-connection.md) and a [Kafka SSL Credential](create-kafka-ssl-credentials.md).
-   Stream Connect Message Replication requires the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

## About this task

This page shows you how to create a Message Replication record and an associated Kafka Topic Replication record.

A Message Replication record represents a single Kafka cluster. For example, if you have two Kafka clusters, you would create two different message replication records, one for each cluster. A Message Replication record is the parent record for all the topics being replicated to or from that cluster. Message Replication records are stored in the Message Replications \[sys\_sc\_message\_replication\] table.

A Kafka Topic Replication record specifies the replication from a single source topic to a single destination topic. You can't replicate a single source topic to multiple destinations. You can only replicate to each destination once. Kafka Topic Replication records are stored in the Kafka Topic Replications \[sys\_kafka\_topic\_replication\] table.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Message Replications** and select **New**.

2.  On the Message Replication form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the message replication.|
    |Messaging service connection|Connection &amp; Credential alias specifying which messaging service to connect to.|
    |Application|Application scope for the message replication. This field is automatically set.|
    |Active|Option to activate the message replication.|

3.  Select **Save**.

    After you save the form, the Message Replication Statuses and Kafka Topic Replications tabs appear at the bottom of the page.

4.  On the Kafka Topic Replications tab, select **New**.

5.  On the Kafka Topic Replication form, fill in the fields.

<table id="table_smq_zzc_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the topic replication. The name is generated automatically based on the values in other fields.

 To generate the **Name**, enter the values for the **Direction**, **ServiceNow topic**, and **Topic name** fields, then select **Save**.

 When the **Direction** is **To ServiceNow**, the **Name** has the following format: `topic name [replication name] -> ServiceNow topic name [SN]`.

 When the **Direction** is **From ServiceNow**, the **Name** has the following format: `ServiceNow topic name [SN] -> topic name [replication name]`.

</td></tr><tr><td>

Direction

</td><td>

Direction of the topic replication.-   **To ServiceNow** replicates a topic from your local Kafka environment to ServiceNow.
-   **From ServiceNow** replicates a topic from ServiceNow to your local Kafka environment.


</td></tr><tr><td>

ServiceNow topic

</td><td>

Reference to the Kafka Topics \[sys\_kafka\_topic\] table.

</td></tr><tr><td>

Replication

</td><td>

Message replication that manages this topic replication.

</td></tr><tr><td>

Topic name

</td><td>

Name of the topic in your local Kafka environment.

</td></tr><tr><td>

Active

</td><td>

Option to activate the topic replication.

</td></tr><tr><td>

Track in current update set

</td><td>

When selected, the topic replication is added to the current update set, so it's simpler to promote it from sub-production to production instances. You may need to configure the form to add this field.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  Follow steps 1–6 to create message and topic replications for all your Kafka clusters and topics.


## Result

After you've created all your message and topic replication records, messages should be replicating. You can check the Message Replication Statuses \[sys\_sc\_message\_replication\_status\] tab on the Message Replication form to view the status, MID Server, and error messages for each message replication.

You can also check the Channel Replication Statuses \[sys\_sc\_channel\_replication\_status\] tab on the Kafka Topic Replication record to view status details for each topic replication, including the **MID Server**, **Error message**, and **Error Since** values.

Each Kafka Topic Replication record also has a related list named Message Replication Statistics. Once replications are running, this list displays metrics records, which are created every 60 seconds for each topic replication. Each metrics record has information about the topic replication, including the **Message count**, which shows the number of messages replicated in each collection interval.

## What to do next

If you're replicating messages from your local Kafka into ServiceNow, you can configure a [Script](configure-script-consumer.md), [ETL](configure-etl-consumer.md), or [Transform Map](configure-transform-map-consumer.md) consumer to process the messages or set up a [Kafka Message trigger](https://www.servicenow.com/docs/access?context=create-flow-kafka&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) to start a flow.

If you're replicating messages from ServiceNow to your local Kafka, you can use a [Kafka Producer step](https://www.servicenow.com/docs/access?context=kafka-producer-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) in Workflow Studio or use the [ProducerV2 API](https://www.servicenow.com/docs/access?context=ProducerV2ScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) to publish messages to the Hermes topic and your local Kafka.

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

