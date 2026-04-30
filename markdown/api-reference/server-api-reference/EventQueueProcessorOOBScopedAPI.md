---
title: EventQueueProcessorOOB - Scoped
description: The EventQueueProcessorOOB script include provides methods to manage event requests on the inbound event queue \(located in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table\).Adds attributes to the passed event snapshot.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# EventQueueProcessorOOB- Scoped

The EventQueueProcessorOOB script include provides methods to manage event requests on the inbound event queue \(located in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table\).

If you want to change the default functionality of this script include, you need to override these methods in the `EventQueueProcessor` script include. You must have the admin role to modify this script include.

This script include runs in the `sn_api_notif_mgmt` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## EventQueueProcessorOOB - transformEventObject\(Object eventSnapshot, Object eventJson, String queueType\)

Adds attributes to the passed event snapshot.

This method is not implemented in the base instance. If you need to add attributes to the event snapshot before processing the event and sending it out on the proper message-bus, you should override this method in the `EventQueueProcessor` script include.

<table id="table_dlh_xrb_vzb" class="parameters"><thead><tr><th>

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

Raw event data in which to add attributes.This object is from the payload field of the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. Inbound queue records are created by business rules, such as Trouble Ticket Attribute Change Event, that are associated with the Incident \[incident\] table.

The format of the event snapshot is defined by the business rule that originally pushed the event into the inbound queue.

</td></tr><tr><td>

eventJson

</td><td>

Object

</td><td>

JSON formatted glide record that caused the event to be triggered. This is the object that was stored in the Inbound Queue table. The format of this object is dependent on the table from which it was generated, such as incident or case.

</td></tr><tr><td>

queueType

</td><td>

String

</td><td>

Queue in which the event was pushed. For the default implementation, this is always `sn_tmt_core_inbound_queue`. If you modify the event queuing implementation in your instance, pass the name of the queue that contains the event record.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
pushEventsToEventQueue: function(eventSnapshot, queueType) {
  if (queueType == Constants.QUEUE_TYPE.INBOUND_QUEUE) {
    var inboundQueueEventJson = this.generateInboundQueueObj(eventSnapshot);
    this.transformEventObject(eventSnapshot, inboundQueueEventJson, queueType);
    // Passing isSecure as false
    new sn_tmt_core.InboundQueue(null, false).createInboundQueueRecord(inboundQueueEventJson);
  }
},
```

