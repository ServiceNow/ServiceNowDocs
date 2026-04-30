---
title: Workflow error handling
description: The personalized JavaScript that users create in workflow activity variables is vulnerable to run-time syntax errors. Available error information is available in a tooltip when you point to a workflow activity in an error state.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow administration, Classic Workflow, Build workflows]
---

# Workflow error handling

The personalized JavaScript that users create in workflow activity variables is vulnerable to run-time syntax errors. Available error information is available in a tooltip when you point to a workflow activity in an error state.

In the base system, workflow activities do not provide condition routing on the error state. As a result, the workflow progresses based on the state of the current record. For example, a workflow contains an **Approval - User** activity that uses an advanced script to add additional approvers. A syntax error in the script results in no approvers being added. Because a state of **no approvers** is a valid return, even without the syntax error, the approval activity is skipped and the workflow progresses along a positive path. However, this might not be a valid response for the workflow designer who does not want the workflow to progress along the positive path without approvers.

Workflow error handling detects and logs syntax errors and provides a state that the workflow designer can use to add error conditions to the workflow. Use error handling to locate syntax errors in advanced script fields for these workflow activities:

-   Approval - User
-   Approval - Group
-   Catalog Task
-   Create Task
-   If
-   Run Script
-   Notification

## Available error information

This table shows which activities support error exits.

<table id="table_tbm_bgz_qq"><thead><tr><th>

Activity

</th><th>

Workflow log

</th><th>

Red error indicator

</th><th>

Activity state

</th><th>

Activity result

</th><th>

Fault description

</th><th>

Reroute on error

</th></tr></thead><tbody><tr><td>

Approval - User

 Approval - Group

</td><td>

Yes

</td><td>

Yes

</td><td>

Error

</td><td>

Skipped

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Catalog Task

 Create Task

</td><td>

Yes

</td><td>

No

</td><td>

Finished

</td><td>

none

</td><td>

No

</td><td>

No

</td></tr><tr><td>

If

</td><td>

Yes

</td><td>

Yes

</td><td>

Error

</td><td>

none

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Run Script

</td><td>

No

</td><td>

Yes

</td><td>

Error

</td><td>

error

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Notification

</td><td>

Yes

</td><td>

Yes

</td><td>

Error

</td><td>

error

</td><td>

Yes

</td><td>

Yes

</td></tr></tbody>
</table>-   **[Workflow error tracking features](../reference/r_TrackingErrors.md)**  
Error handling provides visual cues within the workflow, such as error descriptions for activities in pop-ups, and detailed log records.
-   **[Create an error condition exit](../task/t_CreateAnErrorConditionExit.md)**  
An administrator can reroute the workflow when a script error occurs by creating an error condition exit for specific activities within the workflow. This allows the workflow to process script errors in a predictable way and not create undesirable results.
-   **[Reconfigure an approval condition](../task/t_ReconfigureAnApprovalCondition.md)**  
Approval activities react differently to script errors than the other activities.

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

