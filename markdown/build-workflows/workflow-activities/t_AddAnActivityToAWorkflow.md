---
title: Add an activity to a workflow
description: Available activities are displayed in the Core, Packs, and Custom tabs in the Workflow Editor palette.You can duplicate an activity used in a workflow, including all the configured properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-activities/t\_AddAnActivityToAWorkflow.html
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow activities, Classic Workflow, Build workflows]
---

# Add an activity to a workflow

Available activities are displayed in the **Core**, **Packs**, and **Custom** tabs in the Workflow Editor palette.

## Before you begin

Role required: admin

## Procedure

1.  In the Workflow Editor, check out a workflow.

2.  To add a workflow activity, drag it from the **Core**, **Packs**, or **Custom** tab to the canvas and drop it on a transition line in the workflow body.

    The transition turns blue when it is connected to the new activity. The designer adds the activity to the flow at that point and displays the property form for the new activity.

    If an activity is greyed out, [approval engines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/c_ApprovalEngines.md) are enabled for the table on which the workflow runs. To use the activity, turn approval engines off for the table.

    \[Omitted image "WfAddActivityBlocked.png"\] Alt text: Greyed out activities are unavailable because approval engines are enabled for the table on which the workflow runs.

3.  Create any additional conditions needed for the activity and ensure that [all exits are connected](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/t_MngTstnsWkflAct.md).

4.  Run the [workflow validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowValidation.md) tool prior to publishing to detect missing or disconnected transitions that can cause a workflow to hang.

    **Note:** All [activity descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/t_ViewActivityDescriptions.md) have a **Table** value. If this value is **Global**, the activity is available for use with any workflow regardless of the table selected in the workflow properties. Activities that identify a specific table appear in the palette only if the table configured for the workflow matches or extends the table identified in the activity.

    \[Omitted image "WorkflowAddActivity.png"\] Alt text:


## Duplicate a workflow activity

You can duplicate an activity used in a workflow, including all the configured properties.

### Procedure

1.  Right-click the activity and select **Copy Activity** from the context menu.

    The system automatically duplicates the activity, but does not create transitions.

2.  Double-click the copy and configure the properties appropriately.

3.  Drag the activity to a location in the workflow.

4.  Add [transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/t_MngTstnsWkflAct.md).


