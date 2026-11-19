---
title: Prepare a subflow
description: Review the process of preparing a subflow for use in a parent workflow, and for preparing the parent workflow to use a subflow.After you create a subflow, use this procedure to prepare the parent workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/legacy-workflow/t\_PrepareASubflow.html
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflows used as subflows, Workflow management, Classic Workflow, Build workflows]
---

# Prepare a subflow

Review the process of preparing a subflow for use in a parent workflow, and for preparing the parent workflow to use a subflow.

## Procedure

1.  In the editor, open and check out the workflow that you want to use as a subflow.

2.  In the title bar, click the menu icon and select **Edit Inputs**.

    \[Omitted image "SubflowEditInputs.png"\] Alt text: Editing workflow inputs

3.  In the Workflow Inputs window, click **New** in the **Variables** list.

4.  Add a new variable depending on the type of values that it is going to store.

    The following example sets up a string value.

    \[Omitted image "SubflowNewVariables.png"\] Alt text: Adding new variables

5.  Click **Submit**.

6.  Close the **Workflows Inputs** dialog.

7.  Create a **Run Script** activity on the subflow.

    -   Set the value from the parameter to a field on the current form. This is important because the **Notification** activity can only pull values from the current variable and not from the newly added variable. The following example sets the value in the **Description** field.

        `current.description = workflow.inputs.bluesubvariable;`

    -   Create a new field on the request form but do not display the field. This serves as temporary storage.

        \[Omitted image "RunScriptSetParaValue.png"\] Alt text: Create a script to set the parameter value

8.  Create a **Notification** activity on the subflow and use `${description}` in the subject to return the value from the field.

    \[Omitted image "NotificationActivityValues.png"\] Alt text: Setting up the notification to return a value

    This is what the subflow would look like:

    \[Omitted image "WorkflowWithSubflow.png"\] Alt text: Completed subflow


**Parent Topic:**[Workflows used as subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/workflows-as-subflows.md)

## Prepare a workflow to use a subflow

After you create a subflow, use this procedure to prepare the parent workflow.

### Procedure

1.  On the parent workflow, create a variable similar to what you did on the subflow, but name it something different.

    In the following example, the variable is named **Blue Main Variable**.

    \[Omitted image "ParentWorkflowInputVariable.png"\] Alt text: Creating input variables for the workflow

2.  Click **Submit**.

3.  Insert a **Run Script** activity to return the value from a field to the newly created variable.

    In this example, the value of the **Short Description** field is returned and given to the newly created variable.

    `workflow.scratchpad.bluemainvariable = current.short_description;`

    \[Omitted image "RunScriptActivityProperty.png"\] Alt text: Run script activity properties

4.  Click **Submit**.

5.  In the subflow activity, set the **Blue Sub Variable** to pass the `bluemainvariable` to the `bluesubvariable`.

    `${workflow.scratchpad.bluemainvariable}`

    This is what the main workflow looks like:

    \[Omitted image "WorkflowExampleWithSubflow.png"\] Alt text: Completed sample workflow with a subflow


