---
title: Producer - Scoped \(deprecated\)
description: The Producer API provides methods that enable you to push data from a ServiceNow instance to a Kafka topic.Sends the specified message to the specified Kafka topic.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Producer- Scoped \(deprecated\)

The Producer API provides methods that enable you to push data from a ServiceNow instance to a Kafka topic.

**Note:** This API is deprecated and replaced by the [ProducerV2 - Scoped](../../ProducerV2/concept/ProducerV2ScopedAPI.md#) API.

This API requires the ServiceNow Integration Hub Action Step - Kafka Producer plugin \(com.glide.hub.action\_step.kafka\) and is provided within the `sn_ih_kafka` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Producer - send\(String topic, String key, String message, Boolean isSync\)

Sends the specified message to the specified Kafka topic.

<table id="table_scd_fzf_mrb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topic

</td><td>

String

</td><td>

Name of the topic to publish the message to. A topic stores messages of the same type. For example, a topic named Payments might store messages about recent payments.

 When you enter the topic name, include everything that comes after the instance name prefix. For example, if the complete topic name is `snc.<instancename>.sn_streamconnect.<topicname>`, enter `sn_streamconnect.<topicname>` in the topic field.

</td></tr><tr><td>

key

</td><td>

String

</td><td>

Name of the key for a specific partition. Topics can be partitioned. Messages with the same key are stored in the same partition. For example, payment messages with a key of June would all be stored in the same partition of the Payments topic.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message text.

</td></tr><tr><td>

isSync

</td><td>

Boolean

</td><td>

Flag that indicates whether to require the flow to wait for the step to complete before continuing.Valid values:

-   true: Wait for the step to complete before continuing the associated flow.
-   false: Do not wait for the step to complete before continuing the associated flow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to send changed incident information to the changed\_incidents Kafka topic.

```
var message = {
  'number': current.number.toString(),
  'short_description': current.short_description.toString(),
  'caller_id': current.caller_id.getDisplayValue(),
  'priority': current.priority.toString(),
  'state': current.state.toString()
};

var producer = new sn_ih_kafka.Producer();
producer.send('changed_incidents', current.number.toString(), JSON.stringify(message), false);
```

