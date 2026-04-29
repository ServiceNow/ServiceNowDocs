---
title: Create a workflow
description: Automate a multi-step process by creating a workflow with the Workflow Editor.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow management, Classic Workflow, Build workflows]
---

# Create a workflow

Automate a multi-step process by creating a workflow with the Workflow Editor.

## Before you begin

Role required:

-   You must have the snc\_required\_script\_writer and either the workflow\_admin or workflow\_creator role to use the Workflow Editor.
-   If you are designing the workflow as part of an update set process, see [Workflow movement with update sets](../concept/c_WorkflowMovementWithUpdateSets.md#) before creating the workflow.

## About this task

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

    The **Welcome** tab of the Workflow Editor opens.

2.  On the **Workflows** tab in the palette, click **New Workflow**.

    ![](../image/WorkflowDesignerStart.png)

    A simplified version of the New Workflow form opens.

3.  Fill in the **Name** and **Table** fields

4.  Add a **Description**.

5.  Do one of the following:

    1.  If the **Conditions** UI section is displayed, specify a **Condition** if needed and edit the fields.

        The **Conditions** UI section shows only if the selected table supports conditions for launching workflows. For example, if you select the sc\_req\_item table, conditions are not applicable and the **Conditions** UI section is not displayed.

    2.  If the **Stages** UI section is displayed, check that the **State rendering** and **Stage order** fields contain the correct information.

        The **Stages** UI section shows only if the selected table supports stages. For example, if you select the sc\_req\_item table, the **Stages** UI section is displayed.

6.  Click **Submit**.

    The new workflow is created with the **Begin** and **End**activities connected by a single transition.

    ![New workflow](../image/WorkflowNew.png)

7.  Finish creating the workflow by adding activities, validating, and publishing so the workflow is available to other users.

    For more information, see [Work on workflows](work-on-workflows.md#).

8.  To change advanced settings for the workflow, click the **Properties** icon ![Properties icon](../../workflow/image/WorkflowPropertiesIcon.png).

9.  If you make changes, click **Update**.


-   **[Workflow properties](../reference/r_WorkflowProperties.md)**  
In the properties of a workflow, you can configure settings such as its application scope, start conditions, schedule, inputs, stages, and run time metrics. You can also view information such as the workflow author, version, and history.
-   **[Create a workflow from a table](t_CreateAWorkflowFromATable.md)**  
Automate a multi-step process by creating a workflow from the list view of any table that supports workflows.
-   **[Create a workflow for a new service catalog item](t_CrtWkflwNewSvcCtlgItm.md)**  
When you create a new service catalog item, you can create a new corresponding workflow at the same time.
-   **[Create a workflow for an SLA Definition](t_CreateAWorkflowFromSLADefinition.md)**  
Automate a multi-step process by creating a workflow from an SLA definition.
-   **[Ending workflows with multiple branches](../concept/c_EndingWorkflowsMultipleBranches.md)**  
A workflow is complete when it reaches the **End** activity, even if there are still active branches of the workflow in progress. To ensure that both branches are completed, add a **Join** activity to resolve the branches.

**Parent Topic:**[Workflow management](../concept/managing-workflows.md)

