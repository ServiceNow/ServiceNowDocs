---
title: Configure the Producer Event Notification Framework to use the Hermes Messaging Service
description: If you are using the Hermes Messaging Service in your instance, you must configure the Producer Event Notification Framework for the Kafka message-bus.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Configure the Producer Event Notification Framework to use the Hermes Messaging Service

If you are using the Hermes Messaging Service in your instance, you must configure the Producer Event Notification Framework for the Kafka message-bus.

## Before you begin

Role required: admin

The Hermes Messaging Service must be activated. For details, see [Activating the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service-activation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

The following code snippet shows the HermesEventPublisher methods that must be called to configure the elements needed to send a message to a topic using the Hermes Messaging Service. The [ProducerV2](../../../../app-store/dev_portal/API_reference/ProducerV2/concept/ProducerV2ScopedAPI.md#) API is then called to send the message.

```
publishEventToHermesKafka: function(tmfEventPayload) {
  if (gs.nil(tmfEventPayload)) {
    return;
  }
  this.publishMessageThroughProducerV2API(tmfEventPayload)

},

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

## Procedure

1.  Set up a secure connection to the Hermes Messaging Service.

    For details, see [Set up a secure connection to the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=set-up-secure-connection-to-hermes&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

2.  Override the default functionality in the [HermesEventPublisherOOB - fetchTopicsForMessage\(Object message\)](../../../../app-store/dev_portal/API_reference/HermesEventPublisherOOB/concept/HermesEventPublishOOBScopedAPI.md#) method with your custom topic picker logic when publishing a message to the Hermes Messaging Service.

    In the HermesEventPublisher - fetchTopicsForMessage\(\) method, you must provide logic that determines which Kafka topic or topics to send a specified message to. You then return the sys\_ids of those topic records in an array.

    You can select a topic based on an attribute in the message payload or you can return the same topic for each message if your implementation only utilizes a single topic.

    The following example shows how to return the same topic record sys\_id for each passed message.

    ```
    // Return the same topic for all messages if your 
     // implementation only supports one kind of topic
    
    fetchTopicsForMessage: function(message) { 
    // Return the same sys_id for all passed messages which
    // implies that all of the messages are published to the same topic.
    return ['91564fc087f8351063151f473cbb35f8'];
    },
    ```

    The following example shows how to identify topics to send a message to based on the event type in the message.

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

3.  Override the default functionality in the [HermesEventPublisherOOB - fetchPartionKey\(Object message\)](../../../../app-store/dev_portal/API_reference/HermesEventPublisherOOB/concept/HermesEventPublishOOBScopedAPI.md#) method with your custom logic to return the partition key to use when publishing a message to the Hermes Messaging Service.

    The following list includes some possible types of partition keys to return and their associated benefits:

    -   An auto-generated unique ID. This type of partition key ensures that messages are evenly published across topic partitions. This is the default implementation.
    -   A unique key based on the message event type \(or any other message attribute\). This type of partition key ensures sequencing of messages of that event type \(or other message attribute\).
    -   The same partition key, which causes messages to be sent on the same partition. This type of partition key ensures strict sequencing of messages at the Kafka consumer group level.
    The following example shows how to return a random ID for each partition key.

    ```
    fetchPartionKey: function(message) { 
    // Implement it for custom partition key 
    // Random message keys ensure better distribution of message across partitions. 
    // Same message keys ensure that message always goes to the same partition.   
    // This ensures strict sequencing of messages at the Kafka consumer group level. 
    return gs.generateGUID(); 
    },
    ```

    The following example shows how to return a partition key based on the event type in the message.

    ```
    // Implementation where the partition key is decided based on the event type.
    fetchPartionKey: function(message) { 
    
    var eventType = message.eventType;
    var partionKey = fetchPartionKeyForMessage(eventType);
    return partionKey;
    },
    ```

4.  Override the default functionality in the [HermesEventPublisherOOB - fetchMessageHeaders\(Object message\)](../../../../app-store/dev_portal/API_reference/HermesEventPublisherOOB/concept/HermesEventPublishOOBScopedAPI.md#) method with your custom logic to fetch the header for a specified message before publishing the message through the Hermes Messaging Service.

    Refer to the [Apache Kafka](https://kafka.apache.org/) documentation for more information on these headers.

    The following example shows how to return headers based on the event type in the message.

    ```
    fetchMessageHeaders: function(message) { 
    // Returned headers are based on the event type passed in the message object. 
      var eventType = message.eventType;
      var headerObject = fetchHeadersBasedOnEventType(eventType);
      return headerObject;
    },
    ```


