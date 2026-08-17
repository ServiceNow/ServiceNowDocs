---
title: Create an automation request in Task Mining
description: As a business analyst, review the task timeline for identifying task optimization opportunities and automation candidates. Then, submit an automation request from Task Mining to create an automation in Automation Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/better-together/create-automation-request-tm.html
release: zurich
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 4
keywords: [create agent, decomposed automations, automations blocks, desktop actions, automation center, UI block, non UI block, deterministic desktop actions]
breadcrumb: [Building desktop automations from Task Mining data, Solutions]
---

# Create an automation request in Task Mining

As a business analyst, review the task timeline for identifying task optimization opportunities and automation candidates. Then, submit an automation request from Task Mining to create an automation in Automation Center.

## Before you begin

-   [Create a Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/create-task-mining-projects.md) in Task Mining.
-   Confirm that you select **Capture screenshots to create desktop actions** option while defining the scope for the task. For more information, see [Define user actions for task logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/mine-data.md).
-   Enable workstation users to capture desktop activity data that includes desktop interactions and sequence of steps using the Task Mining agent.
-   Run a mining job on a Task Mining project to generate an analysis of the collected project data. For more information, see [Run a mining job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/mine-project-data.md).
-   Verify that Automation Center is installed to initiate an automation request.
-   Verify that ServiceNow Otto for Platform is installed and the User Task Step Summarization skill is activated to use the AI features in the integration.

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

Create automation requests for your tasks directly from Task Mining. Capture both steps and automation properties in a single recording session, instead of recording the same process twice. When a Task Mining analyst submits an automation request, the recording is delivered to the automation team with all UI screenshots and application metadata needed to build desktop actions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the project with a task timeline analysis that you want to identify task improvement actions for and select the **Task timeline** tab.

3.  Select the task that you want to act on.

4.  Create a copy to make any edits and to take task improvement actions.

    1.  Select **Edit** to create a copy that you use for automation without affecting the original.

    2.  Enter a descriptive name in the **Task name** field.

    3.  Select **Duplicate to edit**.

    The new task is created with the task name appended with Editable.

5.  Edit any of these steps if you want to change task details.

    1.  Select the Duplicate step icon \[Omitted image "image.task-mining-duplicate-step"\] next to the step to make a copy of the step.

        The new task step is created. The **Interaction** column of the duplicated step is empty.

    2.  Select the Delete step icon \[Omitted image "image.tm-delete-step-icon"\] next to the step to remove a step from the task.

    3.  Select the Reorder step icon \[Omitted image "image.tm-reorder-icon"\] next to the step to drag the step to a different order.

    4.  Double-click a task field \(or use the keyboard shortcut\) to edit details, enter the new text, and select **Apply**.

        You can’t edit the **Source** and **Datetime** fields.

6.  From the selected task, select **Request automation**.

7.  Select the task improvement action that you want to take, and select **Continue**.

<table id="choicetable_fll_2fy_yjc"><thead><tr><th align="left" id="d22834e291">

Option

</th><th align="left" id="d22834e294">

Description

</th></tr></thead><tbody><tr><td id="d22834e300">

**Generate with AI**

</td><td>

Open an Automation Center request based on the improvement opportunity. Populate the **Description** and **Detailed sequence of steps** fields with data from the tasks. For more information, see step 8.

</td></tr><tr><td id="d22834e318">

**Complete manually**

</td><td>

Fill in the Automation Center request form with details of the improvement opportunity, and submit the request.**Note:** If an automation request has already been made for this task, a message with a link to the existing automation request is provided.

</td></tr></tbody>
</table>    \[Omitted image "image.tm-io-generate-ai"\] Alt text: Screenshot showing the UI option to generate details with AI.

8.  Select **Generate details** to populate the **Description** and **Detailed sequence of steps** fields with data from the tasks again.

    Review all auto-generated instructions and correct any inaccuracies. The detailed sequence of steps is the basis of the automation.

    A maximum of 250 steps can be generated. If your task has more than 250 steps, try selecting a more appropriate task. If you want to continue with the task, you can simplify the steps to reduce their number. Alternatively, you can manually populate the **Description** field with step details and complete the automation request form.

    **Note:** The generate details option is available only if ServiceNow Otto for Platform is installed and the User Task Step Summarization skill is activated.

9.  Select **Save**.

    An attachment is automatically added to the automation request. The attachment contains the task timeline, screenshots, and interaction summary generated by Task Mining. Automation Center reads this attachment to generate automations. If the attachment is missing, you can request an automation again for the task.

    The automation request is created and associated with the task that it was based on. A link to the automation request record is available under the **Automation request** column of the project's Task timeline analysis.


## What to do next

In Automation Center, generate automations to create automation blocks from user task patterns captured using Task Mining. For more information, see [Create automation blocks from the automation request in Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/better-together/generate-automations-tm.md).

