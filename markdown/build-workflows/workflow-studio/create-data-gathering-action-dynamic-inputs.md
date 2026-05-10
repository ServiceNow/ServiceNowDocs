---
title: Create a data gathering action for a dynamic inputs type input
description: Create a data gathering action to create arbitrary action inputs using a dynamic inputs type input.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Dynamic inputs, Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a data gathering action for a dynamic inputs type input

Create a data gathering action to create arbitrary action inputs using a dynamic inputs type input.

## Before you begin

Role required: admin

**Note:** Dynamic inputs are not available in the base system. To use dynamic inputs in Workflow Studio, you must [Request an Integration Hub plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/request-integrationhub.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Create new** &gt; **Action**.

3.  In the **Action name** field, enter a name for your action, choose the proper **Application** scope, and then select **Submit**.

4.  From the Action Outline, select **Inputs**.

    You may need to create one or more inputs to provide data for your dynamic inputs.

    For example, create a String input to store a table name. See [Create a data gathering action to add dynamic inputs](getting-started-dynamic-input.md#) for instructions.

5.  In the Action Outline under the Inputs section, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) and select the **Script** step.

    1.  From Input Variables, select **Create Variable**, and create an input variable to store any action input values.

        For example create an input variable to store a table name, and map it to the matching action input.

    2.  In Script, enter a script to create a JSON output from the input variable.

        Your script needs to do these tasks.

        -   **Create a new JSON object formatted for an action input**

            You must know the data structure of an action input to create a dynamic input. Your script must create a JSON object that has a property named `data`. The value of the data property must be an array of dynamic inputs. Each dynamic input must has its own required and optional properties.

            This example script sets an outputs variable named data. There is a property for each type of dynamic input available.

            ```
            (function execute(inputs, outputs) { 
              outputs.data = { 
                data: [{
                  label: 'Choice type input',
                  name: 'choicetype',
                  defaultValue: 'choice_1',
                  type: "choice",
                  choices: [
                      { label: "Choice 1", value: "choice_1" },
                      { label: "Choice 2", value: "choice_2" }
                  ]
                }, {
                  label: 'Datetime type input',
                  name: 'datetimetype',
                  type: 'datetime',
                }, {
                  label: 'Decimal type input',
                  name: 'decimaltype',
                  type: 'decimal',
                }, {
                  label: 'Email type input',
                  name: 'emailtype',
                  type: 'email',
                }, {
                  label: 'HTML type input',
                  name: 'htmltype',
                  type: 'html',
                }, {
                  label: 'Integer type input',
                  name: 'integertype',
                  type: 'integer',
                }, {
                  label: 'Password2 type input',
                  name: 'password2type',
                  type: 'password2',
                }, {
                  label: 'Reference type input',
                  name: 'referencetype',
                  reference: 'sys_user',
                  type: 'reference',
                }, {
                  label: 'String type input',
                  name: 'stringtype',
                  defaultValue: 'abcdef',
                  type: 'string',
                  mandatory: true
                }]
              }
            })(inputs, outputs);
            ```

            **Note:** A dynamic inputs type input can only support 40 input values before it risks running out of memory and producing unexpected behavior such as rendering errors and data truncation.

        -   **Set the outputs object**

            Set the outputs object to return the dynamic inputs as a JSON object. See [Create a data gathering action to add dynamic inputs](getting-started-dynamic-input.md#) for an example of creating an output for a Reference field type action input.

    3.  From Output Variables, select **Create Variable**.

        This output variable stores the dynamic inputs your script creates.

    4.  For the output variable type, select **JSON**.

        The script output variable type must be JSON.

6.  In the Action Outline, select **Outputs**

    1.  Select Create Output.

    2.  Set the output label and name `output`.

    3.  Set the output type to **JSON**.

        **Note:** The action can have multiple outputs, but there can only be one of type JSON.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select Script step output variable you created to store dynamic inputs.

7.  Click **Save** and [test the action](test-action.md).

    In the execution details, your data gathering action runs successfully if the runtime value for `output` contains the `data` property in the proper format.

8.  Click **Publish** to make the action available to other flows or actions within the same application scope.


## Result

You can now use your data gathering action to add arbitrary action inputs to a parent action.![Use your data gathering action to populate options for a dynamic template.](../images/create-data-gathering-action-dynamic-inputs-result.png)

**Parent Topic:**[Dynamic inputs](../concept/dynamic-inputs.md)

**Related topics**  


[Get started with dynamic inputs](getting-started-dynamic-input.md#)

[Create a data gathering action for a dynamic choice](create-data-gathering-action-dynamic-choice.md)

[Create a data gathering action for a dynamic template](create-data-gathering-action-dynamic-template.md)

[Dynamic input configuration options](../reference/dynamic-input-options.md)

