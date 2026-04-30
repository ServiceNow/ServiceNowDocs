---
title: GSLog - Scoped, Global
description: GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values.Instantiates a GSLog object.Determines if debug is turned on.Returns the log level.Called by the Prototype JavaScript Framework during object creation to initialize a new instance of this class. Provide the input parameters, but do not call this method directly.Logs a message at the specified level.Logs alert events.Logs critical events.Logs debug events.Logs emergency events.Logs error events.Logs information events.Logs notice events.Logs warning events.Sets the log level.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GSLog - Scoped, Global

GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values.

Logs generated using the GSLog API are logged in the System Logs. Specifically, you can find System Logs in the UI by navigating to **All** &gt; **System Logs** &gt; **System Log**. You can choose to view all logs or specific log types like Application Logs, Errors, Script Log Statements, and so on under this menu item. Filtering the Source column in the **All** logs view can help locate your entries faster.

Logs can be at the level of debug, info, notice, warning, err, or crit \(after BSD syslog.h and followers\). The default logging level is notice, so levels should be chosen accordingly.

Use for any server-side script where you want to implement event logging.

For more information, see [Debugging scripts](../../../../../script/debugging/concept/script-debug-overview.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GSLog – GSLog\(\)

Instantiates a GSLog object.

|Name|Type|Description|
|----|----|-----------|
|traceProperty|String|System property that contains a value indicating the level at or above which messages will be written to the log.|
|caller|String|Name of the script calling the logger.|

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA");
```

## GSLog – debugOn\(\)

Determines if debug is turned on.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kyg_zmx_15b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether debug is on or off.

 Valid values:

-   true: Debug is on.
-   false: Debug is off.

</td></tr></tbody>
</table>```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.setLevel("debug");
gs.print(gl.debugOn());
```

Output:

```
*** Script : true
```

## GSLog – getLevel\(String level\)

Returns the log level.

|Name|Type|Description|
|----|----|-----------|
|level|String|Optional. Log level.|

|Type|Description|
|----|-----------|
|String|Log level.|

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.setLevel("debug");
gs.print(gl.getLevel());
```

Output:

```
*** Script: debug
```

## GSLog – initialize\(String traceProperty, String caller\)

Called by the Prototype JavaScript Framework during object creation to initialize a new instance of this class. Provide the input parameters, but do not call this method directly.

|Name|Type|Description|
|----|----|-----------|
|traceProperty|String|System property that contains a value indicating the level at or above which messages will be written to the log.|
|caller|String|Name of the script calling the logger.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA");

```

## GSLog – log\(String level, String msg\)

Logs a message at the specified level.

|Name|Type|Description|
|----|----|-----------|
|level|String|Log level.|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.log("debug", "debug message");
```

## GSLog – logAlert\(String msg\)

Logs alert events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logAlert("This is an alert");
```

Output:

```
*** Script [TaskSLA]: This is an alert
```

## GSLog – logCrit\(String msg\)

Logs critical events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logCrit("This is a critical message");
```

Output:

```
*** Script [TaskSLA]: This is a critical message
```

## GSLog – logDebug\(String msg\)

Logs debug events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logDebug("This is a debug message");
```

Output:

```
*** Script [TaskSLA]: This is a debug message
```

## GSLog – logEmerg\(String msg\)

Logs emergency events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logEmerg("This is an emergency message");
```

Output:

```
*** Script  [TaskSLA ] : This is an emergency message
```

## GSLog – logErr\(String msg\)

Logs error events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logErr("This is an error message");
```

Output:

```
*** Script [TaskSLA]: This is an error message
```

## GSLog – logInfo\(String msg\)

Logs information events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logInfo("This is an info message");
```

## GSLog – logNotice\(String msg\)

Logs notice events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logNotice("This is a notice");
```

Output:

```
*** Script [TaskSLA]: This is a notice

```

## GSLog – logWarning\(String msg\)

Logs warning events.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Message to write to the log.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.logWarning("This is a warning message");
```

Output:

```
*** Script [TaskSLA]: This is a warning message
```

## GSLog – setLevel\(String level\)

Sets the log level.

|Name|Type|Description|
|----|----|-----------|
|level|String|Log level to set.|

|Type|Description|
|----|-----------|
|None| |

```
var gl = new GSLog("com.snc.sla.tasksla.log", "TaskSLA"); 
gl.setLevel("debug");
```

