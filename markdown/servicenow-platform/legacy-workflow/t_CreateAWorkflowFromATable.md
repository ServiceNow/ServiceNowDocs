---
title: Create a workflow from a table
description: Automate a multi-step process by creating a workflow from the list view of any table that supports workflows.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a workflow from a table

Automate a multi-step process by creating a workflow from the list view of any table that supports workflows.

## Before you begin

If you are designing the workflow as part of an update set process, see [Workflow movement with update sets](../concept/c_WorkflowMovementWithUpdateSets.md#) before creating the workflow.

## Procedure

1.  Open a table, such as Incident or Problem, in list view.

    For example, navigate to **Incident &gt; Open**.

2.  Right-click in the column header and select **Configure &gt; Workflows**.

    ![](../image/ConfigureWorkflowsHeader.png)

    The **Workflow Versions** on that table appear in a list.

3.  Click**New**.

    The **Workflow Version** opens in **New Workflow** view. The **Table** field is filled in with the table you selected in step 1 and is read-only.

4.  Enter **Name**.

5.  Enter **Description**.

6.  Edit conditions fields as necessary.

7.  Click **Submit**.

    The new workflow is added to the **Workflow Versions** list.

8.  Click the workflow **Name**.

    The new workflow is created with the **Begin** and **End**activities connected by a single transition.

    ![New workflow](../image/WorkflowNew.png)

9.  Finish creating the workflow by adding activities, validating, and publishing so the workflow is available to other users.

    For more information, see [Work on workflows](work-on-workflows.md#).

10. To change advanced settings for the workflow, click the **Properties** icon ![Properties icon](../../workflow/image/PropIcon.png).

11. If you made changes, click **Update**.


**Parent Topic:**[Create a workflow](t_CreateAWorkflow.md)

