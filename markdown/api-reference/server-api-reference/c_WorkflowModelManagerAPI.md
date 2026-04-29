---
title: WorkflowModelManager - Global
description: The WorkflowModelManager script include provides methods to query the workflow model, to step backwards and forwards between specified workflow history items, and to query the history for activity and transition-specific information.Creates a new WorkflowModelManager object \(constructor\) within the specified context.Retrieves the history activity that is cached by the wf\_history.sys\_id provided in the argument.Retrieves the history activities that executed and transitioned into the one represented by the sys\_id in the argument.Retrieves the history activities that executed and transitioned into the one represented by the sys\_id in the argument. The next status is based on the wf\_activity.sys\_id associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that executed in the workflow's history. \(This differs from getPreviousByTransition, which returns only TO transitions that come before the haRecord in the execution sequence \(by time\).\) The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity.This is the worker method that must be called to initialize the WorkflowModelManager object. In the process of initializing the WorkflowModelManager object, getExecutedHistory\(\) creates and populates the activityHistoryRecord data object array \(which is a member of the WorkflowModelManager class\). Most WorkflowModelManager methods return a subset of the activityHistoryRecord array. Your script can then call one or more of the activityHistoryRecord methods to accomplish further work.Queries the wf\_history table by context and retrieves all the activities executed in the workflow given by the context set in the construction of this object.Gets the list of wf\_history.sys\_ids of all activities that successfully executed and were not rolled back or skipped up to the moment the function was called.Retrieves the history activity that executed just after the one provided in the argument.Retrieves the history activity that is cached by the wf\_history.sys\_id provided in the argument and then calls into getNextByExecutedOrder\(\) with the retrieved JavaScript object.Retrieves the history activity that executed just after the one identified by the sys\_id provided in the argument.Retrieves the history activity that executed just previous to the one provided in the argument.Retrieves the history activity cached by the wf\_history.sys\_id provided in the argument, then calls getPreviousByExecutedOrder\(\) with the retrieved JavaScript object.Retrieves the history activities that executed just prior to the one provided in the argument.Retrieves the history activities that executed just prior to the one provided in the argument.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WorkflowModelManager- Global

The WorkflowModelManager script include provides methods to query the workflow model, to step backwards and forwards between specified workflow history items, and to query the history for activity and transition-specific information.

The interaction with the WorkflowModelManager script include is through the ActivityHistoryRecord data object. The ActivityHistoryRecord object is an inner class and is only used while interacting with WorkflowModelManager.

To acquire the executed history of the workflow activities:

```
var model = new WorkflowModelManager('myContextId');
var activities = model.getExecutedHistory();

```

To output the playback of the workflow:

```
var model = new WorkflowModelManager('myContextId');
model.getExecutedHistory();
model.playBack();

```

At this time, the playBack is required to load the executed transitions. This will also play a role in walking backwards on a model to rollback to a specific activity.

To see the details of the cached model:

```
var model = new WorkflowModelManager('myContextId');
 model.getExecutedHistory();
 model.dump();
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[WFActivityHandler - Global](../../WFACtivityHandler/concept/c_WFACtivityHandlerAPI.md#)

## WorkflowModelManager - WorkflowModelManager\(String contextId\)

Creates a new WorkflowModelManager object \(constructor\) within the specified context.

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The ID for the context in which you want the WorkflowModelManager created.|

|Type|Description|
|----|-----------|
|ActivityHistoryRecord|The ActivityHistoryRecord JavaScript object requested.|

```
var model = new WorkflowModelManager('MyContextId');
```

## WorkflowModelManager - getActivityHistoryRecordById\(String haRecordSysId\)

Retrieves the history activity that is cached by the **wf\_history.sys\_id** provided in the argument.

|Name|Type|Description|
|----|----|-----------|
|haRecordSysId|String|Sys\_id of the desired Activity History \[wf\_history\] record.|

|Type|Description|
|----|-----------|
|ActivityHistoryRecord|Requested ActivityHistoryRecord JavaScript object.|

This example shows how to use the method to obtain the specified history activity record.

```
var model = new WorkflowModelManager('a71efa6345550110a86630cf9552f3af');  // The sys_id of the wf_context
model.getExecutedHistory();
var current_hist_obj = model.getActivityHistoryRecordById('2b1efa6345550110a86630cf9552f3bc'); // The sys_id of the desired record
gs.info(JSON.stringify(current_hist_obj));
```

Output:

```

{
   "sys_id":"2b1efa6345550110a86630cf9552f3bc",
   "index":"3",
   "startTime":1643795456000,
   "endTime":1643795456000,
   "wfaId":"31bf2a05e7c133009a610558d2f6a968",
   "wfaIsParent":{
     
   },
   "parent":"",
   "wfaName":{
     
   },
   "adId":"db8c65aec0a8016501d00259bc7203a4",
   "adName":{
     
   },
   "transitions":[
      {
         "sys_id":"e31efa6345550110a86630cf9552f3c0",
         "ahrId":"2b1efa6345550110a86630cf9552f3bc",
         "to":"39bf2a05e7c133009a610558d2f6a970",
         "from":"31bf2a05e7c133009a610558d2f6a968",
         "rolledBack":"false",
         "rolledBackBy":""
      },
      {
         "sys_id":"e71efa6345550110a86630cf9552f3c0",
         "ahrId":"2b1efa6345550110a86630cf9552f3bc",
         "to":"7dbf2a05e7c133009a610558d2f6a96b",
         "from":"31bf2a05e7c133009a610558d2f6a968",
         "rolledBack":"false",
         "rolledBackBy":""
      }
   ],
   "rolledBackBy":"",
   "ARRIVED":true,
   "NOT_ARRIVED":false,
   "joinFroms":[
     
   ],
   "joinSatisfied":false,
   "rollingBackBy":0
}
```

## WorkflowModelManager - getAllTransitionedIntoActivity\(Object description\)

Retrieves the history activities that executed and transitioned into the one represented by the **sys\_id** in the argument.

The **next** status is based on the **wf\_activity.sys\_id** associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that executed in the workflow's history. \(This differs from getPreviousByTransition, which only returns TO transitions that come before the haRecord in the execution sequence \(by time\).\) The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity. The return values are based on all transitions in the executed history collection that transition To get the activity that executed prior to this activity in time use getPreviousByExecutedOrder.

|Name|Type|Description|
|----|----|-----------|
|description|Object|ActivityHistoryRecord JavaScript object.|

|Type|Description|
|----|-----------|
|Object Array|Array of ActivityHistoryRecord JavaScript objects.|

## WorkflowModelManager - getAllTransitionedIntoActivityId\(String haRecordSysId\)

Retrieves the history activities that executed and transitioned into the one represented by the **sys\_id** in the argument. The **next** status is based on the **wf\_activity.sys\_id** associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that executed in the workflow's history. \(This differs from getPreviousByTransition, which returns only TO transitions that come before the haRecord in the execution sequence \(by time\).\) The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity.

The **next** status is based on the **wf\_activity.sys\_id** associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that executed in the workflow's history. \(This differs from getPreviousByTransition, which returns only TO transitions that come before the haRecord in the execution sequence \(by time\).\) The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity.

|Name|Type|Description|
|----|----|-----------|
|haRecordSysId|String|The sys\_id of the activity history \(table wf\_history\).|

|Type|Description|
|----|-----------|
|Object Array|Array of ActivityHistoryRecord JavaScript objects requested.|

```
var model = new WorkflowModelManager('a143585c3b001000dada82c09ccf3d44');
      model.getExecutedHistory();
      var activity = model.begin;
      gs.print('activity: ' + activity.wfaName + ', transitions: ' + activity.transitions.length);
      while( activity != null){    
          gs.print('activity: ' + activity.wfaName + ', transitions: ' + activity.transitions.length);    
          var parents = model.getAllTransitionedIntoActivity(activity);
          for( var i = 0; i < parents.length; i++ ){
              gs.print(' ---------------  parent activity: ' + parents[i].wfaName );
            }
           activity = model.getNextByExecutedOrder( activity );
      }
    
```

## WorkflowModelManager - getExecutedHistory\( \)

This is the worker method that must be called to initialize the WorkflowModelManager object. In the process of initializing the WorkflowModelManager object, getExecutedHistory\(\) creates and populates the activityHistoryRecord data object array \(which is a member of the WorkflowModelManager class\). Most WorkflowModelManager methods return a subset of the activityHistoryRecord array. Your script can then call one or more of the activityHistoryRecord methods to accomplish further work.



|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String Array|An ordered array of sys\_ids from table wf\_history. It is unlikely client code would use the return value; it is kept internally to this object for use by subsequent method calls.|

```
var model = new WorkflowModelManager('myContextId');
var activities = model.getExecutedHistory();
var current = model.getActivityHistoryRecordById('d6681d573b130000dada82c09ccf3d10');
```

## WorkflowModelManager - getFinalExecutedActivityList\( \)

Queries the wf\_history table by context and retrieves all the activities executed in the workflow given by the context set in the construction of this object.

This function produces a list of executed activities in the exact order each activity passed through the server side ActivityManager.java using the new activity\_index to force the order coming out of the database. On its this call will not give the full picture; it needs to load and map the transitions.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object Array|Array of ActivityHistoryRecord javascript objects.|

## WorkflowModelManager - getFinalExecutedActivityIdList\( \)

Gets the list of **wf\_history.sys\_ids** of all activities that successfully executed and were not rolled back or skipped up to the moment the function was called.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String Array|Array of wf\_history.sys\_id values for executed activities.|

```
var model = new WorkflowModelManager('ee3e0a053b101000dada82c09ccf3d7c');
      model.getExecutedHistory();
      var finals = model.getFinalExecutedActivityIdList();
      gs.print(' EXECUTION PATH IDs --------------- : '  + finals.length);
      
      for ( var x = 0; x < finals.length; x++ ) {
          gs.print(finals[x] );
      }
```

## WorkflowModelManager - getNextByExecutedOrder\(Object haRecord\)

Retrieves the history activity that executed just after the one provided in the argument.

The **next** status is based on the activity index reflecting the nearest prior activity in time, and not necessarily the nearest next wf\_activity that the provided activity transitioned to. To get the nearest next activity that transitioned to this haRecord passed in, use getNextByTransitionOrder\(haRecord\).

**Note:** In the process of assembling the execution order array, blanks are left in the array where history objects have been deleted. This is done to ensure the index in the array and the activity\_index of the object remain in synch. For that reason, all objects coming out of the execution order array should be tested for nil\(\) and not assumed to be the previous record based on activity\_index or array index value alone.

|Name|Type|Description|
|----|----|-----------|
|haRecord|Object|ActivityHistoryRecord JavaScript object.|

|Type|Description|
|----|-----------|
|Object|The requested ActivityHistoryRecord JavaScript object.|

The following example shows how to use the getNextByExecutedOrder\(\) method to retrieve the history activity that executed after the specified activity.

```
var model = new WorkflowModelManager('34451ec2cb200200d71cb9c0c24c9c66'); // Sys_id of the workflow context
model.getExecutedHistory();
var current_hist_obj = model.getActivityHistoryRecordById('0199483adba52200a6a2b31be0b8f562');// Sys_id of the current activity from wf_history table
var next_hist_obj = model.getNextByExecutedOrder(current_hist_obj);
gs.info(JSON.stringify(next_hist_obj));
```

Output:

```
{
   "sys_id":"b2c5a06e07e0011094b4fe4f7c1ed049",
   "index":"3",
   "startTime":1640265864000,
   "endTime":1640265864000,
   "wfaId":"64d4e4aa07e0011094b4fe4f7c1ed060",
   "wfaIsParent":{
     
   },
   "parent":"",
   "wfaName":{
     
   },
   "adId":"1ca8d7cf0a0a0b265e9a000c2c08248c",
   "adName":{
     
   },
   "transitions":[
      {
         "sys_id":"bac5a06e07e0011094b4fe4f7c1ed07d",
         "ahrId":"b2c5a06e07e0011094b4fe4f7c1ed049",
         "to":"e0d4acaa07e0011094b4fe4f7c1ed062",
         "from":"64d4e4aa07e0011094b4fe4f7c1ed060",
         "rolledBack":"false",
         "rolledBackBy":""
      }
   ],
   "rolledBackBy":"",
   "ARRIVED":true,
   "NOT_ARRIVED":false,
   "joinFroms":[
     
   ],
   "joinSatisfied":false,
   "rollingBackBy":0
}

```

## WorkflowModelManager - getNextByExecutedOrderId\(String haRecordSysId\)

Retrieves the history activity that is cached by the **wf\_history.sys\_id** provided in the argument and then calls into getNextByExecutedOrder\(\) with the retrieved JavaScript object.

|Name|Type|Description|
|----|----|-----------|
|haRecordSysId|String|The sys\_id of the activity history \(table wf\_history\).|

|Type|Description|
|----|-----------|
|Object|The ActivityHistoryRecord JavaScript object requested.|

```
var model = new WorkflowModelManager('7b3e01573b130000dada82c09ccf3dcf');
      model.getExecutedHistory();
      var current = model.getActivityHistoryRecordById('d6681d573b130000dada82c09ccf3d10');
      current.debugDump();
      
      var results = model.getNextByExecutedOrderId(current.sys_id);
      results.debugDump();
```

## WorkflowModelManager - getNextByTransitionId\(String haRecordSysId\)

Retrieves the history activity that executed just after the one identified by the sys\_id provided in the argument.

This function retreives the cached history record associated with the provided **wf\_history.sys\_id** and then calls getNextByTransition. The return values are based on which transitions came before the **haRecord** submitted and not necessarily the activities that executed just prior to the **haRecord** in time. To get the activity that executed prior to this activity in time, use getNextByExecutedOrder.

|Name|Type|Description|
|----|----|-----------|
|haRecordSysId|String|Sys\_id of the desired Activity History \[wf\_history\] record.|

|Type|Description|
|----|-----------|
|Object Array|Array of ActivityHistoryRecord JavaScript objects.|

```
var model = new WorkflowModelManager('7b3e01573b130000dada82c09ccf3dcf');
model.getExecutedHistory();
model.playBack();
      
var current = model.getActivityHistoryRecordById('d6681d573b130000dada82c09ccf3d10');
current.debugDump();
var results = model.getNextByTransitionId(current.sys_id);
gs.print('COMPLETED NEXT' + results.length );
for(var i = 0; i < results.length; i++){
  results[i].debugDump();
}
```

## WorkflowModelManager - getPreviousByExecutedOrder\(Object haRecord\)

Retrieves the history activity that executed just previous to the one provided in the argument.

The **previous** status is based on the activity index reflecting the nearest prior activity in time and not necessarily the nearest prior activity with a valid transition to this activity. To get the nearest prior activity that transitioned to this haRecord passed in use getPreviousByTransition\( haRecord\).

**Note:** In the process of assembling the execution order array, blanks are left in the array where history objects have been deleted. This ensures that the index in the array and the activity\_index of the object remain in sync. For that reason, all objects coming out of the execution order array should be tested for nil\(\) and not assumed to be the previous record based on activity\_index or array index value.

|Name|Type|Description|
|----|----|-----------|
|haRecord|Object|ActivityHistoryRecord JavaScript object|

|Type|Description|
|----|-----------|
|Object|The ActivityHistoryRecord JavaScript object requested.|

## WorkflowModelManager - getPreviousByExecutedOrderId\(String haRecordSysId\)

Retrieves the history activity cached by the **wf\_history.sys\_id** provided in the argument, then calls getPreviousByExecutedOrder\(\) with the retrieved JavaScript object.

|Name|Type|Description|
|----|----|-----------|
|haRecordSysId|String|Workflow history system ID \(wf\_history.sys\_id\)|

|Type|Description|
|----|-----------|
|ActivityHistoryRecord|The ActivityHistoryRecord JavaScript object requested.|

```
var model = new WorkflowModelManager('contextId');
      model.getExecutedHistory();
      var current = model.getActivityHistoryRecordById('wf_history.sys_id');
      current.debugDump();
      
      var results = model.getPreviousByExecutedOrderId(current.sys_id);
      results.debugDump();
```

## WorkflowModelManager - getPreviousByTransition\(Object haRecord\)

Retrieves the history activities that executed just prior to the one provided in the argument.

The **next** status is based on the wf\_activity.sys\_id associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that come before the haRecord in the execution sequence. \(This differs from getAllTransitionedIntoActivity, which returns all TO transitions up to the given haRecord in the execution sequence .\) The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity. The return values are based on which transitions came before the haRecord submitted and not necessarily the activities that executed just prior to the haRecord in time. To get the activity that executed prior to this activity in time, use getPreviousByExecutedOrder.

|Name|Type|Description|
|----|----|-----------|
|haRecord|Object|ActivityHistoryRecord JavaScript object.|

|Type|Description|
|----|-----------|
|Object Array|Array of ActivityHistoryRecord JavaScript objects requested.|

## WorkflowModelManager - getPreviousByTransitionId\(String haRecordSysId\)

Retrieves the history activities that executed just prior to the one provided in the argument.

The **next** status is based on the **wf\_activity.sys\_id** associated with the activity represented in the haRecord existing as a TO in a transition associated with any ActivityHistoryRecords that come before the haRecord in the execution sequence. The return value is a collection of ActivityHistoryRecords that identify the argument haRecord.wfaId as their TO activity. The return values are based on which transitions came before the haRecord sumbitted and not necessarily the activities that executed just prior to the haRecord in time. To get the activity that executed prior to this activity in time use getPreviousByExecutedOrder\(\).

<table id="table_jnc_hqq_rt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

haRecordSysId

</td><td>

String

</td><td>

Sys\_id of the activity history.Table: WorkFlow History \[wf\_history\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Array of ActivityHistoryRecord JavaScript objects requested.|

The following example shows how to use the getPreviousByTransitionId\(\) method to obtain ActivityHistoryRecord objects.

```
var w_history = new GlideRecord('wf_history');
w_history.addQuery('context.id', '089ebdad1b420110c97a40c6cc4bcbf7'); // Pass sys_id of record -> Requested Item / Change Request / Request, etc....
w_history.query();
if (w_history.next()) {
    var model = new WorkflowModelManager(w_history.context); // Call sys_id of the workflow context
    model.getExecutedHistory();
    var previousObje_hist_obj = model.getPreviousByTransitionId(w_history.sys_id); // Sys_id of wf_history table
    gs.info(JSON.stringify(previousObje_hist_obj));
}
```

Output:

```
[
  {
    "sys_id": "a40a92950721011094b4fe4f7c1ed05e",
    "index": "1",
    "startTime": 1644255752000,
    "endTime": 1644255758000,
    "wfaId": "28200e2a77873300b473455caa1061cd",
    "wfaIsParent": {},
    "parent": "",
    "wfaName": {},
    "adId": "3961a1da0a0a0b5c00ecd84822f70d85",
    "adName": {},
    "transitions": [
      {
        "sys_id": "060ad6950721011094b4fe4f7c1ed016",
        "ahrId": "a40a92950721011094b4fe4f7c1ed05e",
        "to": "24204e2a77873300b473455caa10611a",
        "from": "28200e2a77873300b473455caa1061cd",
        "rolledBack": "false",
        "rolledBackBy": ""
      }
    ],
    "rolledBackBy": "",
    "ARRIVED": true,
    "NOT_ARRIVED": false,
    "joinFroms": [],
    "joinSatisfied": false,
    "rollingBackBy": 0
  }
]
```

