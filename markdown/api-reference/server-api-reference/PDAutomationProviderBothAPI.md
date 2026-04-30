---
title: PDAutomationProvider - Scoped, Global
description: The PDAutomationProvider API enables inserting an optional activity into a process while it's executing.Activates a playbook.Adds a specified optional activity to a process to be run relative to another activity during process execution.Assigns an optional activity to a lane to run during that lane's execution context.Deactivates a playbook.Duplicates a playbook.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PDAutomationProvider - Scoped, Global

The PDAutomationProvider API enables inserting an optional activity into a process while it's executing.

This API is part of the Playbooks plugin \(com.glide.pad.core\) and runs in the `sn_pad` namespace.

Calling scripts with this API requires at least one of the following:

-   The caller must be in the same scope in which the optional activity trigger was created.
-   Admin privileges.

A process is a series of activities ordered by lanes. An optional activity is predefined during process design. The activities aren't scheduled to run at a precise time. An activity can be assigned to a lane and made available to run during lane execution. An activity can be assigned to a process and made available to run during lane execution.

To create an optional activity, it must have the **Start rule** set to **Manual** in the Activities \[sys\_pd\_activity\] table. Playbooks doesn't currently support creating manual activities.

An agent adds the optional activity to a lane or activity relative to another activity. The process must be running to insert an optional activity.

See also:

-   [Design an automated process](https://www.servicenow.com/docs/access?context=design-automated-process&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
-   [Process Automation Designer lanes and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PDAutomationProvider – activateProcess\(String processDefinitionSysId\)

Activates a playbook.

|Name|Type|Description|
|----|----|-----------|
|processDefinitionSysId|String|The sys\_id of a playbook located in the Process Definitions \[sys\_pd\_process\_definition\] table.|

<table id="table_alb_lbs_1cc" class="returns"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing process definition activation details.```
{
  "errors": [Array]
  "process_definition": {Object},
  "state": "String"
}
```

</td></tr><tr><td>

errors

</td><td>

List of errors. Empty if successful. Data type: Array of String\(s\)

</td></tr><tr><td>

process\_definition

</td><td>

The activated playbook and its properties.Data type: Object

```
"process_definition":
{
  "active": Boolean,
  "snapshot": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

process\_definition.active

</td><td>

Flag that indicates whether the process definition for the deactivated playbook is active. Find process definitions in the Process Definitions \[sys\_pd\_process\_definition\] list.Valid values:

-   true: The process definition for the deactivated playbook is active.
-   false: The process definition for the deactivated playbook is inactive.

Data type: Boolean

</td></tr><tr><td>

process\_definition.snapshot

</td><td>

Contains details about the process definition at the time of activation.Data type: Object

```
{
  "snapshot":
    {
      "created": "String",
      "processDefinitionSysId": "String"
    }
}
```

</td></tr><tr><td>

process\_definition. snapshot. created

</td><td>

The date that the playbook was created.Data type: String

</td></tr><tr><td>

process\_definition. snapshot. processDefinitionSysId

</td><td>

The sys\_id of the activated playbook.Data type: String

</td></tr><tr><td>

process\_definition.status

</td><td>

Indicates the publishing status of the playbook.Possible values:

-   draft: The playbook is in draft state.
-   published: The playbook is in published state.

Data type: String

</td></tr><tr><td>

state

</td><td>

Indicates whether your request to activate was successful or not.Possible values:

-   SUCCESS – The playbook was successfully activated.
-   FAILURE – The ID for the playbook was not found.

Data type: Object

</td></tr></tbody>
</table>The following example shows how to activate a playbook.

```
var myPlaybook = sn_pad.PDAutomationProvider.activateProcess('cdd1b85e43000210d96e29c28ab8f275');
gs.info(JSON.stringify(myPlaybook));
```

Output:

```
{
  "process_definition": {
    "active": true,
    "snapshot": {
      "processDefinitionId": "cdd1b85e43000210d96e29c28ab8f275",
      "created": "2024-02-19 22:58:12"
    },
    "status": "published"
  },
  "state": "SUCCESS",
  "errors": []
}
```

## PDAutomationProvider – addOptionalActivityRelativeToActivityContext\(String contextID, String activityId, String where, String relativeToId\)

Adds a specified optional activity to a process to be run relative to another activity during process execution.

An activity context is created for each activity when a process executes. The context also handles how the activity handles execution. For information, see [Process Automation Designer lanes and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

<table id="PDAutoParms" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contextID

</td><td>

String

</td><td>

Sys\_id of the activity execution in which to add the optional activity. To access, click the process listed in the Process Executions \[sys\_pd\_context\] table. The execution selected must be in a state of **In Progress**.

</td></tr><tr><td>

activityId

</td><td>

String

</td><td>

Sys\_id of the optional activity listed in the Activities \[sys\_pd\_activity\] table.**Note:** To create an optional activity, it must have the **Start rule** set to **Manual** in the Activities \[sys\_pd\_activity\] table.

</td></tr><tr><td>

where

</td><td>

String

</td><td>

Indicates where to place the activity in the process. Valid values:

-   AFTER – Execute this activity after the relative activity context.
-   WITH – Execute the activity at the same time as another relative activity context.

</td></tr><tr><td>

relativeToId

</td><td>

String

</td><td>

ID of the relative activity context that the optional activity will run after or with. Listed in the Activity Context \[sys\_pd\_activity\_context\] table.

</td></tr></tbody>
</table><table id="PDAutoReturns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the activity was successfully scheduled to run. Valid values:

-   true: Activity is successfully scheduled to run. The output is a string stating `success`.
-   false: Activity isn't successfully scheduled to run. The output is an array of one or more error messages.

 If errors, list of one or more error messages. Message stating `Array of 0 or more elements` otherwise.

</td></tr><tr><td>

Array

</td><td>

If errors, list of one or more error messages. Message stating `Array of 0 or more elements` otherwise. Possible error messages:

-   `Invalid Optional activity Id` – The sys\_id provided for the **activityId** parameter is invalid.
-   `Invalid PD context Id` – The Process Designer \(PD\) sys\_id provided in the **contextID** parameter is invalid.
-   `Invalid position type` – The position type provided is invalid. See the description of the **where** parameter for valid types.
-   `Invalid Relative-to Id` – The sys\_id provided for the **relativeToId** parameter is invalid.
-   `Optional activity not found` – The sys\_id provided for the **activityId** parameter wasn't found.
-   `Process must still be active` – The process containing this activity must be active to run the optional activity.
-   `Relative activity context not found` – The sys\_id provided for the **relativeToId** parameter was not found.

</td></tr></tbody>
</table>The following example shows how to run an optional activity simultaneously with the relative activity context.

```
var contextId = '<context_id>';
var optionalActivityId = '<optional_activity_id>';
var where = 'WITH'; // options AFTER, WITH
var relativeToId = '<relative_activity_context_id>'; // relative activity context ID

var response = sn_pad.PDAutomationProvider.addOptionalActivityRelativeToActivityContext(contextId, optionalActivityId, where, relativeToId);

gs.info(JSUtil.describeObject(response));
```

Output \(success\):

```
success: boolean = true
errors: Array of 0 elements
```

## PDAutomationProvider – addOptionalActivityRelativeToLaneContext\(String contextID, String activityId, String where, String relativeToId\)

Assigns an optional activity to a lane to run during that lane's execution context.

A lane context is created for each lane when a process executes. The context also handles how the lane handles execution. For information, see [Process Automation Designer lanes and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

<table id="PDAutoParms" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contextID

</td><td>

String

</td><td>

Sys\_id of the activity execution in which to add the optional activity. To access, click the process listed in the Process Executions \[sys\_pd\_context\] table. The execution selected must be in a state of **In Progress**.

</td></tr><tr><td>

activityId

</td><td>

String

</td><td>

Sys\_id of the optional activity listed in the Activities \[sys\_pd\_activity\] table.**Note:** To create an optional activity, it must have the **Start rule** set to **Manual** in the Activities \[sys\_pd\_activity\] table.

</td></tr><tr><td>

where

</td><td>

String

</td><td>

Indicates where to place the activity in the process. Valid values:

-   LAST – Execute as the final activity in a lane context.
-   NEXT – Execute in the next activity in a lane context.

</td></tr><tr><td>

relativeToId

</td><td>

String

</td><td>

ID of the relative lane context in which the optional activity is to run. Listed in the Lane Context \[sys\_pd\_lane\_context\] table.

</td></tr></tbody>
</table><table id="PDAutoReturns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the activity was successfully scheduled to run. Valid values:

-   true: Activity is successfully scheduled to run. The output is a string stating `success`.
-   false: Activity isn't successfully scheduled to run. The output is an array of one or more error messages.

</td></tr><tr><td>

Array

</td><td>

If errors, list of one or more error messages. Message stating `Array of 0 or more elements` otherwise. Possible error messages:

-   `Invalid Optional activity Id` – The sys\_id provided for the **activityId** parameter is invalid.
-   `Invalid PD context Id` – The Process Designer \(PD\) sys\_id provided in the **contextID** parameter is invalid.
-   `Invalid position type` – The position type provided is invalid. See the description of the **where** parameter for valid types.
-   `Invalid Relative-to Id` – The sys\_id provided for the **relativeToId** parameter is invalid.
-   `Optional activity cannot be added to lane` – The optional activity provided in the **activityId** parameter can't be added relative to the lane provided in the **relativeToId** parameter. Make sure that the **Activity Execution** selected is in the **In Progress** state.
-   `Optional activity not found` – The sys\_id provided for the **activityId** parameter wasn't found.
-   `Process must still be active` – The process containing this activity must be active to run the optional activity.
-   `Relative lane context not found` – The sys\_id provided for the **relativeToId** parameter was not found.

</td></tr></tbody>
</table>The following example shows how to run an optional activity as the final activity in a lane context.

```
var contextId = '<context_id>';
var optionalActivityId = '<optional_activity_id>';
var where = 'LAST'; // options LAST, NEXT
var relativeToId = '<relative_lane_context_id>'; // relative lane context ID

var response = sn_pad.PDAutomationProvider.addOptionalActivityRelativeToLaneContext(contextId, optionalActivityId, where, relativeToId);

gs.info(JSUtil.describeObject(response));
```

Output \(success\):

```
success: boolean = true
errors: Array of 0 elements
```

## PDAutomationProvider – deactivateProcess\(String processDefinitionSysId\)

Deactivates a playbook.

|Name|Type|Description|
|----|----|-----------|
|processDefinitionSysId|String|The sys\_id of a playbook located in the Process Definitions \[sys\_pd\_process\_definition\] table.|

<table id="table_alb_lbs_1cc" class="returns"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing process definition deactivation details.```
{
  "errors": [Array]
  "process_definition": {Object},
  "state": "String"
}
```

</td></tr><tr><td>

errors

</td><td>

List of errors. Empty if successful. Data type: Array of String\(s\)

</td></tr><tr><td>

process\_definition

</td><td>

The deactivated playbook and its properties.Data type: Object

```
"process_definition":
{
  "active": Boolean,
  "snapshot": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

process\_definition.active

</td><td>

Indicates whether the process definition for the deactivated playbook is active. Find process definitions in the Process Definitions \[sys\_pd\_process\_definition\] list.Possible values:

-   true: The process definition for the deactivated playbook is active.
-   false: The process definition for the deactivated playbook is inactive.

Data type: Boolean

</td></tr><tr><td>

process\_definition.description

</td><td>

Details about your deactivated playbook.Data type: String

</td></tr><tr><td>

process\_definition.label

</td><td>

The name of the deactivated playbook that users see in the interface.Data type: String

</td></tr><tr><td>

process\_definition.name

</td><td>

The name for the deactivated playbook in the code. Only used as a request parameter in scripting.Data type: String

</td></tr><tr><td>

process\_definition.scope

</td><td>

The sys\_id of the application scope that your playbook is deactivated for.Data type: String

</td></tr><tr><td>

process\_definition.status

</td><td>

If the playbook is published, it changes back to a draft.Data type: String

</td></tr><tr><td>

state

</td><td>

Indicates whether deactivation was successful.Possible values:

-   SUCCESS – The playbook was successfully deactivated.
-   FAILURE – The ID for the playbook was not found.

Data type: String

</td></tr></tbody>
</table>Deactivate the playbook.

```
sn_pad.PDAutomationProvider.deactivateProcess('cdd1b85e43000210d96e29c28ab8f275')
```

Outputs:

```
{"process_definition":{"scope":"global","name":"test","active":true,"description":"","label":"test","status":"draft"},"state":"SUCCESS"}
```

## PDAutomationProvider – duplicateProcess\(String processDefinitionSysId, String label, String description, String scopeId, String triggerTypeId\)

Duplicates a playbook.

|Name|Type|Description|
|----|----|-----------|
|processDefinitionSysId|String|The sys\_id of a playbook located in the Process Definitions \[sys\_pd\_process\_definition\] table.|
|label|String|The name of the duplicated playbook.|
|description|String|Optional. Add details about your playbook.|
|scopeId|String|The sys\_id of the application scope that you want your playbook to run in. The scoped name is from the Process Definition \[sys\_pd\_process\_definition\] table in the format `scope.name`. Entering the sys\_id for the global scope lets your playbook run in any application scope.|
|triggerTypeId|String|The sys\_id of the trigger from which to initiate playbook runs. Find the trigger type in the Trigger Type \[sys\_pd\_trigger\_type\] table and copy its sys\_id.|

<table id="table_alb_lbs_1cc" class="returns"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing process definition duplication details.```
{
  "errors": [Array]
  "processDefinitionSysId": "String",
  "state": "String"
}
```

</td></tr><tr><td>

errors

</td><td>

List of errors. Empty if successful. Data type: Array of String\(s\)

Possible error messages:

-   `Scope not found for scopeId: xyz`
-   `Process definition not found for id: xyz`
-   `Trigger type not found for triggerTypeId: xyz`

</td></tr><tr><td>

processDefinitionSysId

</td><td>

The sys\_id of the new playbook in the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

state

</td><td>

Indicates whether playbook duplication was successful.Possible values:

-   SUCCESS – The playbook was successfully duplicated.
-   FAILURE – The ID for the playbook, application scope, or trigger was not found.

Data type: Object

</td></tr></tbody>
</table>This example shows how to duplicate a playbook with the sys\_id `f8ca6192ec210210f8772cbd595eab20`. The new playbook is named **Playbook 2.0**, has an application scope of **Global**, and is triggered when a record is created. The **Record Create** trigger type has a sys\_id of `ab6951170f1200108c87f4f0ff767e4f`.

```
sn_pad.PDAutomationProvider.duplicateProcess('f8ca6192ec210210f8772cbd595eab20', 'Playbook 2.0', '', 'global', 'ab6951170f1200108c87f4f0ff767e4f');
```

Output:

```
{"processDefinitionSysId":"6e4f0b8fece9c210f8772cbd595eabda","state":"SUCCESS"}
```

