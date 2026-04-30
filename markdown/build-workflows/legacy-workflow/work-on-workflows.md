---
title: Work on workflows
description: To complete a workflow, you add workflow activities, validate the workflow, and publish it.Activities determine the functionality of the workflow.When a workflow is complete, publish the workflow so that it is available to all users.You can edit a published workflow after you check it out.Application scoping protects applications by identifying and restricting access to application files and data. You can copy a workflow created in one application scope \(for example, Test\) to another \(Production\) as needed.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-09-22"
reading_time_minutes: 4
breadcrumb: [Workflow management, Classic Workflow, Build workflows]
---

# Work on workflows

To complete a workflow, you add workflow activities, validate the workflow, and publish it.

## Before you begin

Role required: snc\_required\_script\_writer and either workflow\_creator or workflow\_admin.

**Parent Topic:**[Workflow management](../concept/managing-workflows.md)

## Add a workflow activity

Activities determine the functionality of the workflow.

### Before you begin

Role required: snc\_required\_script\_writer and workflow\_admin, workflow\_creator, or admin

### About this task

When they are created, all workflows contain **Start** and **End** activities.

For more information, see [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md).

### Procedure

1.  Open a workflow.

2.  Check out the workflow.

3.  [Drag a workflow activity](../../using-workflows/task/t_AddAnActivityToAWorkflow.md#) from the Activities menu into the workflow body.

4.  Populate the Workflow Activity form that appears.


## Publish a workflow

When a workflow is complete, publish the workflow so that it is available to all users.

### Before you begin

Before you publish a workflow, validate it to test it for issues that might cause it to fail, such as missing subflows or disconnected transitions. For more information, see [../../workflow-validation/concept/c\_WorkflowValidation.md](../../workflow-validation/concept/c_WorkflowValidation.md).

Role required: snc\_required\_script\_writer and workflow\_admin, workflow\_creator, workflow\_publisher, or admin

### About this task

To publish a workflow:

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open the workflow that you want to publish.

3.  In the title bar, click the menu icon and select **Publish**.


### Result

If you published a new version of workflow, the changes are not applied to running [workflow contexts](../reference/r_AdministeringWorkflowContexts.md). Any currently running workflow context continues using the workflow version that was available when the workflow started. The next time the workflow runs, it uses the new version.

## Edit a published workflow

You can edit a published workflow after you check it out.

### Before you begin

Role required: snc\_required\_script\_writer and workflow\_admin, workflow\_creator, workflow\_publisher, or admin

### About this task

**Note:** You cannot check out or delete workflows that are associated with a read-only application file.

To check out a workflow:

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open the workflow that you want to edit.

3.  In the title bar, click the menu icon and select **Checkout**.

    A new [version of the workflow](../../using-workflows/concept/c_WorkflowVersions.md) is created and assigned to you.

    If you are in a different domain than the published workflow, the new workflow version is [created in your domain](../../using-workflows/concept/c_WorkflowsAndDomainSeparation.md#).


### What to do next

After you finish editing the workflow, validate and publish the workflow to make the new version available to other users.

## Copy a workflow between two application scopes

Application scoping protects applications by identifying and restricting access to application files and data. You can copy a workflow created in one application scope \(for example, Test\) to another \(Production\) as needed.

### Before you begin

Role required: snc\_required\_script\_writer and admin

### Procedure

1.  On the Home page, click ![System Settings icon](../../workflow/image/System_Setup.png), located next to the logged in user name.

2.  In the **Developer** tab, in the **Application** field, select the application scope \(for example, Test\) in which you want to operate the ServiceNow platform.

3.  Close the System Settings page.

4.  Navigate to **Workflow** &gt; **Workflow Editor**.

5.  Create a workflow in the Workflow Editor.

    For more details, see [Create a workflow](t_CreateAWorkflow.md).

6.  In the Workflow Editor, click ![Information icon](../../workflow/image/WorkflowPropertiesIcon.png).

7.  In the **Application** tab, **Application** is set to the current application scope selected in System Settings.

8.  In **Accessible from**, select **All application scopes** if the workflow is available to all application scopes, or select **This application scope only** if it is only available to, and accessible in the current application scope only.

    Only those workflows that are accessible from all application scopes can be copied to another application scope.

9.  Go back to the Homepage, click ![System Settings icon](../../workflow/image/System_Setup.png).

10. In the **Developer** tab, in the **Application** field, select the application scope \(for example, Production\) to which you want to copy the workflow.

11. Navigate to **Workflow** &gt; **Workflow Editor**.

12. Refresh the page, then open the same workflow you created.

    An **Out of scope workflow, workflow belongs to &lt;scope name&gt; scope** message appears, where &lt;scope name&gt; is the application scope in which the workflow was originally created.

13. In the Workflow Editor, click ![Context menu](../../workflow/image/WorkflowActionsicon.png).

14. Select **Copy**.

    The **Workflow Name** dialog appears:

    ![Add a name for the workflow copy in the Workflow Name dialog.](../../workflow/image/Workflowname.png)

    1.  In **Workflow Name**, type the new name for the copied workflow.

    2.  Click **OK**.

        The system creates a workflow in the current application scope.

15. In the Workflow Editor, click ![Information icon](../../workflow/image/WorkflowPropertiesIcon.png).

16. In the **Application** tab, **Application** is set to the current application scope.

17. In **Accessible from**, select **This application scope only** if to make the newly copied workflow a private one that cannot be accessed from outside current scope.

18. Click **Update**.


### Result

A new workflow record is created in the selected application scope and marked as private if designated as one in the Workflow Editor.

