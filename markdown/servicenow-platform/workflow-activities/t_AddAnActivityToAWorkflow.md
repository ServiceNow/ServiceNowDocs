---
title: Add an activity to a workflow
description: Available activities are displayed in the Core, Packs, and Custom tabs in the Workflow Editor palette.You can duplicate an activity used in a workflow, including all the configured properties.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add an activity to a workflow

Available activities are displayed in the **Core**, **Packs**, and **Custom** tabs in the Workflow Editor palette.

## Before you begin

Role required: admin

## Procedure

1.  In the Workflow Editor, check out a workflow.

2.  To add a workflow activity, drag it from the **Core**, **Packs**, or **Custom** tab to the canvas and drop it on a transition line in the workflow body.

    The transition turns blue when it is connected to the new activity. The designer adds the activity to the flow at that point and displays the property form for the new activity.

    If an activity is greyed out, [approval engines](../../service-administration/concept/c_ApprovalEngines.md) are enabled for the table on which the workflow runs. To use the activity, turn approval engines off for the table.

    ![Greyed out activities are unavailable because approval engines are enabled for the table on which the workflow runs.](../image/WfAddActivityBlocked.png "Unavailable activities and approval engines")

3.  Create any additional conditions needed for the activity and ensure that [all exits are connected](t_MngTstnsWkflAct.md#).

4.  Run the [workflow validation](../../workflow-validation/concept/c_WorkflowValidation.md) tool prior to publishing to detect missing or disconnected transitions that can cause a workflow to hang.

    **Note:** All [activity descriptions](t_ViewActivityDescriptions.md#) have a **Table** value. If this value is **Global**, the activity is available for use with any workflow regardless of the table selected in the workflow properties. Activities that identify a specific table appear in the palette only if the table configured for the workflow matches or extends the table identified in the activity.

    ![](../image/WorkflowAddActivity.png "Adding an activity to a workflow")


## Duplicate a workflow activity

You can duplicate an activity used in a workflow, including all the configured properties.

### Procedure

1.  Right-click the activity and select **Copy Activity** from the context menu.

    The system automatically duplicates the activity, but does not create transitions.

2.  Double-click the copy and configure the properties appropriately.

3.  Drag the activity to a location in the workflow.

4.  Add [transitions](t_MngTstnsWkflAct.md#).


