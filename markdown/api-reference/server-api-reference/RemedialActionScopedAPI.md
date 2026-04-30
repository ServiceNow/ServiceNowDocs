---
title: RemedialActionEngine - Scoped
description: The RemedialActionEngine API provides methods for working with remedial actions.Starts any remedial action from the parent record against a target record. This method creates a new remedial action execution record in a 'Ready' state.This method is used to check if the current user can or cannot cancel the given remedial action execution.Cancels a remedial action execution request, then updates the execution record to the state ‘cancelled’ and returns true upon success.Triggers any remedial action execution that was started and is currently in Ready state. This method starts the targeted Action \(e.g. CI Action\) and moves the remedial action execution state to 'In Progress'.Gets the current execution status and output payload of the targeted Action.Checks the applicability of any remedial action against a target record.Checks if the user is authorized to execute the remedial action.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RemedialActionEngine- Scoped

The RemedialActionEngine API provides methods for working with remedial actions.

This API is part of the Remedial Actions Framework and can be used to perform the following actions:

-   Kick start a remedial action.
-   Trigger the execution of a remedial action.
-   Check the authorization of logged in user to execute the remedial action.
-   Check the applicability of the remedial action against the target record.
-   Get the current execution status and output payload of the targeted action.

This API requires the Remedial Actions Framework \(com.snc.sn\_reacf\) store application and is provided within the `sn_reacf` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RemedialActionEngine - beginRemediation \(String remedialAction, String parentTable, String parentRecord, Object actionParams, String targetRecord, String originRecord\)

Starts any remedial action from the parent record against a target record. This method creates a new remedial action execution record in a 'Ready' state.

**Note:** When defining request parameters, remember that:

-   If the parameter type is an object or array, define each property and its type.
-   If the parameter type is GlideRecord, provide the associated table in your request.

<table id="table_dcp_cgs_gxb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

remedialAction

</td><td>

String or GlideRecord

</td><td>

Sys\_id or internal\_name or GlideRecord of the femedial action \[sn\_reacf\_remedial\_action\] table.

</td></tr><tr><td>

parentTable

</td><td>

String

</td><td>

Table name of the parent record.

</td></tr><tr><td>

parentRecord

</td><td>

String

</td><td>

Sys\_id of the parent record.

</td></tr><tr><td>

actionParams

</td><td>

Object

</td><td>

Optional. Map of remedial action parameter names and values.

 ```
{
    “<parameter name>”: <parameter value>
}
```

 **Note:** Parameter value should be of type defined in remedial action Parameter \[sn\_reacf\_remedial\_action\_parameter\] table.

</td></tr><tr><td>

targetRecord

</td><td>

String or GlideRecord

</td><td>

Optional. Sys\_id or GlideRecord of the configured Target table.

</td></tr><tr><td>

originRecord

</td><td>

String or GlideRecord

</td><td>

Optional. Sys\_id or GlideRecord of the Remedial Action Origin \[sn\_reacf\_remedial\_action\_origin\] table.

</td></tr></tbody>
</table><table id="table_ecp_cgs_gxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

```
{
    "statusCode": "String",
    "actionExecutionRequestId": "String",
    "parentRecord": "String",
    "parentTable": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.statusCode

</td><td>

Status code of the remedial action execution request i.e. successful, duplicate\_request or failed

</td></tr><tr><td>

&lt;Object&gt;.actionExecutionRequestId

</td><td>

Sys\_id of the new Rremedial action execution record or duplicate concurrent Remedial Action Execution record

</td></tr><tr><td>

&lt;Object&gt;.parentRecord

</td><td>

Sys\_id of the Parent record of the duplicate concurrent remedial action execution record.

</td></tr><tr><td>

&lt;Object&gt;.parentTable

</td><td>

Table name of the Parent record of the duplicate concurrent remedial action execution record.

</td></tr></tbody>
</table>The following example shows how to start any remedial action. Here, the remedial action uses a CI Action internally to kill a process on a CI.

```
var remedialAction = "9ef9924c436521101a24ff53e9b8f2d2" //sys_id of the Action
var parentTable = "incident"; //table name of the Parent record
var parentRecord = "62733787871e25105763ec6d0ebb3579" //sys_id of the Parent record
var actionParams = {
    process_id: "322113"
}
var targetRecord = "af57a3418775e5105763ec6d0ebb356d"; //sys_id of the Target record
var originRecord = "26e78022c3d525104f1a722e3f40dd99"; //sys_id of the Origin record

var remedialActionEngine = new sn_reacf.RemedialActionEngine();
var response = remedialActionEngine.beginRemediation(remedialAction, parentTable, parentRecord, actionParams, targetRecord, originRecord);
 
gs.info(JSON.stringify(response));

```

Output object:

```
Case 1 :successful : 
{
  ‘statusCode’: ‘successful’,
  ‘actionExecutionRequestId: ‘979b6060a5954300964fa3aa92874155’

}

Case 2 :Duplicate : 
{
  ‘statusCode’: ‘duplicate_request,
  ‘actionExecutionRequestId’: ‘552c48888c033300964f4932b03eb092’,
  ‘parentRecord’ : ‘1a14620f973be110539e35d11153afc8’,
  ‘parentTable’: ‘incident’

}

Case 3 : Failed 
{
  ‘statusCode’: ‘failed,
}

```

## RemedialActionEngine - canCancel\(String remedialActionExecution\)

This method is used to check if the current user can or cannot cancel the given remedial action execution.

**Note:** When defining request parameters, remember that:

-   If the parameter type is an object or array, define each property and its type.
-   If the parameter type is GlideRecord, provide the associated table in your request.

|Name|Type|Description|
|----|----|-----------|
|remedialActionExecution|String or GlideRecord|Sys\_id or GlideRecord of the Remedial Action Execution \[sn\_reacf\_remedial\_action\_execution\] table.|

<table id="table_mkw_xrd_3yb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the remedial action execution request can or cannot be canceled.

 Valid values:

-   true: The specified remedial action execution request can be canceled.
-   false: The specified remedial action execution request cannot be canceled.

</td></tr></tbody>
</table>The following example shows how to validate whether the current user can cancel any remedial action execution in its current state.

```
var remedialActionExecutionId = "9ef9924c436521101a24ff53e9b8f2d2" //sys_id of sn_reacf_remedia_action_execution record

var remedialActionEngine = new sn_reacf.RemedialActionEngine();
var canCancel = remedialActionEngine.canCancel(remedialActionExecutionId)

gs.info("canCancel: " + canCancel);

```

Output:

```
canCancel: true
```

## RemedialActionEngine - cancelExecution\(String remedialActionExecution\)

Cancels a remedial action execution request, then updates the execution record to the state ‘cancelled’ and returns true upon success.

**Note:** When defining request parameters, remember that:

-   If the parameter type is an object or array, define each property and its type.
-   If the parameter type is GlideRecord, provide the associated table in your request.

|Name|Type|Description|
|----|----|-----------|
|remedialActionExecution|String or GlideRecord|Sys\_id or GlideRecord of the Remedial Action Execution \[sn\_reacf\_remedial\_action\_execution\] table.|

<table id="table_mkw_xrd_3yb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the remedial action execution request can or cannot be canceled.

 Valid values:

-   true: The specified remedial action execution request is canceled successfully. A status of true updates the execution record to the state ‘cancelled'.
-   false: The specified remedial action execution request is not canceled successfully.

</td></tr></tbody>
</table>The following example shows how to cancel any remedial action execution from its current state.

```
var remedialActionExecutionId = "9ef9924c436521101a24ff53e9b8f2d2" //sys_id of sn_reacf_remedia_action_execution record

var remedialActionEngine = new sn_reacf.RemedialActionEngine();
var cancelExecution = remedialActionEngine.cancelExecution(remedialActionExecutionId)

gs.info(‘cancelExecution: ’ + cancelExecution);
```

Output:

```
cancelExecution : true
```

## RemedialActionEngine - executeRemedialAction \(String remedialActionExecution\)

Triggers any remedial action execution that was started and is currently in Ready state. This method starts the targeted Action \(e.g. CI Action\) and moves the remedial action execution state to 'In Progress'.

|Name|Type|Description|
|----|----|-----------|
|remedialActionExecution|String or GlideRecord|Sys\_id or GlideRecord of the Remedial Action Execution \[sn\_reacf\_remedial\_action\_execution\] table.|

<table id="table_itl_mfs_gxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object contains the action\_execution\_table and action\_execution\_id of the remedial action execution.

 ```
{
   “action_execution_table”: “String”,
   “action_execution_id”: “Sys_id”
}

```

</td></tr></tbody>
</table>The following example shows how to execute any remedial action.

```
var remedialActionExecution = "8ed58be387d2a5100295ebd73cbb35a3"; //Sys_id of the Remedial Action Execution record 
 
var remedialActionEngine = new sn_reacf.RemedialActionEngine(); 
var response = remedialActionEngine.executeRemedialAction(remedialActionExecution); 
gs.info("Response: " + JSON.stringify(response, null, 2));
```

Output:

```
{ 
  "action_execution_table": "sn_cimaf_action_request", 
  "action_execution_id": "2d7843a787d2a5100295ebd73cbb35d4" 
}
```

## RemedialActionEngine - getRemedialActionOutput \(String remedialActionExecution\)

Gets the current execution status and output payload of the targeted Action.

|Name|Type|Description|
|----|----|-----------|
|remedialActionExecution|String or GlideRecord|Sys\_id or GlideRecord of the Remedial Action Execution \[sn\_reacf\_remedial\_action\_execution\] table.|

<table id="table_stg_32s_gxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object contains the status object having value and display value of the target Action status, and payload array having the target Action outputs executed as part of the Remedial Action execution.

 Data type: String

 ```
{
  "status": {
    "value": "completed",
    "displayValue": "Completed"
  },
  "payload": [
    "{\"output\":\"SUCCESS: The process with PID 19604 has been terminated.\\r\\n\",\"cmd\":\"taskkill /pid 19604 /f\"}"
  ]
}
```

</td></tr></tbody>
</table>The following example shows how to get current execution status and output payload of the targeted Action.

```
var remedialActionExecution = "8ed58be387d2a5100295ebd73cbb35a3"; //sys_id of the Remedial Action Execution record

var remedialActionEngine = new sn_reacf.RemedialActionEngine();
var response = remedialActionEngine.getRemedialActionOutput(remedialActionExecution);

gs.info("Response: " + JSON.stringify(response, null, 2));

```

Output:

```
{
  "status": {
    "value": "completed",
    "displayValue": "Completed"
  },
  "payload": [
    "{\"output\":\"SUCCESS: The process with PID 19604 has been terminated.\\r\\n\",\"cmd\":\"taskkill /pid 19604 /f\"}"
  ]
}
```

## RemedialActionEngine - isApplicable \(String remedialAction, String targetRecord\)

Checks the applicability of any remedial action against a target record.

|Name|Type|Description|
|----|----|-----------|
|remedialAction|String or GlideRecord|Sys\_id or internal\_name or GlideRecord of the remedial action \[sn\_reacf\_remedial\_action\] table.|
|targetRecord|String or GlideRecord|Sys\_id or GlideRecord of the configured Target table.|

<table id="table_n4x_wcs_gxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the target record's applicability for the remedial action.

-   true: the Remedial Action is applicable to the specified target record.
-   false: the Remedial Action is not applicable to the specified target record.

</td></tr></tbody>
</table>The following example shows how to check applicability of any remedial action against a target record.

```
var remedialAction = "9ef9924c436521101a24ff53e9b8f2d2"; //Sys_id of the Remedial Action Execution record 
var targetRecord = "df3799a387a921100295ebd73cbb35c4"; //Sys_id of the Target Record 
 
var remedialActionEngine = new sn_reacf.RemedialActionEngine(); 
var isApplicable = remedialActionEngine.isApplicable(remedialAction, targetRecord); 
gs.info("Is applicable: " + isApplicable);
```

Output:

```
Is applicable: true
```

## RemedialActionEngine - isAuthorized\(String remedialAction\)

Checks if the user is authorized to execute the remedial action.

|Name|Type|Description|
|----|----|-----------|
|remedialAction|String or GlideRecord|Sys\_id or internal\_name or GlideRecord of the Remedial Action \[sn\_reacf\_remedial\_action\] table.|

<table id="table_xpy_jzr_gxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the resulting success status of the user's authorization.

 -   true: The user's authorization is successful.
-   false: The user's authorization is unsuccessful.

</td></tr></tbody>
</table>The following example shows how to check authorization to execute any remedial action.

```
var actionSysId = "e62f550843e121101a24ff53e9b8f23b"; //Sys_id of the Action 
 
var remedialActionEngine = new sn_reacf.RemedialActionEngine(); 
var isAuthorized = remedialActionEngine.isAuthorized(actionSysId); 
gs.info("Is user authorized: " + isAuthorized);
```

Output:

```
Is user authorized: true
```

