---
title: Script step
description: Add custom JavaScript to execute within a reusable action. While most core actions and steps fit common use cases, you can build a Script step to execute behavior not satisfied by the core steps.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Script step

Add custom JavaScript to execute within a reusable action. While most core actions and steps fit common use cases, you can build a Script step to execute behavior not satisfied by the core steps.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

**Note:** Integration Hub See Request Integration Hub for information about Integration Hub usage and subscriptions.

## Fields

The Script step includes separate input and output variables that enable you to map JavaScript data to Workflow Studio data. By defining input and output variables within the step, you can define what Workflow Studio data is available within your script, and which scripting variables are available to other steps in your action.

<table id="table_qdk_35f_kcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required Runtime

</td><td>

The runtime environment required to support the script. Choices include:

-   **Instance**: The action step runs the script from instance. Select this option when the script needs access to the ServiceNow API or instance data. This is the default value.
-   **MID**: The action step runs the script from the MID Server. Select this option when the script needs access to MID Server script files and APIs. Selecting this option displays the **Select MID Server Using** field.
-   **Vanilla \(Core JavaScript\)**: The action step runs the script from either the instance or MID Server. Select this option when the script only needs the core JavaScript APIs and not the ServiceNow API or instance data.

 The runtime you select determines the JavaScript objects and methods displayed in the Context-sensitive help.

 **Note:** This field is only visible when Integration Hub is activated.

</td></tr><tr><td>

Select MID Server Using

</td><td>

Specify the MID Server selection process to use. Choices include:

-   **Any MID**. The system runs the action step from any available MID Server.
-   **Use Connection Alias**. The system runs the action using the connection alias you specify. Selecting this option displays the **Connection Alias** field.
-   **Use Inline Selection**. The system runs the action using the connection details you specify in the action. Selecting this option displays the **Host**, **MID Application**, and **Capabilities** fields.

 **Note:** This field is only visible when Integration Hub is activated, and you select **MID** from **Required Runtime**.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. Only aliases of connection type Basic are supported.**Note:** This field is only visible when Integration Hub is activated, and you select **Use Connection Alias** from **Select MID Server Using**.

</td></tr><tr><td>

Host

</td><td>

The fully-qualified domain name of the MID Server where the system runs the action step. For example, mid-server.domain.com. **Note:** This field is only visible when Integration Hub is activated, and you select **Use Inline Selection** from **Select MID Server Using**.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see Configure a MID Server cluster.


 This field is available when **MID** is selected from the Required Runtime list, and **Use Inline Selection** is selected from the Select MID Server Using list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **MID** is selected from the Required Runtime list, and **Use Inline Selection** is selected from the Select MID Server Using list.

</td></tr><tr><td>

MID Application

</td><td>

Specify the application the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected application. This field is only visible when Integration Hub is activated, **Auto-Select MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

</td></tr><tr><td>

Capabilities

</td><td>

Capabilities the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected capabilities. This field is only visible when Integration Hub is activated, **Auto-Select MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

</td></tr><tr><td>

Specific MID Server

</td><td>

Data pill of the required MID Server. This field is only visible when Integration Hub is activated, **Specific MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

</td></tr><tr><td>

Input variables

</td><td>

Name-value pairs that represent data from the action, enabling you to use action inputs and data from other steps within a script.

</td></tr><tr><td>

Script

</td><td>

Script that executes within the action. To access input and output variables in your script, use the global objects inputs and outputs. For example, `inputs.myVariable`.

**Note:** Script step input and output names can't include any of the following reserved system names:

-   sys\_id
-   sys\_created\_by
-   sys\_created\_on
-   sys\_updated\_on
-   sys\_updated\_by
-   sys\_mod\_count

In general, don't create a variable that has the same name as a system field. The Script step may confuse such an input variable for a field name and use the wrong value.

 The Script step always converts data stored in the inputs and outputs global objects into strings. If your Script step needs to work with JSON data, you can use the inputs global object to convert the JSON data into a string. Alternatively, you can define a JavaScript variable as a string rather than a JavaScript object. For example, this script illustrates two ways you can output JSON data.

```
(function execute(inputs, outputs) {
  outputs.json_object_1 = inputs.json_input;
  var array_of_objs = '[{"name1":"value1"}, {"id":"abcd"}]';
  outputs.json_object_2 = array_of_objs;
})(inputs, outputs);
```

 By default, Workflow Studio run scripts on the instance. To run script from a MID Server requires an Integration Hub subscription.

 Workflow Studio runs script from the domain from which it is triggered or initiated. See [Domain separation and Workflow Studio](../concept/flow-designer-domain-separation.md).

 For available classes and methods, see the JavaScript API context-sensitive help or the API reference.

</td></tr><tr><td>

Output variables

</td><td>

Map JavaScript output to Workflow Studio data pills. Define output variables when you want other steps in the action to use the script output.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Example

This example builds a JSON payload that can be easily updated or changed and added to a subsequent REST step.

**Note:** REST step is not available in the base system and requires the ServiceNow® Integration Hub subscription.

![Example Script step in an action.](../images/script-step-example.png)

By creating an output variable that represents the payload, you can drag the **\[Payload\]** data pill into the REST step **Body** field.

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

