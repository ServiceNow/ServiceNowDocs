---
title: ActivityHistoryRecord - Global
description: The ActivityHistoryRecord API provides methods that facilitate interacting with a WorkflowModelManager object. It is a data object that is a member of the WorkflowModelManager class.Changes the arrivedState of already known ids to true.Seeds all the expected wf\_activity sys\_ids that are expected to pass through this join and sets their arriveState = false.As model is cached by \_getExecutedTransitions\(\), this method adds transitions that have gone FROM this activity towards the .to activity.Prints debug information.Tests the incoming wf\_activity sys\_id, presumed to be seeded in this history record. If it is, it is tested to see if it is an activity that would come through this join.Returns the log string from the history record.Returns the sys\_ids of the history records that transition to this Join activity that have already come through.Returns the transition count for this activity.Returns the sys\_ids of the history records that transition to this Join activity that the join is still waiting for.Determines if this activity is one of the rollback activities.Determines if the sys\_id passed in is a destination of any of the transitions associated with this instance of an ActivityHistoryRecord.Determines if this activity is a join.Examines the value of the arriveState.Tests the incoming wf\_activity sys\_id, presumed to be seeded in this history record.Determines if this workflow was rolled back.Determines if the current activity is a turnstile.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 21
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ActivityHistoryRecord- Global

The ActivityHistoryRecord API provides methods that facilitate interacting with a WorkflowModelManager object. It is a data object that is a member of the WorkflowModelManager class.

This API is basically a copy of the data from a glide record on the table Activity History \[wf\_history\]. There are some helper methods defined for this class as well. There are no accessors or mutator to the simple data elements of this class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ActivityHistoryRecord - addArrivedActivityToJoin\(String Array activityIds\)

Changes the **arrivedState** of already known ids to **true**.

As soon as this method changes the **arrivedState** of known ids to **true**, it tests to see if the join is satisfied. if it is, the model walk can continue; if not, it should continue to next appropriate transition. This is called during playback, as expected wf\_activities flow to the join.

|Name|Type|Description|
|----|----|-----------|
|activityIds|String Array|Array of wf\_activity.sys\_ids that are headed towards join.|

|Type|Description|
|----|-----------|
|void| |

## ActivityHistoryRecord - addJoinFromActivityIds\(String Array activityIds\)

Seeds all the expected wf\_activity sys\_ids that are expected to pass through this join and sets their arriveState = false.

This state is flipped to **true** as each expected activity transitions to this instance of the Join. This method is called as part of building the cached model in memory, and is not called during playback.

|Name|Type|Description|
|----|----|-----------|
|activityIds|String Array|Array of wf\_activity.sys\_ids that are headed towards join.|

|Type|Description|
|----|-----------|
|void| |

## ActivityHistoryRecord - addTransition\(Object InTransition\)

As model is cached by \_getExecutedTransitions\(\), this method adds transitions that have gone FROM this activity towards the .to activity.

|Name|Type|Description|
|----|----|-----------|
|InTransition|Object|ExecutedTransition Javascript object to add to this activity.|

|Type|Description|
|----|-----------|
|void| |

## ActivityHistoryRecord - debugDump\( \)

Prints debug information.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to use this method. It uses the oldest workflow history records of a base instance.

```
// These are associated with the Change Request - Normal workflow for CHG0000037.
var wfhGR = new GlideRecord ('wf_history');
wfhGR.addQuery('context.id', '41cdb152db252200a6a2b31be0b8f527');
wfhGR.addQuery('context.table', 'change_request');
wfhGR.orderBy ('activity_index');
wfhGR.query();
while (wfhGR.next())  {
  var script_name = 'AHR';
  //
  //  Acquire the execution history of the workflow's activities.
  //  Do this just once while processing the first activity.

  if(wfhGR.activity_index == 0) {
    var model = new WorkflowModelManager( wfhGR.context );
    model.getExecutedHistory();
  }

//
// Access a hash of ActivityHistoryRecord javascript objects,
// hashed by the sys_id of the wf_history record.
// There will be one ActivityHistoryRecord for each activity.

  var ActivityHistoryRecord = model.getActivityHistoryRecordById(wfhGR.sys_id);

//
// Use ActivityHistoryRecord methods to display selected values

  gs.log('Log String [' + ActivityHistoryRecord.getLogString() + ']', script_name);
  gs.log('debugDump START', script_name);
  ActivityHistoryRecord.debugDump();
  gs.log('debugDump END', script_name);
  gs.log('Turnstile?[' + ActivityHistoryRecord.isTurnstile() + ']', script_name);
  gs.log('Transition Count[' + ActivityHistoryRecord.getTransitionCount() + ']\n', script_name );
}
```

Output:

```
[0:00:00.133] Script completed in scope global: script
Script execution history and recovery available here
AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57a  History INDEX:0  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:e233b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Begin  WF Activity DEF ID:c7a5e32c0a0a0b3a002377c24ed8ea76  WF Activity DEF NAME:Begin  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57a
*** Script:        History INDEX: 0
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 0
*** Script:       WF Activity ID: e233b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Begin
*** Script:   WF Activity DEF ID: c7a5e32c0a0a0b3a002377c24ed8ea76
*** Script: WF Activity DEF NAME: Begin
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57d  History INDEX:1  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:2e33b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Change moves to Assess  WF Activity DEF ID:d93a02ae0a0a0aa30077abad3fdac035  WF Activity DEF NAME:Wait for condition  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57d
*** Script:        History INDEX: 1
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 1
*** Script:       WF Activity ID: 2e33b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Change moves to Assess
*** Script:   WF Activity DEF ID: d93a02ae0a0a0aa30077abad3fdac035
*** Script: WF Activity DEF NAME: Wait for condition
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:3e28c4b6dba52200a6a2b31be0b8f57e  History INDEX:2  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:6e33b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Requested  WF Activity DEF ID:50a78fa50a6a803f66d064255f7201a5  WF Activity DEF NAME:Approval Action  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 3e28c4b6dba52200a6a2b31be0b8f57e
*** Script:        History INDEX: 2
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 2
*** Script:       WF Activity ID: 6e33b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Requested
*** Script:   WF Activity DEF ID: 50a78fa50a6a803f66d064255f7201a5
*** Script: WF Activity DEF NAME: Approval Action
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:0d38c4b6dba52200a6a2b31be0b8f5cc  History INDEX:3  History START TIME:1585659881000  History END TIME:1585659891000  WF Activity ID:2a33b949cb020200d71cb9c0c24c9c26  WF Activity NAME:Technical approvals  WF Activity DEF ID:354e911f0a0a029a00e6a0e6ad74206f  WF Activity DEF NAME:Approval - Group  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 0d38c4b6dba52200a6a2b31be0b8f5cc
*** Script:        History INDEX: 3
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 3
*** Script:       WF Activity ID: 2a33b949cb020200d71cb9c0c24c9c26
*** Script:     WF Activity NAME: Technical approvals
*** Script:   WF Activity DEF ID: 354e911f0a0a029a00e6a0e6ad74206f
*** Script: WF Activity DEF NAME: Approval - Group
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:c538c4b6dba52200a6a2b31be0b8f5ce  History INDEX:4  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:6233b949cb020200d71cb9c0c24c9c5b  WF Activity NAME:Check if Change is "On hold"  WF Activity DEF ID:98f621ca0a0a0b5900f7c291f5e45a0e  WF Activity DEF NAME:If  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: c538c4b6dba52200a6a2b31be0b8f5ce
*** Script:        History INDEX: 4
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 4
*** Script:       WF Activity ID: 6233b949cb020200d71cb9c0c24c9c5b
*** Script:     WF Activity NAME: Check if Change is "On hold"
*** Script:   WF Activity DEF ID: 98f621ca0a0a0b5900f7c291f5e45a0e
*** Script: WF Activity DEF NAME: If
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:cd3808b6dba52200a6a2b31be0b8f501  History INDEX:5  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:e633b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Move to Authorize  WF Activity DEF ID:1ca8d7cf0a0a0b265e9a000c2c08248c  WF Activity DEF NAME:Set Values  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: cd3808b6dba52200a6a2b31be0b8f501
*** Script:        History INDEX: 5
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 5
*** Script:       WF Activity ID: e633b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Move to Authorize
*** Script:   WF Activity DEF ID: 1ca8d7cf0a0a0b265e9a000c2c08248c
*** Script: WF Activity DEF NAME: Set Values
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]

```

## ActivityHistoryRecord - doesJoinContainActivity\( \)

Tests the incoming wf\_activity sys\_id, presumed to be seeded in this history record. If it is, it is tested to see if it is an activity that would come through this join.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True, if it is an activity that would come through this join.|

## ActivityHistoryRecord - getLogString\( \)

Returns the log string from the history record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The log string.|

The following code example shows how to use this method. It uses the oldest workflow history records of a base instance.

```
// These are associated with the Change Request - Normal workflow for CHG0000037.
var wfhGR = new GlideRecord ('wf_history');
wfhGR.addQuery('context.id', '41cdb152db252200a6a2b31be0b8f527');
wfhGR.addQuery('context.table', 'change_request');
wfhGR.orderBy ('activity_index');
wfhGR.query();
while (wfhGR.next())  {
  var script_name = 'AHR';
  //
  //  Acquire the execution history of the workflow's activities.
  //  Do this just once while processing the first activity.

  if(wfhGR.activity_index == 0) {
    var model = new WorkflowModelManager( wfhGR.context );
    model.getExecutedHistory();
  }

//
// Access a hash of ActivityHistoryRecord javascript objects,
// hashed by the sys_id of the wf_history record.
// There will be one ActivityHistoryRecord for each activity.

  var ActivityHistoryRecord = model.getActivityHistoryRecordById(wfhGR.sys_id);

//
// Use ActivityHistoryRecord methods to display selected values

  gs.log('Log String [' + ActivityHistoryRecord.getLogString() + ']', script_name);
  gs.log('debugDump START', script_name);
  ActivityHistoryRecord.debugDump();
  gs.log('debugDump END', script_name);
  gs.log('Turnstile?[' + ActivityHistoryRecord.isTurnstile() + ']', script_name);
  gs.log('Transition Count[' + ActivityHistoryRecord.getTransitionCount() + ']\n', script_name );
}
```

Output:

```
[0:00:00.133] Script completed in scope global: script
Script execution history and recovery available here
AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57a  History INDEX:0  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:e233b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Begin  WF Activity DEF ID:c7a5e32c0a0a0b3a002377c24ed8ea76  WF Activity DEF NAME:Begin  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57a
*** Script:        History INDEX: 0
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 0
*** Script:       WF Activity ID: e233b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Begin
*** Script:   WF Activity DEF ID: c7a5e32c0a0a0b3a002377c24ed8ea76
*** Script: WF Activity DEF NAME: Begin
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57d  History INDEX:1  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:2e33b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Change moves to Assess  WF Activity DEF ID:d93a02ae0a0a0aa30077abad3fdac035  WF Activity DEF NAME:Wait for condition  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57d
*** Script:        History INDEX: 1
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 1
*** Script:       WF Activity ID: 2e33b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Change moves to Assess
*** Script:   WF Activity DEF ID: d93a02ae0a0a0aa30077abad3fdac035
*** Script: WF Activity DEF NAME: Wait for condition
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:3e28c4b6dba52200a6a2b31be0b8f57e  History INDEX:2  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:6e33b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Requested  WF Activity DEF ID:50a78fa50a6a803f66d064255f7201a5  WF Activity DEF NAME:Approval Action  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 3e28c4b6dba52200a6a2b31be0b8f57e
*** Script:        History INDEX: 2
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 2
*** Script:       WF Activity ID: 6e33b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Requested
*** Script:   WF Activity DEF ID: 50a78fa50a6a803f66d064255f7201a5
*** Script: WF Activity DEF NAME: Approval Action
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:0d38c4b6dba52200a6a2b31be0b8f5cc  History INDEX:3  History START TIME:1585659881000  History END TIME:1585659891000  WF Activity ID:2a33b949cb020200d71cb9c0c24c9c26  WF Activity NAME:Technical approvals  WF Activity DEF ID:354e911f0a0a029a00e6a0e6ad74206f  WF Activity DEF NAME:Approval - Group  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 0d38c4b6dba52200a6a2b31be0b8f5cc
*** Script:        History INDEX: 3
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 3
*** Script:       WF Activity ID: 2a33b949cb020200d71cb9c0c24c9c26
*** Script:     WF Activity NAME: Technical approvals
*** Script:   WF Activity DEF ID: 354e911f0a0a029a00e6a0e6ad74206f
*** Script: WF Activity DEF NAME: Approval - Group
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:c538c4b6dba52200a6a2b31be0b8f5ce  History INDEX:4  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:6233b949cb020200d71cb9c0c24c9c5b  WF Activity NAME:Check if Change is "On hold"  WF Activity DEF ID:98f621ca0a0a0b5900f7c291f5e45a0e  WF Activity DEF NAME:If  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: c538c4b6dba52200a6a2b31be0b8f5ce
*** Script:        History INDEX: 4
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 4
*** Script:       WF Activity ID: 6233b949cb020200d71cb9c0c24c9c5b
*** Script:     WF Activity NAME: Check if Change is "On hold"
*** Script:   WF Activity DEF ID: 98f621ca0a0a0b5900f7c291f5e45a0e
*** Script: WF Activity DEF NAME: If
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:cd3808b6dba52200a6a2b31be0b8f501  History INDEX:5  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:e633b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Move to Authorize  WF Activity DEF ID:1ca8d7cf0a0a0b265e9a000c2c08248c  WF Activity DEF NAME:Set Values  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: cd3808b6dba52200a6a2b31be0b8f501
*** Script:        History INDEX: 5
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 5
*** Script:       WF Activity ID: e633b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Move to Authorize
*** Script:   WF Activity DEF ID: 1ca8d7cf0a0a0b265e9a000c2c08248c
*** Script: WF Activity DEF NAME: Set Values
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]

```

## ActivityHistoryRecord - getSatisfiedJoinActivities\( \)

Returns the sys\_ids of the history records that transition to this Join activity that have already come through.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String Array|Array of sys\_ids of the history records that transition to this Join activity.|

## ActivityHistoryRecord - getTransitionCount\( \)

Returns the transition count for this activity.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of transitions from this activity.|

The following code example shows how to use this method. It uses the oldest workflow history records of a base instance.

```
// These are associated with the Change Request - Normal workflow for CHG0000037.
var wfhGR = new GlideRecord ('wf_history');
wfhGR.addQuery('context.id', '41cdb152db252200a6a2b31be0b8f527');
wfhGR.addQuery('context.table', 'change_request');
wfhGR.orderBy ('activity_index');
wfhGR.query();
while (wfhGR.next())  {
  var script_name = 'AHR';
  //
  //  Acquire the execution history of the workflow's activities.
  //  Do this just once while processing the first activity.

  if(wfhGR.activity_index == 0) {
    var model = new WorkflowModelManager( wfhGR.context );
    model.getExecutedHistory();
  }

//
// Access a hash of ActivityHistoryRecord javascript objects,
// hashed by the sys_id of the wf_history record.
// There will be one ActivityHistoryRecord for each activity.

  var ActivityHistoryRecord = model.getActivityHistoryRecordById(wfhGR.sys_id);

//
// Use ActivityHistoryRecord methods to display selected values

  gs.log('Log String [' + ActivityHistoryRecord.getLogString() + ']', script_name);
  gs.log('debugDump START', script_name);
  ActivityHistoryRecord.debugDump();
  gs.log('debugDump END', script_name);
  gs.log('Turnstile?[' + ActivityHistoryRecord.isTurnstile() + ']', script_name);
  gs.log('Transition Count[' + ActivityHistoryRecord.getTransitionCount() + ']\n', script_name );
}
```

Output:

```
[0:00:00.133] Script completed in scope global: script
Script execution history and recovery available here
AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57a  History INDEX:0  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:e233b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Begin  WF Activity DEF ID:c7a5e32c0a0a0b3a002377c24ed8ea76  WF Activity DEF NAME:Begin  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57a
*** Script:        History INDEX: 0
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 0
*** Script:       WF Activity ID: e233b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Begin
*** Script:   WF Activity DEF ID: c7a5e32c0a0a0b3a002377c24ed8ea76
*** Script: WF Activity DEF NAME: Begin
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:a228c4b6dba52200a6a2b31be0b8f57d  History INDEX:1  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:2e33b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Change moves to Assess  WF Activity DEF ID:d93a02ae0a0a0aa30077abad3fdac035  WF Activity DEF NAME:Wait for condition  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: a228c4b6dba52200a6a2b31be0b8f57d
*** Script:        History INDEX: 1
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 1
*** Script:       WF Activity ID: 2e33b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Change moves to Assess
*** Script:   WF Activity DEF ID: d93a02ae0a0a0aa30077abad3fdac035
*** Script: WF Activity DEF NAME: Wait for condition
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:3e28c4b6dba52200a6a2b31be0b8f57e  History INDEX:2  History START TIME:1585659881000  History END TIME:1585659881000  WF Activity ID:6e33b949cb020200d71cb9c0c24c9c1f  WF Activity NAME:Requested  WF Activity DEF ID:50a78fa50a6a803f66d064255f7201a5  WF Activity DEF NAME:Approval Action  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 3e28c4b6dba52200a6a2b31be0b8f57e
*** Script:        History INDEX: 2
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659881000
*** Script:        History INDEX: 2
*** Script:       WF Activity ID: 6e33b949cb020200d71cb9c0c24c9c1f
*** Script:     WF Activity NAME: Requested
*** Script:   WF Activity DEF ID: 50a78fa50a6a803f66d064255f7201a5
*** Script: WF Activity DEF NAME: Approval Action
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:0d38c4b6dba52200a6a2b31be0b8f5cc  History INDEX:3  History START TIME:1585659881000  History END TIME:1585659891000  WF Activity ID:2a33b949cb020200d71cb9c0c24c9c26  WF Activity NAME:Technical approvals  WF Activity DEF ID:354e911f0a0a029a00e6a0e6ad74206f  WF Activity DEF NAME:Approval - Group  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: 0d38c4b6dba52200a6a2b31be0b8f5cc
*** Script:        History INDEX: 3
*** Script:   History START TIME: 1585659881000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 3
*** Script:       WF Activity ID: 2a33b949cb020200d71cb9c0c24c9c26
*** Script:     WF Activity NAME: Technical approvals
*** Script:   WF Activity DEF ID: 354e911f0a0a029a00e6a0e6ad74206f
*** Script: WF Activity DEF NAME: Approval - Group
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:c538c4b6dba52200a6a2b31be0b8f5ce  History INDEX:4  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:6233b949cb020200d71cb9c0c24c9c5b  WF Activity NAME:Check if Change is "On hold"  WF Activity DEF ID:98f621ca0a0a0b5900f7c291f5e45a0e  WF Activity DEF NAME:If  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: c538c4b6dba52200a6a2b31be0b8f5ce
*** Script:        History INDEX: 4
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 4
*** Script:       WF Activity ID: 6233b949cb020200d71cb9c0c24c9c5b
*** Script:     WF Activity NAME: Check if Change is "On hold"
*** Script:   WF Activity DEF ID: 98f621ca0a0a0b5900f7c291f5e45a0e
*** Script: WF Activity DEF NAME: If
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]


AHR: Log String [HISTORY RECORD:  History ID:cd3808b6dba52200a6a2b31be0b8f501  History INDEX:5  History START TIME:1585659891000  History END TIME:1585659891000  WF Activity ID:e633b949cb020200d71cb9c0c24c9c20  WF Activity NAME:Move to Authorize  WF Activity DEF ID:1ca8d7cf0a0a0b265e9a000c2c08248c  WF Activity DEF NAME:Set Values  Transition Count: 1  Is Turnstile (loop) : false  Is Join: false]
AHR: debugDump START
*** Script: 
*** Script: WF HISTORY RECORD:
*** Script:           History ID: cd3808b6dba52200a6a2b31be0b8f501
*** Script:        History INDEX: 5
*** Script:   History START TIME: 1585659891000
*** Script:     History END TIME: 1585659891000
*** Script:        History INDEX: 5
*** Script:       WF Activity ID: e633b949cb020200d71cb9c0c24c9c20
*** Script:     WF Activity NAME: Move to Authorize
*** Script:   WF Activity DEF ID: 1ca8d7cf0a0a0b265e9a000c2c08248c
*** Script: WF Activity DEF NAME: Set Values
*** Script:     Transition Count: 1
*** Script: Roll Back Originator: 
*** Script:  Is Turnstile (loop): false
*** Script:              Is Join: false
AHR: debugDump END
AHR: Turnstile? [false]
AHR: Transition Count [1]

```

## ActivityHistoryRecord - getUnSatisfiedJoinActivities\( \)

Returns the sys\_ids of the history records that transition to this Join activity that the join is still waiting for.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String Array|Array of sys\_ids of the history records that transition to this Join activity.|

## ActivityHistoryRecord - isARollback\( \)

Determines if this activity is one of the rollback activities.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_osx_ttx_rt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the activity is one of the rollback activities.

 Valid values:

-   true: Activity is a rollback.
-   false: Activity is not a rollback.

</td></tr></tbody>
</table>## ActivityHistoryRecord - isIdADestination\(String ahrSys\_id\)

Determines if the sys\_id passed in is a destination of any of the transitions associated with this instance of an ActivityHistoryRecord.

|Name|Type|Description|
|----|----|-----------|
|ahrSys\_id|String|Activity history sys\_id from table wf\_history.|

|Type|Description|
|----|-----------|
|Boolean|True, if the sys\_id passed in is a destination of any of the transitions.|

## ActivityHistoryRecord - isJoin\( \)

Determines if this activity is a join.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True, if the activity is "Join".|

## ActivityHistoryRecord - isJoinSatisfied\( \)

Examines the value of the arriveState.

Called during playback when the transition to sys\_id of a transition points to an activity that is a join.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True, if the join is satisfied.|

## ActivityHistoryRecord - isJoinWaitingForActivity\(String Array activityIds\)

Tests the incoming wf\_activity sys\_id, presumed to be seeded in this history record.

If it is, it is tested to see if it has already been through; if it has, then this join is not waiting on this activity and it should look further downstream for the one that is waiting. This test is called in sequence as the model is walked, so it does presume in the instances of rollbacks and loops. If the sys\_id is in here and the flag is **true**, this waiting Join is further up the sequence. This sort of check is required as the history records of Joins are removed from the history table, and so it is possible for a record to be in the transition table with no match in the corresponding history table, but is still an appropriate match for an earlier executed instance of the same Join.

|Name|Type|Description|
|----|----|-----------|
|activityIds|String Array|Array of wf\_activity.sys\_ids that are headed towards join.|

|Type|Description|
|----|-----------|
|Boolean|True, if the activity has already been through.|

## ActivityHistoryRecord - isRolledBack\( \)

Determines if this workflow was rolled back.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True, if this workflow was rolled back.|

## ActivityHistoryRecord - isTurnstile\( \)

Determines if the current activity is a turnstile.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_msx_ttx_rt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the activity is a [turnstile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/r_TurnstileActivity.md).

 Valid values:

-   true: Activity is a turnstile.
-   false: Activity is not a turnstile.

</td></tr></tbody>
</table>The following code example shows how to use this method to detect a turnstile. It is based on the workflow found in [Rollback To workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/r_RollbackTo.md). You can confirm the output of this script by examining the **Workflow Activity History** tab when you **Show Workflow** on the requested items \(RITM\) form.

```
var wfhGR = new GlideRecord ('wf_history');
wfhGR.addQuery ('context.id','cc45480d2f9b8110b99eb2e72799b6f9'); // sys_id of the RITM
wfhGR.addQuery ('context.table','sc_req_item'); // Table for the RITM
wfhGR.orderBy  ('activity_index');
wfhGR.query();
var turnstile_count = 0;
while (wfhGR.next())  {
  var script_name = 'AHR';
  //
  // Acquire the execution history of the workflow's activities.
  // Do this just once while processing the first activity.

  if(wfhGR.activity_index == 0) {
    var model = new WorkflowModelManager(wfhGR.context);
    model.getExecutedHistory();
  }

  //
  // Access a hash of ActivityHistoryRecord javascript objects,
  // hashed by the sys_id of the wf_history record.
  // There will be one ActivityHistoryRecord for each activity.

  var ActivityHistoryRecord = model.getActivityHistoryRecordById(wfhGR.sys_id);

  //
  // Use ActivityHistoryRecord methods to display turnstile activities.

  if(ActivityHistoryRecord.isTurnstile()) {
    var log_string = ActivityHistoryRecord.getLogString();
    var name_start = log_string.indexOf('WF Activity NAME:');
    var name_end = log_string.indexOf('WF Activity DEF ID:');
    var name = log_string.substring(name_start, name_end).trim();
    gs.log(name + ' Activity ' + wfhGR.activity_index + ' is a turnstile.', script_name);
    turnstile_count++;
  } 
} 
gs.log ('Turnstile activities detected: ' + turnstile_count, script_name);
```

Output:

```
AHR: WF Activity NAME:Prevent infinite loops Activity 8 is a turnstile.
AHR: WF Activity NAME:Prevent infinite loops Activity 13 is a turnstile.
AHR: WF Activity NAME:Prevent infinite loops Activity 18 is a turnstile.
AHR: WF Activity NAME:Prevent infinite loops Activity 23 is a turnstile.
AHR: Turnstile activities detected: 4
```

