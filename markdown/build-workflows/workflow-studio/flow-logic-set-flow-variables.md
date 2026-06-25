---
title: Set Flow Variables flow logic
description: Assign a value to one or more flow variables, which store flow data as data pills. Access flow variable values by referring to their data pill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-logic-set-flow-variables.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Set Flow Variables flow logic

Assign a value to one or more flow variables, which store flow data as data pills. Access flow variable values by referring to their data pill.

**Important:** This flow logic sets values for flow variables that have already been created. For instructions on creating flow variables, see [Create a flow variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow-variables.md).

## Inputs

<table id="table_m4w_ktt_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the variable. Select from the list of variables available for the flow.

</td></tr><tr><td>

Data

</td><td>

Value for the variable. Enter a string value, input a script, or use a data pill. Variable values can reference any data pill from earlier in the flow, including other variables. If you set variable values by reference to other data pills, you must maintain the order of the variable assignments. The referenced value must always come before the variable that uses the referenced value. Changing the order may produce null values. To assign an empty value, leave this field empty.**Note:** Flow variable values are set in the order in which they're assigned from top to bottom. If you set the value of the same variable multiple times, the flow only uses the last value set.

To enter a script, select the **Toggle scripting on for \[variable\]** icon. Enter your script in the script editor. For more information about inline scripting, see [Inline scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/inline-scripts.md).

</td></tr></tbody>
</table>## Outputs

This flow logic produces no outputs but does change the value of flow variables.

## Usage

Flow variables store flow data as data pills of a specific data type. You can access flow variable data pills from the Flow Variables section of the Data pane. To use a flow variable value, select the data pill from the Data pane or the pill picker just as you would any other data pill.

## Set the incident number variable value to a flow data pill value

In this example, the flow checks the category of an incident record. If the category is network, a flow variable is used to store the record number.

\[Omitted image "set-flow-variables-flow-logic.png"\] Alt text: Use a data pill value to set a flow variable.

Later in the flow, the Send Email action uses the incident number flow variable as part of the email subject and body.

\[Omitted image "example-use-flow-variable-in-send-email.png"\] Alt text: Send Email action that uses the Flow Variable incident number in both the subject and body of the email.

## Set the incident number variable value using a script

In this example, the flow checks the category of an incident record. If the category is network, a flow variable is used to store the record number. In this example, the flow variable is set from a script rather than a data pill value.

```
/*
**Access Flow/Action data using the fd_data object. Script must return a value. 
**Order number is offset by +1 in Error Handling Section.
**Available options display upon pressing "." after fd_data
**example: var shortDesc = fd_data.trigger.current.short_description;
**return shortDesc;
*/
var incNumber = fd_data.trigger.current.number;
return incNumber;
```

\[Omitted image "flow-logic-set-flow-variables-script.png"\] Alt text: Use a script to set a flow variable.

## Execution details

\[Omitted image "set-flow-variables-execution-details.png"\] Alt text: Example execution details of setting a flow variable with a data pill.

\[Omitted image "flow-logic-set-flow-variables-script-execution-details.png"\] Alt text: Example execution details of setting a flow variable with a script. \[Omitted image ""\] Alt text: Example execution details of setting a flow variable with an inline script.

**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

[Assign subflow outputs flow logic]()

[Call a workflow flow logic]()

[Do the following until flow logic]()

[Do the following in parallel flow logic]()

[Dynamic flows flow logic]()

[End Flow flow logic]()

[Exit Loop flow logic]()

[For Each flow logic]()

[Get Flow Outputs flow logic]()

[Go back to flow logic]()

[If flow logic]()

[Make a decision flow logic]()

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

