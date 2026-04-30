---
title: ValidateSubflows
description: The ValidateSubflows validator detects any workflows included as subflows that are either inactive, deleted, or not available as a published workflow for the current user.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateSubflows

The **ValidateSubflows** validator detects any workflows included as subflows that are either inactive, deleted, or not available as a published workflow for the current user.

Any of these conditions cause the workflow to hang when the workflow activity in the main flow is encountered.

**Warning:** This is a critical error that prevents a workflow from running.

## Validation summary

-   Risk: A parent workflow that transitions to a deleted subflow hangs indefinitely, with no recovery options.
-   Severity Level: Critical
-   Valid Result: Valid
-   Valid Message: This workflow contains &lt;count&gt; valid subflows.
-   Invalid Result: Invalid
-   Invalid Message: This workflow contains &lt;invalid count&gt; invalid subflow\(s\) of &lt;total subflow count&gt; total subflows.
-   Suggested Action: Remove the link in the parent workflow to the questionable subflow, examine the subflow to ensure that it is valid and published, or that it is checked out to the current user. After making the correction to the state of the subflow, run the validation again to test your changes.
-   Publishable: No
-   Runnable: No
-   Related Information: [Workflows used as subflows](../../workflow-activities/reference/workflows-as-subflows.md)

## Troubleshooting

When a workflow runs, regardless of whether it is a subflow or a main flow, the script engine determines which version of a workflow should execute, given the current user and workflow conditions. When a workflow is checked out by the same user who is running the workflow, the checked out version is the version that executes. If the user is not the same person who has the workflow checked out, the published version of the workflow executes. If there is no published workflow, no workflow runs.

One scenario addressed by the **ValidateSubflows** validator is when a workflow:

-   Is checked out to User A.
-   Is a subflow in a parent workflow being run by User B.
-   Has no published alternative to the subflow being run by User B.

When this occurs, the parent workflow runs to the execution of the unpublished subflow and then hangs at that activity, with no means to transition forward. Main flows that encounter this condition in a subflow are not permitted to execute against a current record's transaction. Instead, a critical log entry detailing the subflow's state is added to the current workflow's Workflow Context record. To correct the problem, remove the subflow from the main flow, or publish the subflow so it is available to User B. This allows the workflow to execute on the next appropriate transaction.

Another scenario addressed by the **ValidateSubflow** validator is when a workflow:

-   Is a subflow in a parent workflow being run by any user.
-   Has no published alternative to the subflow, because the workflow has been deleted or all versions of the workflow are unpublished or inactive.

**Note:** You cannot delete a from a list or form workflow that is a subflow. However, you can create one of these unstable conditions with advanced scripting, SQL options, or incomplete update sets that contain main flows, but not the referenced subflows. When troubleshooting a workflow that triggered this validator, consider the history of the subflow while assessing the error condition.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

