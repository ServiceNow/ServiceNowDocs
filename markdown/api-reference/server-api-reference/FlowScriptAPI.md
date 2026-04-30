---
title: FlowScriptAPI - Scoped
description: The FlowScriptAPI API provides a method to return the context ID of the running flow.Returns the context ID of the running flow.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# FlowScriptAPI- Scoped

The FlowScriptAPI API provides a method to return the context ID of the running flow.

You cannot instantiate objects of this type. Objects of this type are created automatically and are accessible only in script steps and inline scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## FlowScriptAPI - getContextID\(\)

Returns the context ID of the running flow.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the running flow.|

This example assumes you have created a flow containing a **Log** action. This inline script generates the content of the Log message.

```
var contextId = FlowScriptAPI.getContextID();
return contextId;
```

Output:

```
4ecead85c4da0010598d0c7c6bf73554
```

