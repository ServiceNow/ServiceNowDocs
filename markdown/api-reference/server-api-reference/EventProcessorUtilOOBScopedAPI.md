---
title: EventProcessorUtilOOB - Scoped
description: The EventProcessorUtilOOB script include provides methods to construct and publish events on the configured message broker.Constructs a TMF688 compliant payload based on the passed information and publishes the event to the configured publishing platform.Converts the passed raw event object into a TMF-compliant event object by invoking a payload generator based on the event type.Instantiates the HermesEventPublisher class and publishes the passed event payload to the Hermes Kafka message broker.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# EventProcessorUtilOOB- Scoped

The EventProcessorUtilOOB script include provides methods to construct and publish events on the configured message broker.

If you want to change the default functionality of this script include, you need to override these methods in the `EventProcessorUtil` script include. You must have the admin role to modify this script include.

This script include runs in the `sn_api_notif_mgmt` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## EventProcessorUtilOOB - constructandPublishEvent\(Object inboundEventPayloadRecord, String eventId\)

Constructs a TMF688 compliant payload based on the passed information and publishes the event to the configured publishing platform.

The default publishing platform is defined in the sn\_api\_notif\_mgmt.publisher\_message\_bus\_config system property.

**Note:** This method is a core utility method of queue management. You should not need to override this method unless you plan on redesigning the underlying notification framework.

|Name|Type|Description|
|----|----|-----------|
|inboundEventPayloadRecord|Object|Information associated with the event. The format of this payload is dependent on the event type. In the base implementation, this is the glide record data of the associated event in JSON format.|
|eventId|String|Unique ID of the event to publish such as a GUID.|

|Type|Description|
|----|-----------|
|tmfEventPayload|TMF688-compliant event payload created for the event. For a description of the default format of this event payload, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method.

```
processIndividualEventRecord: function(inboundQueueGr, node_id) {
  var isError = false;
  var errorMessage;
  try {
    new EventProcessorUtil().constructandPublishEvent(JSON.parse(inboundQueueGr.getValue('payload')), inboundQueueGr.getValue('record_id'));
  } catch (ex) {
    this._logger.logErr("Event processing failed " + ex);
    isError = true;
    errorMessage = JSON.stringify(ex);
  }

  // Update the inbound queue record based on processing
  var inboundQueueObj = new sn_tmt_core.BaseObject();
  if (isError == true) {
    inboundQueueObj.setValue('state', sn_tmt_core.Constants.INBOUND_QUEUE_STATE.ERROR);
    inboundQueueObj.setValue('error_message', errorMessage);
  } else {
    inboundQueueObj.setValue('state', sn_tmt_core.Constants.INBOUND_QUEUE_STATE.COMPLETED);
  }
    var inboundQueue = new sn_tmt_core.InboundQueue(inboundQueueGr, false);
    inboundQueue.updateInboundQueueRecord(inboundQueueObj);
},
```

## EventProcessorUtilOOB - fetchEventHandlerAndCreateTMFEvent\(Object eventSnapshot, String eventType, String eventId\)

Converts the passed raw event object into a TMF-compliant event object by invoking a payload generator based on the event type.

You will need to override this method if your implementation does any of the following:

-   Modifies the existing event handling.
-   Adds a new event type. You must add the event type and its associated payload generator.
-   Adds a new object in the Producer Event Notification Framework.

You may also need to override the methods within the `TroubleTicketNotificationUtil` script include to add attributes to the returned TMF-compliant payload or modify the default handling of the payload.

For additional information, see [Configure trouble ticket notifications using the Producer Event Notification Framework](../../../../../integrate/guides/ProducerEventNotifFramework/concept/prd_evt_not-dev_gd-cfg_trbl_tkt_not.md).

<table id="table_bq5_4nz_5zb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventSnapshot

</td><td>

Object

</td><td>

Raw data to transform into a TMF-compliant object.You can obtain this object from the payload field of the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. Inbound queue records are created by business rules, such as Trouble Ticket Attribute Change Event, which is associated with the Incident \[incident\] table.

The format of the event snapshot is defined by the business rule that originally pushed the event into the inbound queue.

</td></tr><tr><td>

eventType

</td><td>

String

</td><td>

Event type. This value specifies the type of event data that is passed in the **eventSnapshot** payload. The passed payload is processed based on this event type. The event type is stamped on the inbound queue record by the associated business rule on the associated table. Each event type has its own event payload structure. For example:```
{
  "eventId":"dc2003c2c3bb3550054e20bdc0013136",
  "@type":"Troubleticket",
  "eventType":"TroubleTicketCreateEvent",
  "event":{
    "troubleTicket":{
      "short_description":"Test payload",
      "severity":3,
      "ticketType":"incident"
    }
  }
}
```

Default values for trouble ticket event types are defined in the **EVENT\_TYPES** parameter in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

eventId

</td><td>

String

</td><td>

Unique identifier of the event to convert.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|tmfEventPayload|Event payload in TMF-compliant format. To see the transformation process of the passed **eventSnapshot** object to the TMF-compliant payload, review the code in the `TroubleTicketNotificationUtilOOB` script include.|

The following code example shows how to call this method.

```
constructandPublishEvent: function(inboundEventPayloadRecord, eventId) {
  if (gs.nil(inboundEventPayloadRecord)) return;
  var tmfEventPayload = this.fetchEventHandlerAndCreateTMFEvent(inboundEventPayloadRecord.eventSnapshot, inboundEventPayloadRecord.eventType, eventId);

  this._logger.debug("Event payload generated for the event id " + eventId + " is " + JSON.stringify(tmfEventPayload));

  if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.OPEN_MESSAGE_BUS) {
    // Publish event in custom message bus
      this.publishEventToOpenMessageBus(tmfEventPayload);

  } else if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.HERMES) {
    // Publish event in hermes kafka
    try {
      this.publishMessageToHermesKafka(tmfEventPayload);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  } else if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.BOTH_MESSAGE_BUS_CONFIGURATIONS) {
    // Publish event in both custom message bus and hermes kafka
    this.publishEventToOpenMessageBus(tmfEventPayload);
    try {
      this.publishMessageToHermesKafka(tmfEventPayload);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  }
  return tmfEventPayload;
},
```

The following code example shows the switch case statements used by this method to determine how to transform the passed event payload based on the **eventType** parameter. If you add other event types to your implementation, you must override this method and include the processing for the new event type.

```
fetchEventHandlerAndCreateTMFEvent: function(eventSnapshot, eventType, eventId) {
var eventPayload;
switch (eventType) {
  case Constants.EVENT_TYPES.TROUBLE_TICKET_STATUS_CHANGE:
    eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateTroubleTicketStatusChangePayload(eventSnapshot, eventType, eventId);
    break;

  // New event type in trouble ticket
  case ‘troubleTicketPriorityChange’
    eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateTroubleTicketAttributeChangePayload(eventSnapshot, eventType, eventId);
    break;

  // New event type of object other than trouble ticket
  case ‘domainOrderStatusChange’
    eventPayload = new sn_ind_tmt_orm().domainOrderNotification().generatedomainOrderStatusChangePayoad(eventSnapshot, eventType, eventId);
    break;

  default:
    this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
    eventPayload = null;
  }
return eventPayload;
},
```

## EventProcessorUtilOOB - publishMessageToHermesKafka\(Object tmfEventPayload\)

Instantiates the HermesEventPublisher class and publishes the passed event payload to the Hermes Kafka message broker.

|Name|Type|Description|
|----|----|-----------|
|tmfEventPayload|Object|TMF688-compliant event payload created for the event. For a description of the default format of this event payload, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
constructandPublishEvent: function(inboundEventPayloadRecord, eventId) {
  if (gs.nil(inboundEventPayloadRecord)) return;
  var tmfEventPayload = this.fetchEventHandlerAndCreateTMFEvent(inboundEventPayloadRecord.eventSnapshot, inboundEventPayloadRecord.eventType, eventId);

  this._logger.debug("Event payload generated for the event id " + eventId + " is " + JSON.stringify(tmfEventPayload));

  if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.OPEN_MESSAGE_BUS) {
    // Publish event in open message bus
    this.publishEventToOpenMessageBus(tmfEventPayload);

  } else if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.HERMES) {
    // Publish event in Hermes Kafka
    try {
      this.publishMessageToHermesKafka(tmfEventPayload);
    } catch (ex) {
        this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  } else if (gs.getProperty(Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION) == Constants.EVENT_PUBLISH_MESSAGE_BUS_CONFIGURATION_VALUES.BOTH_MESSAGE_BUS_CONFIGURATIONS) {
    // Publish event in both custom message bus and Hermes Kafka
    this.publishEventToOpenMessageBus(tmfEventPayload);
    try {
      this.publishMessageToHermesKafka(tmfEventPayload);
    } catch (ex) {
      this._logger.logErr("Publishing message to Hermes Kafka Failed, error is: " + ex);
    }
  }
  return tmfEventPayload;
},
```

