---
title: StateManagementScriptableApi - Global
description: The StateManagementScriptableApi provides a set of methods for manipulating configuration item \(CI\) operational states and applying CI actions.Add a CI action to a list of CIs.Extend the CI-action-lease time for the registered user. If the previous lease has expired, the new lease time starts now.Returns a list of active CI actions for the specified CI.Returns the operational state of the CI.Determines if the two specified actions are compatible.Determines if the lease has expired for the requestor of a specified CI Action.For a type of CI, determine if a CI action is not allowed for an operational state.For a type of CI, determine if an operational state transition is not allowed.Determines if the specified requestor is a valid active workflow user or a registered user.Registers an operator for a non-workflow user.Removes a CI action for a list of CIs.Set the operational state for list of CIs.Unregisters an operator for non-workflow users.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# StateManagementScriptableApi- Global

The StateManagementScriptableApi provides a set of methods for manipulating configuration item \(CI\) operational states and applying CI actions.

The StateManagementScriptableApi methods adhere to restrictions and allowances specified by not allowed CI actions, compatible CI actions, and not allowed operational transitions. If a method attempts to perform a restricted operation, the operation is blocked, an error is logged, and a task is created if appropriate.

The StateManagementScriptableApi methods are static methods. You access the methods using the `SNC.StateManagementScriptableApi` global object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## StateManagementScriptableApi - addBulkCIAction\(String requestorId, String sysIdList, String ciActionName, String ciActionListOld, String leaseTime\)

Add a CI action to a list of CIs.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|A sys\_id of a workflow context, or the GUID returned from the registerOperator\(\) method.|
|sysIdList|String|A list comma separated list of CI sys\_ids.|
|ciActionName|String|The CI action name.|
|ciActionListOld|String|\(Optional\) A comma separated list of old CI actions that all CIs should be in.|
|leaseTime|String|\(Optional\) Time duration for which the lease is valid for specified CI Action. In the format HH:MM:SS.|

<table id="table_h5l_w4s_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   result - true if the action is set for all CIs in the list; otherwise, false.
-   errors - list of errors.

</td></tr></tbody>
</table>## StateManagementScriptableApi - extendCIActionLease\( String requestorId, String ciSysId, String ciActionName, String leaseTime\)

Extend the CI-action-lease time for the registered user. If the previous lease has expired, the new lease time starts now.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|A sys\_id of a workflow context, or the GUID returned from the registerOperator\(\) method.|
|ciSysId|String|The CI's sys\_id.|
|ciActionName|String|The CI action name.|
|leaseTime|String|Time duration for which the lease is valid for specified CI Action. In the format HH:MM:SS.|

<table id="table_g24_j3s_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   result - true if the lease time has been set.
-   errors - list of errors.

</td></tr></tbody>
</table>## StateManagementScriptableApi - getCIActions\(String ciSysId\)

Returns a list of active CI actions for the specified CI.

|Name|Type|Description|
|----|----|-----------|
|ciSysId|String|Sys\_id of the CI.|

<table id="table_rl1_fws_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs. Possible values:

-   ciActions - Comma-separated list of active CI actions for the CI, or `no_active_action`.
-   errors - List of errors.

</td></tr></tbody>
</table>The following example shows how to get active actions for a list of configuration items.

```
// Store sys_ids of configuration items for which to get data
var CIArray = ["a9c0c8d2c6112276018f7705562f9cb0","0c43bc4fc61122750182c132411702f2","46bbf419a9fe1981009802288c1eb79d","46a4381ca9fe1981005c3e99af3cd164","0c43bcbdc61122750182c132e9b6565d"];

var output = '';

// looping above array to fetch each sys_id and passing to method
for(var i=0; i < CIArray.length; i++) {

  // passing sys_id of CI stored in array to method
  output = SNC.StateManagementScriptableApi.getCIActions(CIArray[i]);

  // print a JSON formatted string with name-value pairs
  gs.print(output);
}
```

Output:

```
{"ciActions":["no_active_action"],"result":true}
{"ciActions":["no_active_action"],"result":true}
{"ciActions":["no_active_action"],"result":true}
{"ciActions":["no_active_action"],"result":true}
{"ciActions":["no_active_action"],"result":true}
```

## StateManagementScriptableApi - getOperationalState\(String ciSysId\)

Returns the operational state of the CI.

|Name|Type|Description|
|----|----|-----------|
|ciSysId|String|Sys\_id of the CI.|

<table id="table_o5f_1ns_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs. Possible values:

-   ciActions - String choice values of the operational\_status field, or `UNKNOWN`.
-   errors - List of errors.

</td></tr></tbody>
</table>The following example shows how to get the operational states of a list of specified configuration items.

```
// Store sys_ids of configuration items for which to get the operational state.
var CIArray = ["0c43bc4fc61122750182c132411702f2","46bbf419a9fe1981009802288c1eb79d","46a4381ca9fe1981005c3e99af3cd164","0c43bcbdc61122750182c132e9b6565d","a9c0c8d2c6112276018f7705562f9cb0"];

var output = '';

// Loop the array to fetch each sys_id and pass to the method.
for(var i=0;i<CIArray.length;i++) {
  // Pass sys_id of CI stored in array to the method  
  output = SNC.StateManagementScriptableApi.getOperationalState(CIArray[i]); 

  // prints a JSON formatted string with name-value pairs
  gs.print(output);
}
```

Output:

```
*** Script: {"operationalState":"Operational","result":true}
*** Script: {"operationalState":"Operational","result":true}
*** Script: {"operationalState":"Operational","result":true}
*** Script: {"operationalState":"Operational","result":true}
ci_state_management                        : INVALID_SYS_ID: Invalid sys_id [a9c0c8d2c6112276018f7705562f9cb0]: no thrown error
*** Script: {"errors":[{"error":"INVALID_SYS_ID","message":"Invalid sys_id [a9c0c8d2c6112276018f7705562f9cb0]"}],"operationalState":"unknown","result":false}
```

## StateManagementScriptableApi - isCompatibleCIAction\(String actionName, String otherActionName\)

Determines if the two specified actions are compatible.

|Name|Type|Description|
|----|----|-----------|
|actionName|String|A CI action name|
|otherActionName|String|A CI action name|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the two specified CI actions are compatible.|

## StateManagementScriptableApi - isLeaseExpired\(String requestorId, String ciSysId, String ciActionName\)

Determines if the lease has expired for the requestor of a specified CI Action.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|A sys\_id of a workflow context, or the GUID returned from the registerOperator\(\) method.|
|ciSysId|String|The CI's sys\_id.|
|ciActionName|String|Name of the CI action.|

<table id="table_pt5_v5r_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   result - true if the user's lease has expired.
-   errors - list of errors.

</td></tr></tbody>
</table>## StateManagementScriptableApi - isNotAllowedAction\(String ciType, String opsLabel, String actionName\)

For a type of CI, determine if a CI action is not allowed for an operational state.

|Name|Type|Description|
|----|----|-----------|
|ciType|String|The CI type|
|opsLabel|String|The operational state|
|actionName|String|The CI action name|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the action is not allowed on the specified CI type in the specified operational state.|

## StateManagementScriptableApi - isNotAllowedOpsTransition\(String ciType, String opsLabel, String transitionOpsLabel\)

For a type of CI, determine if an operational state transition is not allowed.

|Name|Type|Description|
|----|----|-----------|
|ciType|String|The CI type|
|opsLabel|String|The label of the beginning operational state.|
|transitionOpsLabel|String|The label of the ending operational state.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if specified operational state transition is not allowed on the specified CI type.|

## StateManagementScriptableApi - isValidRequestor\(String requestorId\)

Determines if the specified requestor is a valid active workflow user or a registered user.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|Sys\_id of a workflow context or the GUID returned from the registerOperator\(\) method.|

<table id="table_er5_5sr_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

JSON formatted name-value pairs. Possible values:

-   result - `true` if the requestorId is valid.
-   errors - list of errors.

</td></tr></tbody>
</table>This example show how to use the isValidRequestor\(\) method to check if an operator is a registered user.

```
var output = SNC.StateManagementScriptableApi.registerOperator();
var jsonUtil = new JSON();
var result = jsonUtil.decode(output);
var requestorId = result.requestorId; // Fetching requestorId

output = SNC.StateManagementScriptableApi.isValidRequestor(requestorId);
gs.info(output);
```

Output:

```
{"result":true}
```

## StateManagementScriptableApi - registerOperator\(\)

Registers an operator for a non-workflow user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_m5c_hvl_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   requestorid - Registered user GUID that is used to set CI Action/operational states.
-   result - true if successfully registered.
-   errors - list of errors.

</td></tr></tbody>
</table>```

var output = SNC.StateManagementScriptableApi.registerOperator();
var jsonUntil = new JSON();
var result = jsonUntil.decode(output);
var requestorId = result.requestorId;

```

## StateManagementScriptableApi - removeBulkCIAction\(String requestorId, String sysIdList, String ciActionName\)

Removes a CI action for a list of CIs.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|A sys\_id of a workflow context, or the GUID returned from the registerOperator\(\) method.|
|sysIdList|String|A comma separated list of CI sys\_ids|
|ciActionName|String|The CI action name|

<table id="table_jz1_2vs_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   result - true if the action is removed for all CIs in the list; otherwise, false.
-   errors - list of errors.

</td></tr></tbody>
</table>## StateManagementScriptableApi - setBulkCIOperationalState\(String requestorId, String sysIdList, String opsLabel, String opsStateListOld\)

Set the operational state for list of CIs.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|A sys\_id of a workflow context, or the GUID returned from the registerOperator\(\) method.|
|sysIdList|String|A comma separated list of CI sys\_ids.|
|opsLabel|String|This is the string label of an operational\_status choice.|
|opsStateListOld|String|\(Optional\) A comma separated list of old CI states that all CIs should be in.|

<table id="table_igf_5ks_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string with name-value pairs for -   result - true if the state is set for all CIs in the list; otherwise, false.
-   errors - list of errors.

</td></tr></tbody>
</table>```
var output = SNC.StateManagementScriptableApi.registerOperator();
var jsonUntil = new JSON();
var result = jsonUtil.decode(output);
var requestorId = result.requestorId;

// list of sys_ids to update
var sys_ids;

// Set list of sys_ids's Operational State to 'Repair in Progress'
output = SNC.StateManagementScriptableApi.setBulkCIOperationalState(requestorId, sys_ids,'Repair in Progress');
gs.print(output);

```

## StateManagementScriptableApi - unregisterOperator\( String requestorId\)

Unregisters an operator for non-workflow users.

|Name|Type|Description|
|----|----|-----------|
|requestorId|String|Sys\_id of a workflow context or the GUID returned from the registerOperator\(\) method.|

<table id="table_qwv_2xl_px" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

JSON formatted name-value pairs. Possible values:

-   result - `true` if successfully unregistered
-   errors - list of errors.

</td></tr></tbody>
</table>This example show how to use the unregisterOperator\(\) method to unregister a registered user.

```
var output = SNC.StateManagementScriptableApi.registerOperator();
var jsonUtil = new JSON();
var result = jsonUtil.decode(output);
var requestorId = result.requestorId; // Fetching requestorId

output = SNC.StateManagementScriptableApi.unregisterOperator(requestorId);
gs.info(output); 
```

Output:

```
{"result":true}
```

