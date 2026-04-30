---
title: Select a stage field
description: A Stage field allows the workflow context to show additional workflow information, such as the stage name and the estimated completion time for an activity.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a workflow stage field, Workflow stages, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Select a stage field

A **Stage field** allows the workflow context to show additional workflow information, such as the stage name and the estimated completion time for an activity.

## Before you begin

Ensure that the workflow field you want to use as the stage field is configured to properly display stages. For detailed steps, see [Create a workflow stage field](t_CreateAWorkflowStageField.md).

## About this task

Unless the workflow uses the Requested Item \[sc\_req\_item\] table, you can specify which field from the workflow table is the stage field. For workflows that use the Requested Item \[sc\_req\_item\] table, the stage field is automatically set to the **Stage** field of the table and cannot be changed.

To add or edit a workflow stage field:

## Procedure

1.  Navigate to **Workflow &gt; Workflow Editor**.

2.  Create or check out the workflow.

3.  In the title bar, click the menu icon and select **Properties**.

4.  In the Workflow Properties dialog box, click the **General** tab.

5.  In the **Table** list, verify that the table containing the workflow field is selected.

6.  Click the **Stages** tab.

7.  From the **Stage field** list, select the workflow field.

8.  Click **Update**.


**Parent Topic:**[Create a workflow stage field](t_CreateAWorkflowStageField.md)

