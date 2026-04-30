---
title: Copy an action
description: Copy an action to give it a new name and move it to another application scope.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-06-30"
reading_time_minutes: 1
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Copy an action

Copy an action to give it a new name and move it to another application scope.

## Before you begin

Role required: action\_designer or admin

## About this task

You can copy a custom action that you created to give it a new name or move it to another application scope. The new action has the same action properties, inputs, steps, and outputs as the source action.

You can't copy the default actions created by ServiceNow, Inc., nor can you copy actions that have a protection policy. You must have write access to an action to copy it.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select the action that you want to copy.

4.  Click the more actions icon \(![More actions menu](../images/more-actions-menu-icon.png)\) and select **Copy action**.

    **Note:** If the **Copy action** option is not visible, then you don't have permission to copy the action. This could be because the action has a protection policy or because you lack the necessary user role or developer permissions.

5.  In **New action name**, enter a unique name you want the copied action to have.

    ![Copying a get notifications details action.](../images/example-copy-action-modal.png)

6.  From **Application**, select the application scope where you want to copy the action.

7.  Select **Copy**.


## Result

![New copied action.](../images/example-copy-action-result.png)

Workflow Studio opens the new action.

**Parent Topic:**[Create an action in Workflow Studio](create-action.md)

