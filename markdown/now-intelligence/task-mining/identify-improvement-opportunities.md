---
title: Identify task improvement actions
description: Initiate an automation request from a Task Mining task timeline analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/identify-improvement-opportunities.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Task Mining, Platform Analytics]
---

# Identify task improvement actions

Initiate an automation request from a Task Mining task timeline analysis.

## Before you begin

The project requires a task timeline analysis to take task improvement actions. A task timeline analysis contains tasks with sequential task time steps of user interactions. Use these task steps as the basis of your improvement opportunities. For more information, see [Task Mining analyses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/task-mining-dashboard.md).

Automation Center must be installed to initiate an automation request. To use the Now Assist feature in the integration, you must install Now Assist for Platform and activate the User Task Step Summarization skill. For more information, see [Integration with Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/integration-with-automation-center.md).

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

Create automation requests for your tasks directly from Task Mining. Capture both steps and desktop actions automation properties in a single recording session, instead of recording the same process twice. When a Task Mining analyst submits an automation request, the recording is delivered to the automation team with all UI properties needed to build desktop actions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the project with a task timeline analysis that you want to identify task improvement actions for and select the **Task timeline** tab.

3.  Select the task that you want to act on.

    \[Omitted image "tm-io-1.png"\] Alt text: Screenshot showing the task steps view.

4.  Create a copy to make any edits and to take task improvement actions.

    1.  Select **Edit** to create a copy that you use for automation without affecting the original.

    2.  Enter a descriptive name in the **Task name** field.

    3.  Select **Duplicate to edit**.

        \[Omitted image "tm-io-2.png"\] Alt text: Screenshot showing the edit task steps dialog.

    The new task is created with the task name appended with Editable.

5.  Edit any of these steps if you want to change task details.

    1.  Select the Duplicate step icon \[Omitted image "task-mining-duplicate-step.png"\] next to the step to make a copy of the step.

        The new task step is created. The **Interaction** column of the duplicated step is empty.

    2.  Select the Delete step icon \[Omitted image "tm-delete-step-icon.png"\] next to the step to remove a step from the task.

    3.  Select the Reorder step icon \[Omitted image "tm-reorder-icon.png"\] next to the step to drag the step to a different order.

    4.  Double-click a task field \(or use the keyboard shortcut\) to edit details, enter the new text, and select **Apply**.

        You can’t edit the **Source** and **Datetime** fields.

    \[Omitted image "tm-io-3.png"\] Alt text: Screenshot showing the editable task steps view.

6.  Select **Request automation**.

7.  Select the task improvement action that you want to take, and select **Continue**.

    The available options are:

    -   **__Generate with AI__**

        Open an Automation Center request based on the improvement opportunity. Populate the **Description** and **Detailed sequence of steps** fields with data from the tasks. For more information, see step 8.

    -   **__Complete manually__**

        Fill in the Automation Center request form with details of the improvement opportunity, and submit the request.

        **Note:** If an automation request has already been made for this task, a message with a link to the existing automation request is provided.

8.  Select **Regenerate details** to populate the **Description** and **Detailed sequence of steps** fields with data from the tasks again.

    Review all auto-generated instructions and correct any inaccuracies. The detailed sequence of steps is the basis of the automation.

    A maximum of 250 steps can be generated. If your task has more than 250 steps, try selecting a more appropriate task. If you want to continue with the task, you can simplify the steps to reduce their number. Alternatively, you can manually populate the **Description** field with step details and complete the automation request form.

    **Note:** The generate details option is available only if Now Assist for Platform is installed and the User Task Step Summarization skill is activated.

    \[Omitted image "tm-automation-request.png"\] Alt text: Screenshot showing the New Automation Request form.

9.  Add a value in the **Frequency** field to specify in minutes how often the process should be executed.

10. Add business applications associated with the process in the **Applications used** field.

11. Select **Save**.

    The automation request is created and associated with the task that it was based on. A link to the automation request record is available under the **Automation request** column of the project's Task timeline analysis.


**Related topics**  


[Integration with Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/integration-with-automation-center.md)

[Task Mining analyses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/task-mining-dashboard.md)

