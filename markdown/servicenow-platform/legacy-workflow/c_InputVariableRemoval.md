---
title: Input variable removal
description: Deleting workflow input variables, like insert and update actions, creates a customer update record in a user's current update set.An existing workflow already contains two input variables.When editing workflows, particularly when deleting input variables, be sure to use a single update set for all variable editing and workflow publishing.Prior to publishing a workflow version, the system validates the workflow model to assist the designer in planning for deployment.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Input variable movement, Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Input variable removal

Deleting workflow input variables, like insert and update actions, creates a customer update record in a user's current update set.

These deletions migrate to a new instance with the update set, regardless of whether the workflow that owns the input variables is published in the same update set. Plan carefully and use caution when editing a workflow and selecting update sets.

**Parent Topic:**[Input variable movement](c_InputVariableMovement.md)

## Input variable removal risk

An existing workflow already contains two input variables.

1.  The workflow was migrated to a production instance with the two variables.
2.  On a development instance, User A selects Update Set A and checks out the workflow.
3.  User A removes one input variable and all references to it in the workflow.

    The system enters into Update Set A one customer update record reflecting the deletion of the input variable. No record is added for the new workflow version which no longer depends on the input. This does not happen until the workflow is published.

4.  User A continues working on other features in Update Set A that need to be moved to production.
5.  User A completes Update Set A and migrates it to the production instance without publishing the workflow.

    The update set entry that deletes the workflow input variable now applies to the production instance. The prior version of the workflow is running on this instance and still references the missing variable.


## Input variable removal solution

When editing workflows, particularly when deleting input variables, be sure to use a single update set for all variable editing and workflow publishing.

If necessary, merge the update set into a more general set targeted for deployment after the workflow is published. For information about update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

**Note:** If a workflow version is already running on a production system and input variables are deleted from a newer version, those deletions could affect transactions already running against the earlier version. Use extreme caution when deleting workflow input variables and plan the migration carefully.

## Input variable removal prevention

Prior to publishing a workflow version, the system validates the workflow model to assist the designer in planning for deployment.

This validation warns of critical errors that can prevent a workflow from running successfully, but also warns of dependencies and conflicts in update sets. See [ValidateUpdateSetDependencies](../../workflow-validation/reference/r_VldtUpdtStDpnd.md) for more details.

