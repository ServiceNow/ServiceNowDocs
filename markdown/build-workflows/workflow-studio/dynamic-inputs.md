---
title: Dynamic inputs
description: Generate a list of action inputs or input values each time that someone configures the action in a flow. Dynamic inputs can display a list of related action inputs, a list of fields from a record, or a list of options available in a choice list.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Create an action in Workflow Studio, Building actions, Use, Workflow Studio, Build workflows]
---

# Dynamic inputs

Generate a list of action inputs or input values each time that someone configures the action in a flow. Dynamic inputs can display a list of related action inputs, a list of fields from a record, or a list of options available in a choice list.

**Note:** Dynamic inputs are not available in the base system. To use dynamic inputs in Workflow Studio, you must [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). Dynamic inputs are part of the ServiceNow Flow Designer - Introspection \[com.glide.hub.flow\_designer\_introspection\] plugin.

During flow design, dynamic inputs retrieve values and display them as inputs within an action dynamically. These types of dynamic inputs are available to action authors.

-   **Dynamic Choice**

    The Dynamic Choice type input gathers a list of choice values to display. For more information on building a dynamic choice, see [Create a data gathering action for a dynamic choice](../task/create-data-gathering-action-dynamic-choice.md).

-   **Dynamic Inputs**

    The Dynamic Inputs type input gathers a list of additional action inputs to display. Use Dynamic Inputs to add arbitrary inputs to an action. For more information on building dynamic inputs, see [Create a data gathering action for a dynamic inputs type input](../task/create-data-gathering-action-dynamic-inputs.md).

-   **Dynamic Template**

    The Dynamic Template type input gathers a list of fields from a dynamically selected record type. Flow authors can then select which fields to include in their flow. Because the list of fields is dynamically generated, you don't have to change the action when fields are added or removed from the source table. For more information on building a dynamic template, see [Create a data gathering action for a dynamic template](../task/create-data-gathering-action-dynamic-template.md).


There are three general steps to using dynamic inputs.

1.  An action author creates a data gathering action to generate dynamic data.
2.  An action author creates an action with a dynamic input and configures the dynamic input to call the data gathering action.
3.  A flow author adds the action to a flow and configures the action with dynamically gathered data.

## Data gathering actions

A data gathering action collects data to be used by other actions. Data gathering actions are intended to be called from dynamic inputs rather than be added directly to a flow. Data gathering actions typically collect data from third-party systems using a REST call. All data gathering actions must meet these requirements and constraints.

-   The action has a [script step](../reference/javascript-step-action-designer.md) that contains an output variable of type JSON.
-   The action has an output named **output** of type JSON whose value is derived from the script step's JSON output variable.

    **Note:** The action can have multiple outputs but can only have one of type JSON.

-   The script step formats the JSON output to have a property named `data`.
-   The JSON output should not return more than 5000 choice options, field template values, or array element items when the data is intended for a dynamic choice or a dynamic template input.

    **Note:** Dynamic choice and dynamic template inputs can only display up to 5000 choice options or 5000 template values from the JSON output.

-   The action waits for up to 300 seconds \(5 minutes\) to gather data before it times out.

    **Note:** To change the timeout period for all actions, modify the value of the **sn\_flow\_designer.sync\_action\_execution\_timeout\_in\_seconds** system property.


## Supported dynamic input data types

Dynamic inputs support a limited number of ServiceNow AI Platform data types. You can use the example JSON to build your own dynamic inputs. You can change the values of the label and name properties to met your needs. The type property must specify a ServiceNow AI Platform data type name. For more information about ServiceNow AI Platform field data types and how to configure them, see [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

<table id="table_xv2_2lh_xcc"><thead><tr><th>

Input data type

</th><th>

Example JSON

</th></tr></thead><tbody><tr><td>

[Choice](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

</td><td>

```
{ 
    data: [{
      label: 'Choice type input',
      name: 'choicetype',
      defaultValue: 'choice_1',
      type: 'choice',
      choices: [
          { label: 'Choice 1', value: 'choice_1' },
          { label: 'Choice 2', value: 'choice_2' }
      ]
    }]
  }
```

</td></tr><tr><td>

Datetime

</td><td>

```
{ 
    data: [{
      label: 'Datetime type input',
      name: 'datetimetype',
      type: 'datetime',
    }]
  }
```

</td></tr><tr><td>

Decimal

</td><td>

```
{ 
    data: [{
      label: 'Decimal type input',
      name: 'decimaltype',
      type: 'decimal',
    }]
  }
```

</td></tr><tr><td>

Email

</td><td>

```
{ 
    data: [{
      label: 'Email type input',
      name: 'emailtype',
      type: 'email',
    }]
  }
```

</td></tr><tr><td>

[HTML](https://www.servicenow.com/docs/access?context=c_UseHTMLFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

</td><td>

```
{ 
    data: [{
      label: 'HTML type input',
      name: 'htmltype',
      type: 'html',
    }]
  }
```

</td></tr><tr><td>

Integer

</td><td>

```
{ 
    data: [{
      label: 'Integer type input',
      name: 'integertype',
      type: 'integer',
    }]
  }
```

</td></tr><tr><td>

Password 2

</td><td>

```
{ 
    data: [{
      label: 'Password2 type input',
      name: 'password2type',
      type: 'password2',
    }]
  }
```

</td></tr><tr><td>

[Reference](https://www.servicenow.com/docs/access?context=c_ReferenceField&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

</td><td>

```
{ 
    data: [{
      label: 'Reference type input',
      name: 'referencetype',
      reference: 'sys_user',
      type: 'reference',
    }]
  }
```

</td></tr><tr><td>

String

</td><td>

```
{ 
    data: [{
      label: 'String type input',
      name: 'stringtype',
      defaultValue: 'abcdef',
      type: 'string',
      mandatory: true
    }]
  }
```

</td></tr></tbody>
</table>## General guidelines

-   **Consider dynamic inputs for third-party integrations**

    Dynamic inputs let you create flows that fetch data dynamically from external sources. In third-party integrations, dynamic inputs can provide data values that pertain to a particular endpoint. For more information on setting up third-party integrations with Workflow Studio, see [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

-   **Be aware of the time required to retrieve large amounts of data**

    By default, dynamic inputs have up to 300 seconds to gather data before they time out. If your data gathering action needs more time to gather data, set the **sn\_flow\_designer.sync\_action\_execution\_timeout\_in\_seconds** system property to a higher value. However, don't use long timeout values for interactive flows where an end user must enter or select a value.

-   **Be aware of scripting errors**

    Because all data gathering actions use a script step, potential errors could occur from scripting. When using scripts to output JSON variables for your dynamic inputs, you may encounter errors that prevent inputs from receiving the JSON values they need. When a dynamic input scripting error occurs, the following warning message may appear.

    ![Dynamic action error message](../images/warning-dynamic-action-error.png "Message displayed for scripting error")

-   **Limit dynamic inputs type inputs to 40 input values**

    A dynamic inputs type input can only render a certain number of inputs before the JSON object becomes to too big to store in memory. Limiting your dynamic inputs to 40 input values minimizes the chances that you will run out of memory and experience unexpected behaviors such as rendering errors or data truncation.

-   **Limit JSON output to 5000 array items for dynamic templates and dynamic choices**

    Dynamic choice and dynamic template inputs can only display up to 5000 array items. A dynamic choice can only display up to 5000 choice list options, and a dynamic template can only display up to 5000 field template values. If your data gathering action collects data for a dynamic template or a dynamic choice, restrict the maximum number of array items it returns to 5000. The 5000 array items limit prevents the instance from having performance issues when rendering the choices or field values.


-   **[Get started with dynamic inputs](../task/getting-started-dynamic-input.md#)**  
Create a sample action that illustrates using all available types of dynamic inputs in a flow.
-   **[Create a data gathering action for a dynamic choice](../task/create-data-gathering-action-dynamic-choice.md)**  
Create a data gathering action to generate a list of choice options for a dynamic choice input.
-   **[Create a data gathering action for a dynamic template](../task/create-data-gathering-action-dynamic-template.md)**  
Create a data gathering action to collect record field values for a dynamic template input.
-   **[Create a data gathering action for a dynamic inputs type input](../task/create-data-gathering-action-dynamic-inputs.md)**  
Create a data gathering action to create arbitrary action inputs using a dynamic inputs type input.
-   **[Dynamic input configuration options](../reference/dynamic-input-options.md)**  
Use these options to configure dynamic inputs.

**Parent Topic:**[Create an action in Workflow Studio](../task/create-action.md)

