---
title: Avoiding duplicate workflows
description: Update sets manage the published state of all versions of a workflow prior to committing the workflow version on a local instance.Follow the steps in this page to commit a workflow in an update set.It is not possible to have multiple published versions as a result of update set commits. However, this does not eliminate risk, and care should be taken when migrating update sets.Update Set B is migrated and committed to the production instance.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Input variable movement, Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Avoiding duplicate workflows

Update sets manage the published state of all versions of a workflow prior to committing the workflow version on a local instance.

The last version of a workflow committed as an Insert or Update using an update set becomes the currently published version, regardless of the publishing sequence for the workflow versions.

**Parent Topic:**[Input variable movement](c_InputVariableMovement.md)

## Commit a workflow in an update set

Follow the steps in this page to commit a workflow in an update set.

### Procedure

1.  Workflow A - Version 1 is created and published in Update Set A.

2.  Update Set A is completed and migrated to a local instance.

3.  When the update set is committed, the system sets all prior versions of Workflow A to published = false.

    In the first migration, there are no prior versions.

4.  Workflow A - Version 1 becomes the only published version of the workflow.


## Update set migration example

It is not possible to have multiple published versions as a result of update set commits. However, this does not eliminate risk, and care should be taken when migrating update sets.

Consider this example:

1.  Workflow A - Version 1 is migrated and committed to the production instance.
2.  Update Set B is created.
3.  Update Set C is created.
4.  Workflow A - Version 2 is published in Update Set B.

    A customer update record is added to Update Set B with the Version 2 payload.

    A customer update record is added to Update Set B with the Version 1 workflow left unpublished.

5.  Update Set B is completed.
6.  Workflow A - Version 3 is published in Update Set C.

    A customer update record is added to Update Set C with the Version 3 payload.

    A customer update record is added to Update Set C with the Version 2 workflow left unpublished.

7.  Update Set C is completed.
8.  Update Set C is migrated and committed to the production instance.

    Workflow A - Version 1 is set to unpublished.

    Workflow A - Version 2 update is skipped since Update Set B, which contains Version 2, was never migrated.

    Workflow A - Version 3 is committed and becomes the only published version of the workflow.


## Update set migration risk

Update Set B is migrated and committed to the production instance.

1.  Workflow A - Version 3 is set to unpublished.
2.  Workflow A - Version 1 remains unpublished.
3.  Workflow A - Version 2 is committed and becomes the only published version of the workflow.

    The workflow has gone back a version, perhaps unintentionally. The regressed version becomes the currently published version.


