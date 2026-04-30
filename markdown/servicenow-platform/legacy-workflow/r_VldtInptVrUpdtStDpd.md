---
title: ValidateInputVarUpdateSetDependencies
description: The ValidateInputVarUpdateSetDependencies validator examines update sets to ensure that workflow input variables for a given workflow have not been deleted in different update sets than those currently In progress.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateInputVarUpdateSetDependencies

The **ValidateInputVarUpdateSetDependencies** validator examines update sets to ensure that workflow input variables for a given workflow have not been deleted in different update sets than those currently **In progress**.

## Validation summary

-   Risk: Workflows and their input variables are not moved together in a single update set. The deletion of input variables is captured in a different update entry. If these two entries are not in the same update set, the workflow execution can be unstable.
-   Purpose: Determine whether input variables that belonged to this workflow were deleted in a different update set.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: There were no Input Variable Update Set dependency issues found.
-   Invalid Result: Invalid
-   Invalid Message: There are input variables that have been deleted and logged in a different update set.
-   Suggested Action: If the deletion is not intended to be separate from the workflow, ensure that both update sets are committed concurrently to the new instance, or merge both payloads into a single update set.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow movement with update sets](../../workflow-administration/concept/c_WorkflowMovementWithUpdateSets.md#)

## Troubleshooting

Workflow input variables get individual entries in the **Customer Update** related list in the current user's update set. This validator reports to the user when workflow input deletions have happened in an update set other than the current user's update set.

Follow the instructions for [Input variable removal](../../workflow-administration/concept/c_InputVariableRemoval.md#) when the validator issues this warning.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

