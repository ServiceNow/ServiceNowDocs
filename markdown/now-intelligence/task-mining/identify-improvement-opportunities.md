---
title: Identify task improvement actions
description: Initiate an automation request from a Task Mining task timeline analysis or share the details of the analysis.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Task Mining, Platform Analytics]
---

# Identify task improvement actions

Initiate an automation request from a Task Mining task timeline analysis or share the details of the analysis.

## Before you begin

The project requires a task timeline analysis to take task improvement actions. A task timeline analysis contains tasks with sequential task time steps of user interactions. Use these task steps as the basis of your improvement opportunities. For more information, see [Task Mining analyses](../concept/task-mining-dashboard.md).

Automation Center must be installed to initiate an automation request. To use the Now Assist feature in the integration, you must install Now Assist for Platform and activate the User Task Step Summarization skill. For more information, see [Integration with Automation Center](../concept/integration-with-automation-center.md).

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the project with a task timeline analysis that you want to identify task improvement actions for and select the **Task timeline** tab.

3.  Select the task that you want to act on.

    ![Screenshot showing the task steps view.](../image/tm-io-1.png)

4.  Create a copy to make any edits and to take task improvement actions.

    1.  Select **Edit** to create a copy that you use for automation without affecting the original.

    2.  Enter a descriptive name in the **Task name** field.

    3.  Select **Duplicate to edit**.

        ![Screenshot showing the edit task steps dialog.](../image/tm-io-2.png)

    The new task is created with the task name appended with Editable.

5.  Edit any of these steps if you want to change task details.

    1.  Select the Duplicate step icon ![](../image/task-mining-duplicate-step.png) in the left column to make a copy of the step.

        The new task step is created. The **Interaction** column of the duplicated step is empty.

    2.  Select the Delete step icon ![](../image/tm-delete-step-icon.png) in the left column to remove a step from the task.

    3.  Select the Reorder step icon ![](../image/tm-reorder-icon.png) in the left column to drag the step to a different order.

    4.  Double-click a task field \(or use the keyboard shortcut\) to edit details, enter the new text, and select **Apply**.

        You can’t edit the **Source** and **Datetime** fields.

    ![Screenshot showing the editable task steps view.](../image/tm-io-3.png)

6.  Select**Take action**.

7.  Select the task improvement action that you want to take, and select **Continue**.

    The available options are:

    -   **Request automation**

        Open an Automation Center request based on the improvement opportunity. For more information, see step 8.

        **Note:** If an automation request has already been made for this task, a message with a link to the existing automation request is provided.

    -   **Share link**

        Share details of the task to initiate further action. A link is copied to the task steps. You can choose who to send the improvement initiative to.

    ![Screenshot showing the Take action options.](../image/tm-io-4.png)

8.  Select **Generate details** to populate the **Description** and **Detailed sequence of steps** fields with data from the tasks.

    Review all auto-generated instructions and correct any inaccuracies. The detailed sequence of steps is the basis of the automation.

    A maximum of 250 steps can be generated. If your task has more than 250 steps, try selecting a more appropriate task. If you want to continue with the task, you can simplify the steps to reduce their number. Alternatively, you can manually populate the **Description** field with step details and complete the automation request form.

    **Note:** The generate details option is available only if Now Assist for Platform is installed and the User Task Step Summarization skill is activated.

    ![Screenshot showing the New Automation Request form.](../image/tm-automation-request.png)

9.  Add a value in the **Frequency** field to specify in minutes how often the process should be executed.

10. Add business applications associated with the process in the **Applications used** field.

11. Select **Save**.

    The automation request is created and associated with the task that it was based on. A link to the automation request record is available under the **Automation request** column of the projects Task timeline analysis.


**Related topics**  


[Integration with Automation Center](../concept/integration-with-automation-center.md)

[Task Mining analyses](../concept/task-mining-dashboard.md)

