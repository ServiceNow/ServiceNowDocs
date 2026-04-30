---
title: Configure ServiceNow Kafka Consumer
description: Retrieve events pertaining to the specified topics and store it in the required ServiceNow tables.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow Kafka Consumer, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure ServiceNow Kafka Consumer

Retrieve events pertaining to the specified topics and store it in the required ServiceNow tables.

## Before you begin

-   Request Integration Hub subscription.
-   Activate and set up the [Confluent Kafka REST Proxy Spoke](../concept/conf-kafka-spoke.md).
-   Activate ServiceNow Kafka Consumer.
-   Define entities and mapping between entities. For information, see [Robust Import Set Transformers](../../import-sets/concept/robust-import-set-transformers.md).
-   Role required: import\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Kafka Consumer**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the record.|
    |Broker Connection Alias|Connection alias of the [Confluent Kafka REST Proxy Spoke](../concept/conf-kafka-spoke.md).|
    |Topic|Topic from which you want to retrieve the events.|
    |Robust Transformer Definition|Robust Transformer Definition that is used for the event transformation and data storage in ServiceNow tables. For information, see [Robust Import Set Transformers](../../import-sets/concept/robust-import-set-transformers.md).|
    |Offset Starting Point|Value of the Kafka Consumer auto.offset.reset. This specifies what the Kafka Consumer should do when there is no initial offset or if the current offset does not exist any more on the server. See the [Kafka 2.7 documentation](https://kafka.apache.org/documentation/#consumerconfigs_auto.offset.reset) for more information.|
    |Partitions per group|Number of partitions per consumer thread.|
    |Page size \(bytes\)|Maximum size of a request.|
    |Page limit|Maximum number of requests per iteration.|
    |Embedded Format|Format of the Kafka message for the topic.|
    |Request timeout \(ms\)|Value of the Kafka Consumer consumer.request.timeout.ms. This specified the maximum amount of time the client waits for the response of a request. See the [Kafka 2.7 documentation](https://kafka.apache.org/documentation/#consumerconfigs_auto.offset.reset) for more information.|
    |Stop Upon Transform Errors|Option to stop listening when transformation errors are encountered.|
    |Verbose transformation|Option to log all the imported events to import set and produce additional debug logs for transformation.|

    **Note:** You must create one Kafka Consumer record for each topic.

4.  Click the **Start Sink Listener** related link.

    The Kafka Partition Group Listener States table is populated with the topic partition data.

5.  If you want to stop listening, click the **Start Sink Listener** related link.

6.  Navigate to **System Scheduler** &gt; **Scheduled Jobs**.

7.  Open the record, **Kafka Consumer Trigger**.

8.  From the **Trigger Type** list, select **Interval**.

9.  Click **Update**.


**Parent Topic:**[ServiceNow Kafka Consumer](../concept/kafka-consumer.md)

