---
title: Queue - Global
description: The Queue API \(Advanced Work Assignment\) provides methods to route a document to a queue.Gets a queue record by sys\_id.Routes an active work item to the queue object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Queue- Global

The Queue API \(Advanced Work Assignment\) provides methods to route a document to a queue.

This API is provided within the `sn_awa` namespace.

Requires the following:

-   Advanced Work Assignment plugin \(com.glide.awa\)
-   Role: awa\_integration\_user or admin

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Queue - get\(String queue\_id\)

Gets a queue record by sys\_id.

|Name|Type|Description|
|----|----|-----------|
|queue\_id|String|Represents sys\_id of queue record from awa\_queue table|

|Type|Description|
|----|-----------|
|Boolean|True if queue record exists, false otherwise.|

```
var queue = sn_awa.Queue.get("<queue_id>");
var workItem = queue.route({ 
    document_sys_id: "<sys_id>",
    document_table: "<table>"
});
```

## Queue – route\(Object options\)

Routes an active work item to the queue object.

If an active work item does not exist for the specified document, this method creates a work item and set its fields accordingly.

<table id="table_hqw_pbm_yfb" class="parameters"><thead><tr><th>

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

Contains document sys\_id and table associated with work item:-   `document_sys_id: "<sys_id>"`
-   `document_table: "<table>"`, e.g., interaction

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|True if successful, error message otherwise.|

```
var queue = sn_awa.Queue.get("<queue_id>");
var workItem = queue.route({ 
    document_sys_id: "<sys_id>",
    document_table: "<table>"
});
```

