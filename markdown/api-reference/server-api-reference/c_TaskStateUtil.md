---
title: TaskStateUtil - Global
description: The TaskStateUtil script include provides methods for working with task-type table state attributes.Creates a TaskStateUtil object.The name of the attribute that identifies default work state.The name of the attribute that identifies the default close state.The name of the attribute that identifies inactive states.The value of the default close state is Closed Complete on the Task table.The value of the default work state is Work in progress on the Task table.The values of the default inactive states: Closed Complete, Closed Incomplete, Closed Skipped on the Task table.Returns the value for the default closed state.Returns the value for the default work state.Returns a list of the inactive state values.Returns the active status of the specified state.Decides whether the mark closed business rule should be run or not.Decides whether the task closer business rule should be run or not.Decides whether the task reopener business rule should be run or not.Enables the user to specify their own default work state.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TaskStateUtil- Global

The TaskStateUtil script include provides methods for working with task-type table state attributes.

This script include is primarily used by the Task Active State Management business rule to set the active field based on state changes. Configurations are defined in the task.state dictionary element, usually using dictionary overrides since state values vary by table.

You can call the TaskStateUtil script include in any server script to determine inactive states, default work, or default close states for a table.

The required attributes are defined on the planned\_task table so all planned task types are supported. We will eventually add the attributes to other task types and eventually the base task table. You are free to do this if you want to leverage this feature now.

These attributes can be defined on the task.state dictionary element or a dictionary override for extended task tables.

<table id="table_hv2_51h_1s"><thead><tr><th>

Attribute

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

close\_states

</td><td>

Semicolon delimited list of state values that are inactive, used to identify whether the task should be set to active or inactive.

</td></tr><tr><td>

default\_close\_state

</td><td>

Optional. Attribute to define the state value of the default close state if you want to define business rules that automatically close a task. Default: 3, typically Closed Complete if attribute is not defined.

</td></tr><tr><td>

default\_work\_state

</td><td>

Optional. Attribute to define the state value of the default working state if you want to define business rules that automatically set a task for working. Default: 2, typically Work in Progress if the attribute is not defined.

</td></tr></tbody>
</table>**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TaskStateUtil - TaskStateUtil\(GlideRecord task\)

Creates a TaskStateUtil object.

|Name|Type|Description|
|----|----|-----------|
|task|GlideRecord|This must be a GlideRecord from a task table.|

```
var stateUtil = new TaskStateUtil(current);
```

## TaskStateUtil - ATTR\_DEFAULT\_WORK

The name of the attribute that identifies default work state.

|Name|Type|Description|
|----|----|-----------|
|ATTR\_DEFAULT\_WORK|String|Identifies default work state. Value: default\_work\_state|

## TaskStateUtil - ATTR\_DEFAULT\_CLOSE

The name of the attribute that identifies the default close state.

|Name|Type|Description|
|----|----|-----------|
|ATTR\_DEFAULT\_CLOSE|String|Identifies the default close state. Value: default\_close\_state|

## TaskStateUtil - ATTR\_INACTIVE\_STATES

The name of the attribute that identifies inactive states.

|Name|Type|Description|
|----|----|-----------|
|ATTR\_INACTIVE\_STATES|String|Identifies inactive states. Value: close\_states|

## TaskStateUtil - SYSTEM\_DEFAULT\_CLOSE

The value of the default close state is Closed Complete on the Task table.

|Name|Type|Description|
|----|----|-----------|
|SYSTEM\_DEFAULT\_CLOSE|Integer|Value of the default close state is Closed Complete on the Task table. Value: 3|

## TaskStateUtil - SYSTEM\_DEFAULT\_WORK

The value of the default work state is Work in progress on the Task table.

|Name|Type|Description|
|----|----|-----------|
|SYSTEM\_DEFAULT\_WORK|Integer|Value of the default work state is Work in progress on the Task table. Value: 2|

## TaskStateUtil - SYSTEM\_INACTIVE\_STATES

The values of the default inactive states: Closed Complete, Closed Incomplete, Closed Skipped on the Task table.

|Name|Type|Description|
|----|----|-----------|
|SYSTEM\_INACTIVE\_STATES|Integer array|Values of the default inactive states: Closed Complete, Closed Incomplete, Closed Skipped on the Task table. Value: 3, 4, 7|

## TaskStateUtil - getDefaultCloseState

Returns the value for the default closed state.

The default closed state value is 3 if the default\_close\_state attribute has not been specified.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|State value representing the closed state.|

```
var stateUtil = new TaskStateUtil(current);
//get the close state
var defaultCloseState =  stateUtil.getDefaultCloseState();
current.state = defaultCloseState;
```

## TaskStateUtil - getDefaultWorkState\(\)

Returns the value for the default work state.

The default work state value is 2 if the default\_work\_state attribute has not been specified.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The state value representing the working state.|

```
var stateUtil = new TaskStateUtil(current);
//get the work state
var defaultWorkState =  stateUtil.getDefaultWorkState();
current.state = defaultWorkState;
```

## TaskStateUtil - getInactiveStates

Returns a list of the inactive state values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of state values that are inactive.|

```
var stateUtil = new TaskStateUtil(current);
//get the inactive state values
var inactiveStates = stateUtil.getInactiveStates();
```

## TaskStateUtil - isStateInactive\(String state\)

Returns the active status of the specified state.

|Name|Type|Description|
|----|----|-----------|
|state|String|The state value to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the state is inactive.|

```
var stateUtil = new TaskStateUtil(current);
var previousStateInactive = stateUtil.isStateInactive(previous.state);
var currentStateInactive = stateUtil.isStateInactive(current.state);
```

## TaskStateUtil - runMarkClosed

Decides whether the **mark closed** business rule should be run or not.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Whether the business rule should be allowed to run or not.|

## TaskStateUtil - runTaskCloser

Decides whether the **task closer** business rule should be run or not.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Determines whether the business rule should be allowed to run or not.|

## TaskStateUtil - runTaskReopener

Decides whether the **task reopener** business rule should be run or not.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Whether the business rule should be allowed to run or not.|

## TaskStateUtil - setDefaultWorkState\(String defaultWorkState\)

Enables the user to specify their own default work state.

|Name|Type|Description|
|----|----|-----------|
|defaultWorkState|String|The value to use for the default work state.|

|Type|Description|
|----|-----------|
|TaskStateUtil|A self-reference to allow for method chaining.|

