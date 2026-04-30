---
title: Copy a flow
description: Copy a flow to give it a new name and move it to another application scope.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a flow, Building flows, Use, Workflow Studio, Build workflows]
---

# Copy a flow

Copy a flow to give it a new name and move it to another application scope.

## Before you begin

Role required: admin or flow\_designer

## About this task

You can copy a flow to give it a new name or move it to another application scope. The new flow has the same flow properties, trigger, actions, and flow logic as the source flow.

You can't copy flows that have a protection policy. You must have write access to a flow to copy it.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Flows**.

3.  Open the flow that you want to copy.

4.  Click the more actions icon \(![More actions menu](../images/more-actions-menu-icon.png)\) and select **Copy flow**.

    **Note:** If the **Copy flow** option is not visible, then you don't have permission to copy the flow. This could be because the flow has a protection policy or because you lack the necessary user role or developer permissions.

5.  In **New flow name**, enter a unique name you want the copied flow to have.

    ![Copying an email flow.](../images/example-copy-flow-modal.png)

6.  From **Application**, select the application scope where you want to copy the flow.

7.  Select **Copy**.


## Result

![New copied flow.](../images/example-copy-flow-result.png)

Workflow Studio opens the new flow.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

