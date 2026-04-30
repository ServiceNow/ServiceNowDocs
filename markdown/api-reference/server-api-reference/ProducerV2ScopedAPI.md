---
title: ProducerV2 - Scoped
description: The ProducerV2 API provides methods to publish messages from your ServiceNow instance to a Kafka topic.Sends the specified message to the specified Kafka topic.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProducerV2- Scoped

The ProducerV2 API provides methods to publish messages from your ServiceNow instance to a Kafka topic.

**Note:** This API requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

This API requires the ServiceNow Stream Connect Installer plugin \(com.glide.hub.stream\_connect.installer\) and runs in the `sn_ih_kafka` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProducerV2 - send\(String topicSysID, String key, String message, Boolean isSync, Object headers, String schemaID\)

Sends the specified message to the specified Kafka topic.

<table id="table_vn5_c3f_nvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicSysID

</td><td>

String

</td><td>

Sys\_id of the topic to publish the message to. Topics are stored in the Kafka Topics \[sys\_kafka\_topic\] table.

</td></tr><tr><td>

key

</td><td>

String

</td><td>

Name of the key for a specific partition in the topic.

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

Flag that indicates whether to require the script to wait for the send method to complete before continuing.Valid values:

-   true: Wait for the step to complete before continuing the associated flow.
-   false: Do not wait for the step to complete before continuing the associated flow.

</td></tr><tr><td>

headers

</td><td>

Object

</td><td>

Headers for the message, defined as key-value pairs. ```
"headers": {
  "<key>": "<value>"
}
```

For example, `var headers = { "origin": "sn_business_rule" };` -   `key`: String. Name of the header.
-   `value`: String. Value of the header.

</td></tr><tr><td>

schemaID

</td><td>

String

</td><td>

Sys\_id of the schema record.

 Required if you're using a schema to convert plain-text messages to Avro messages and back. Schemas are stored in the Stream Connect Schemas \[stream\_connect\_schema\] table. For more information, see [Schema management in Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to send changed incident information to the Kafka topic with a sys\_id of 75135aa2ff0311105cf343d0653bf155, using a schema with a sys\_id of f9d083f3ff610210ef7343d3653bf12e.

```
var message = {
  'number': current.number.toString(),
  'short_description': current.short_description.toString(),
  'caller_id': current.caller_id.getDisplayValue(),
  'priority': current.priority.toString(),
  'state': current.state.toString()
};

var headers = {
    'origin': 'sn_business_rule'
};

var producer = new sn_ih_kafka.ProducerV2();
producer.send('75135aa2ff0311105cf343d0653bf155', gs.generateGUID(), JSON.stringify(message), false, headers, 'f9d083f3ff610210ef7343d3653bf12e');

```

