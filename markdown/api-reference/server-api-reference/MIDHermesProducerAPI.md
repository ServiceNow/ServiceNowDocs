---
title: MIDHermesProducer - Global
description: The MIDHermesProducer API provides a method to send data from the MID Server to a Hermes topic.Creates a MIDHermesProducer for sending messages to Hermes topics.Sends a message from the MID Server to the specified Hermes topic.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDHermesProducer- Global

The MIDHermesProducer API provides a method to send data from the MID Server to a Hermes topic.

Sending data via the Hermes Messaging Service rather than using the MID Server ECC Queue can be a more efficient way to get data to a ServiceNow instance.

This API requires the ServiceNow MID Hermes API \(com.glide.mid.hermes\_api\) plugin. The calling user must have the kafka\_admin role. Before calling this API, follow the steps to Configure the MID Hermes API Extension.

Use this API in scripts that run on the MID Server, such as MID Server background scripts or in Workflow Studio action script steps with the **Required Runtime** set to **MID**.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDHermesProducer - MIDHermesProducer\(\)

Creates a MIDHermesProducer for sending messages to Hermes topics.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates a MIDHermesProducer.

```
var producer = new MIDHermesProducer();
```

## MIDHermesProducer - send\(Object options\)

Sends a message from the MID Server to the specified Hermes topic.

The 4000-4050 port range must be open to send messages to a Hermes topic. For more information, see Producing and consuming messages from a Kafka client.

<table id="table_n1j_g1c_23c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

Contains configuration parameters for the message.```
{
   applicationId: "String",
   callbackFunction: function(),
   headers: {Object},
   key: "String",
   message: "String",
   topic: "String"
}
```

</td></tr><tr><td>

options.applicationId

</td><td>

String

</td><td>

Optional. Application identifier for topic routing. When provided, messages are routed to `snc.{instance}.{applicationId}.{topic}`, otherwise they are routed to `snc.{instance}.{topic}`.

</td></tr><tr><td>

options.onErrorCallback

</td><td>

Function

</td><td>

Optional. JavaScript function to execute if message delivery fails. The function accepts two parameters: String `errorMessage` and String `errorType` \(the fully qualified Java exception class name\).```
function(errorMessage, errorType) { 
   //implement error handling here
};
```

</td></tr><tr><td>

options.headers

</td><td>

Object

</td><td>

Optional. Key-value pairs for message headers. Any headers supported by Apache Kafka are valid.

</td></tr><tr><td>

options.key

</td><td>

String

</td><td>

Optional. Message key for partitioning in Apache Kafka. Messages with the same key are sent to the same partition, ensuring ordering.

</td></tr><tr><td>

options.message

</td><td>

String

</td><td>

Content of the message to send to the topic. Any value formatted as a string is valid.

</td></tr><tr><td>

options.topic

</td><td>

String

</td><td>

Name of the Hermes topic to send the message to.**Note:** Don't include the instance prefix; it is added automatically.

</td></tr></tbody>
</table><table id="table_o1j_g1c_23c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

This method does not return a value. Message delivery is asynchronous. Success: Messages are delivered asynchronously to Hermes Kafka brokers. Check MID Server logs for delivery confirmation.

Failure: If message delivery fails, the optional callback function \(if provided\) is invoked with error details. Common errors include:

-   `org.apache.kafka.common.errors.TimeoutException`: Kafka broker unreachable or network issues. Check firewall rules for Hermes bootstrap address and ports.
-   `com.service_now.mid.hermes_api.exception.MIDHermesAPIExtensionNotStartedException`: Extension not started. Verify MID Hermes API extension context is active.
-   `java.lang.IllegalArgumentException`: Invalid parameters. Ensure topic and message are provided.

Additional steps to resolve errors:

-   Verify MID Hermes API extension is running in MID Server UI.
-   Check network connectivity to Hermes.
-   Review MID Server logs with property **mid.hermes.debug=true** for detailed diagnostics.
-   Confirm IPKI certificate is valid in MID Server keystore.

</td></tr></tbody>
</table>This example sends a message to a Hermes topic.

```
// Create producer instance 
var producer = new MIDHermesProducer(); 

// Define error callback function 
var errorCallback = function(errorMessage, errorType) {
    gs.error("Message delivery failed: " + errorType + " - " + errorMessage);
}; 

// Send message with all optional parameters 
producer.send({ 
    topic: "order-events", 
    applicationId: "sn_streamconnect", 
    message: JSON.stringify({ 
        orderId: "ORD-12345", 
        status: "completed", 
        timestamp: new Date().getTime() 
    }), 
    key: "customer-456", 
    headers: { 
        "content-type": "application/json", 
        "source": "mid-server", 
        "version": "1.0" 
    }, 
    onErrorCallback: errorCallback 
});
```

The message is sent asynchronously. Check MID Server logs for delivery confirmation.

