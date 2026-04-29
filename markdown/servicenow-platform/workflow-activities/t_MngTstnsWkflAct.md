---
title: Manage transitions between workflow activities
description: Transitions define the processing path of the workflow, depending on conditions defined in each activity.Controls on the Approval - User activity enable an administrator to add additional workflow transitions to the activity other than the default transitions of Approved or Rejected.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage transitions between workflow activities

Transitions define the processing path of the workflow, depending on conditions defined in each activity.

## Before you begin

Role required: admin

## About this task

All conditions in an activity must have a transition and all transitions must have a connection to another activity or to the **End** activity.

**Note:**

Run the [workflow validation](../../workflow-validation/concept/c_WorkflowValidation.md) tool prior to publishing to detect missing or disconnected transitions that could cause a workflow to hang.

## Procedure

1.  Add transitions to the workflow using either of these methods:

    -   Drag and drop an activity directly onto a transition line to connect it to the adjacent activities. The transition line turns blue when the connection is made. The system updates the transitions automatically to reflect the new sequence.

        ![Add a transition by dragging and dropping an activity on an existing transition line.](../image/WorkflowAddActivity.png)

    -   Drag the activity to an open area in the canvas and create the transitions manually. Click the yellow square on the right side of the activity condition and drag a connector to the next task.

        ![Draw a line from one activity to another to create a transition manually.](../../workflow-activities/image/CreateTransitionManually.png)

2.  You can draw multiple transitions from the same activity condition if the activity executes concurrently.

3.  To remove a transition, click to highlight it, and then press **Delete**.


## Custom activity transitions

Controls on the **Approval - User** activity enable an administrator to add additional workflow transitions to the activity other than the default transitions of **Approved** or **Rejected**.

Transitions defined using this method do not become a permanent feature of the **Approval - User** activity. After a new transition is configured, that transition must be applied manually to subsequent instances of the activity, where desired.

