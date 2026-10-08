---
title: KafkaProducerAPI - Scoped
description: The KafkaProducerAPI provides a method to produce messages from server-side scripts to an Apache Kafka topic.Instantiates a KafkaProducerAPI.Sends a message to a Kafka topic, optionally running a script include if an asynchronous send fails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/server-api-reference/KafkaProducerAPIScoped.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-09-15"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# KafkaProducerAPI- Scoped

The KafkaProducerAPI provides a method to produce messages from server-side scripts to an Apache Kafka topic.

To access this API, the ServiceNow IntegrationHub Action Step - Kafka Producer plugin \(`com.glide.hub.action_step.kafka`\) must be activated. This API runs in the `sn_ih_kafka` namespace.

Use the send\(\) method to deliver a message to a Kafka topic. Before calling send\(\), a [topic alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-topic-alias.md) record for the target Kafka topic must exist in the Topic Alias \[sys\_sc\_topic\_alias\] table.

Permission for sending messages to a given topic is enforced by access control on the topic alias record.

For more information about working with Kafka topics, see [Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/stream-connect-apache-kafka.md).

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/api-server.md)

## KafkaProducerAPI - KafkaProducerAPI\(\)

Instantiates a KafkaProducerAPI.

|Name|Type|Description|
|----|----|-----------|
|None| ||

Creates an instance of KafkaProducerAPI.

```
var kafkaProducerAPI = new sn_ih_kafka.KafkaProducerAPI();
```

## KafkaProducerAPI - send\(Object params\)

Sends a message to a Kafka topic, optionally running a script include if an asynchronous send fails.

Before calling this method for asynchronous message delivery, create a script include to handle delivery failures. When the script include executes, an array of error objects \(**callbackErrors**\) is passed to the callback function. Each error object represents one message delivery failure.

<table id="table_send_errorobj"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

String

</td><td>

The value passed as **params.context** in the original send\(\) call for the failed message. Data type: String

</td></tr><tr><td>

errorMessage

</td><td>

String

</td><td>

Error message describing the reason for failure. Data type: String

</td></tr><tr><td>

errorType

</td><td>

String

</td><td>

The fully qualified class name for the exception. Data type: String

</td></tr><tr><td>

producerId

</td><td>

String

</td><td>

Sys\_id of the producer event associated with the failed send.Table: Kafka Producers \[sys\_kafka\_producer\]

Data type: String

</td></tr></tbody>
</table><table id="table_send_params" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

params

</td><td>

Object

</td><td>

Object containing parameters to use for sending the message.```
{
   context: "String",
   headers: {Object},
   isSync: Boolean,
   key: "String",
   message: "String",
   onErrorScriptIncludeId: "String",
   topicSysId: "String" 
}
```

</td></tr><tr><td>

params.context

</td><td>

String

</td><td>

Optional. Caller-supplied context string to pass to the script include if an asynchronous send fails. Used to identify the message that triggered the failure.

</td></tr><tr><td>

params.headers

</td><td>

Object

</td><td>

Optional. Key-value pairs for message headers. Any headers supported by Apache Kafka are valid. For example:```
{
   "source": "order_update_br",
   "correlation_id": "8a1c3f2b1b3a10"
}
```

</td></tr><tr><td>

params.isSync

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to send the message synchronously. Possible values:-   true: Send synchronously and block for the result.
-   false: Send asynchronously. An error callback can be specified in **onErrorScriptIncludeId** to execute when an asynchronous send fails.

Default: false

</td></tr><tr><td>

params.key

</td><td>

String

</td><td>

Optional. Message key for partitioning in Apache Kafka. Messages with the same key are sent to the same partition, ensuring ordering.Default: Empty string

</td></tr><tr><td>

params.message

</td><td>

String

</td><td>

Content of the message to send to the topic.

</td></tr><tr><td>

params.onErrorScriptIncludeId

</td><td>

String

</td><td>

Optional. Sys\_id of the script include to run if an asynchronous send fails. Default: None

Table: Script Includes \[sys\_script\_include\]

</td></tr><tr><td>

params.schemaSysId

</td><td>

String

</td><td>

Optional. Sys\_id of a registered schema record to use for encoding the message.Default: The message is sent as plain text.

Table: Stream Connect Schemas \[stream\_connect\_schema\]

</td></tr><tr><td>

params.topicSysId

</td><td>

String

</td><td>

Sys\_id of the target Kafka topic alias record.Table: Topic Alias \[sys\_sc\_topic\_alias\]

</td></tr></tbody>
</table><table id="table_send_returns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Map containing delivery result information.For synchronous delivery, the method returns after the message is delivered. For asynchronous delivery, the method returns immediately. The delivery may later succeed or fail. Asynchronous delivery failure can be handled using the provided **onErrorScriptIncludeId**.

```
{
   delivery: "String",
   offset: Number,
   partition: Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.delivery

</td><td>

Delivery type.Possible values:

-   `async`: The message will be sent asynchronously.
-   `sync`: The message was sent synchronously.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.offset

</td><td>

Unique ID assigned to the message within the topic partition. Only returned for `sync` delivery.Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.partition

</td><td>

Partition that the message was delivered to. Only returned for `sync` delivery.Data type: Number

</td></tr></tbody>
</table>This business rule sends an order-updated event asynchronously, routing any delivery failure to the example `KafkaSendFailureHandler` script include. Note that `KafkaSendFailureHandler` is shown only as an example; you must create your own script include to handle delivery failures.

```
var kafkaProducerAPI = new sn_ih_kafka.KafkaProducerAPI();

var response = kafkaProducerAPI.send({
    topicSysId: '8a1c3f2b1b3a1010e7cfc51b1ce0bc42', // sys_id for 'orders.updated'
    key: current.getUniqueValue(),
    message: JSON.stringify({
        order_id: current.getUniqueValue(),
        status: current.getValue('status')
    }),
    isSync: false,
    headers: { source: 'order_update_br' },
    onErrorScriptIncludeId: 'b2e4a1c3f2b1a1010e7cfc51b1ce0c99', // sys_id of KafkaSendFailureHandler
    context: current.getUniqueValue()
});

gs.info('Kafka send submitted, delivery mode: ' + response.delivery);
// Output:
// Kafka send submitted, delivery mode: async
```

This script include reads **callbackErrors** and logs each delivery failure.

```
// Script include: KafkaSendFailureHandler
(function callback(callbackErrors) {

    gs.info("callback size: ", callbackErrors.length);

    for (var i = 0; i < callbackErrors.length; i++) {
        gs.info("callback " + callbackErrors[i].errorMessage + " " +
            callbackErrors[i].errorType + " " +
            JSON.stringify(callbackErrors[i].context) + " " +
            callbackErrors[i].producerId);
    }

})(callbackErrors);
```

