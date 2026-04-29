---
title: Workflow - Global
description: The Workflow script include provides methods that interface with the Workflow engine.Sends the specified event \(message\) into the workflow context to pass along to the executing activities.Cancels all running workflows on this record by broadcasting the cancel event to activities in all running workflows on this record.Cancels this running context by broadcasting a cancel event to activities in this workflow context.Deletes all the workflows on the record.Fires the named event of a running workflow on the input record.Fires the named event on the record specified by record ID.Returns all workflow contexts for a specified record.Gets the estimated time for a workflow to complete.Get the estimated elapsed execution time for the workflow version.Gets the appropriate workflow return value for the input workflow ID. This is either the workflow checked out by the current user or the published workflow with the most recent date.Gets all the currently running workflow contexts for the input record.Gets the appropriate workflow version for the input workflow ID. This is either the workflow checked out by the current user or the published workflow with the most recent date.Returns the appropriate workflow version for the input workflow name.Returns the sys\_id of the workflow associated with the specified workflow name.Determines if a specified record has any workflow contexts associated to it.Recalculates the approvals and tasks for a workflow by adding new approvals and tasks, while not resetting current approvals and tasks.Runs all workflows for a given record in a given table and its descendant tables.Starts a specified workflow.Helper method for business rule Auto start on context.Used by business rule Start Workflow on table task\_sla. This starts a workflow and the extra arguments to this method are used by activity "Timer" to pause the execution of the workflow for some duration.Constructor for Workflow class.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Workflow- Global

The Workflow script include provides methods that interface with the Workflow engine.

Use these methods to manipulate workflows.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Workflow - broadcastEvent\(String contextId, String eventName\)

Sends the specified event \(message\) into the workflow context to pass along to the executing activities.

Typical use of this method is to enable activities that wait for some action to occur before proceeding. For additional information on using broadcastEvent, refer to [Workflow event-specific functions](https://www.servicenow.com/docs/access?context=r_WorkflowEventSpecificFunctions&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

For a list of the available OOB events, refer to [Workflow events in the base system](https://www.servicenow.com/docs/access?context=r_WorkflowEventsInTheBaseSystem&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The context ID.|
|eventName|String|The name of the event.|

|Type|Description|
|----|-----------|
|void| |

```
//where current is a task record with a workflow context
      var wf = new Workflow().getRunningFlows(current);
      while(wf.next()) {     
          new Workflow().broadcastEvent(wf.sys_id, 'resume');
      }
```

## Workflow - cancel\(GlideRecord record\)

Cancels all running workflows on this record by broadcasting the **cancel** event to activities in all running workflows on this record.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|GlideRecord on any table. All workflows running on this record will be cancelled.|

|Type|Description|
|----|-----------|
|void| |

```
//get workflow helper
      var workflow = new Workflow();
      //cancel all the workflows, where current is a task record with a workflow context
      workflow.cancel(current);
      gs.addInfoMessage(gs.getMessage("Workflows for {0} have been cancelled", current.getDisplayValue()));
```

## Workflow - cancelContext\(GlideRecord context\)

Cancels this running context by broadcasting a **cancel** event to activities in this workflow context.

|Name|Type|Description|
|----|----|-----------|
|context|GlideRecord|GlideRecord of the running context to cancel.|

|Type|Description|
|----|-----------|
|void| |

```
// If a workflow has started for this item, cancel it, where current is a task record with a workflow context
      if ((current.stage == 'Request Cancelled') && current.context 
          && !current.context.nil()) {
      var w = new Workflow();
      var now_GR = new GlideRecord('wf_context');
      
      if (now_GR.get(current.context)) 
          w.cancelContext(now_GR);
      }
```

## Workflow - deleteWorkflow\(GlideRecord current\)

Deletes all the workflows on the record.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|GlideRecord for which the caller wants to delete all workflows. This can be any record on any table.|

|Type|Description|
|----|-----------|
|void| |

```
//where current is a task record with a workflow context
      var wkfw = new Workflow();
      wkfw.deleteWorkflow(current);
    
```

## Workflow - fireEvent\(GlideRecord eventRecord, String eventName, Object eventParms\)

Fires the named event of a running workflow on the input record.

Used in Activities **Approval Coordinator**, **Timer**, **Lock**, and some others.

|Name|Type|Description|
|----|----|-----------|
|eventRecord|GlideRecord|Event record listed in the Workflow Executing Activites \[wf\_executing\] table.|
|eventName|String|The name of the event to send to the executing workflow.|
|eventParms|Object|Optional. Parameters in JSON format used by the event.|

|Type|Description|
|----|-----------|
|void| |

```
// where current is a task record with a workflow context
  var w = new Workflow(); 
  w.fireEvent(current, 'execute');
```

## Workflow - fireEventById\(String eventRecordId, String eventName\)

Fires the named event on the record specified by record ID.

Used in Activities **Approval Coordinator**, **Timer**, **Lock**, and some others.

|Name|Type|Description|
|----|----|-----------|
|eventRecordId|String|The sys\_id of the glide record.|
|eventName|String|The name of the event to send to the executing workflow.|

|Type|Description|
|----|-----------|
|void| |

```
var wkfw = new Workflow();
      wkfw.fireEventById('f2400ec10b0a3c1c00ca5bb5c6fae427','Timer');
```

## Workflow - getContexts\(GlideRecord record\)

Returns all workflow contexts for a specified record.

|Name|Type|Description|
|----|----|-----------|
|record|[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord for which the caller wants a list of all workflow contexts. This can be any record on any table for which the caller wants the running workflow contexts.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord in the Workflow context \[wf\_context\] table filtered for all workflow contexts for the specified record \(in any state, such as running, cancelled, finished\).|

```
//where current is a task record with a workflow context
var wkfw = new Workflow();
var context = wkfw.getContexts(current);
while (context.next())
  gs.print(context.started);
```

## Workflow - getEstimatedDeliveryTime\(String workflowId\)

Gets the estimated time for a workflow to complete.

|Name|Type|Description|
|----|----|-----------|
|workflowId|String|Sys\_id of the workflow \(table wf\_workflow\) to get the estimated run time.|

|Type|Description|
|----|-----------|
|String|Display value from a GlideDuration \(e.g., 3 days\), or blank if unknown.|

```
var wkfw = new Workflow();
      gs.print(wkfw.getEstimatedDeliveryTime('b99a866a4a3623120074c033e005418f'));
```

2 Days

## Workflow - getEstimatedDeliveryTimeFromWFVersion\(GlideRecord wfVersion\)

Get the estimated elapsed execution time for the workflow version.

|Name|Type|Description|
|----|----|-----------|
|wfVersion|GlideRecord|GlideRecord on table wf\_workflow\_version of a specific workflow version for which the caller wants the estimated during of executing.|

|Type|Description|
|----|-----------|
|String|Display value from a GlideDuration \(e.g., 3 days\), or blank if unknown.|

```
//where current is a task record with a workflow context
      var wkfw = new Workflow();
      var context = wkfw.getContexts(current);
      gs.print(wkfw.getEstimatedDeliveryTimeFromWFVersion(context.wf_version));
```

## Workflow - getReturnValue\(String workflowID, Number amount, Boolean result\)

Gets the appropriate workflow return value for the input workflow ID. This is either the workflow checked out by the current user or the published workflow with the most recent date.

This is either the workflow checked out by the current user or the published workflow with the most recent date. This method is available starting with the Fuji release.

|Name|Type|Description|
|----|----|-----------|
|workflowID|String|The sys\_id of the workflow \(table wf\_workflow\)|
|amount|Number|amount|
|result|Boolean|**True**, if true|

|Type|Description|
|----|-----------|
|???|The return value of the workflow as specified by the Return Value activity. Workflows without a Return Value activity return a null value.|

```
var wkfw = new Workflow();
      wkfw.getReturnValue('context');
```

Output:

```
*** Script: b99a866a4a3623120074c033e005418f
      
```

## Workflow - getRunningFlows\(GlideRecord record\)

Gets all the currently running workflow contexts for the input record.

The input record is any record on any table for which the caller wants the running workflow contexts.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|GlideRecord of the record for which the caller wants a list of all running workflows.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord on table wf\_context and filtered for all executing workflow contexts.|

```
//where current is a task record with a workflow context
      var wf = new Workflow().getRunningFlows(current);
      while(wf.next()) {     
          new Workflow().broadcastEvent(wf.sys_id, 'pause');
      }
```

## Workflow - getVersion\(String workflowID\)

Gets the appropriate workflow version for the input workflow ID. This is either the workflow checked out by the current user or the published workflow with the most recent date.

This is either the workflow checked out by the current user or the published workflow with the most recent date.

|Name|Type|Description|
|----|----|-----------|
|workflowID|String|The sys\_id of the workflow \(table wf\_workflow\)|

|Type|Description|
|----|-----------|
|none| |

```
var wkfw = new Workflow();
      wkfw.getVersion('b99a866a4a3623120074c033e005418f');
```

## Workflow - getVersionFromName\(String workflowName\)

Returns the appropriate workflow version for the input workflow name.

See getVersion\(\) for more information.

|Name|Type|Description|
|----|----|-----------|
|workflowName|String|Name of the workflow \(table wf\_workflow\)|

|Type|Description|
|----|-----------|
|void| |

```
var wkfw = new Workflow();
      wkfw.getVersionFromName('Emergency Change');
```

## Workflow - getWorkflowFromName\(String workflowName\)

Returns the sys\_id of the workflow associated with the specified workflow name.

|Name|Type|Description|
|----|----|-----------|
|workflowName|String|Name of the workflow.|

|Type|Description|
|----|-----------|
|String|The sys\_id of the workflow associated with the passed in name.|

```
var wflw = new Workflow();
      gs.print(wflw.getWorkflowFromName('Emergency Change'));
```

## Workflow - hasWorkflow\(GlideRecord record\)

Determines if a specified record has any workflow contexts associated to it.

This includes running and completed workflow contexts.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|GlideRecord under scrutiny. This GlideRecord can be from any table.|

|Type|Description|
|----|-----------|
|Boolean|True, if record has associated workflow; otherwise, returns False.|

```
var wkfw = new Workflow();
      gs.print(wkfw.hasWorkflow('f2400ec10b0a3c1c00ca5bb5c6fae427'));
```

false

## Workflow - restartWorkflow\(GlideRecord current, Boolean maintainStateFlag\)

Recalculates the approvals and tasks for a workflow by adding new approvals and tasks, while not resetting current approvals and tasks.

You can use this method to perform such tasks as adding a company to a change request, without resetting the current approvals for companies already in the workflow.

<table id="table_up5_d1s_nt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

current

</td><td>

GlideRecord

</td><td>

GlideRecord of the record this workflow is executing. This can by any record on any table.

</td></tr><tr><td>

maintainStateFlag

</td><td>

Boolean

</td><td>

Flag that indicates whether to maintain all approvals and tasks in their current state.Valid values:

-   true: Maintain all approvals and tasks in their current state.
-   false: Update all approval and task states.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows the workflow being restarted with the approval file changing from Rejected to Requested.

```
(function(){
  var comment = 'Workflow Restarted - the Approval Field changing from Rejected to Requested';
  var gLock = new GlideRecordLock(current);
    gLock.setSpinWait(50);
  if (gLock.get()) {
    new Workflow().restartWorkflow(current, false);
    current.setDisplayValue('approval_history', comment);
  }
})
```

## Workflow - runFlows\(GlideRecord record, String operation\)

Runs all workflows for a given record in a given table and its descendant tables.

Sample usage can be seen in the Script Includes "SNC - Run parent workflows", and "SNC - Run parent workflows \(Approval\)".

<table id="table_u2y_bjp_mt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record

</td><td>

GlideRecord

</td><td>

GlideRecord to run workflows against.

</td></tr><tr><td>

operation

</td><td>

String

</td><td>

Database operation.Valid values:

-   insert
-   update
-   delete

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('wf_test');
now_GR.addQuery('parent', current.parent);
now_GR.addQuery('sys_id','!=',current.sys_id);
now_GR.query();
while(now_GR.next()) {
    new Workflow().runFlows(now_GR, 'update');
}
```

## Workflow - startFlow\(String workflowId, GlideRecord current, String operation, Array vars\)

Starts a specified workflow.

See script include WorkflowScheduler and Business Rule "Start Workflow" on table sc\_req\_item for examples of use.

|Name|Type|Description|
|----|----|-----------|
|workflowId|String|The sys\_id of the workflow to start. This sys\_id refers to table wf\_workflow.|
|current|GlideRecord|The record to use as current in this workflow. This is normally from the **Table** field of the workflow properties for this workflow.|
|operation|String|The operation to perform on **current**. Possible values: **insert**, **update**, **delete**.|
|vars|Array|Collection of variables to add to the workflow|

```
////where current is a task record with a workflow context
      var w = new Workflow();
      var context = w.startFlow(id, current, current.operation(), getVars());
```

## Workflow - startFlowFromContextInsert\(GlideRecord context, String operation\)

Helper method for business rule **Auto start on context**.

|Name|Type|Description|
|----|----|-----------|
|context|GlideRecord|GlideRecord on table wf\_context of a new record \(the "current" record in the business rule\).|
|operation|String|Database operation being performed. One of **insert**, **update**, **delete**.|

|Type|Description|
|----|-----------|
|void| |

```
//where current is a task record with a workflow context
      current.name = current.workflow_version.name;
      current.started_by.setValue(gs.userID());
      
      if (gs.nil(current.id)) {
        var now_GR = new GlideRecord('wf_workflow_execution');
        now_GR.name = current.name;
        now_GR.insert();
      
        current.table = 'wf_workflow_execution';
        current.id = now_GR.sys_id;
      }
      
      var wf = new Workflow();
      wf.startFlowFromContextInsert(current, current.operation())
```

## Workflow - startFlowRetroactive\(String workflowId, Number retroactiveMSecs, GlideRecord current, String operation, Array, ???\)

Used by business rule **Start Workflow** on table task\_sla. This starts a workflow and the extra arguments to this method are used by activity "Timer" to pause the execution of the workflow for some duration.

|Name|Type|Description|
|----|----|-----------|
|workflowID|String|The sys\_id of the workflow to start. This sys\_id refers to table wf\_workflow.|
|retroactiveMSecs|Number|Delay in milliseconds used by Activity **Timer**.|
|current|GlideRecord|GlideRecord of the record to use as current in this workflow. This is normally from the **Table** field of the workflow properties for this workflow|
|operation|String|Database operation being performed.One of **insert**, **update**, **delete**.|
|vars|Array|Collection of variables to add to the workflow.|
|withSchedule|???|Schedule used by Activity **Timer**|

|Type|Description|
|----|-----------|
|GlideRecord|A GlideRecord on table wf\_context on the inserted record for this newly created workflow context.|

```
// is this a retroactive start?
      ////where current is a task record with a workflow context
      var msecs = new GlideDateTime().getNumericValue() - current.start_time.getGlideObject().getNumericValue();
      
      // treat this as a retroactive workflow start if the SLA started more than 5 seconds ago
      var w = new Workflow();
      if (msecs <= 5000)
        w.startFlow(id, current, current.operation());
      else
        w.startFlowRetroactive(id, msecs, current, current.operation());
      
      // update the record in case the workflow changed some values
      current.update();
      
    
```

## Workflow - Workflow\(\)

Constructor for Workflow class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var w = new Workflow();
```

