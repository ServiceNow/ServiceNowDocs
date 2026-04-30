---
title: Workflow - Scoped
description: The scoped Workflow API provides methods that can be used in an activity definition script.Adds a debug message to the log.Adds an error message to the log.Returns the specified variable's value.Adds an informational message to the log.Object that contains the workflow variables.Returns the workflow name.Removes the specified variable from the workflow.Element of the workflow object that contains the workflow results.Returns the workflow's scratchpad object.Sets the workflow's result.Sets the specified variable to the specified value.Adds a warning message to the log.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Workflow- Scoped

The scoped Workflow API provides methods that can be used in an activity definition script.

There are no constructors for creating an instance of a scoped workflow object. Instead, use the global workflow object available in activity scripts. This workflow object is available in any script location inside a workflow.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped Workflow - debug\(String message, Object args\)

Adds a debug message to the log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to add to the log.|
|args|Object|Arguments to add to the message.|

|Type|Description|
|----|-----------|
|String|The message added to the log.|

```
var loggedMessage = workflow.debug("All is well");
```

## Scoped Workflow - error\(String message, Object args\)

Adds an error message to the log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to add to the log.|
|args|Object|Arguments to add to the message.|

|Type|Description|
|----|-----------|
|String|The logged message|

```
var loggedMessage = workflow.error("An error has occurred. ");
```

## Scoped Workflow - getVariable\(String name\)

Returns the specified variable's value.

|Name|Type|Description|
|----|----|-----------|
|name|String|The variable name|

|Type|Description|
|----|-----------|
|Object|The variable's value|

```
var value = workflow.getVariable("task");
```

## Scoped Workflow - info\(String message, Object args\)

Adds an informational message to the log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to add to the log.|
|args|Object|Arguments to add to the message.|

|Type|Description|
|----|-----------|
|String|The message that is logged.|

```
var loggedMessage = workflow.info("All is well");
```

## Scoped Workflow - inputs

Object that contains the workflow variables.

This is not a method, but rather a way to reference the variables in a workflow object, such as the user. Workflow variables are defined in the properties of the workflow or by scripted activities.

|Name|Type|Description|
|----|----|-----------|
|inputs|Object|Workflow variables as name value pairs. The variables of a workflow object are custom to an integrator's implementation.|

```
var user = workflow.inputs.u_user;
```

## Scoped Workflow - name\(\)

Returns the workflow name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The workflow name|

```
var name = workflow.name();
```

## Scoped Workflow - removeVariable\(String name\)

Removes the specified variable from the workflow.

|Name|Type|Description|
|----|----|-----------|
|name|String|The variable name|

|Type|Description|
|----|-----------|
|void| |

```
var value = workflow.removeVariable("task");
```

## Scoped Workflow - result

Element of the workflow object that contains the workflow results.

This is not a method, but rather the element in the workflow object that contains the results of a workflow.

|Name|Type|Description|
|----|----|-----------|
|result|String|Workflow results.|

```
var wfResult = workflow.result;
```

## Scoped Workflow - scratchpad\(\)

Returns the workflow's scratchpad object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The scratchpad object.|

```
var scratchpad = workflow.scratchpad();
```

## Scoped Workflow - setResult\(String result\)

Sets the workflow's result.

|Name|Type|Description|
|----|----|-----------|
|result|String|The workflow's result|

|Type|Description|
|----|-----------|
|void| |

```
workflow.setResult("Success");
```

## Scoped Workflow - setVariable\(String name, Object value\)

Sets the specified variable to the specified value.

|Name|Type|Description|
|----|----|-----------|
|name|String|The variable name|
|value|Object|The value to be assigned to the variable.|

|Type|Description|
|----|-----------|
|void| |

```
workflow.setVariable("task", "terrible");
```

## Scoped Workflow - warn\(String message, Object args\)

Adds a warning message to the log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to add to the log.|
|args|Object|Arguments to add to the message.|

|Type|Description|
|----|-----------|
|String|The logged message|

```
var loggedMessage = workflow.warn("Check your permissions.");
```

