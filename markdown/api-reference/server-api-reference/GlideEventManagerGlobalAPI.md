---
title: GlideEventManager - Global
description: The GlideEventManager API provides methods to process events.Instantiates a GlideEventManager object.Processes the eligible events in a queue.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideEventManager- Global

The GlideEventManager API provides methods to process events.

For information on creating an event queue, see [Creating custom queues to process events](../../../../../script/useful-scripts/concept/useful-server-side-scripts.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideEventManager - GlideEventManager\(String queueName\)

Instantiates a GlideEventManager object.

|Name|Type|Description|
|----|----|-----------|
|queueName|String|Name of a queue for an event listed in the Event Registry \[sysevent\_register\] table. If no queue is provided, GlideEventManager processes against the default queue.|

The following example shows how to instantiate a GlideEventManager object.

```
var eventMgr = new GlideEventManager('my_queue');
```

## GlideEventManager - process\(Number limit\)

Processes the eligible events in a queue.

You can use the **limit** parameter to identify a range of process\_on times for events in the queue and it isn’t a hard limit. For example, if the limit is 10, the system looks for the 10 oldest pending process\_on times. If multiple events have the same process\_on time, more than 10 events might be claimed \(that is, ready to process\).

|Name|Type|Description|
|----|----|-----------|
|limit|Number|Optional. Limits the number of events claimed. If this value isn’t passed, no limit is applied.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to limit the number of events processed to roughly 200.

```
GlideEventManager('my_event_queue').process(200);
```

