---
title: Queue - Scoped
description: The Queue API provides methods that allow you to retrieve or join a Connect Support chat queue.Retrieves a specified chat queue.Adds the current user to an existing Connect Support chat queue and posts the specified question.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Queue- Scoped

The Queue API provides methods that allow you to retrieve or join a Connect Support chat queue.

To execute this class in a scoped application, use the `sn_connect` namespace identifier. The Connect Scriptable APIs plugin \(ID: com.glide.connect.scriptable\) must be enabled to access the Queue API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped Queue - get\(String sysID\)

Retrieves a specified chat queue.

|Name|Type|Description|
|----|----|-----------|
|SysID|String|Sys\_id of a queue from the Chat Queue \[chat\_queue\] table.|

|Type|Description|
|----|-----------|
|Object|Returns a conversation queue object.|

```
var queue = sn_connect.Queue.get("ab73be7dc09a4300964f336ee6b74361");
```

## Scoped Queue - join\(String question\)

Adds the current user to an existing Connect Support chat queue and posts the specified question.

Before calling this method, you must call the [Scoped Queue - get\(String sysID\)](QueueScopedAPI.md#) method to retrieve the chat queue to which to attach the current user.

|Name|Type|Description|
|----|----|-----------|
|Question|String|Question to add to the chat queue.|

|Type|Description|
|----|-----------|
|Object|Record \(GlideRecord object\) in the Chat Queue Entry \[chat\_queue\_entry\] table.|

```
var queue = sn_connect.Queue.get("ab73be7dc09a4300964f336ee6b74361");
queue.join("How do I access my email?");
```

