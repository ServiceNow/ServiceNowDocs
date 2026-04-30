---
title: Dynamic outputs
description: Access action and subflow outputs as dynamically generated data pills during flow design. You can also build data gathering actions to generate complex objects from ServiceNow AI Platform and Integration Hub outputs.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-02-05"
reading_time_minutes: 3
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Dynamic outputs

Access action and subflow outputs as dynamically generated data pills during flow design. You can also build data gathering actions to generate complex objects from ServiceNow AI Platform and Integration Hub outputs.

**Note:** Dynamic outputs are not available in the base system. To use dynamic outputs in Workflow Studio, you must [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US). Dynamic outputs are part of the ServiceNow Flow Designer - Introspection \[com.glide.hub.flow\_designer\_introspection\] plugin.

During the flow design, a dynamic output retrieves the complex object's schema values and displays them as data pills in the data panel.

A dynamic output must point to a data gathering action that collects the displayed data. For example, a data gathering action can retrieve values from a third-party system as part of an [Integration Hub spoke](https://www.servicenow.com/docs/access?context=spokes-list&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US). To use a dynamic output in Workflow Studio:

1.  An action designer creates a data gathering action.
2.  An action designer creates a parent action with a dynamic output that points to the child data gathering action.
3.  A flow designer adds the parent action to a flow.

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


## Dynamic object

A dynamic object is either a complex object or an array of complex objects. Action designers build the object structure dynamically with a data gathering action rather than hard-coding it. For more information on building a dynamic object, see [Create a data gathering action for a dynamic object](../task/create-data-gathering-action-dynamic-object.md).

## General guidelines

-   **Use dynamic outputs for third-party integrations**

    Use dynamic outputs to introspect and fetch data from external systems during the flow design. For example, you can specify service endpoints or call actions that interact with specific endpoint APIs. For more information on setting up third-party integrations with Workflow Studio, see [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **Note the time that is required to retrieve large amounts of data**

    By default, dynamic outputs have up to 300 seconds to gather data before the system stops them. If your data gathering action needs more time to gather data, set the **sn\_flow\_designer.sync\_action\_execution\_timeout\_in\_seconds** system property to a greater value. Avoid long timeout values for interactive flows where an end user is expecting to enter or select a value.

-   **Be aware of scripting errors**

    Because all data gathering actions use a script step, potential errors could occur from scripting. Review any scripts that are used to output JSON variables because script errors may prevent the outputs from receiving the JSON values that they need. When a dynamic output scripting error occurs, the following warning message may appear.

    ![Dynamic action error message](../images/warning-dynamic-action-error.png "Message that is displayed for scripting error")


-   **[Get started with dynamic outputs](../task/getting-started-dynamic-output.md#)**  
Create a sample action that builds dynamic outputs for use in a flow.
-   **[Create a data gathering action for a dynamic object](../task/create-data-gathering-action-dynamic-object.md)**  
Create an action to collect output values. Then, pass the values to a parent action as a dynamic object.
-   **[Dynamic output configuration options](../reference/dynamic-output-options.md)**  
Use these options to configure your dynamic outputs for a parent action.

**Parent Topic:**[Create an action in Workflow Studio](../task/create-action.md)

