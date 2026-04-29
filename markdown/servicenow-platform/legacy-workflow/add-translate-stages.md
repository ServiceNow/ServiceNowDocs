---
title: Add and translate stages
description: You can add default stages to use for a table, and stages to existing workflowYou can assign a stage set as a default set to any number of tables.If a stage required for a workflow has not been imported or is not in the stage set assigned to the workflow table, you can add it to the workflow manually.After stages are added to a workflow, you can assign them to the workflow activities.You can provide translations for workflow stage names so the names appear in the language selected for the instance.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add and translate stages

You can add default stages to use for a table, and stages to existing workflow

**Parent Topic:**[Workflow stages](../concept/c_WorkflowStages.md)

## Add default stages for a table

You can assign a stage set as a default set to any number of tables.

### About this task

The stages in the assigned stage set pre-fill the workflow version stages when you create a new workflow for the associated table.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Default Stages \(by table\)**.

2.  Click **New**.

3.  Select a stage **Set**.

    You can create a new set by clicking **New**, typing a name, and clicking **Submit**.

4.  Select a corresponding **Table**.

5.  Click **Submit**.

    The stages in the selected stage set are automatically added to any new workflows that use the corresponding table.


## Add a stage to an existing workflow

If a stage required for a workflow has not been imported or is not in the stage set assigned to the workflow table, you can add it to the workflow manually.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  In the title bar, click the menu icon and select **Edit Stages**.

4.  In the Workflow Stages list, click **New**.

5.  On the Workflow Stage form, fill in the fields as appropriate.

    Do not use a **Name** or **Value** field value that already exists in the base system.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the stage as it appears in workflow fields.|
    |Value|The value of the stage when it is referenced from elsewhere in the system, such as in a script.|
    |Duration|The default duration for the stage. Currently not used.|

6.  Click **Submit**.

7.  Publish the workflow.


## Add a stage to a workflow activity

After stages are added to a workflow, you can assign them to the workflow activities.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  Double-click the activity.

4.  In the **Stage** field on the Activity Properties form, find and select the stage to display when the workflow reaches the activity.

5.  Click **Update**.


## Translate workflow stages

You can provide translations for workflow stage names so the names appear in the language selected for the instance.

### Before you begin

The instance must already have language internationalization plugins installed. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

### About this task

Language-specific text appears in [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=australia&pubname=australia-platform-administration&ft:locale=en-US) displayed in a list, [workflow stage sets](../concept/c_WorkflowStageSets.md#), and the Workflow Editor for users with that language selected. Language-specific text does not automatically appear when [displaying stages on a form](../../workflow-administration/task/t_CreateAWorkflowStageField.md). To translate stages on a form, add translated text to the workflow field choices.

You can add translated text for any language enabled on the instance. For example, to translate workflow stages into French:

### Procedure

1.  Set the interface language to **French**.

2.  Navigate to **Workflow** &gt; **Workflow Editor**.

3.  Open and check out a workflow.

4.  In the title bar, click the menu icon and select **Edit Stages**.

5.  Edit the **Name** field for each stage and enter the text to display to French users.

    Do not change the **Value** field.

6.  Confirm that the workflow stages display the French text.


### Result

Alternatively, to translate stages for multiple workflows at once, you can directly edit the Workflow Stages \[wf\_stage\] table. For example, to translate workflow stages from multiple workflows into French:

1.  Set the interface language to **French**.
2.  In the application navigation filter, enter `wf_stage.list`.
3.  Edit the **Name** field for each stage and enter the text to display to French users. Do not change the **Value** field.

