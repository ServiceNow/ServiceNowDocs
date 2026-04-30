---
title: Workflow stage sets
description: Stage sets are named groups of workflow stages commonly used together. Create a stage set and assign it as a default set to any number of tables. You can import the choice list values of a workflow field as stages for a workflow, and export a stage set to create a new one.You can create a new stage set by creating a stage set record and adding stage set entries manually.You can assign a stage set as a default set to any number of tables.You can import the choice list values of a workflow field as stages for a workflow.You can create a new stage set by exporting the stages from an existing workflow as a set, instead of manually adding stage set entries to a stage set record.You can add any number of stage sets to an existing workflow.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, Build workflows]
---

# Workflow stage sets

Stage sets are named groups of workflow stages commonly used together. Create a stage set and assign it as a default set to any number of tables. You can import the choice list values of a workflow field as stages for a workflow, and export a stage set to create a new one.

A single stage set usually represents a process, such as the stages required to display the progress of a service catalog request. You can also assign a stage set as the default set for workflows on specific tables.

In an active context, workflow stages provide summary-level feedback about the progress of a workflow. Stage icons display the status of each activity as it is being driven by a workflow. The system updates a **Stage** field, defined in the workflow properties, to indicate the progress of the workflow through the possible stage values.

## Updates to workflow stage values

During an upgrade, the system makes changes to the **Value** field of records in the Workflow Stage \[wf\_stage\] table.

-   All entries are made lowercase.
-   All spaces and special characters are replaced with underscores.

These changes support [System Localization](https://www.servicenow.com/docs/access?context=system-localization-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and enable workflows to display translated text in the **Stage** field.

**Parent Topic:**[Workflow stages](c_WorkflowStages.md)

## Create a new stage set

You can create a new stage set by creating a stage set record and adding stage set entries manually.

### About this task

Create a stage set record only when you want additional stages that are not available on the table by default.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Stage Sets**.

2.  Click **New**.

3.  Enter a **Name** that indicates the purpose of the stage set.

    For example, you can create a Requested Item stage set to hold the stages commonly used by inventory tracking workflows or service catalog fulfillment workflows.

4.  Click **Submit**.

5.  Open the new stage set record.

6.  In the **Stage Set Entries** related list, click **New**.

    Each stage set entry can be used as the **Stage** for an activity in a workflow that uses this stage set.

7.  Enter a **Name** that indicates the stage name to appear in workflow fields.

8.  Enter a **Value** to use when referencing the entry, such as in a script.

9.  Click **Submit**.

10. In the **Stage Set Entries** related list, ensure that each entry has a unique **Order** value.

    Enter a low value for stages that should appear early in the workflow and a higher value for later stages.

    ![Create stage set](../image/CreateStageSet.png)


### What to do next

The stage set can be added to a workflow or assigned as the default stage set for workflows that are created for a specific table.

## Use a default stage set

You can assign a stage set as a default set to any number of tables.

### About this task

The stages in the assigned stage set pre-fill the workflow version stages when you create a new workflow for the associated table.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Default Stages \(by table\)**.

2.  Click **New**.

3.  Select a **Table**.

4.  Select the **Set** you want to assign to the selected table.

5.  Click **Submit**.


## Import stages from a choice list

You can import the choice list values of a workflow field as stages for a workflow.

### Before you begin

Create a choice list as follows:

-   Add a custom field of Type **Workflow** to the table.
-   Configure the custom field to use a choice list.
-   If you are creating a new field, set the **Choice List type** to **Display without --None--** and create the choices for the newly created field.

For more information, see [Create a workflow stage field](../../workflow-administration/task/t_CreateAWorkflowStageField.md).

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  In the title bar, click the menu icon and select **Properties**

4.  In the Workflow Properties dialog box, click the **Stages** tab.

5.  From the **Stage field** list, verify that the correct workflow field is selected.

6.  In the Related Links section, click **Import Stages from Choice List**.

7.  In the dialog box asking you to confirm that you want to import the choice list, click **OK**.

8.  Click **Update**.


### What to do next

The stage set can be added to a workflow or assigned as the default set for workflows that are created for a specific table.

## Export a stage set from a workflow

You can create a new stage set by exporting the stages from an existing workflow as a set, instead of manually adding stage set entries to a stage set record.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow containing stages that you want to export as a new stage set.

3.  In the title bar, click the menu icon and select **Edit Stages** to open the Workflow Stages dialog box.

4.  In the Related Links section, click **Export to Stage Set**.

5.  Enter a unique **Name** for the new stage set.

6.  Click **OK**.


### What to do next

The stage set can be added to a workflow or assigned as the default set for workflows that are created for a specific table.

## Add a stage set to a workflow

You can add any number of stage sets to an existing workflow.

### About this task

When multiple stage sets have stage set entries with the same **Value**, the stage appears on the workflow only once.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  In the title bar, click the menu icon and select **Edit Stages** to open the Workflow Stages dialog box.

4.  In the Related Links section, click **Import from Stage Set**.

5.  Select the stage set.

6.  Click **Ok**.

7.  Import additional stage sets as needed for the workflow.


### What to do next

After you add all necessary stage sets to the workflow, you can add them to the workflow activities. For more information, see [Add a stage to a workflow activity](../task/add-translate-stages.md#).

