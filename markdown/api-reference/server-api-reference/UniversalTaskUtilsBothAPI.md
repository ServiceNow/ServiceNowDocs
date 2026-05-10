---
title: UniversalTaskUtils - Scoped, Global
description: The UniversalTaskUtils script include provides methods for managing universal tasks.Applies the specified universal task template to the specified universal task record.Returns the active child task records, in the form of a GlideRecord, for the specified parent ticket.Checks whether the specified parent ticket has any universal tasks that are in the work-in progress or complete state.Changes the state of all active universal tasks under the specified parent ticket to "Cancelled".Changes the state of all active child universal tasks associated with the specified parent ticket to "Complete".
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UniversalTaskUtils - Scoped, Global

The UniversalTaskUtils script include provides methods for managing universal tasks.

With the ServiceNow Universal Task application, agents can create tasks for employees. For example, agents can ask for additional information or request an action to resolve a parent ticket or request. Universal tasks are available for any ticket type that extends the Task \[task\] table.

Using this script include you can change the state of active universal tasks to "Complete" or "Cancelled", obtain all active universal tasks for a specified parent task, check whether a parent universal task has any children, and apply templates to a universal task record. You can use these methods in scripts and in the Visable condition builders on the **Tab configuration** form to manage the data that appears on the **Universal Task** tab. For additional information, see [Add a Task tab on the Standard Ticket page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-task/config-stdtktpage-for-ut.md).

![Tab Configuration conditional builder example](../image/tab_config-method-imp.png)

You can use this script include in both scoped and global applications. The Universal Task application \(sn\_uni\_task\) must be installed on the associated instance to have access to this script include. You must always specify the `sn_uni_task` namespace when calling methods in this API.

For additional information on the Universal Task application, see [Universal Task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-task/universal-task-landing.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UniversalTaskUtils - applyTemplate\(String templateSysId, GlideRecord uniTaskGr\)

Applies the specified universal task template to the specified universal task record.

Before you can use this method, there must be universal task templates configured in your instance. For details, see [Universal Task templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-task/ut-task-template-landing.md).

<table id="table_c3g_znf_hpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

templateSysId

</td><td>

String

</td><td>

Sys\_id of universal task template to apply to the specified universal task record.Table: Universal Task Template \[sn\_uni\_task\_template\]

</td></tr><tr><td>

uniTaskGr

</td><td>

GlideRecord

</td><td>

GlideRecord of the universal task record to which to apply the template.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None|Any errors are written to the system log.|

This code example shows a function that acquires, and then applies, the Feedback Template.

```
(function executeRule(current, previous /*null when async*/) {
  var templateGr = new GlideRecord('sn_uni_task_template');
  templateGr.get('name','Feedback Template');
  var templateSysId = templateGr.getValue('sys_id');
  new sn_uni_task.UniversalTaskUtils().applyTemplate (templateSysId,current);
})(current, previous);
```

## UniversalTaskUtils - getActiveChildTasks\(String parentSysId\)

Returns the active child task records, in the form of a GlideRecord, for the specified parent ticket.

You can then use the GlideRecord API, [scoped](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) or [global](../../GlideRecord/concept/c_GlideRecordAPI.md#) depending on the calling application's scope, to access the returned data, such as using the getRowCount\(\) method to count active tasks.

|Name|Type|Description|
|----|----|-----------|
|parentSysId|String|Sys\_id of the parent ticket whose active child tickets to return.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord that contains all active child task records for the specified parent task.|

The following example shows a function that obtains all active child tasks for the current sys\_id and then uses getRowCount\(\) to obtain the number of active child tasks.

```
(function executeRule(current, previous /*null when async*/) {
  var gr_ActiveTasks = new sn_uni_task.UniversalTaskUtils().getActiveChildTasks(current.sys_id);
  var count = gr_ActiveTasks.getRowCount();
})(current, previous);
```

## UniversalTaskUtils - hasTasksToShow\(GlideRecord current\)

Checks whether the specified parent ticket has any universal tasks that are in the work-in progress or complete state.

You can use this method to determine whether to show the Universal Task tab to a requester in a standard ticket configuration only if there are tasks that are work-in progress or complete.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|GlideRecord of the parent ticket to check.|

<table id="table_lvg_43f_hpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

If universal tasks are associated with the parent ticket, the sys\_id of the parent ticket; otherwise null.Data type: String

</td></tr></tbody>
</table>The following example shows a function that calls this method to check for universal tasks.

```
(function executeRule(current, previous /*null when async*/) {
  var sysId = new sn_uni_task.UniversalTaskUtils().hasTasksToShow(current);           
})(current, previous);
```

## UniversalTaskUtils - markActiveChildTasksCancelled\(String parentSysId\)

Changes the state of all active universal tasks under the specified parent ticket to "Cancelled".

|Name|Type|Description|
|----|----|-----------|
|parentSysId|String|Sys\_id of the parent ticket whose active child universal tasks' state should be changed to "Cancelled".|

|Type|Description|
|----|-----------|
|None| |

This code example shows how to use this method to update the states of all universal tasks associated with the specified parent task to cancelled.

```
(function executeRule(current, previous /*null when async*/) {
  new sn_uni_task.UniversalTaskUtils().markActiveChildTasksCancelled(current.sys_id);
})(current, previous);
```

## UniversalTaskUtils - markActiveChildTasksCompleted\(String parentSysId\)

Changes the state of all active child universal tasks associated with the specified parent ticket to "Complete".

|Name|Type|Description|
|----|----|-----------|
|parentSysId|String|Sys\_id of the parent ticket whose active child universal tasks' state should be changed to "Complete".|

|Type|Description|
|----|-----------|
|None| |

This code example shows how to use this method to update the states of all universal tasks associated with the specified parent task to completed.

```
(function executeRule(current, previous /*null when async*/) {
  new sn_uni_task.UniversalTaskUtils().markActiveChildTasksCompleted(current.sys_id);
})(current, previous);
```

