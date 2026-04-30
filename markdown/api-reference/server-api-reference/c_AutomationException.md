---
title: AutomationException - Global
description: The AutomationException script include provides generic exception wrapping for automation.Retrieves the error message.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AutomationException- Global

The AutomationException script include provides generic exception wrapping for automation.

Include this in automation code to implement error handling.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AutomationException - getMessage\(\)

Retrieves the error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The error message|

```
var ae = new AutomationException("This is an error message");
gs.print(ae.getMessage());
```

Output:

```
This is an error message
```

