---
title: HermesEventPublisherOOB - Scoped
description: The HermesEventPublisherOOB script include provides methods to publish messages to the Hermes Messaging Service.Returns the message headers associated with the passed message.Returns the partition key associated with the passed message.Returns all Kafka topics that are associated with the passed message.Publishes the passed TMF688-compliant payload using the Hermes Messaging Service.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# HermesEventPublisherOOB- Scoped

The HermesEventPublisherOOB script include provides methods to publish messages to the Hermes Messaging Service.

If you want to change the default functionality of this script include, you need to override the methods contained in this script include in the `HermesEventPublisher` script include. For additional information on overriding the methods in this script include, see [Configure the Producer Event Notification Framework to use the Hermes Messaging Service](../../../../../integrate/guides/ProducerEventNotifFramework/task/prod_evt_not-dev_gd-cfg_herm_bus.md).

This script include runs in the `sn_api_notif_mgmt` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## HermesEventPublisherOOB - fetchMessageHeaders\(Object message\)

Returns the message headers associated with the passed message.

You must call this method before publishing the message through the Hermes Messaging Service.

The default implementation of this method only sets the *origin* header value to `TMT_SERVICENOW`. If any other header attributes should be passed back by this method based on your business requirements, you must override this method in the `HermesEventPublisher` script include and provide the additional header attributes.

|Name|Type|Description|
|----|----|-----------|
|message|Object|TMF event to publish to the Hermes Kafka message broker. For details on the format of this message, see [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

<table id="table_vwm_zd1_vzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Kafka headers to use for the passed message.For example:

```
{
  origin: 'TMT_SERVICENOW'
}
```

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
publishMessageThroughProducerV2API: function(message) {
  if (gs.nil(message)) return;
  var comptableTopicSysIds = this.fetchTopicsForMessage(message);
  if (gs.nil(comptableTopicSysIds)) return;

  for (var i = 0; i < comptableTopicSysIds.length; i++) {
    var partitionKey = this.fetchPartionKey(message);
    var headers = this.fetchMessageHeaders(message)
    try {
      var producer = new sn_ih_kafka.ProducerV2();
      producer.send(comptableTopicSysIds[i], partitionKey, JSON.stringify(message), false, headers);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  }
},
```

## HermesEventPublisherOOB - fetchPartionKey\(Object message\)

Returns the partition key associated with the passed message.

You must call this method before publishing the message through the Hermes Messaging Service.

The default implementation for this method returns an auto-generated unique ID as the partition key. This type of implementation ensures that messages are evenly published across all partitions of the topic. If you want to modify the handling of partitions, you must override this method in the `HermesEventPublisher` script include. Another possible implementation is to return a unique partition key based on the message event type, or other attribute, to ensure the sequencing of messages of the same event type or attribute.

|Name|Type|Description|
|----|----|-----------|
|message|Object|Message to publish using the Hermes Kafka message broker. For details on the format of this message, see [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

<table id="table_vwm_zd1_vzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Kafka partition key to use for the passed message.For example: 6B29FC40-CA47-1067-B31D-00DD010662DA

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
publishMessageThroughProducerV2API: function(message) {
  if (gs.nil(message)) return;
  var comptableTopicSysIds = this.fetchTopicsForMessage(message);
  if (gs.nil(comptableTopicSysIds)) return;

  for (var i = 0; i < comptableTopicSysIds.length; i++) {
    var partitionKey = this.fetchPartionKey(message);
    var headers = this.fetchMessageHeaders(message)
    try {
      var producer = new sn_ih_kafka.ProducerV2();
      producer.send(comptableTopicSysIds[i], partitionKey, JSON.stringify(message), false, headers);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  }
},
```

The following code example shows how to override this method to include your own logic for determining the partition key to use for the specified message.

```
// Existing implementation for fetching a partition key which is an auto-generated unique ID.
fetchPartionKey: function(message) { 
  // Implement it for custom partition key 
  // Random message key ensures better distribution of messages across partitions. 
  // Same message key ensures that messages always goes to the same partition. This ensures a strict sequencing
  //  of messages at the Kafka consumer group level. 
  return gs.generateGUID(); 
}, 

// Implementation where the partition key is determined based on the event type.
fetchPartionKey: function(message) {
  var eventType = message.eventType;
  var partionKey = fetchPartionKeyForMessage(eventType);
  return partionKey;
},
```

## HermesEventPublisherOOB - fetchTopicsForMessage\(Object message\)

Returns all Kafka topics that are associated with the passed message.

This method is not implemented in the base implementation, it only returns a static sys\_id. You must override this method in the `HermesEventPublisher` script include and provide logic that determines which Kafka topic or topics to send the passed message to.

For additional information on how to implement this method, see [Configure the Producer Event Notification Framework to use the Hermes Messaging Service](../../../../../integrate/guides/ProducerEventNotifFramework/task/prod_evt_not-dev_gd-cfg_herm_bus.md).

|Name|Type|Description|
|----|----|-----------|
|message|Object|TMF message to publish to the Hermes Kafka message broker. For details on the format of this message, see [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

<table id="table_vwm_zd1_vzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of sys\_ids of the Kafka topics to which the message should be sent.For example:

```
[
  "9d385017c611228701d22104cc95c371",
  "8438201ec613628421e13105d396d421"
]
```

Table: Kafka Topic \[cmdb\_ci\_appl\_kafka\_topic\]

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
publishMessageThroughProducerV2API: function(message) {
  if (gs.nil(message)) return;
  var comptableTopicSysIds = this.fetchTopicsForMessage(message);
  if (gs.nil(comptableTopicSysIds)) return;

  for (var i = 0; i < comptableTopicSysIds.length; i++) {
    var partitionKey = this.fetchPartionKey(message);
    var headers = this.fetchMessageHeaders(message)
    try {
      var producer = new sn_ih_kafka.ProducerV2();
      producer.send(comptableTopicSysIds[i], partitionKey, JSON.stringify(message), false, headers);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  }
},
```

The following code example shows how to override this method to return the same topic record sys\_id for each passed message.

```
// Return the same topic for all messages if your 
 // implementation only supports one kind of topic

fetchTopicsForMessage: function(message) { 
// Return the same sys_id for all passed messages which
// implies that all of the messages are published to the same topic.
return ['91564fc087f8351063151f473cbb35f8'];
},
```

The following code example shows how to override this method to identify topics to send a message to based on the event type in the message.

```
// Fetch the topic based on the message content. 
// This could be based on the message domain type or the message event type.

fetchTopicsForMessage: function(message) { 
// Implement to return topic based on a message content
// Implementor may decide a topic based on 'eventType' or any other attribute.

var eventType = message.eventType;

var topicSysIdsArr = this.fetchTopicBasedOnEventType(eventType);
return topicSysIdsArr

},
```

## HermesEventPublisherOOB - publishEventToHermesKafka\(Object tmfEventPayload\)

Publishes the passed TMF688-compliant payload using the Hermes Messaging Service.

This is a parent method that calls other methods to publish the event. It is unlikely that you will need to override this method unless you want to change the Kafka publishing mechanism, such as using Workflow Studio instead of using the [ProducerV2](../../ProducerV2/concept/ProducerV2ScopedAPI.md#) API.

|Name|Type|Description|
|----|----|-----------|
|tmfEventPayload|Object|TMF688-compliant event payload. For a description of the format of this event payload, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
publishMessageToHermesKafka: function(tmfEventPayload) {
  new HermesEventPublisher().publishEventToHermesKafka(tmfEventPayload);
},
```

