---
title: Create an action in Workflow Studio
description: Create a reusable component to automate one or more steps of a process.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Building actions, Use, Workflow Studio, Build workflows]
---

# Create an action in Workflow Studio

Create a reusable component to automate one or more steps of a process.

## Before you begin

-   Role required: flow\_designer, action\_designer or admin

## About this task

Action designers should know the application table structure and be aware of any existing business logic associated with the target tables of an action. Be sure to disable any conflicting business rules or workflows before creating an action.

Creating a custom application to contain your Workflow Studio content enables you to [deploy](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=zurich&pubname=zurich-application-development&ft:locale=en-US) it using the application repository or the ServiceNow Store.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **New** &gt; **Action**.

3.  Fill in the Action Properties and select **Submit**.

    |Field|Description|
    |-----|-----------|
    |Action name|Enter a unique name for your action.|
    |Description|Description of the action.|
    |Application|Application scope of the action.|
    |Domain|Domain scope of the action. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).|
    |**Additional properties**|
    |Accessible From|Accessible from all application scoped or only within the specified application scope.|
    |Category|Defined category within the application scope for an action. Beginning with the Xanadu release, you can create a custom category to organize your actions.|
    |Protection|Select whether the action is read-only. You can only select a value when you create the action in an application scope you own. The default value is None.|
    |Action annotation|Help text that appears under the action title in Workflow Studio to help action authors understand what the action does when used in a flow.|

    An empty action opens.

4.  Define action inputs to make data available to the action steps and outputs.

    1.  Select **+ Create Input** and complete the fields.

<table id="table_w3x_gt5_gcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the input. This value is used as the name of the data pill in the right-hand pane.**Note:** Action input names can't include any of the following reserved system names:

-   sys\_id
-   sys\_created\_by
-   sys\_created\_on
-   sys\_updated\_on
-   sys\_updated\_by
-   sys\_mod\_count


</td></tr><tr><td>

Type

</td><td>

Data type of the input. For supported data types, see [Workflow Studio input and output data variables](../reference/action-inputs-outputs.md).

</td></tr><tr><td>

Reference Table

</td><td>

Reference table for the data type. Only required for the following data types: -   Records
-   Reference


</td></tr><tr><td>

Advanced options

</td><td>

Inputs provide advanced options based on their data type. All inputs have advanced options to add a hint or provide a default value. Use advanced options to guide flow designers through adding and configuring an action to a flow. For example, create a choice input to provide flow designers with a pre-defined list of configuration options to choose from. For more information about the configuration options available to particular data types, see [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 Select ![Open icon](../images/icon-advanced-input.png) to view the advanced options and define values.

</td></tr></tbody>
</table>        Inputs are represented as data pills in the right-hand pane. You can add inputs to steps and outputs in the flow by dragging and dropping data pills.

5.  Add an action step to perform an operation on the action inputs.

    1.  Select the **+** underneath Inputs in the Action Outline.

    2.  Select the step you would like to perform.

    3.  Complete the fields in the step.

6.  For **If this step fails**, select the action error evaluation behavior you want the step to take.

    |Option|Description|
    |------|-----------|
    |Stop the action and go to error evaluation|Stop running the action at the current step and go to error evaluation. The Step Status object contains the error information returned by the step.|
    |Don't stop the action and go to the next step|Ignore the failure and continue running the action from the next step. The Step Status object contains the error information returned by the step. Action error evaluation runs regardless of whether the action continues running.|

7.  Add action outputs to make data available to a flow.

    1.  Select **+ Create Outputs** and complete the fields.

<table id="table_d1v_z55_gcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the output. This value is the name of the data pill in the right-hand pane when the action is added to a flow.**Note:** Action output names can't include any of the following reserved system names:

-   sys\_id
-   sys\_created\_by
-   sys\_created\_on
-   sys\_updated\_on
-   sys\_updated\_by
-   sys\_mod\_count


</td></tr><tr><td>

Value

</td><td>

Data used previously in the action either in a step or input. Adding a variable to the output makes the value available to the flow.

</td></tr></tbody>
</table>8.  Select **Save**.

    Workflow Studio saves a draft of the action.


## What to do next

[Test the action](test-action.md) until it is ready to be published. [See related flows for action](see-related-flows-for-action.md) to verify that action changes will function in the flows that use the action.

**Note:** By default, the system only runs published actions.

-   **[Create an action input from a step input](create-action-input-from-step-input.md)**  
Create an action input based on the data type of a step input. Map the step input value to the new action input.
-   **[Test an action](test-action.md)**  
Test an action before publishing it for other users.
-   **[Copy an action](copy-action.md)**  
Copy an action to give it a new name and move it to another application scope.
-   **[Dynamic inputs](../concept/dynamic-inputs.md)**  
Generate a list of action inputs or input values each time that someone configures the action in a flow. Dynamic inputs can display a list of related action inputs, a list of fields from a record, or a list of options available in a choice list.
-   **[Dynamic outputs](../concept/dynamic-outputs.md)**  
Access action and subflow outputs as dynamically generated data pills during flow design. You can also build data gathering actions to generate complex objects from ServiceNow AI Platform and Integration Hub outputs.
-   **[Action error evaluation](../concept/action-error-evaluation.md)**  
Enable actions to catch step failures and continue running. Identify when specific error conditions occur and return your own action status code, status message, and error state.
-   **[Retry policy](../concept/retry-policy.md#)**  
Automatically retry failed requests when a step encounters an intermittent issue such as a network failure or request rate limit. Set a retry policy to prevent having to manually trigger the step again.

**Parent Topic:**[Building actions](../concept/actions.md)

