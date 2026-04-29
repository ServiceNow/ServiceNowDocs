---
title: Use workflow stages
description: You can add or modify workflow stages.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use workflow stages

You can add or modify workflow stages.

## Before you begin

Role required: workflow\_admin, workflow\_creator, or admin

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Create a new workflow by clicking **New** or open an existing workflow.

3.  In the Workflow Properties form, if the table is not the Requested Item \[sc\_req\_item\] table, select a field to display stages in the **Stage** field property.

    [Available fields](../concept/c_WorkflowStages.md) depend on the table selected for the workflow.

4.  After assigning a list of stages to the workflow, you can set a stage value in any of the workflow activities that provide a **Stage** field in their dialog box.

    Setting a stage value in a workflow activity tells the workflow engine to assign that stage to the record associated with the workflow context when the activity is encountered during a run.

    When an activity starts with a specified stage, the platform updates the **Stage** field with the current value. In workflows run against the Requested Item \[sc\_req\_item\] table, the `sc_req_item.stage` field is defined as a workflow type field.

    When displaying the stages for a workflow on the Requested Item \[sc\_req\_item\] table, the stage state is based on the state of the workflow activities. If an activity has a stage specified for it, and the activity is currently active in the workflow, then the stage is shown with an **In progress** state. Similarly, if the activity is in the **Pending** or **Completed** state, the stage reflects this state.

5.  To edit the workflow-specific stages for an existing workflow, click the gear icon in the header bar and select **Edit Stages**.

    Again, these stage values are combined with the choices, defaults, and existing values.

    ![Workflow Stages Menu Option](../image/WorkflowStagesMenuOption.png)


## Workflow stages

To optimize the use of stages, you can assign a stage to multiple activities in a workflow. For example, if your workflow uses the following activities to create tasks:

1.  Get approval
2.  Order equipment
3.  Receive equipment
4.  Add equipment to CMDB
5.  Set up equipment
6.  Install software
7.  Configure software
8.  Deliver to user

The following stages might be used:

-   Approval
-   Order
-   Configure
-   Deliver

A good practice is to assign stages to the activities as follows:

|Activity|Assigned stage|
|--------|--------------|
|Get approval|Approval|
|Order equipment|Order|
|Receive equipment|Order|
|Add equipment to CMDB|Order|
|Set up equipment|Configure|
|Install software|Configure|
|Configure software|Configure|
|Deliver to user|Deliver|

When the **Order equipment**, **Receive equipment**, or **Add equipment to CMDB** activity is active, the **Stage** display shows that the **Order** stage is **In progress**.

**Parent Topic:**[Workflow stages](../concept/c_WorkflowStages.md)

