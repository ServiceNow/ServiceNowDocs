---
title: Create a data gathering action for a dynamic template
description: Create a data gathering action to collect record field values for a dynamic template input.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Dynamic inputs, Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a data gathering action for a dynamic template

Create a data gathering action to collect record field values for a dynamic template input.

## Before you begin

-   Role required: action\_designer or admin
-   Create credentials and connections for your REST endpoint

**Note:** Dynamic inputs are not available in the base system. To use dynamic inputs in Workflow Studio, you must [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Create new** &gt; **Action**.

3.  In the **Action name** field, enter a name for your action, choose the proper **Application** scope, and then select **Submit**.

4.  From the Action Outline, select **Inputs**.

    You may need to create an input to provide a table name or a dynamic URL path to your REST step.

    For example, create a String input to store a table name. See [Create a data gathering action to get field names](getting-started-dynamic-input.md#) for instructions.

5.  In the Action Outline under Inputs, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) and select the **REST** step.

    1.  From the Connection Details, select a connection alias or define a connection inline.

        A connection alias allows you to update connection details without having to edit the action.

        For example, select an connection alias to your local instance.

    2.  For the Request Details, select a method to build a request, provide a resource path, select an HTTP method, and provide any query parameters.

        Data gathering actions generally use a GET HTTP method to request data from a REST endpoint. For more information on using the REST step in Integration Hub, see [REST step](../reference/rest-request-action-designer.md) and [REST in IntegrationHub](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_paris_rest_in_integrationhub/app_store_learnv2_rest_paris_rest_in_integrationhub_objectives?v=paris).

6.  In the Action Outline under the REST step, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) and select the **Script** step.

    1.  From Input Variables, select **Create Variable**, and create an input variable to store the REST response body.

    2.  For the input variable Value, select the data pill for the REST step's **Response Body** output.

    3.  In Script, enter a script to create a JSON output from the input variable.

        Your script needs to do these tasks.

        -   **Parse the input variable as JSON**

            You can use the [JSON - Global](https://www.servicenow.com/docs/access?context=c_JSONAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API to transform the input variable from a string to a JSON object.

        -   **Create a new JSON object formatted for a dynamic template**

            You must know the data structure of the REST Response to map response values to template values. Your script must create a dynamic template JSON object that has a property named `data`. The value of the data property must be an array of template values. Each template value must have a `label` property, a `name` property, and an empty `value` property. The label property determines how the template value option appears in the action. The name property determines how the template value option is stored and referred to in the system. The value property is empty so that the value can be set dynamically when the action is configured.

            For example, this JSON object defines an array of template values from the incident table.

            ```
            {
                "data": [
                  {
                    "name": "parent",
                    "label": "Parent",
                    "value": ""
                  },
                  {
                    "name": "number",
                    "label": "Number",
                    "value": ""
                  },
                  {
                    "name": "state",
                    "label": "State",
                    "value": ""
                  },
                  {
                    "name": "active",
                    "label": "Active",
                    "value": ""
                  },
                  {
                    "name": "priority",
                    "label": "Priority",
                    "value": ""
                  },
                  {
                    "name": "caller_id",
                    "label": "Caller id",
                    "value": ""
                  },
                  {
                    "name": "short_description",
                    "label": "Short description",
                    "value": ""
                  },
                  {
                    "name": "description",
                    "label": "Description",
                    "value": ""
                  },
                  {
                    "name": "sys_id",
                    "label": "Sys id",
                    "value": ""
                  },
                  {
                    "name": "urgency",
                    "label": "Urgency",
                    "value": ""
                  },
                  {
                    "name": "assigned_to",
                    "label": "Assigned to",
                    "value": ""
                  },
                  {
                    "name": "severity",
                    "label": "Severity",
                    "value": ""
                  },
                  {
                    "name": "category",
                    "label": "Category",
                    "value": ""
                  }
                ]
            }
            ```

            **Note:** A dynamic template input can only display up to 5000 field template values. A JSON object that returns more than 5000 field template values will be truncated when it is rendered.

        -   **Set the outputs object**

            Set the outputs object to return your dynamic template JSON object.

    4.  From Output Variables, select **Create Variable**.

        This output variable stores the template values your script creates.

    5.  For the output variable type, select **JSON**.

        The script output variable type must be JSON.

7.  In the Action Outline, select **Outputs**

    1.  Select Create Output.

    2.  Set the output label and name `output`.

    3.  Set the output type to **JSON**.

        **Note:** The action can have multiple outputs, but there can only be one of type JSON.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select Script step output variable you created to store template values.

8.  Click **Save** and [test the action](test-action.md).

    In the execution details, your data gathering action runs successfully if the runtime value for `output` contains the `data` property in the proper format.

9.  Click **Publish** to make the action available to other flows or actions within the same application scope.


## Result

You can now use your data gathering action to populate the options that appear for a dynamic template input in a parent action.![Use your data gathering action to populate options for a dynamic template.](../images/create-data-gathering-action-dynamic-template-result.png)

**Parent Topic:**[Dynamic inputs](../concept/dynamic-inputs.md)

**Related topics**  


[Get started with dynamic inputs](getting-started-dynamic-input.md#)

[Create a data gathering action for a dynamic choice](create-data-gathering-action-dynamic-choice.md)

[Create a data gathering action for a dynamic inputs type input](create-data-gathering-action-dynamic-inputs.md)

[Dynamic input configuration options](../reference/dynamic-input-options.md)

