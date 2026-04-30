---
title: DuplicateTemplate - Scoped
description: The DuplicateTemplate API provides methods for users to interact with de-duplication templates by enforcing a set of validations for each method.Checks if the provided list of tasks can be added to a template.Creates a de-duplication template in draft state.Gets the template object.Generates a preview of how different template options were applied to the de-duplication task and how it’s to be remediated.Publishes a template. When successful, the template moves from draft to published state.Remediates a de-duplication task using the template.Cancels an existing template run.Retires a template.Schedules a remediation run for a de-duplication template in the published state. A template can be run multiple times but you can only schedule one run at a time.Unpublishes a template.Updates a de-duplication template in draft state.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 26
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DuplicateTemplate- Scoped

The DuplicateTemplate API provides methods for users to interact with de-duplication templates by enforcing a set of validations for each method.

De-duplication task remediation can be more time consuming than desirable when handled individually. Duplication templates enable grouping a set of duplicate tasks and running them together. Use the DuplicateTemplate API to create and consume de-duplication templates. This API runs in the `sn_cmdb` namespace and requires the cmdb\_dedup\_admin role to access.

When an instance detects duplicate configuration items \(CIs\) during identification and reconciliation, it groups each set of duplicate CIs into a de-duplication task for review and remediation. De-duplication tasks provide details about the duplication, including a list of all duplicate CIs. For information, see [Duplicate CIs remediation](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

See also: [IdentificationEngine - Scoped](../../IdentificationEngineScoped/concept/IdentificationEngineScopedAPI.md#)

-   **Template life cycle**
    1.  Use the [CreateTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to create a template in the draft state.

        You can use the following methods to retrieve or update the template:

        -   [getTemplate\(\)](DuplicateTemplateScopedAPI.md#)
        -   [canAddTasksToTemplate\(\)](DuplicateTemplateScopedAPI.md#)
        -   [updateTemplate\(\)](DuplicateTemplateScopedAPI.md#)
    2.  Use the [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to move the template from draft to published state.

        **Note:** Use the [unPublishTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to return a published template to draft state and update the template.

    3.  Optional. Use the [CMDBDuplicateTemplateUtil](../../CMDBDuplicateTemplateUtils/concept/CMDBDuplicateTemplateUtilAPI.md#) script include to add or remove tasks.
    4.  Use the [runTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to run the template.

        To cancel a running task, use the [requestCancellation\(\)](DuplicateTemplateScopedAPI.md#) method.

    5.  If the template is no longer needed, you can retire the template using the [retireTemplate\(\)](DuplicateTemplateScopedAPI.md#) method.
-   **Remediating a single task using a template**

    To remediate a single task without running the template, you can preview and remediate de-duplication tasks.

    1.  Use the [previewTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to preview the remediation of a single-task with a template.
    2.  Use the [remediateTask\(\)](DuplicateTemplateScopedAPI.md#) method to remediate the de-duplication task with a template.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DuplicateTemplate - canAddTasksToTemplate\(Array taskIds, String templatId\)

Checks if the provided list of tasks can be added to a template.

Use this method to determine whether tasks are suitable for adding to the template. For example, the specified template might be created for Application Server Tomcat, but the specified de-duplication tasks are created for Linux Server. These tasks don’t have a matching template class, so they can’t be added to the template.

|Name|Type|Description|
|----|----|-----------|
|taskIds|Array|Array of sys\_ids of the de-duplication tasks to add to the template.|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing what tasks can be added, skipped, or failed.```
{
  "success": [
    "<task_id_1>",
    "<task_id_2>",
    "<task_id_3>"
  ],
  "failed": [
    "<task_id_4>"
  ],
  "skipped": [
    "<task_id_5>"
  ]
}
```

</td></tr><tr><td>

failed

</td><td>

Error occurred while checking if the task is compatible with the template. See also [Detecting duplicate CIs](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

skipped

</td><td>

The tasks are incompatible because they don’t have a matching template class, so the task was skipped.

</td></tr><tr><td>

success

</td><td>

The task matches the template class and can be added to the template.

</td></tr></tbody>
</table>The following example shows how to check for tasks that can be added to the template.

```
var taskIds = [];
taskIds.push(<task_id_1>);
taskIds.push(<task_id_2>);
taskIds.push(<task_id_3>);

var result = sn_cmdb.DuplicateTemplate.canAddTasksToTemplate(taskIds, <template_id>);

gs.info('Success:' + result.success);
gs.info('Failed:' + result.failed);
gs.info('Skipped:' + result.skipped);
```

Output:

```
Success: <task_id_1>
Failed: <task_id_2>
Skipped: <task_id_3>
```

## DuplicateTemplate - createTemplate\(Object template\)

Creates a de-duplication template in draft state.

<table id="table_rl4_t5c_txb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

template

</td><td>

Object

</td><td>

The template object with different options for creating the template. ```
{
  "allow_master_ci_null_update": Boolean,
  "allow_null_attribute_update": Boolean,
  "description": "String",
  "duplicate_ci_action": "String",
  "duplicate_ci_updates": [Array],
  "master_ci_condition": "String",
  "master_ci_option": "String",
  "merge_related_items": "String",
  "merge_related_items_condition": [Array],
  "merge_relations_condition": "String",
  "merge_relations": "String",
  "most_related_items_merge_attributes": "String",
  "most_relations_merge_attributes": "String",
  "name": "String",
  "newest_updated_merge_attributes": "String",
  "oldest_created_merge_attributes": "String",
  "table": "String",
  "task_conditions": "String"
}
```

</td></tr><tr><td>

template.allow\_null\_​attribute\_update

</td><td>

Boolean

</td><td>

Optional. Flag that indicates if main CI attributes are updated with null values from duplicate CIs when resolving attribute conflicts for CIs within a de-duplication task.Valid values:

-   true: The main CI attributes are updated with null values from duplicate CIs.
-   false: The main CI attributes aren’t updated with null values from duplicate CIs.

Default: False

</td></tr><tr><td>

template.allow\_master\_ci\_​null\_update

</td><td>

Boolean

</td><td>

Optional. Only includes updates from duplicate CIs if the main CI value is null.Flag that indicates whether to include only updates from duplicate CIs if the main CI value is null.

Valid values:

-   true: Only include updates from duplicate CIs if the main CI value is null.
-   false: Include updates from all duplicate CIs.

Default: False

</td></tr><tr><td>

template.description

</td><td>

String

</td><td>

Optional. Description to store more information about the template.

</td></tr><tr><td>

template.duplicate\_​ci\_action

</td><td>

String

</td><td>

Optional. Specifies if the duplicate CI is to be deleted or updated with unique custom values.Possible options:

-   delete
-   update \(requires specifying **duplicate\_ci\_updates**\)

</td></tr><tr><td>

template.duplicate\_​ci\_updates

</td><td>

Array

</td><td>

Optional, unless the setting for **duplicate\_ci\_action** is `update`. Array of objects specifying how the duplicate CI values are updated.```
[
  {
    "element": "String",
    "element_label": "String",
    "value": "String",
    "display": "String"
  }
]
```

</td></tr><tr><td>

template.duplicate\_​ci\_updates.element

</td><td>

String

</td><td>

The system dictionary name of a reference field.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.element\_label

</td><td>

String

</td><td>

The label that the reference field displays.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.value

</td><td>

String

</td><td>

Value for a reference field, that is, the contents of the reference field.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.display

</td><td>

String

</td><td>

Display value for a reference field.

</td></tr><tr><td>

template.master\_ci\_​option

</td><td>

String

</td><td>

Optional. Specifies how the main CI is selected for a de-duplication task when applying this template. Possible options:

-   conditional \(must specify **master\_ci\_condition**\)
-   most\_related\_items – Attributes to be merged from the CI with the most related items to the main CI.
-   most\_relations – Attributes to be merged from the CI with the most relationships to the main CI.
-   newest\_created – separated attributes to be merged from the most recently updated CI to the main CI.
-   oldest\_created – Comma-separated attributes to be merged from the oldest-created CI to the main CI.

</td></tr><tr><td>

template.master\_ci\_condition

</td><td>

String

</td><td>

Optional \(required if the value of **master\_ci\_option** is `conditional`\). Encoded query to specify how the main CI is selected. If multiple CIs or no CIs match the query, the method selects the most recently updated CI as the main CI. The encoded query is evaluated for the template table. This table is identified in the **table** property.For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.merge\_relations

</td><td>

String

</td><td>

Optional. Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template. Possible options:

-   all
-   conditional
-   none

</td></tr><tr><td>

template.merge\_relations

</td><td>

String

</td><td>

Optional. Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template. Possible options:

-   all
-   conditional
-   none

</td></tr><tr><td>

template.merge\_relations\_​condition

</td><td>

String

</td><td>

Optional \(required if the value of **merge\_relations** is `conditional`\). Encoded query to specify if all or none of the relationships from duplicate CIs are merged. The query is evaluated on the main CI that is selected for the de-duplication task. If the query returns true, all relationships are merged. If false, no relationships are merged.The encoded query is evaluated for the template table. This table is identified in the **table** property.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.merge\_related\_items

</td><td>

String

</td><td>

Optional. Specifies which related tables for duplicate CIs within a de-duplication task are merged to the main CI when applying this template. See also [Remediate a de-duplication task \(legacy\)](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).Possible options:

-   all\_available – Includes the default-related tables and any related tables that reference duplicate CIs for the de-duplication task remediated via the template.
-   conditional
-   default – Includes related entries provided by the Duplicate CI Remediator Default Related Items module.
-   none

</td></tr><tr><td>

template.merge\_related\_items\_​condition

</td><td>

Array

</td><td>

Optional. List of related entries with an encoded query for each related entry. Each query is evaluated on the main CI that is selected for the task. If the query returns true, the related entries are merged during the remediation of a de-duplication task. If false, related entries aren’t merged.```
"merge_related_items_condition": [
  {
    "related_entry": "String",
    "condition": "String"
  }
]
```

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.most\_relations\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the CI with the most relationships to the main CI.

</td></tr><tr><td>

template.most\_related\_items\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the CI with the most related items to the main CI.

</td></tr><tr><td>

template.name

</td><td>

String

</td><td>

Name of the template.

</td></tr><tr><td>

template.newest\_updated\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the most recently updated CI to the main CI.

</td></tr><tr><td>

template.oldest\_created\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the oldest-created CI to the main CI.

</td></tr><tr><td>

template.table

</td><td>

String

</td><td>

Table for which the template is created.

</td></tr><tr><td>

template.task\_conditions

</td><td>

String

</td><td>

Optional. Encoded query to be evaluated when the template runs. This query is evaluated on the Reconcile Duplicate Task Data \[reconcile\_duplicate\_task\_data\] table. All tasks returned from this query are considered during the template evaluation. **Note:** Even if a task is returned as a part of the query, it doesn’t guarantee that the template run processes the task. Other factors might cause the task to be skipped during template processing.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the template created in the Reconcile Duplicate Templates \[reconcile\_duplicate\_template\] table.|

The following example shows how to create a de-duplication template.

```
var template = {
  "name": "Test Windows Template",
  "table": "cmdb_ci_win_server",
  "description": "This is a Windows server template",
  "master_ci_option": "oldest_created",
  "master_ci_condition": "",
  "allow_null_attribute_update": false,
  "allow_master_ci_null_update": false,
  "oldest_created_merge_attributes": "serial_number,os_version",
  "merge_relations": "all",
  "merge_relations_condition": "",
  "merge_related_items": "conditional",
  "merge_related_items_condition": [
    {
      "related_entry": "change_request.cmdb_ci",
      "condition": "ramCONTAINS1024"
    },
    {
      "related_entry": "incident.cmdb_ci",
      "condition": "os_versionCONTAINSWindows"
    }
  ],
  "duplicate_ci_action": "delete",
  "duplicate_ci_updates":   [{
    "element": "ram",
    "element_label": "RAM (MB)",
    "value": "1024",
    "display": "1024"
  }],
  "task_conditions": "category=attribute^key=serial_number^value=E2BX1^EQ"
};

var templateId = sn_cmdb.DuplicateTemplate.createTemplate(template);

gs.info(templateId);
```

Output:

```
8dfcd36e042b2510f877c1665753a485
```

## DuplicateTemplate - getTemplate\(String templateId\)

Gets the template object.

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="row_DupTemp-templateObj"><td>

Object

</td><td>

The template object with different options for creating the template.```
{
  "allow_master_ci_null_update": Boolean,
  "allow_null_attribute_update": Boolean,
  "description": "String",
  "duplicate_ci_action": "String",
  "duplicate_ci_updates": [Array],
  "master_ci_condition": "String",
  "master_ci_option": "String",
  "merge_related_items": "String",
  "merge_related_items_condition": [Array],
  "merge_relations_condition": "String",
  "merge_relations": "String",
  "most_related_items_merge_attributes": "String",
  "most_relations_merge_attributes": "String",
  "name": "String",
  "newest_updated_merge_attributes": "String",
  "oldest_created_merge_attributes": "String",
  "table": "String",
  "task_conditions": "String"
}
```

</td></tr><tr id="row_DupTemp-template-allow-null-attr"><td>

&lt;Object&gt;.allow\_null\_ attribute\_update

</td><td>

Flag that indicates if main CI attributes are updated with null values from duplicate CIs when resolving attribute conflicts for CIs within a de-duplication task.Valid values:

-   true: The main CI attributes are updated with null values from duplicate CIs.
-   false: The main CI attributes aren’t updated with null values from duplicate CIs.

Data type: Boolean

</td></tr><tr id="row_DupTemp-template-master-ci-nul"><td>

&lt;Object&gt;.allow\_master\_ci\_ null\_update

</td><td>

Only includes updates from duplicate CIs if the main CI value is null.Valid values:

-   true: Only include updates from duplicate CIs if the main CI value is null.
-   false: Include updates from all duplicate CIs.

Data type: Boolean

</td></tr><tr id="row_DupTemp-template-desc"><td>

&lt;Object&gt;.description

</td><td>

Description to store more information about the template.Data type: String

</td></tr><tr id="row_DupTemp-template-dup-ci-action"><td>

&lt;Object&gt;.duplicate\_ ci\_action

</td><td>

Specifies if the duplicate CI is to be deleted or updated with unique custom values.Possible options:

-   delete
-   update \(requires specifying **duplicate\_ci\_updates**\)

Data type: String

</td></tr><tr id="row_DupTemp-template-dup-ci-updts"><td>

&lt;Object&gt;.duplicate\_ ci\_updates

</td><td>

Array of objects specifying how the duplicate CI values are updated.```
[
  {
    "element": "String",
    "element_label": "String",
    "value": "String",
    "display": "String"
  }
]
```

Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.element

</td><td>

The system dictionary name of a reference field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.element\_label

</td><td>

The label that the reference field displays.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.value

</td><td>

Value for a reference field, that is, the contents of the reference field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.display

</td><td>

Display value for a reference field.Data type: String

</td></tr><tr id="row_DupTemp-template-master-ci-opt"><td>

&lt;Object&gt;.master\_ci\_ option

</td><td>

Specifies how the main CI is selected for a de-duplication task when applying this template.Possible options:

-   conditional \(must specify **master\_ci\_condition**\)
-   most\_related\_items – Attributes to be merged from the CI with the most related items to the main CI.
-   most\_relations – Attributes to be merged from the CI with the most relationships to the main CI.
-   newest\_created – separated attributes to be merged from the most recently updated CI to the main CI.
-   oldest\_created – Comma-separated attributes to be merged from the oldest-created CI to the main CI.

Data type: String

</td></tr><tr id="row_DupTemp-template-mrg-relations"><td>

&lt;Object&gt;.merge\_relations

</td><td>

Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template.Possible options:

-   all
-   conditional
-   none

Data type: String

</td></tr><tr id="row_DupTemp-template-mrgRel-itms"><td>

&lt;Object&gt;.merge\_related\_items

</td><td>

Specifies which related tables for duplicate CIs within a de-duplication task are merged to the main CI when applying this template. See also [Remediate a de-duplication task \(legacy\)](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).Possible options:

-   all\_available – Includes the default-related tables and any related tables that reference duplicate CIs for the de-duplication task remediated via the template.
-   conditional
-   default – Includes related entries provided by the Duplicate CI Remediator Default Related Items module.
-   none

Data type: String

</td></tr><tr id="row_DupTemp-template-mrgRel-itmCnd"><td>

&lt;Object&gt;.merge\_related\_items\_ condition

</td><td>

List of related entries with an encoded query for each related entry. Each query is evaluated on the main CI that is selected for the task. If the query returns true, the related entries are merged during the remediation of a de-duplication task. If false, related entries aren’t merged.For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Data type: Array

</td></tr><tr id="row_DupTemp-template-most-relationsMA"><td>

&lt;Object&gt;.most\_relations\_ merge\_attributes

</td><td>

Comma-separated attributes to be merged from the CI with the most relationships to the main CI.Data type: String

</td></tr><tr id="row_DupTemp-template-mostRel-itmMA"><td>

&lt;Object&gt;.most\_related\_items\_ merge\_attributes

</td><td>

Comma-separated attributes to be merged from the CI with the most related items to the main CI.Data type: String

</td></tr><tr id="row_DupTemp-template-name"><td>

&lt;Object&gt;.name

</td><td>

Name of the template.Data type: String

</td></tr><tr id="row_DupTemp-template-newst-updtdMA"><td>

&lt;Object&gt;.newest\_updated\_ merge\_attributes

</td><td>

Comma-separated attributes to be merged from the most recently updated CI to the main CI.Data type: String

</td></tr><tr id="row_DupTemp-template-oldst-crtdMA"><td>

&lt;Object&gt;.oldest\_created\_ merge\_attributes

</td><td>

Comma-separated attributes to be merged from the oldest-created CI to the main CI.Data type: String

</td></tr><tr id="row_DupTemp-template-table"><td>

&lt;Object&gt;.table

</td><td>

Table for which the template is created.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.task\_condition\_table

</td><td>

Location of the table task conditions, that is, the Reconcile Duplicate Task Data \[reconcile\_duplicate\_task\_data\] table. The value never changes and the table is intended for internal use only.Data type: String

</td></tr><tr id="row_DupTemp-template-task-cond"><td>

&lt;Object&gt;.task\_conditions

</td><td>

Encoded query to be evaluated when the template runs. This query is evaluated on the Reconcile Duplicate Task Data \[reconcile\_duplicate\_task\_data\] table. All tasks returned from this query are considered during the template evaluation. **Note:** Even if a task is returned as a part of the query, it doesn’t guarantee that the template run processes the task. Other factors might cause the task to be skipped during template processing.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Data type: String

</td></tr></tbody>
</table>The following example shows how to retrieve a template.

```
var template = sn_cmdb.DuplicateTemplate.getTemplate('<template_id>');
gs.info(JSON.stringify(template));
```

Output:

```
{
  "most_relations_merge_attributes": "",
  "task_conditions": "category=attribute^key=serial_number^value=E2BX1^EQ",
  "duplicate_ci_updates": "org.mozilla.javascript.NativeArray@5d3b19ef",
  "description": "This is a Windows server template",
  "master_ci_option": "oldest_created",
  "merge_related_items": "conditional",
  "duplicate_ci_action": "delete",
  "newest_updated_merge_attributes": "",
  "merge_related_items_condition": [
    {
      "condition": "os_versionCONTAINSWindows",
      "related_entry": "incident.cmdb_ci"
    },
    {
      "condition": "ramCONTAINS1024",
      "related_entry": "change_request.cmdb_ci"
    }
  ],
  "most_related_items_merge_attributes": "",
  "merge_relations": "all",
  "task_condition_table": "reconcile_duplicate_task_data",
  "name": "Test Windows Template",
  "allow_null_attribute_update": false,
  "table": "cmdb_ci_win_server",
  "allow_master_ci_null_update": false,
  "oldest_created_merge_attributes": "serial_number,os_version"
}
```

## DuplicateTemplate - previewTemplate\(String templateId, String taskId\)

Generates a preview of how different template options were applied to the de-duplication task and how it’s to be remediated.

This method validates all the required attributes before generating the preview for the task using the template. Templates can be created or updated without specifying the required attributes. The required attributes must be provided to preview any de-duplication task.

The following attributes are required:

-   duplicate\_ci\_action
-   master\_ci\_option
-   merge\_related\_items
-   merge\_relations
-   name
-   table

**Note:** Although this method validates all of the attributes, there’s no requirement for the template to be in the published state for a preview.

Use the [remediateTask\(\)](DuplicateTemplateScopedAPI.md#) method to remediate de-duplication tasks.

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|
|taskId|String|Sys\_id of the de-duplication task listed in the Remediate Duplicate Task \[reconcile\_duplicate\_task\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Preview object with values showing how the de-duplication tasks can be remediated using the template.```
{
  "allClassCIMap": {Object},
  "duplicateCIAction": "String",
  "duplicateCIUpdates": [Array],
  "masterCI": "String",
  "mergeRelations": Boolean,
  "relatedTablesMerged": [Array],  
  "resolvedFieldCIMap": [Array],
  "taskId": "String",
  "tooManyDuplicates": Boolean
}
```

</td></tr><tr><td>

&lt;Object&gt;.allClassCIMap

</td><td>

List of sys\_ids of the CIs within a de-duplication task, grouped by CI class. For example, **cmdb\_ci\_computer**.```
"allClassCIMap": {
  "<ci_class_name>": [
    "<ci_sys_id_1>",
    "<ci_sys_id_2>"
  ]
}
```

Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIAction

</td><td>

Specifies if the duplicate CI is to be deleted or updated with unique custom values.Possible options:

-   delete
-   update \(requires specifying **duplicate\_ci\_updates**\)

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates

</td><td>

Array of objects specifying how the duplicate CI values are updated.```
[
  {
    "element": "String",
    "element_label": "String",
    "value": "String",
    "display": "String"
  }
]
```

Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.element

</td><td>

The system dictionary name of a reference field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.element\_label

</td><td>

The label that the reference field displays.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.value

</td><td>

Value for a reference field, that is, the contents of the reference field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.duplicateCIUpdates.display

</td><td>

Display value for a reference field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.masterCI

</td><td>

Sys\_id of the CI that was selected as the main CI.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.mergeRelations

</td><td>

Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template.Possible options:

-   all
-   conditional
-   none

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.relatedTablesMerged

</td><td>

Specifies which related tables for duplicate CIs within a de-duplication task are merged to the main CI when applying this template. See also [Remediate a de-duplication task \(legacy\)](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).Possible options:

-   all\_available – Includes the default-related tables and any related tables that reference duplicate CIs for the de-duplication task remediated via the template.
-   conditional
-   default – Includes related entries provided by the Duplicate CI Remediator Default Related Items module.
-   none

Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.resolvedFieldCIMap

</td><td>

Array of elements to be merged from duplicate CIs to the main CI.```
"resolvedFieldCIMap": [
  {
    "element": "String",
    "sys_id": "String"
  }
]
```

Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.resolvedFieldCIMap.​element

</td><td>

Name of the element to be merged from a duplicate CI to the main CI.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.resolvedFieldCIMap.​sys\_id

</td><td>

Sys\_id of the element to be merged from a duplicate CI to the main CI.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.taskId

</td><td>

Sys\_id of the de-duplication task listed in the Remediate Duplicate Task \[reconcile\_duplicate\_task\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.tooManyDuplicates

</td><td>

Flag that indicates whether the task has more than the maximum number of CIs. The threshold is determined by comparing the value of the system property glide.duplicate\_ci\_ remediator.max.cis \(default value 1000 CIs\).Valid values:

-   true: Task number of CIs exceeds the maximum number of CIs.
-   false: Task number of CIs don't exceed the maximum number of CIs.

Data type: Boolean

</td></tr></tbody>
</table>The following example shows how to get a preview of de-duplication remediation for a specified template.

```
var preview = sn_cmdb.DuplicateTemplate.previewTemplate("<template_id>", "<task_id>");
gs.info(JSON.stringify(preview));
```

Output:

```
{
  "taskId": "<task_id>",
  "masterCI": "<ci_sys_id_1>",
  "allClassCIMap": {
    "cmdb_ci_computer": [
      "<ci_sys_id_1>",
      "<ci_sys_id_2>"
    ]
  },
  "resolvedFieldCIMap": [
    {
      "element": "ram",
      "sys_id": "<ci_sys_id_2>"
    },
    {
      "element": "os_version",
      "sys_id": "<ci_sys_id_2>"
    }
  ],
  "mergeRelations": true,
  "relatedTablesMerged": [
    "incident.cmdb_ci",
    "change_request.cmdb_ci"
  ],
  "duplicateCIAction": "delete",
  "duplicateCIUpdates": [],
  "tooManyDuplicates": false
}
```

## DuplicateTemplate - publishTemplate\(String templateId\)

Publishes a template. When successful, the template moves from draft to published state.

This method validates all the required attributes before publishing the template. You can create or update templates without specifying the required attributes, but the attributes must be provided before publishing a template.

The following attributes are required:

-   duplicate\_ci\_action
-   master\_ci\_option
-   merge\_related\_items
-   merge\_relations
-   name
-   table

In published state, you can run the template using the [runTemplate\(\)](DuplicateTemplateScopedAPI.md#) method.

See also:

-   [previewTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [unPublishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [updateTemplate\(\)](DuplicateTemplateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the template was published.

 Valid values:

-   true: The template was published.
-   false: The template wasn’t published.

</td></tr></tbody>
</table>The following example shows how to publish a template and display results.

```
var isPublished = sn_cmdb.DuplicateTemplate.publishTemplate('<template_id>');
gs.info(isPublished);
```

Output:

```
true
```

## DuplicateTemplate - remediateTask\(String templateId, String taskId\)

Remediates a de-duplication task using the template.

If the template isn’t in the published state, the template can't be run and the method throws an exception.

Use the [previewTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to preview how de-duplication tasks are to be remediated.

See also.

-   [Duplicate CIs remediation](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [Remediate a de-duplication task \(legacy\)](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|
|taskId|String|Sys\_id of the de-duplication task listed in the Remediate Duplicate Task \[reconcile\_duplicate\_task\] table.|

|Type|Description|
|----|-----------|
|String|If successful, the merge resolution ID for the de-duplication task remediation. This merge resolution ID the sys\_id of a record in the Duplicate CI Remediation \[cmdb\_duplicate\_ci\_remediation\] table. If unsuccessful, the template might not be in the published state.|

The following example shows how to remediate a de-duplication task.

```
var mergeResolutionId = sn_cmdb.DuplicateTemplate.remediateTask("<template_id>", "<task_id>");
gs.info(mergeResolutionId);
```

Output:

```
<merge_resolution_id>
```

## DuplicateTemplate - requestCancellation\(String templateRunId\)

Cancels an existing template run.

A cancel request can only be made for a template run if it's in draft, ready, or running state.

After a template run cancel request, the template run state changes to the intermediate stage Cancel Requested.

Running this method doesn’t automatically cancel template runs in Ready or Draft state. The template run state doesn’t change to Cancelled until any tasks running are complete. At that point any remaining tasks staged for remediation change from cancel requested to canceled.

See also:

-   [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [runTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [retireTemplate\(\)](DuplicateTemplateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|templateRunId|String|Sys\_id of the template run listed in the De-Duplication Template Run \[reconcile\_duplicate\_template\_run\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Flag that indicates whether the cancel request was successful.

 Valid values:

-   true: The cancel request was successful.
-   false: The cancel request wasn’t successful.

</td></tr></tbody>
</table>The following example shows how to cancel a template run and display whether the operation is successful.

```
var isCancelled = sn_cmdb.DuplicateTemplate.requestCancellation("487c67e2046b2510f877c1665753a4cc");
gs.info(isCancelled);
```

Output:

```
true
```

## DuplicateTemplate - retireTemplate\(String templateId\)

Retires a template.

Use this method to move a template to the retire state if it’s no longer needed.

The template can't be retired and the method throws an exception under the following conditions:

-   The template is in the published state.
-   The template is running or scheduled to run.

See also:

-   [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [runTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [requestCancellation\(\)](DuplicateTemplateScopedAPI.md#)
-   [DuplicateTemplate - unPublishTemplate\(String templateId\)](DuplicateTemplateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the template is retired.Valid values:

-   true: The template is retired.
-   false: The template couldn’t be retired because it was running, scheduled to be run, or in published state

</td></tr></tbody>
</table>The following example shows how to retire a template and display results.

```
var isRetired = sn_cmdb.DuplicateTemplate.retireTemplate(<template_id>);
gs.info(isRetired);
```

Output:

```
true
```

## DuplicateTemplate - runTemplate\(String templateId\)

Schedules a remediation run for a de-duplication template in the published state. A template can be run multiple times but you can only schedule one run at a time.

If the template isn’t in published state, it can't be run and the method throws an exception. Use the [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#) method to move the template from draft to published state.

To cancel a running task, use the [requestCancellation\(\)](DuplicateTemplateScopedAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the template that was run listed in the De-Duplication Template Run \[reconcile\_duplicate\_template\_run\] table. If unsuccessful, the template might not be in published state.|

The following example shows how to schedule a run for a published de-duplication template.

```
var template = sn_cmdb.DuplicateTemplate.runTemplate('<template_id>');
gs.info(JSON.stringify(template));
```

Output:

```
487c67e2046b2510f877c1665753a4cc
```

## DuplicateTemplate - unPublishTemplate\(String templateId\)

Unpublishes a template.

This method moves the template from the published state to the draft state, which enables updating the template. The template can't be unpublished if it is running or scheduled to be run.

See also:

-   [publishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [requestCancellation\(\)](DuplicateTemplateScopedAPI.md#)
-   [updateTemplate\(\)](DuplicateTemplateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|templateId|String|Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.|

<table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the template was successfully unpublished.

 Valid values:

-   true: The template was successfully unpublished.
-   false: The template wasn’t successfully unpublished. The template might be running or scheduled to be run.

</td></tr></tbody>
</table>The following example shows how to unpublish a template and display results.

```
var isUnPublished = sn_cmdb.DuplicateTemplate.unPublishTemplate(<template_id>);
gs.info(isUnPublished);
```

Output:

```
true
```

## DuplicateTemplate - updateTemplate\(String templateId, Object template\)

Updates a de-duplication template in draft state.

See also:

-   [unPublishTemplate\(\)](DuplicateTemplateScopedAPI.md#)
-   [canAddTasksToTemplate\(\)](DuplicateTemplateScopedAPI.md#)

<table id="table_rl4_t5c_txb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

templateId

</td><td>

String

</td><td>

Sys\_id of the template listed in the Reconcile Duplicate Template \[reconcile\_duplicate\_template\] table.

</td></tr><tr><td>

template

</td><td>

Object

</td><td>

The template object with different options for creating the template. ```
{
  "allow_master_ci_null_update": Boolean,
  "allow_null_attribute_update": Boolean,
  "description": "String",
  "duplicate_ci_action": "String",
  "duplicate_ci_updates": [Array],
  "master_ci_condition": "String",
  "master_ci_option": "String",
  "merge_related_items": "String",
  "merge_related_items_condition": [Array],
  "merge_relations_condition": "String",
  "merge_relations": "String",
  "most_related_items_merge_attributes": "String",
  "most_relations_merge_attributes": "String",
  "name": "String",
  "newest_updated_merge_attributes": "String",
  "oldest_created_merge_attributes": "String",
  "table": "String",
  "task_conditions": "String"
}
```

</td></tr><tr><td>

template.allow\_null\_​attribute\_update

</td><td>

Boolean

</td><td>

Optional. Flag that indicates if main CI attributes are updated with null values from duplicate CIs when resolving attribute conflicts for CIs within a de-duplication task.Valid values:

-   true: The main CI attributes are updated with null values from duplicate CIs.
-   false: The main CI attributes aren’t updated with null values from duplicate CIs.

Default: False

</td></tr><tr><td>

template.allow\_master\_ci\_​null\_update

</td><td>

Boolean

</td><td>

Optional. Only includes updates from duplicate CIs if the main CI value is null.Flag that indicates whether to include only updates from duplicate CIs if the main CI value is null.

Valid values:

-   true: Only include updates from duplicate CIs if the main CI value is null.
-   false: Include updates from all duplicate CIs.

Default: False

</td></tr><tr><td>

template.description

</td><td>

String

</td><td>

Optional. Description to store more information about the template.

</td></tr><tr><td>

template.duplicate\_​ci\_action

</td><td>

String

</td><td>

Optional. Specifies if the duplicate CI is to be deleted or updated with unique custom values.Possible options:

-   delete
-   update \(requires specifying **duplicate\_ci\_updates**\)

</td></tr><tr><td>

template.duplicate\_​ci\_updates

</td><td>

Array

</td><td>

Optional, unless the setting for **duplicate\_ci\_action** is `update`. Array of objects specifying how the duplicate CI values are updated.```
[
  {
    "element": "String",
    "element_label": "String",
    "value": "String",
    "display": "String"
  }
]
```

</td></tr><tr><td>

template.duplicate\_​ci\_updates.element

</td><td>

String

</td><td>

The system dictionary name of a reference field.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.element\_label

</td><td>

String

</td><td>

The label that the reference field displays.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.value

</td><td>

String

</td><td>

Value for a reference field, that is, the contents of the reference field.

</td></tr><tr><td>

template.duplicate\_​ci\_updates.display

</td><td>

String

</td><td>

Display value for a reference field.

</td></tr><tr><td>

template.master\_ci\_​option

</td><td>

String

</td><td>

Optional. Specifies how the main CI is selected for a de-duplication task when applying this template. Possible options:

-   conditional \(must specify **master\_ci\_condition**\)
-   most\_related\_items – Attributes to be merged from the CI with the most related items to the main CI.
-   most\_relations – Attributes to be merged from the CI with the most relationships to the main CI.
-   newest\_created – separated attributes to be merged from the most recently updated CI to the main CI.
-   oldest\_created – Comma-separated attributes to be merged from the oldest-created CI to the main CI.

</td></tr><tr><td>

template.master\_ci\_condition

</td><td>

String

</td><td>

Optional \(required if the value of **master\_ci\_option** is `conditional`\). Encoded query to specify how the main CI is selected. If multiple CIs or no CIs match the query, the method selects the most recently updated CI as the main CI. The encoded query is evaluated for the template table. This table is identified in the **table** property.For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.merge\_relations

</td><td>

String

</td><td>

Optional. Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template. Possible options:

-   all
-   conditional
-   none

</td></tr><tr><td>

template.merge\_relations

</td><td>

String

</td><td>

Optional. Specifies how the relationships for duplicate CIs within a de-duplication task are merged when applying this template. Possible options:

-   all
-   conditional
-   none

</td></tr><tr><td>

template.merge\_relations\_​condition

</td><td>

String

</td><td>

Optional \(required if the value of **merge\_relations** is `conditional`\). Encoded query to specify if all or none of the relationships from duplicate CIs are merged. The query is evaluated on the main CI that is selected for the de-duplication task. If the query returns true, all relationships are merged. If false, no relationships are merged.The encoded query is evaluated for the template table. This table is identified in the **table** property.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.merge\_related\_items

</td><td>

String

</td><td>

Optional. Specifies which related tables for duplicate CIs within a de-duplication task are merged to the main CI when applying this template. See also [Remediate a de-duplication task \(legacy\)](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).Possible options:

-   all\_available – Includes the default-related tables and any related tables that reference duplicate CIs for the de-duplication task remediated via the template.
-   conditional
-   default – Includes related entries provided by the Duplicate CI Remediator Default Related Items module.
-   none

</td></tr><tr><td>

template.merge\_related\_items\_​condition

</td><td>

Array

</td><td>

Optional. List of related entries with an encoded query for each related entry. Each query is evaluated on the main CI that is selected for the task. If the query returns true, the related entries are merged during the remediation of a de-duplication task. If false, related entries aren’t merged.```
"merge_related_items_condition": [
  {
    "related_entry": "String",
    "condition": "String"
  }
]
```

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

template.most\_relations\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the CI with the most relationships to the main CI.

</td></tr><tr><td>

template.most\_related\_items\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the CI with the most related items to the main CI.

</td></tr><tr><td>

template.name

</td><td>

String

</td><td>

Name of the template.

</td></tr><tr><td>

template.newest\_updated\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the most recently updated CI to the main CI.

</td></tr><tr><td>

template.oldest\_created\_​merge\_attributes

</td><td>

String

</td><td>

Optional. Comma-separated attributes to be merged from the oldest-created CI to the main CI.

</td></tr><tr><td>

template.table

</td><td>

String

</td><td>

Table for which the template is created.

</td></tr><tr><td>

template.task\_conditions

</td><td>

String

</td><td>

Optional. Encoded query to be evaluated when the template runs. This query is evaluated on the Reconcile Duplicate Task Data \[reconcile\_duplicate\_task\_data\] table. All tasks returned from this query are considered during the template evaluation. **Note:** Even if a task is returned as a part of the query, it doesn’t guarantee that the template run processes the task. Other factors might cause the task to be skipped during template processing.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table><table id="table_sl4_t5c_txb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the template was updated.

 Valid values:

-   true: The template was updated.
-   false: The template was updated. The template might not be in draft \(unpublished\) state.

</td></tr></tbody>
</table>The following example shows how to update several properties of an existing de-duplication template.

```
var template = {
  "name": "Test Windows Template",
  "table": "cmdb_ci_win_server",
  "description": "This is a windows server template",
  "master_ci_option": "newest_updated",
  "master_ci_condition": "",
  "allow_null_attribute_update": false,
  "allow_master_ci_null_update": false,
  "oldest_created_merge_attributes": "",
  "newest_updated_merge_attributes": "ram,cpu_count",
  "most_relations_merge_attributes": "",
  "most_related_items_merge_attributes": "",
  "merge_relations": "all",
  "merge_relations_condition": "",
  "merge_related_items": "conditional",
  "merge_related_items_condition": [
    {
      "related_entry": "change_request.cmdb_ci",
      "condition": "ramCONTAINS1024"
    },
    {
      "related_entry": "incident.cmdb_ci",
      "condition": "os_versionCONTAINSWindows"
    }
  ],
  "duplicate_ci_action": "delete",
  "duplicate_ci_updates": "",
  "task_conditions": "category=attribute^key=serial_number^value=E2BX1^EQ"
};

sn_cmdb.DuplicateTemplate.updateTemplate(<template_id>, template);
```

Output:

```
true
```

