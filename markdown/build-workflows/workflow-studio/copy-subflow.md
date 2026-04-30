---
title: Copy a subflow
description: Copy a subflow to give it a new name and move it to another application scope.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Building subflows, Use, Workflow Studio, Build workflows]
---

# Copy a subflow

Copy a subflow to give it a new name and move it to another application scope.

## Before you begin

Role required: admin or flow\_designer

## About this task

You can copy a subflow to give it a new name or move it to another application scope. The new subflow has the same subflow properties, inputs, actions, flow logic, and outputs as the source subflow.

You can't copy subflows that have a protection policy. You must have write access to a subflow to copy it.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  Select the subflow that you want to copy.

4.  Click the more actions icon \(![More actions menu](../images/more-actions-menu-icon.png)\) and select **Copy subflow**.

    **Note:** If the **Copy subflow** option is not visible, then you don't have permission to copy the subflow. This could be because the subflow has a protection policy or because you lack the necessary user role or developer permissions.

5.  In **New subflow name**, enter a unique name you want the copied subflow to have.

    ![Copying an item review subflow.](../images/example-copy-subflow-modal.png)

6.  From **Application**, select the application scope where you want to copy the subflow.

7.  Select **Copy**.


## Result

![New copied subflow.](../images/example-copy-subflow-result.png)

Workflow Studio opens the new subflow.

**Parent Topic:**[Building subflows](../concept/subflows.md)

