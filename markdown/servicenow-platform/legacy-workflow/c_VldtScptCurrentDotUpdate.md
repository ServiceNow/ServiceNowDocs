---
title: ValidateScriptForCurrentDotUpdate
description: The ValidateScriptForCurrentDotUpdate validator finds workflow activities with scripts that use the current.update\(\) function.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateScriptForCurrentDotUpdate

The **ValidateScriptForCurrentDotUpdate** validator finds workflow activities with scripts that use the current.update\(\) function.

Calling current.update\(\) causes significant performance delays in transaction processing and might cause an instance to hang.

## Validation summary

-   Risk: At best, a workflow that uses current.update\(\) in scripts experiences degraded performance. In the worst case, the workflow enters an infinite, recursive loop that crashes the server.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: The JavaScript in this workflow has no instances of 'current.update\(\)'.
-   Invalid Result: Invalid
-   Invalid Message: This workflow uses 'current.update\(\)' in &lt;count of current.update references&gt; JavaScript statements.
-   Suggested Action: Remove current.update\(\) from the activity scripts cited by this validator. Workflows execute within a transaction, and current is updated, or possibly inserted, at the end of the transaction, as appropriate. There is no need to explicitly update the record during the transaction.
-   Publishable: Yes
-   Runnable: Yes

## Problems with current.update\(\) in workflow scripts

A workflow initiates execution in one of these ways:

-   Script Engine: If a workflow is assigned to a specific table, and given a run condition, the workflow runs on INSERT.
-   Script: Any business rule, script include, background script, or client script can initiate a workflow using the workflow script include and calling startFlow\(\).

The workflow engine initiates a workflow based on the matched criteria of the current record being inserted. The transaction for current is managed by the script engine and not the workflow. Workflows that progress on the update\(\) of the current record are not invoked via the workflow engine, but as a call from either a client script or business rule. In either case, the script engine is invoked, and the current record is put in memory. Edits and modifications to any current fields are made and are available to other activities and scripts that are executed in the same transaction.

When appropriate, other engines that run in sequence with the workflow engine, such as the business rule engine or field normalization, are invoked against the same current record transaction. Any changes made to current through these scripts and activities modify the record in memory. These changing values are available for reference in any other transactions called from activities and scripts in the same INSERT transaction. When all expected changes are executed, the current record is inserted.

When one of these scripts calls current.update\(\) on a record that has yet to be inserted, the action forces an unnecessary and error-prone database transaction. If a record is not yet in the database, it cannot be updated. Business rules that trigger on update\(\) on a record that is in the process of being inserted can cause a very unstable and potentially infinite looping condition.

## Troubleshooting

This validator detects the use of current.update\(\) in any of the editable script fields. Do not call current.update\(\) from within a workflow script. In the event of an INSERT or UPDATE of current, the changes made to current are available to all scripts executing in the same transaction, and the script engine stores all changes in the database. Leave the update of current to the engine. Use the scripts only for setting and referencing the current field values.

**Parent Topic:**[Workflow validator](../reference/r_WorkflowValidator.md)

