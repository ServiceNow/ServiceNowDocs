---
title: CMDBDuplicateTemplateUtil - Global
description: The CMDBDuplicateTemplateUtil script include provides methods to add and remove de-duplication tasks to/from a de-duplication template.Creates an instance of the CMDBDuplicateTemplateUtils class.Adds one or more de-duplication tasks to a specified de-duplication template.Clears the de-duplication template value in the specified de-duplication task records. By clearing this value, the association between a template and the task is removed.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CMDBDuplicateTemplateUtil- Global

The CMDBDuplicateTemplateUtil script include provides methods to add and remove de-duplication tasks to/from a de-duplication template.

For more information on de-duplication of CIs, de-duplication tasks, and de-duplication templates, see [Duplicate CIs remediation](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CMDBDuplicateTemplateUtils - CMDBDuplicateTemplateUtils\(\)

Creates an instance of the CMDBDuplicateTemplateUtils class.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following code example shows how to call this method to create a CMDBDuplicateTemplateUtils object.

```

var dupTemp = new CMDBDuplicateTemplateUtils();
```

## CMDBDuplicateTemplateUtils - addTasksToTemplate\(String templateId, Array taskIds\)

Adds one or more de-duplication tasks to a specified de-duplication template.

This method overwrites any existing template values, but logs the previous values for each template in the system logs.

The following list describes scenarios where a task isn’t added to a template and is then marked as either skipped or failed:

-   The specified template isn’t in the published state. All tasks are marked as skipped.
-   The specified template is running. All tasks are marked as skipped.
-   The task isn’t in the open state. The task is marked as skipped.
-   The task isn’t compatible with the specified template. For example, the specified template might be created for Application Server Tomcat, but the specified de-duplication task is created for Linux Server. The task is marked as skipped.
-   The specified template doesn’t exist. All tasks are marked as failed.
-   The GlideRecord update for the template column on the task fails. The task is marked as failed.

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the de-duplication template to associate with the de-duplication task.|
|taskIds|Array|List of sys\_ids of the de-duplication tasks to associate with the specified template.|

<table id="table_uch_4y5_xxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing the status of all the tasks that were attempted to be associated with the specified template.Data type: Object

```
{
  "failed": [Array],
  "skipped": [Array],
  "success": [Array],
  "summary": "String"
}
```

</td></tr><tr><td>

failed

</td><td>

List of tasks that failed to be associated with the template.Data type: Array of Objects

```
"failed": [
  {
    "message": "String",
    "messageType: "String",
    "taskId": "String"
  }
]
```

</td></tr><tr><td>

failed.message

</td><td>

Message that describes why the task failed to be associated with the template.Data type: String

</td></tr><tr><td>

failed.messageType

</td><td>

Reason for the failure.Data type: String

</td></tr><tr><td>

failed.taskId

</td><td>

Sys\_id of a task that failed to be associated with the template.Data type: String

</td></tr><tr><td>

skipped

</td><td>

List of tasks that didn't fail, but weren't associated with the template \(skipped\).Data type: Array of Objects

```
"skipped": [
  {
    "message": "String",
    "messageType: "String",
    "taskId": "String"
  }
]
```

</td></tr><tr><td>

skipped.message

</td><td>

Message that describes why the task was skipped.Data type: String

</td></tr><tr><td>

skipped.messageType

</td><td>

Reason for the task being skipped.Data type: String

</td></tr><tr><td>

skipped.taskId

</td><td>

Sys\_id of a task that the method skipped associated with the template.Data type: String

</td></tr><tr><td>

success

</td><td>

List of tasks that were successfully associated with the template.Data type: Array of Objects

```
"success": [
  {
    "message": "String",
    "messageType: "String",
    "taskId": "String"
  }
]
```

</td></tr><tr><td>

success.message

</td><td>

Not currently in use.Data type: String

</td></tr><tr><td>

success.messageType

</td><td>

Not currently in use.Data type: String

</td></tr><tr><td>

success.taskId

</td><td>

Sys\_id of a task that was associated with the template.Data type: String

</td></tr><tr><td>

summary

</td><td>

Brief description of any overall processing errors that occurred, such as if the specified template doesn't exist.Data type: String

</td></tr></tbody>
</table>The following code example shows how to call this method to add de-duplication tasks to a de-duplication template.

```
// Add tasks to template
var taskIds = [];
taskIds.push("96d2d25113152200eef2dd828144b0a4");
taskIds.push("f785a2c3d7012201de92a5f75e610398");
taskIds.push("635dd3dbc128ce0100655f1ec66ed41d");

var result = new CMDBDuplicateTemplateUtils().addTasksToTemplate("6b43105c37301000deeabfc8bcbe5db2", taskIds);
); 
gs.info('Success: ' + result.success);
gs.info('Failed: ' + result.failed);
gs.info('Skipped: ' + result.skipped);
gs.info(Summary: ' + result.summary);

```

Output:

```
Success: [
    {
      "taskId": "f785a2c3d7012201de92a5f75e610398",
      "message": "",
      "messageType": ""
    }
  ]
Failed: [
    {
      "taskId": "96d2d25113152200eef2dd828144b0a4",
      "message": "Failed to add task 96d2d25113152200eef2dd828144b0a4 to template 6b43105c37301000deeabfc8bcbe5db2 because there were update errors.",
      "messageType": "update_failed"
    }
  ]
Skipped: [
    {
      "taskId": "635dd3dbc128ce0100655f1ec66ed41d",
      "message": "Cannot add de-duplication task(s) to template 6b43105c37301000deeabfc8bcbe5db2 because the template is not published. Publish the template before adding tasks.",
      "messageType": "unpublished_template"
    }
  ]
Summary:

```

## CMDBDuplicateTemplateUtils - removeTemplateFromTask\(Array taskIds\)

Clears the de-duplication template value in the specified de-duplication task records. By clearing this value, the association between a template and the task is removed.

The following list describes scenarios where the template value isn’t removed from the task record and is marked as either skipped or failed:

-   The de-duplication template associated with the task is running. The task is marked as skipped.
-   The task state is "work in progress" or the task isn’t found. The task is marked as skipped.
-   The GlideRecord update for the template column on the task fails. The task is marked as failed.

|Name|Type|Description|
|----|----|-----------|
|taskIds|Array|List of sys\_ids of the de-duplication task records from which to clear the de-duplication template value.|

<table id="table_qn5_g3v_xxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing the count of tasks for which the template value removal was successful, skipped, or failed.

```
{
  "failed": Number,
  "success": Number,
  "skipped": Number
}
```

</td></tr><tr><td>

failed

</td><td>

Number of tasks that failed to remove the de-duplication template value.Data type: Number

</td></tr><tr><td>

success

</td><td>

Number of tasks that successfully removed the de-duplication template value.Data type: Number

</td></tr><tr><td>

skipped

</td><td>

Number of tasks that the method skipped removing the de-duplication template value.Data type: Number

</td></tr></tbody>
</table>The following code example shows how to call this method to remove de-duplication template values from de-duplication task records.

```
// Remove tasks from template
var taskIds = [];
taskIds.push("96d2d25113152200eef2dd828144b0a4");
taskIds.push("f785a2c3d7012201de92a5f75e610398");
taskIds.push("635dd3dbc128ce0100655f1ec66ed41d");

var result = new CMDBDuplicateTemplateUtils().removeTemplateFromTasks(taskIds);
); 
gs.info('Success: ' + result.success);
gs.info('Failed: ' + result.failed);
gs.info('Skipped: ' + result.skipped);
```

Output:

```
Success: 2
Failed: 0
Skipped: 1
```

