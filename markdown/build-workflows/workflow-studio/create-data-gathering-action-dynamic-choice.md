---
title: Create a data gathering action for a dynamic choice
description: Create a data gathering action to generate a list of choice options for a dynamic choice input.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Dynamic inputs, Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a data gathering action for a dynamic choice

Create a data gathering action to generate a list of choice options for a dynamic choice input.

## Before you begin

-   Role required: action\_designer or admin
-   Create credentials and connections for your REST endpoint

**Note:** Dynamic inputs are not available in the base system. To use dynamic inputs in Workflow Studio, you must Request an Integration Hub plugin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Create New** &gt; **Action**.

3.  In the **Name** field, enter a name for your action, choose the proper **Application** scope, and then select **Submit**.

4.  In the Action Outline, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) under **Inputs** and select the **REST** step.

    Configure your REST step to get data from the proper **Base URL** and **Resource Path** with any applicable **Query Parameters** for the **HTTP Method** `GET`. For more information on using the REST step in Integration Hub, see [REST step](../reference/rest-request-action-designer.md) and [REST in IntegrationHub](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_paris_rest_in_integrationhub/app_store_learnv2_rest_paris_rest_in_integrationhub_objectives?v=paris).

5.  In the Action Outline under the REST step, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) and select the **Script** step.

    1.  From Input Variables, select **Create Variable**.

        This input variable stores the REST response body.

        For example for the input variable Name, enter `payload`.

    2.  For the input variable Value, select the data pill for the REST step's **Response Body** output.

    3.  In Script, enter a script to create a JSON output from the input variable.

        Your script needs to do these tasks.

        -   **Parse the input variable as JSON**

            You can use the JSON - Global API to transform the input variable from a string to a JSON object.

        -   **Create a new JSON object formatted for a dynamic choice**

            You must know the data structure of the REST Response to map response values to choice list options. Your script must create a dynamic choice JSON object that has a property named `data`. The value of the data property must be an array of choice list options. Each choice list option must have a `label` and a `name` property set to string values. The label property determines how the option appears in the choice list. The name property determines how the option is stored and referred to in the system.

            For example, this JSON object defines an array with three choice list options.

            ```
            {
                data: [
                    {
                        label: "Choice Option 1",
                        name: "choice_option_1"
                        
                    }, 
                    {
                        label: "Choice Option 2",
                        name: "choice_option_2"
                    }, 
                    {	
                        label: "Choice Option 3",
                        name: "choice_option_3"
                    }
                ]
            }
            ```

            **Note:** A dynamic choice input can only display up to 5000 choice list options. A JSON object that returns more than 5000 choice list options will be truncated when it is rendered.

        -   **Set the outputs object**

            Set the outputs object to return your dynamic choice JSON object.

    4.  From Output Variables, select **Create Variable**.

        This output variable stores the choice list options your script creates.

    5.  For the output variable type, select **JSON**.

        The script output variable type must be JSON.

6.  In the Action Outline, select **Outputs**

    1.  Select Create Output.

    2.  Set the output label and name `output`.

    3.  Set the output type to **JSON**.

        **Note:** The action can have multiple outputs, but there can only be one of type JSON.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select Script step output variable you created to store choice list options.

7.  Select **Save** and [test the action](test-action.md).

    The runtime value for `output` must be a JSON object that has a `data` property and an array of choice list options.

    ![Example output from testing action](../images/example-output-dga-dynamic-choice.png)

8.  Select **Publish** to make the action available to other flows and actions within the same application scope.


## Result

You can now use your data gathering action to populate the options that appear for a dynamic choice input in a parent action.![Use your data gathering action to populate options for a dynamic choice.](../images/create-data-gathering-action-dynamic-choice-result.png)

**Parent Topic:**[Dynamic inputs](../concept/dynamic-inputs.md)

**Related topics**  


[Get started with dynamic inputs](getting-started-dynamic-input.md#)

[Create a data gathering action for a dynamic template](create-data-gathering-action-dynamic-template.md)

[Create a data gathering action for a dynamic inputs type input](create-data-gathering-action-dynamic-inputs.md)

[Dynamic input configuration options](../reference/dynamic-input-options.md)

