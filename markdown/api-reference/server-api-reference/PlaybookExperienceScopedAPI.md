---
title: PlaybookExperience - Scoped
description: The PlaybookExperience API provides methods for handling playbook executions.Cancel an individual playbook.Cancels playbook executions for a given parent record.Gets a list of playbook executions for a given parent record.Checks whether a parent record has playbook executions.Restarts an execution from the beginning \(the entire playbook\) or from a specific stage or activity of a playbook.Initiates a playbook for a parent record.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 17
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PlaybookExperience- Scoped

The PlaybookExperience API provides methods for handling playbook executions.

This API requires the Playbook Experience Core plugin \(com.glide.playbook\_experience.config\) and is provided within the `sn_playbook` namespace.

This API requires at least one playbook in the Process Definition \[sys\_pd\_process\_definition\] table. To use this API, you must have the roles required to view and cancel a running process in Process Automation Designer. For more information, see [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PlaybookExperience - cancelPlaybook\(String playbookContext, String cancellationReason, String playbookExperienceId, Boolean force\)

Cancel an individual playbook.

<table id="table_xxz_j4z_dfc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

playbookContext

</td><td>

GlideRecord

</td><td>

The \[sys\_pd\_context\] record that you want to cancel.

</td></tr><tr><td>

cancellationReason

</td><td>

String

</td><td>

The reason for canceling the playbook execution. This appears in the UI for runtime users as well.

</td></tr><tr><td>

playbookExperienceId

</td><td>

String

</td><td>

Optional. Sys\_id of the playbook experience record in the Playbook Experience \[sys\_playbook\_experience\] table to use for the cancellation. Use this parameter if you've defined custom activity state mappings. See [Playbook activity state mapping](https://www.servicenow.com/docs/access?context=playbook-activity-state-mapping&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).Default: Sys\_id of the Global Playbook Experience record.

</td></tr><tr><td>

force

</td><td>

Boolean

</td><td>

Optional. If set to true, cancels the underlying flows for activities that are In Progress. The cancellationReason parameter is not used when this parameter is set to true. You can only force cancel activities after the playbook is cancelled and the sys\_pd\_context is in a Pending Cancel state.**Note:** The flow engine attempts to cancel all underlying flows without creating issues when a playbook is canceled, but we cannot guarantee that no issues will occur.

</td></tr></tbody>
</table><table id="table_yxz_j4z_dfc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;.canceledPlaybookContext

</td><td>

The cancelled playbook execution associated data, such as the reason why it was cancelled.Data type: Array

 ```
"canceledPlaybookContext": [
    {
      "can_read": Boolean,
      "canceled_by": "String",
      "can_add_activity": Boolean,
      "snapshot_id": "string",
      "can_restart": Boolean,
      "can_cancel": Boolean,
      "cancellation_reason": "String",
      "errors": [Array],
      "parent_record": "String",
      "parent_table": "String",
      "playbook_id": "String",
      "playbook_table": "String",
      "scoped_name": "String",
      "variant_id": "String",
      "is_archived": Boolean,
      "state": {Object},
      "sys_id": "String",
      "title": "String"   
    }
]
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_add\_activity

</td><td>

Flag that indicates whether a user can add an optional activity to the playbook.Valid values:

-   true: Current user can add an optional activity to the playbook.
-   false: Current user can’t add an optional activity to the playbook.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_cancel

</td><td>

Flag that indicates whether a user can cancel a playbook.-   true: The process definition for the deactivated playbook is active.
-   false: The process definition for the deactivated playbook is inactive.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_read

</td><td>

Flag that indicates whether the current user can read the playbook execution record. The current user must have read access to the parent record to be able to read the playbook execution record.

 Valid values:

-   true: Current user has read access to the playbook execution record.
-   false: Current user doesn't have read access to the playbook execution record.

 Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_restart

</td><td>

Flag that indicates whether a user can restart a playbook, stage, or activity.-   true: Current user can restart the playbook, stage, or activity.
-   false: Current user can’t restart the playbook, stage, or activity.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.canceled\_by

</td><td>

The **User ID** of the user who cancelled the playbook execution.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.cancellation\_reason

</td><td>

The cancellation reason input by the user who cancelled the playbook execution.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors

</td><td>

List of cancellation errors. Each error is an object in the array.Data type: Array

 ```
"errors": [
    {      
      "message": "String",
      "type": "String"  
    }
]
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors.message

</td><td>

The error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors.type

</td><td>

The type of error.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.is\_archived

</td><td>

Flag that indicates whether playbook context records are archived. Set to true. This value can’t be modified.Possible values:

-   true: Playbook context records are archived.
-   false: Playbook context records aren’t archived.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.parent\_record

</td><td>

Sys\_id of the parent record that playbook executions were cancelled for.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.parent\_table

</td><td>

The name of the table that the parent record is from.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.playbook\_id

</td><td>

Sys\_id of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.playbook\_table

</td><td>

The name of the table that the playbook is from, generally the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.scoped\_name

</td><td>

The scoped name of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table in the format `scope.name`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.snapshot\_id

</td><td>

Sys\_id of the snapshot of the playbook execution from the \[sys\_pd\_snapshot\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state

</td><td>

The state of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: Object

 ```
"state": {    
   "displayValue": "String",    
   "value": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state.displayValue

</td><td>

The display value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state.value

</td><td>

The value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.sys\_id

</td><td>

Sys\_id of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.title

</td><td>

The label of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.variant\_id

</td><td>

Sys\_id of the playbook variant execution from the Process Executions \[sys\_pd\_context\] table.

</td></tr></tbody>
</table>This example shows how to cancel a single execution of a specific playbook that is running too long.

```
var process = new GlideRecord('sys_pd_context');

process.get("SYS_ID");

var cancelPlaybookReturn = sn_playbook.PlaybookExperience.cancelPlaybook(process, "This playbook ran for too long");

gs.info(JSON.stringify(cancelPlaybookReturn));
```

Output:

```
{
 "scoped_name": "global.test_user_form",
 "canceled_by": "maint",
 "can_add_activity": true,
 "snapshot_id": "28ec63425459e250f87766647bf35e7e",
 "playbook_table": "sys_pd_process_definition",
 "can_restart": false,
 "can_cancel": true,
 "title": "Test User Form",
 "cancellation_reason": "This process ran for too long",
 "parent_table": "incident",
 "can_read": true,
 "sys_id": "418b1e7ea722435bb4facac50fc9b4f3",
 "variant_id": null,
 "is_archived": false,
 "state": {
   "displayValue": "Pending Cancel",
   "value": "PENDING_CANCEL"
 },
 "parent_record": "8cdc23425459e250f87766647bf35ea1",
 "playbook_id": "d589efca5419e250f87766647bf35e29",
 "errors": []
}
```

Force cancel a single execution of a specific playbook.

```
var forceCancelPlaybookReturn = sn_playbook.PlaybookExperience.cancelPlaybook(process, "This playbook did not cancel", undefined, true);

gs.info(JSON.stringify(forceCancelPlaybookReturn));
```

Output:

```
{
 "scoped_name": "global.test_user_form",
 "canceled_by": "maint",
 "can_add_activity": true,
 "snapshot_id": "28ec63425459e250f87766647bf35e7e",
 "playbook_table": "sys_pd_process_definition",
 "can_restart": false,
 "can_cancel": true,
 "title": "Test User Form",
 "cancellation_reason": "This process ran for too long",
 "parent_table": "incident",
 "can_read": true,
 "sys_id": "418b1e7ea722435bb4facac50fc9b4f3",
 "variant_id": null,
 "is_archived": false,
 "state": {
   "displayValue": "Cancelled",
   "value": "CANCELLED"
 },
 "parent_record": "8cdc23425459e250f87766647bf35ea1",
 "playbook_id": "d589efca5419e250f87766647bf35e29",
 "errors": []
}
```

## PlaybookExperience - cancelPlaybooksByParentRecord\(GlideRecord parentRecord, String cancellationReason, String scopedName, String playbookExperienceId\)

Cancels playbook executions for a given parent record.

<table id="table_udh_zjr_ypb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

parentRecord

</td><td>

GlideRecord

</td><td>

The parent record to cancel playbook executions for. The parent record can be any record that has playbook executions, such as an interaction record or an onboarding case record.

</td></tr><tr><td>

cancellationReason

</td><td>

String

</td><td>

The reason for cancelling the playbook executions.

</td></tr><tr><td>

scopedName

</td><td>

String

</td><td>

Optional. The scoped name of the playbook to cancel. The scoped name is from the Process Definition \[sys\_pd\_process\_definition\] table in the format `scope.name`. If provided, only executions of this playbook are cancelled for the given parent record. If not provided, all executions of all playbooks are cancelled for the given parent record.

</td></tr><tr><td>

playbookExperienceId

</td><td>

String

</td><td>

Optional. Sys\_id of the playbook experience record in the Playbook Experience \[sys\_playbook\_experience\] table to use for the cancellation. Use this parameter if you've defined custom activity state mappings. See[Playbook activity state mapping](https://www.servicenow.com/docs/access?context=playbook-activity-state-mapping&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).Default: Sys\_id of the Global Playbook Experience record.

</td></tr></tbody>
</table><table id="table_vdh_zjr_ypb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the cancelled playbook executions and any skipped playbook executions that were unable to be cancelled. ```
{
  "canceledPlaybookContext": [Array],
  "skippedPlaybookContext": [Array]
}

```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext

</td><td>

List of the cancelled playbook executions. Each playbook execution is an object in the array.Data type: Array

 ```
"canceledPlaybookContext": [
    {
      "can_read": Boolean,
      "canceled_by": "String",
      "cancellation_reason": "String",
      "errors": [Array],
      "parent_record": "String",
      "parent_table": "String",
      "playbook_id": "String",
      "playbook_table": "String",
      "scoped_name": "String",
      "state": {Object},
      "sys_id": "String",
      "title": "String"   
    }
]
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_add\_activity

</td><td>

Flag that indicates whether a user can add an optional activity to the playbook.Valid values:

-   true: Current user can add an optional activity to the playbook.
-   false: Current user can’t add an optional activity to the playbook.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_cancel

</td><td>

Flag that indicates whether a user can cancel a playbook.-   true: The process definition for the deactivated playbook is active.
-   false: The process definition for the deactivated playbook is inactive.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_read

</td><td>

Flag that indicates whether the current user can read the playbook execution record. The current user must have read access to the parent record to be able to read the playbook execution record.

 Valid values:

-   true: Current user has read access to the playbook execution record.
-   false: Current user doesn't have read access to the playbook execution record.

 Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.can\_restart

</td><td>

Flag that indicates whether a user can restart a playbook, stage, or activity.-   true: Current user can restart the playbook, stage, or activity.
-   false: Current user can’t restart the playbook, stage, or activity.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.canceled\_by

</td><td>

The **User ID** of the user who cancelled the playbook execution.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.cancellation\_reason

</td><td>

The cancellation reason input by the user who cancelled the playbook execution.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors

</td><td>

List of cancellation errors. Each error is an object in the array.Data type: Array

 ```
"errors": [
    {      
      "message": "String",
      "type": "String"  
    }
]
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors.message

</td><td>

The error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.errors.type

</td><td>

The type of error.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.is\_archived

</td><td>

Flag that indicates whether playbook context records are archived. Set to true. This value can’t be modified.Possible values:

-   true: Playbook context records are archived.
-   false: Playbook context records aren’t archived.

Data type: Boolean

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.parent\_record

</td><td>

Sys\_id of the parent record that playbook executions were cancelled for.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.parent\_table

</td><td>

The name of the table that the parent record is from.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.playbook\_id

</td><td>

Sys\_id of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.playbook\_table

</td><td>

The name of the table that the playbook is from, generally the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.scoped\_name

</td><td>

The scoped name of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table in the format `scope.name`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.snapshot\_id

</td><td>

Sys\_id of the snapshot of the playbook execution from the \[sys\_pd\_snapshot\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state

</td><td>

The state of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: Object

 ```
"state": {    
   "displayValue": "String",    
   "value": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state.displayValue

</td><td>

The display value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.state.value

</td><td>

The value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.sys\_id

</td><td>

Sys\_id of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.title

</td><td>

The label of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.skippedPlaybookContext

</td><td>

List of the skipped playbook executions. Each playbook execution is an object in the array. For descriptions of the object properties, see the **canceledPlaybookContext** array. Data type: Array

 ```
"skippedPlaybookContext": [
    {
      "can_read": Boolean,
      "canceled_by": "String",
      "cancellation_reason": "String",
      "errors": [Array],
      "parent_record": "String",
      "parent_table": "String",
      "playbook_id": "String",
      "playbook_table": "String",
      "scoped_name": "String",
      "state": {Object},
      "sys_id": "String",
      "title": "String"   
    }
]
```

</td></tr><tr><td>

&lt;Object&gt;.canceledPlaybookContext.variant\_id

</td><td>

Sys\_id of the playbook variant execution from the Process Executions \[sys\_pd\_context\] table.

</td></tr></tbody>
</table>This example shows how to cancel all executions of a specific playbook \(in this case, the Playbook Experience Demo\) for a given interaction record. To use this method in a UI action or business rule, pass the `current` object as the parentRecord instead.

```
var parentRecord = new GlideRecordUtil().getGR("interaction", "d91742531b343010a26c98a1b24bcbe0");

var cancellationReason = "Cancelling this playbook";

// demo playbook from Process Automation Experience Demo store app
var scopedName = "sn_pad_demo.playbook_experience_demo"; 

// demo playbook experience from Process Automation Experience Demo store app
var playbookExperienceId = "a56d8d93ff311010cc0853ea793bf1a6"; 
	
var cancelPlaybookReturn = sn_playbook.PlaybookExperience.cancelPlaybooksByParentRecord(parentRecord, cancellationReason, scopedName, playbookExperienceId);
	

gs.info(JSON.stringify(cancelPlaybookReturn, null, 2));
```

Output:

```
{
  "canceledPlaybookContext": [
    {
      "can_read": true,
      "sys_id": "d02782533d343010ac50ee17e75d3466",
      "scoped_name": "sn_pad_demo.playbook_experience_demo",
      "canceled_by": "admin",
      "playbook_table": "sys_pd_process_definition",
      "state": {
        "displayValue": "Pending Cancel",
        "value": "PENDING_CANCEL"
      },
      "title": "Playbook Experience Demo",
      "parent_record": "d91742531b343010a26c98a1b24bcbe0",
      "playbook_id": "0d35ee1807301010cc08d9630ad3002a",
      "cancellation_reason": "Cancelling this playbook",
      "parent_table": "interaction",
      "errors": []
    }
  ],
  "skippedPlaybookContext": []
}
```

## PlaybookExperience - getPlaybooksForParentRecord\(GlideRecord parentRecord\)

Gets a list of playbook executions for a given parent record.

|Name|Type|Description|
|----|----|-----------|
|parentRecord|GlideRecord|The parent record to get playbook executions for. The parent record can be any record that can have playbook executions, such as an interaction record or an onboarding case record.|

<table id="table_jpb_gyn_cqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of playbook executions for the parent record. Each playbook execution is an object in the array.```
[
    {
      "can_read": Boolean,
      "canceled_by": "String",
      "cancellation_reason": "String",
      "errors": [Array],
      "parent_record": "String",
      "parent_table": "String",
      "playbook_id": "String",
      "playbook_table": "String",
      "scoped_name": "String",
      "state": {Object},
      "sys_id": "String",
      "title": "String"   
    }
]
```

</td></tr><tr><td>

&lt;Array&gt;.can\_read

</td><td>

Flag that indicates whether the current user can read the playbook execution record. The current user must have read access to the parent record to be able to read the playbook execution record.

 Valid values:

-   true: Current user has read access to the playbook execution record.
-   false: Current user doesn't have read access to the playbook execution record.

 Data type: Boolean

</td></tr><tr><td>

&lt;Array&gt;.canceled\_by

</td><td>

The **User ID** of the user who cancelled the playbook execution. Empty if the playbook is not cancelled.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.cancellation\_reason

</td><td>

The cancellation reason input by the user who cancelled the playbook execution. Empty if the playbook is not cancelled.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.errors

</td><td>

List of errors. Each error is an object in the array.Data type: Array

 ```
"errors": [
    {      
      "message": "String",
      "type": "String"  
    }
]
```

</td></tr><tr><td>

&lt;Array&gt;.errors.message

</td><td>

The error message.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.errors.type

</td><td>

The type of error.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.parent\_record

</td><td>

Sys\_id of the parent record.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.parent\_table

</td><td>

The name of the table that the parent record is from.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.playbook\_id

</td><td>

Sys\_id of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.playbook\_table

</td><td>

The name of the table that the playbook is from, generally the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.scoped\_name

</td><td>

The scoped name of the playbook from the Process Definitions \[sys\_pd\_process\_definition\] table in the format `scope.name`.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.state

</td><td>

The state of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: Object

 ```
"state": {    
   "displayValue": "String",    
   "value": "String"
}
```

</td></tr><tr><td>

&lt;Array&gt;.state.displayValue

</td><td>

The display value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.state.value

</td><td>

The value of the playbook execution state.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.sys\_id

</td><td>

Sys\_id of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.title

</td><td>

The label of the playbook execution from the Process Executions \[sys\_pd\_context\] table.Data type: String

</td></tr></tbody>
</table>This example shows how to get playbook executions for a given interaction record. To use this method in a UI action or business rule, pass the `current` object as the parentRecord instead.

```
var parentRecord = new GlideRecordUtil().getGR("interaction", "148776e5818d7410f87701eb89fdc824");
var playbook = sn_playbook.PlaybookExperience.getPlaybooksForParentRecord(parentRecord);
gs.info(JSON.stringify(playbook, null, 2));

```

Output:

```
[
  {
    "can_read": true,
    "sys_id": "bd87bae50b8d7410807a8ffed6d0909e",
    "scoped_name": "sn_pad_demo.playbook_experience_demo",
    "canceled_by": "",
    "playbook_table": "sys_pd_process_definition",
    "state": {
      "displayValue": "In Progress",
      "value": "IN_PROGRESS"
    },
    "title": "Playbook Experience Demo",
    "parent_record": "148776e5818d7410f87701eb89fdc824",
    "playbook_id": "0d35ee1807301010cc08d9630ad3002a",
    "cancellation_reason": "",
    "parent_table": "interaction",
    "errors": []
  }
]

```

## PlaybookExperience - parentRecordContainsPlaybook\(GlideRecord parentRecord, String scopedName\)

Checks whether a parent record has playbook executions.

|Name|Type|Description|
|----|----|-----------|
|parentRecord|GlideRecord|The parent record to check for playbook executions. The parent record can be any record that can have playbook executions, such as an interaction record or an onboarding case record.|
|scopedName|String|Optional. The scoped name of the playbook to check for. The scoped name is from the Process Definition \[sys\_pd\_process\_definition\] table in the format `scope.name`. If provided, only executions of this playbook are checked for. If not provided, executions of all playbooks are checked for.|

<table id="table_b4v_txn_cqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the parent record has playbook executions.

 Valid values:

-   true: Parent record has playbook executions.
-   false: Parent record doesn't have playbook executions.

</td></tr></tbody>
</table>This example shows how to check if a given interaction record has executions of a specific playbook \(in this case, the Playbook Experience Demo\). To use this method in a UI action or business rule, pass the `current` object as the parentRecord instead.

```
var parentRecord = new GlideRecordUtil().getGR("interaction", "148776e5818d7410f87701eb89fdc824");

// demo playbook from Process Automation Experience Demo store app
var scopedName = "sn_pad_demo.playbook_experience_demo"; 

var hasPlaybooks = sn_playbook.PlaybookExperience.parentRecordContainsPlaybook(parentRecord, scopedName);
gs.info(hasPlaybooks);
```

Output:

```
true
```

## PlaybookExperience - restartPlaybook\(GlideRecord playbookContext, String laneContextId, String activityContextId, String playbookExperienceId\)

Restarts an execution from the beginning \(the entire playbook\) or from a specific stage or activity of a playbook.

**Note:** Only playbooks that are In Progress, Queued, or Pending Cancel state can be restarted.

<table id="table_udh_zjr_ypb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

playbookContext

</td><td>

GlideRecord

</td><td>

The playbook context record for the playbook run or execution that you want to restart.Table: Process Execution \[sys\_pd\_context\]

</td></tr><tr><td>

laneContextId

</td><td>

String

</td><td>

Optional. The sys\_id of the stage context record for the stage run or execution that you want to restart from. **laneContextId** and **activityContextId** are mutually exclusive; only one of these values can be specified at a time, while the other should be either an empty string or null.

**Note:** Only complete stages can be restarted.

Table: Lane Executions \[sys\_pd\_lane\_context\]

</td></tr><tr><td>

activityContextId

</td><td>

String

</td><td>

Optional. The sys\_id of the activity context record for the activity run or execution that you want to restart from. **laneContextId** and **activityContextId** are mutually exclusive; only one of these values can be specified at a time, while the other should be either an empty string or null.

**Note:** Only complete activities can be restarted.

Table: Activity Executions \[sys\_pd\_activity\_context\]

</td></tr><tr><td>

playbookExperienceId

</td><td>

String

</td><td>

Optional. The sys\_id of the playbook experience that you want to use for the restarted run. Use this parameter if you have defined custom activity state mappings. See [Playbook activity state mapping](https://www.servicenow.com/docs/access?context=playbook-activity-state-mapping&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).Default: Global Playbook Experience

Table: Playbook Experience \[sys\_playbook\_experience\]

</td></tr></tbody>
</table><table id="table_vdh_zjr_ypb" class="returns"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the restarted playbook execution details.```
{
 "can_add_activity": Boolean,
 "can_cancel": Boolean,
 "can_read": Boolean
 "can_restart": Boolean,
 "canceled_by": "String",
 "cancellation_reason": "String",
 "errors": [Array]
 "is_archived": Boolean
 "parent_record": "String",
 "parent_table": "String",
 "playbook_id": "String",
 "playbook_table": "String",
 "scoped_name": "String",
 "state": {Object},
 "sys_id": "String",
 "title": "String",
}
```

</td></tr><tr><td>

can\_add\_activity

</td><td>

Flag that indicates whether a user can add an optional activity to the playbook.Valid values:

-   true: Current user can add an optional activity to the playbook.
-   false: Current user can’t add an optional activity to the playbook.

Data type: Boolean

</td></tr><tr><td>

can\_cancel

</td><td>

Flag that indicates whether a user can cancel a playbook.-   true: The process definition for the deactivated playbook is active.
-   false: The process definition for the deactivated playbook is inactive.

Data type: Boolean

</td></tr><tr><td>

can\_read

</td><td>

Flag that indicates whether the current user can read the playbook execution record. The current user must have read access to the parent record to be able to read the playbook execution record.-   true: Current user has read access to the playbook execution record.
-   false: Current user doesn't have read access to the playbook execution record.

Data type: Boolean

</td></tr><tr><td>

can\_restart

</td><td>

Flag that indicates whether a user can restart a playbook, stage, or activity.-   true: Current user can restart the playbook, stage, or activity.
-   false: Current user can’t restart the playbook, stage, or activity.

Data type: Boolean

</td></tr><tr><td>

canceled\_by

</td><td>

**User ID** of the user who canceled the playbook execution.Data type: String

</td></tr><tr><td>

cancellation\_reason

</td><td>

Cancellation reason entered by the user who canceled the playbook execution.Data type: String

</td></tr><tr><td>

errors

</td><td>

List of restart errors. Each error is an object in the array.Data type: Array

```
"errors": [
 {      
  "message": "String",
  "type": "String"  
 }
]
```

</td></tr><tr><td>

is\_archived

</td><td>

Flag that indicates whether playbook context records are archived.Possible values:

-   true: Playbook context records are archived.
-   false: Playbook context records aren’t archived.

Data type: Boolean

</td></tr><tr><td>

parent\_record

</td><td>

Sys\_id of the parent record that playbook executions were restarted for.Data type: String

</td></tr><tr><td>

parent\_table

</td><td>

Name of the table that the parent record is from.Data type: String

</td></tr><tr><td>

playbook\_id

</td><td>

Sys\_id of the playbook.Data type: String

Table: Process Definitions \[sys\_pd\_process\_definition\]

</td></tr><tr><td>

playbook\_table

</td><td>

Name of the table that the playbook is from, generally the Process Definitions \[sys\_pd\_process\_definition\] table.Data type: String

</td></tr><tr><td>

scoped\_name

</td><td>

Optional. The scoped name of the playbook to restart. The scoped name is from the Process Definition \[sys\_pd\_process\_definition\] table in the format `scope.name`. If provided, only executions of this playbook are restarted for the given parent record. If not provided, all executions of all playbooks are restarted for the given parent record.Data type: String

</td></tr><tr><td>

state

</td><td>

Indicates whether your request to activate was successful.Data type: Object

Possible values:

-   SUCCESS: The playbook was successfully activated.
-   FAILURE: The ID for the playbook wasn’t found.

```
"state": [
    {      
      "displayValue": "String",
      "value": "String"  
    }
]
```

</td></tr><tr><td>

state.displayValue

</td><td>

Display value of the playbook execution state.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Value of the playbook execution state.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the playbook execution.Data type: String

Table: Process Executions \[sys\_pd\_context\]

</td></tr><tr><td>

title

</td><td>

Label of the playbook execution.Data type: String

Table: Process Executions \[sys\_pd\_context\]

</td></tr></tbody>
</table>This example shows how to restart an entire playbook run with the Process Executions \[sys\_pd\_context\] record ID 98e4fe04591b4caca59583f7b8e30b0a.

```
var gr = new GlideRecord('sys_pd_context');
var found = gr.get('98e4fe04591b4caca59583f7b8e30b0a'); 
if (found) {
    var result = sn_playbook.PlaybookExperience.restartPlaybook(gr);
    gs.info(JSON.stringify(result));
}
else
    gs.info('invalid pd context');
```

Output:

```
{
 "scoped_name": "global.restart_scriptable_demo",
 "canceled_by": "",
 "can_add_activity": true,
 "playbook_table": "sys_pd_process_definition",
 "can_restart": true,
 "can_cancel": true,
 "title": "Restart scriptable demo",
 "cancellation_reason": "",
 "parent_table": "interaction",
 "can_read": true,
 "sys_id": "98e4fe04591b4caca59583f7b8e30b0a",
 "is_archived": false,
 "state": {
   "displayValue": "In Progress",
   "value": "IN_PROGRESS"
 },
 "parent_record": "b88623beb5e10210f877d783f6f83a46",
 "playbook_id": "12d5a7fab5e10210f877d783f6f83aff",
 "errors": []
}
```

## PlaybookExperience - triggerPlaybook\(String scopedName, GlideRecord parentRecord\)

Initiates a playbook for a parent record.

|Name|Type|Description|
|----|----|-----------|
|scopedName|String|The scoped name of the playbook to initiate. The scoped name is from the Process Definition \[sys\_pd\_process\_definition\] table in the format `scope.name`.|
|parentRecord|GlideRecord|The parent record to initiate a playbook for. The parent record can be any record that can have playbook executions, such as an interaction record or an onboarding case record.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the playbook execution from the Process Executions \[sys\_pd\_context\] table that was created for the parent record. Null if a playbook execution wasn't successfully created.|

This example shows how to initiate a playbook for a given interaction record. To use this method in a UI action or business rule, pass the `current` object as the parentRecord instead.

```
var parentRecord = new GlideRecordUtil().getGR("interaction", "148776e5818d7410f87701eb89fdc824");

// demo playbook from Process Automation Experience Demo store app
var scopedName = "sn_pad_demo.playbook_experience_demo"; 

var playbookExecution = sn_playbook.PlaybookExperience.triggerPlaybook(scopedName, parentRecord);
gs.info(playbookExecution);

```

Output:

```
f059958267cdb410952864f0fed358cc
```

