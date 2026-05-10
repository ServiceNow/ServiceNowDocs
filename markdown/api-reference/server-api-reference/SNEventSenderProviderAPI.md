---
title: SNEventSenderProvider - Global
description: The SNEventSenderProvider API provides a method to instantiate an IEventSender instance.Returns an IEventSender object to use to send events from a MID Server to a ServiceNow instance.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SNEventSenderProvider- Global

The SNEventSenderProvider API provides a method to instantiate an IEventSender instance.

Use this API when writing scripts that will run on MID Servers to instantiate the object to send an event to your ServiceNow instance.

Use the [IEventSender](../../IEventSender/concept/IEventSenderAPI.md#) API to send the event to the ServiceNow instance. Use the [Event](../../Event/concept/EventAPI.md#) API to add/update fields within an event.

You must activate the Event Management \(com.glideapp.itom.snac\) plugin before attempting to access this API. The Event Management plugin requires a separate subscription and must be activated. This plugin includes demo data and activates related plugins if they are not already active.

For additional information on event management, see [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EM.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## EventSender - getEventSender\(\)

Returns an IEventSender object to use to send events from a MID Server to a ServiceNow instance.

You must call this method before calling any IEventSender API methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|IEventSender|IEventSender object to use to send an event to a ServiceNow instance.|

```
var eventSender = SNEventSenderProvider.getEventSender();
```

