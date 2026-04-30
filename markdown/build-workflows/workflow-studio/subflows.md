---
title: Building subflows
description: Workflow Studio is the default ServiceNow AI Platform process automation builder used to create subflows. Workflow Studio replaces the Workflow Editor.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Use, Workflow Studio, Build workflows]
---

# Building subflows

Workflow Studio is the default ServiceNow AI Platform process automation builder used to create subflows. Workflow Studio replaces the Workflow Editor.

Unlike flows, subflows lack a trigger. Use a subflow when:

-   You only want to start a flow by calling it from another flow or script.
-   You want to create a set of reusable operations for use in multiple flows.
-   You want to specify the inputs available to the subflow when it starts.
-   You want to specify the outputs available to the parent flow after the subflow ends.

All subflows consist of properties, one or more inputs, one or more outputs, a sequence of actions and flow logic, and the data collected or created.

## Subflow properties

The subflow properties specify the subflow name, application, category, description, in-flow annotation, roles, and status. Flow designers can update the subflow name, category, description, in-flow annotation, and roles at any time, but can only set the application during subflow creation. The subflow status is set when you save or publish a subflow.

## Subflow inputs

Subflow inputs specify the data available to the subflow when it starts. Each input you define for a subflow becomes a configuration option in the Workflow Studio interface. To use the subflow in a flow, you must define a value for each mandatory input. The more inputs a subflow has, the more data you must define and the more familiar you must be with the underlying data model to use the subflow effectively.

Inputs provide advanced options based on their data type. All inputs have advanced options to add a hint or provide a default value. Use advanced options to guide flow designers through adding and configuring a subflow to a flow. For example, create a choice input to provide flow designers with a pre-defined list of configuration options to choose from. For more information about the configuration options available to particular data types, see [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Subflow outputs

Subflow outputs specify the data available to the parent flow after the subflow completes. Subflow outputs are defined as variables with a name and data type. Subflow designers assign values to an output using the **Assign Subflow Output** flow logic. Output values can be based on the subflow logic conditions, action results, or a manually set value. For example, an output may have one value when a condition is met and another value when a condition is not met. During runtime, the value of the output is determined by the condition that is met.

Consider the following example of a subflow with two conditions that both result in a value for a single output variable. The value of the variable depends on which condition is met during runtime.

-   **Outputs**

    \[Manager ID\] \[String\]

-   **Actions**
    -   1 Look Up \[User\] Record where \(Created on Today\)
    -   2 If \(**\[1-&gt;User Record-&gt;Title\]** contains Manager\) then, Assign Subflow Outputs \[Manager ID\] to **\[1-&gt;User Record-&gt;User ID\]**
    -   3 Else, Assign Subflow Outputs \[Manager ID\] to **\[1-&gt;User Record-&gt;Manager-&gt;User ID\]**

In this case, if the user's title contains "Manager" then the user ID is assigned as output. Otherwise, the subflow looks up the user's manager and assigns the user ID of the manager as output.

Workflow Studio allows you to define a value for the same variable multiple times. However, if a variable is given two or more possible values without conditional logic, only the last value defined in the subflow is applied to the output at runtime.

-   **Outputs**

    \[Manager ID\] \[String\].

-   **Actions**
    -   1 Look Up \[User\] Record where \(Created on Today\)
    -   2 Assign Subflow Outputs \[Manager ID\] to **\[1-&gt;User Record-&gt;User ID\]**
    -   3 Assign Subflow Outputs \[Manager ID\] to **\[1-&gt;User Record-&gt;Manager-&gt;User ID\]**

In this example, action three overwrites the value of action two and **\[1-&gt;User Record-&gt;Manager-&gt;User ID\]** is applied to the \[Manager ID\] output at runtime because it was the last value defined. Typically, subflows should only include multiple values for one variable if conditional flow logic is used.

## Subflow execution details

Process analysts can view subflow execution details from multiple locations.

-   **Parent flow execution details**

    Workflow Studio displays subflow execution details within the parent flow execution details. The parent flow execution details list each subflow as inline elements. You can expand a subflow step to see its execution details.

-   **Subflow execution details**

    The system generates flow execution details for each subflow run. View subflow execution details directly from the list of flow executions.


## Actions

Within **Actions**, flow designers can add actions, flow logic, flows, or other subflows.

An action is a reusable operation that enables process analysts to automate ServiceNow AI Platform features without having to write code. For example, the **Create Record** action allows process analysts to generate records in a particular table with particular values when certain conditions occur. ServiceNow core actions like Create Record require some familiarity with ServiceNow AI Platform tables and fields. Action designers can create application-specific actions to pre-set configuration details. For example, creating a Create Incident Task action ensures that the process analyst uses the correct table and field configuration each time the action is used. You can add application-specific actions by activating the associated spoke.

## Flow logic

Subflows can contain flow logic to specify conditional or repeated actions, or to assign output variables to subflow data. The system provides these flow logic options.

<table id="table_lw2_zxz_mbb"><thead><tr><th>

Flow logic

</th><th>

Description

</th></tr></thead><tbody><tr><td>

For Each

</td><td>

Applies actions to each record in a list of records. Flow designers must specify the list of records from the subflow data. **Note:** You can nest a **For Each** flow logic block inside of another flow logic block to repeat an action over a series of records. However, avoid nested For Each loops that process many records. Nested loops may cause the flow to run until it is stopped by the flow transaction quota rule, which prevents flows from running longer than an hour. For more information about transaction quotas, see [Transaction quotas](https://www.servicenow.com/docs/access?context=c_TransactionQuotas&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

If

</td><td>

Applies actions when a list of conditions is met. Flow designers can specify the conditions with subflow data. Once an If condition is added, you can add an Else or Else If flow logic option to define behavior when conditions are not met.

</td></tr><tr><td>

Assign Subflow Outputs

</td><td>

Assigns an output variable to subflow data. Only outputs defined in **Inputs &amp; Outputs** can be assigned a value. Assigning outputs enables you to assign a different output variable for each logical path in the subflow.

</td></tr></tbody>
</table>## More Actions

Click the **More Actions** \(![More Actions icon](../images/MoreActionsIcon.png)\) button to access additional options for the subflow.

-   **Copy action**

    Create a copy of the open subflow in an application you specify.

-   **Configurations**

    Enable or disable the **Show draft actions**, **Show triggered flows**, **Show store spokes**, and **Show inline script toggle** options.

-   **Code Snippet**

    Generate a code snippet for the action.

-   **Manage security**

    Enable or disable the **Callable by Client API** option.

-   **Manage natural language title**

    Create or edit a subflow title with styled or dynamic text. For more information, see [Manage natural language titles](../task/manage-natural-language-title.md).


## Testing subflows

You can test a subflow alone, or when added to a flow. When testing a subflow alone, you must define the inputs that the subflow uses in its actions. Because a subflow does not have a trigger, testing a subflow runs the actions using the defined input values.

**Note:** Because testing a subflow creates or changes records on the instance, flow designers should always test subflows on a non-production instance containing relevant demonstration data.

## Roles

To access subflows, a user must have the flow\_designer or admin role.

## General guidelines

General guidelines that apply to [flows](flows.md) also apply to subflows.

Reasons to use a subflow instead of a flow include:

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Configure different input values for each call**

    Configure a subflow's input values differently each time you call it. For example, design a subflow to accept different record types as an input run. Reuse this generic record subflow instead of writing a specific flow for each record type.

-   **Improve performance and readability of large flows**

    Use subflows when a flow exceeds 25 actions. 50 is the maximum number of actions specified by the sn\_flow\_designer.max\_actions system property, but limit a flow to 25 actions for the best performance.

-   **Limit subflows to 20 inputs**

    The more inputs your subflow has, the more resources it takes to open and run it. Processing more than 20 inputs risks the subflow being slow to open and run.

-   **Pass inputs and outputs with subflows**

    Call subflows if you want to pass inputs and outputs. Use subflows if you want to specify the inputs available to a subflow when it starts, or if you want to specify the outputs available to the parent flow after a subflow ends.

-   **Trigger multiple flows on a single event vs. using parallel subflows**
    -   Use parallel subflows if there are interrelated outputs or if some action must be taken when all are available. If not, then it’s simpler to trigger multiple flows.
    -   To configure parallel subflows, launch each subflow without a wait and then use wait for condition to wait for each subflow to be terminal \(complete, error, canceled\)
-   **Use dynamic flows if you have multiple subflows with similar functionality**

    Dynamic flows let you compartmentalize your processes by applying a template to handle the inputs of multiple similar subflows. Compartmentalization lets you distinguish between subflows that perform similar functions, such as subflows for [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) spokes.

-   **Avoid the 10-item limit in the error-handling-process**

    Rather than force your error-handling-process to fit within a 10-item limit, call subflows, which can contain many more items. You can also use the subflow outputs to trigger automation in other flows.

-   **Take corrective actions**

    Rather than recreate the same sequence of actions in multiple flows, create reusable subflows to correct errors to your record data. When a flow error leaves your record data in an undesired state, use subflows to correct these records. You can use the error handler to identify such record data as a subflow output.


-   **[Create a subflow in Workflow Studio](../task/create-subflow.md)**  
Reuse an entire flow's content as a subflow. Define the input data the subflow uses and the output data it generates. Call subflows from other flows or script.​
-   **[Create a subflow with Now Assist](../task/create-subflow-now-asist.md)**  
Use generative AI to create a subflow from text directionsand images.
-   **[Create conversational subflow skill](../task/create-conversational-subflow-skill.md)**  
Create a skill for the conversational subflow and make the skill available for users in a conversation. You can have multiple skills for the same subflow.
-   **[Configure subflow conversational settings](../task/configure-subflow-conversation-settings.md)**  
Configure conversation settings to make a subflow available to conversational interfaces.
-   **[Configure LLM to generate descriptions for conversational subflows](../task/configure-llm-for-conversational-subflow.md)**  
Choose which LLM you want to use by default to generate descriptions for inputs, outputs, and skills for conversational subflows.
-   **[Copy a subflow](../task/copy-subflow.md)**  
Copy a subflow to give it a new name and move it to another application scope.
-   **[Create a decision table in a subflow](../task/create-decision-table-subflow.md)**  
Create a decision table structure while you author your flow in Workflow Studio. Use data from the subflow to create inputs, conditions, and results for the decision table, all in a convenient modal.
-   **[Convert items to subflow](../task/convert-items-subflow.md)**  
Convert consecutive items of a flow into a new subflow that preserves data pill references between the converted items. Update the original flow to replace the converted items with a call to the new subflow.
-   **[Create a template value input](../task/template-value.md)**  
Enable flow authors to set field values for a record being created or updated. Use a template value input to set different field values each time you add an action or subflow to a flow.
-   **[Get started with Dynamic Flow and Get Flow Outputs](../task/getting-started-dynamic-flow-get-flow-outputs.md#)**  
Create a sample flow that dynamically calls subflows for provisioning cloud services.
-   **[Publish a subflow](../task/publish-subflow.md)**  
Publish a subflow to make it available to other users and to add it to activated flows.
-   **[Summarize a subflow](../task/summarize-a-subflow.md)**  
Generate a summary of a subflow with Now Assist for Creator.
-   **[Subflow history](subflow-history.md)**  
View and manage the history of a subflow. See past configurations of a subflow to copy, restore, or remove them.
-   **[Test a subflow](../task/test-subflow.md)**  
You can test a subflow alone, or when added to a flow. When testing a subflow alone, you must define the inputs that the subflow uses in its actions. Because a subflow does not have a trigger, testing a subflow runs the actions using the defined input values. Unless updated, subsequent tests use the same inputs defined in the initial test run.

**Parent Topic:**[Using Workflow Studio](../../workflow-studio/reference/building-workflow-studio-components.md)

