---
title: IEventSender - Global
description: The IEventSender API provides methods to send events from a MID Server to a ServiceNow instance and to query the status of the event queue.Returns the size of the event queue.Checks if the event queue has exceeded its maximum size.Places the specified event in the event queue.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IEventSender- Global

The IEventSender API provides methods to send events from a MID Server to a ServiceNow instance and to query the status of the event queue.

Before calling any methods within this class, you must call the SNEventSenderProvider.getEventSender\(\) method to instantiate an IEvent object.

Use the Event API to add/update fields within an event. Use the SNEventSenderProvider API to instantiate an event sender object. Then use the IEventSender API to send the event to a ServiceNow instance.

You must activate the Event Management \(com.glideapp.itom.snac\) plugin before attempting to access this API. The Event Management plugin requires a separate subscription and must be activated. This plugin includes demo data and activates related plugins if they are not already active.

For additional information on event management, see [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EM.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IEventSender - getQueueSize\(\)

Returns the size of the event queue.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_arg_4gn_kkb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Size of the event queue.If an event queue is not currently implemented, returns "0".

</td></tr></tbody>
</table>```
var event = new Event();
event.setField("source","SAP Solman");
event.setField("severity","3");
event.setField("time_of_event", "2019-18-05 13:12:05");
event.setField("type", "SAP object");
event.setField("user", "admin"); // parameter added to additional info section

var eventSender = SNEventSenderProvider.getEventSender();
var sendStatus = eventSender.sendEvent(event); //send event     
var queueSize = eventSender.getQueueSize() // check the size of the event queue
```

## IEventSender - isFullQueue\(\)

Checks if the event queue has exceeded its maximum size.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ihk_2jn_kkb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the event queue has exceeded its maximum size. When this happens, no additional event messages can be queued until the queue decreases in size.Valid values:

-   true: Event queue is full.
-   false: Event queue is not full and can add more event entries.

</td></tr></tbody>
</table>```
var eventSender = SNEventSenderProvider.getEventSender();
if (!eventSender.isFullQueue()) // If queue is not full, send event
  eventSender.sendEvent(event);     

```

## IEventSender - sendEvent\(Object event\)

Places the specified event in the event queue.

|Name|Type|Description|
|----|----|-----------|
|event|IEventSender|Event object to place in the events queue.|

<table id="table_skl_ppm_kkb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the event was successfully queuedValid values:

-   true: Event was queued
-   false: Error

</td></tr></tbody>
</table>```
var eventSender = SNEventSenderProvider.getEventSender();
eventSender.sendEvent(event); //send event     

```

