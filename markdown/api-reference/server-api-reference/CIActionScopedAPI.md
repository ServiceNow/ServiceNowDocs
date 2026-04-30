---
title: CIActionEngine - Scoped
description: The CIActionEngine API provides methods that enable you to execute any action on a configuration item \(CI\), to check the authorization of a user before executing an action, and to get the status and action outputs of any action execution request.Executes any action on a CI with the configured action parameters.Gets the status and action outputs of an action execution request.Checks the authorization of the signed-in user before they can execute an action according to specified configurations.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIActionEngine- Scoped

The CIActionEngine API provides methods that enable you to execute any action on a configuration item \(CI\), to check the authorization of a user before executing an action, and to get the status and action outputs of any action execution request.

The CI action is associated with the Metrics and CI Actions Framework application. To use this class in a scoped application, use the `sn_cimaf` namespace identifier. The CIActionEngine API requires the Metrics and CI Actions Framework \(com.snc.sn\_cimaf\) plugin and is provided within the `sn_cimaf` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIActionEngine - execute\(\)

Executes any action on a CI with the configured action parameters.

<table id="table_i2w_kg1_fxb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

String or Glide Record

</td><td>

Sys\_id or GlideRecord of the Action \[sn\_cimaf\_action\] table.

</td></tr><tr><td>

ci

</td><td>

String or Glide Record

</td><td>

Sys\_id or GlideRecord of the CMDB \[cmdb\_ci\] table on which the Action needs to be executed

</td></tr><tr><td>

actionParams

</td><td>

Object

</td><td>

Optional. Map of Action parameter names and values.

 ```
{
 “<parameter name>”: <parameter value>
}
```

 **Note:** Parameter values should be of the type defined in the Action parameter \[sn\_cimaf\_action\_parameter\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the new or existing duplicate in-progress Action Request.|

The following example shows how to kill a process on a CI.

```
var actionSysId = "6303db0d53b99910ae50ddeeff7b121e";	 
//Sys_id of the Action – End Process 
var ciSysId = "b4fd7c8437201000deeabfc8bcbe5dc1"; //Sys_id of the CI 
var actionParams = { 
    process_id: 23342 //Process id of the process to be killed 
}; 
 
var ciActionEngine = new sn_cimaf.CIActionEngine(); 
var actionRequestId = ciActionEngine.execute(actionSysId, ciSysId, actionParams); 
 
gs.info("Action Request Id: " + actionRequestId);
```

Output:

```
Action Request Id: e34e3a199d16a510f877a45cc5e8a492
```

## CIActionEngine - getActionRequestOutput\(\)

Gets the status and action outputs of an action execution request.

|Name|Type|Description|
|----|----|-----------|
|actionRequest|Glide Record|GlideRecord of the Action Request \[sn\_cimaf\_action\_request\] table.|

<table id="table_eqv_nh1_fxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object contains the status and list of the action outputs of the provided action request.```
{ 
    “sys_id”: “String”, 
    “state”: “String”, //Possible values: completed, in_progress, failed 
    “sn_cimaf_action_output”: [ 
          { 
                “sys_id”: “String”, 
                “action_command”: “String”, //Sys_id of the Action Configuration Step table 
                “payload”: “String”, 
                “state”: “String”, //Possible values: completed, in_progress, failed, validation_failure 
                “request_id”: “String” //Unique id returned by Provider on executing action_command 
          } 
      ] 
} 
```

</td></tr></tbody>
</table>The following example shows how to get status and action outputs for any action request.

```
var actionRequestGr = new GlideRecord('sn_cimaf_action_request'); 
actionRequestGr.get('e34e3a199d16a510f877a45cc5e8a492'); 
 
var ciActionEngine = new sn_cimaf.CIActionEngine(); 
var actionRequestOutput = ciActionEngine.getActionRequestOutput(actionRequestGr); 
gs.info("Action Request Output: " + JSON.stringify(actionRequestOutput, null, 2));
```

Output:

```
{
  "sys_id": "e34e3a199d16a510f877a45cc5e8a492",
  "state": "completed",
  "sn_cimaf_action_output": [
    {
      "sys_id": "405ef2599d16a510f877a45cc5e8a41e",
      "action_command": "b0e43efb53259510ae50ddeeff7b129b",
      "payload": "{\"output\":\"SUCCESS: The process with PID 23342 has been terminated.\\r\\n\",\"cmd\":\"taskkill /pid 23342 /f\"}",
      "state": "completed",
      "request_id": "cc5ef2599d16a510f877a45cc5e8a41d"
    }
  ]
}
```

## CIActionEngine - isAuthorized\(\)

Checks the authorization of the signed-in user before they can execute an action according to specified configurations.

The configurations are defined in the Action Role \[sn\_cimaf\_action\_role\], User Criteria Action Inclusion \[sn\_cimaf\_action\_user\_criteria\_mtom\], and User Criteria Action Exclusion \[sn\_cimaf\_action\_user\_criteria\_no\_mtom\] tables.

**Note:** By default, if there is no configuration present in any of these tables for the Action, the authorization fails.

|Name|Type|Description|
|----|----|-----------|
|action|Glide Record|GlideRecord of the Action \[sn\_cimaf\_action\] table.|

<table id="table_ugh_xn5_2xb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the success of the user's authorization.

 Valid values:

-   true: User is authorized to execute the action.
-   false: User is authorized to execute the action.

</td></tr></tbody>
</table>The following example uses the isAuthorized\(\) method to check a user's authorization to execute any action on a CI.

```
var actionSysId = "6303db0d53b99910ae50ddeeff7b121e" //Sys_id of the Action 
var actionGr = new GlideRecord('sn_cimaf_action'); 
actionGr.get('6303db0d53b99910ae50ddeeff7b121e'); 
 
var ciActionEngine = new sn_cimaf.CIActionEngine(); 
var isAuthorized = ciActionEngine.isAuthorized(actionGr); 
gs.info("Is user authorized: " + isAuthorized);
```

```
Is user authorized: true
```

