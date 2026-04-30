---
title: Inline scripts
description: Enable users with coding experience to write inline scripts that set and modify input values during the configuration of an action or flow. Use inline scripts to modify input values that require small format conversions, data transformations, or math operations.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Building flows, Use, Workflow Studio, Build workflows]
---

# Inline scripts

Enable users with coding experience to write inline scripts that set and modify input values during the configuration of an action or flow. Use inline scripts to modify input values that require small format conversions, data transformations, or math operations.

You can also modify input values without scripting by using transform functions. For a list of available options, see [Transform functions](transform-functions.md).

Workflow Studio displays a Script button when you configure these components.

-   Action inputs when you configure the action for a flow
-   Action outputs when you configure the action for a flow
-   Flow logic inputs when you configure the flow logic for a flow
-   Flow logic outputs when you configure the flow logic for a flow
-   Step inputs when you configure the step for an action.
-   Subflow inputs when you configure the subflow for a flow.
-   Subflow ouputs when you configure the subflow for a flow.

Inline scripts must return values in the same data type as the input expects. For example, an inline script for a Record input must return a GlideRecord object and an inline script for a Date input must return a date-time value. Always test actions and flows containing inline scripts, and verify that there are no runtime errors in the flow execution details.

Script writers should be familiar with ServiceNow AI Platform table structures and [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). In addition, they should know how to work with record and system data using the ServiceNow API.

## Benefits

Inline scripts offer these benefits.

-   Enable simple data conversion or transformation without having to create custom actions or flows.
-   Identify which input data a script affects.
-   Restricted access to scripting features to users or groups who are knowledgeable with the available ServiceNow APIs.

## Access to inline script

You can grant users access to online scripting by either granting them the flow\_designer\_scripting role or the **Allow Scripting** delegated development permission. Both the role and the developer permission display a script button field for each Workflow Studio input.

## Script button

When you enable a user to create inline scripts, Workflow Studio displays a script button next to flow and step inputs.

![Inputs available for the Log action. The Level and Message inputs display Script buttons.](../images/inline-script-button-01.png "Script buttons display beside inputs")

Clicking the **Script** button opens the Script editor, which replaces the standard input interface. Enter a script to compute the input value.

Ensure your script includes a `return` statement with the results of your script. For example, `return shortDesc;` returns the value of the `shortDesc` variable.

![Inputs available for the Log action. The Message input displays the Script editor and a script that returns a math calculation for the square root of 64.](../images/inline-script-button-02.png "Script editor for input")

Clicking the **Collapse Script** button hides the Script editor and displays a read-only version of the input. Clicking the **Expand Script** button displays the Script editor and allows you to edit the script.

![Inputs available for the Log action. The Message input displays the text Scripted (expand to edit).](../images/inline-script-button-03.png "Input containing script")

## Workflow Studio data object

Script writers can use the `fd_data` object to access data from previous actions and steps. Use the `fd_data` object to dot-walk to a specific output of the flow. You can use the script editor type ahead suggestions to select a specific output value. For example, enter `fd_data` and select `_2__for_each.item` from the type ahead suggestions to create a dot-walk reference to `fd_data._2__for_each.item`. This reference accesses data from the second output of the flow, which in this example is a For Each flow logic item.

**Important:** The fd\_data object always requires a dot-walk reference to a specific flow output. Without a dot-walk reference, the inline script cannot access Workflow Studio data.

Workflow Studio updates the data object each time you save your action, flow, or subflow. If the type ahead suggestions do not include your target, try saving the action, flow, or subflow, and then retyping the period character to refresh the list of suggestions.

|Data Target|Reference Syntax|Example|
|-----------|----------------|-------|
|Action input|`fd_data.action_inputs.`*action-input-name*|`var task = fd_data.action_inputs.task;`|
|Flow variable|`fd_data.flow_var.`*flow-variable-name*|`var shortDesc = fd_data.flow_var.short_description;`|
|Output of prior action, flow logic, or step|`fd_data._`*output-target-step-number*`__`*output-target-name*|`var taskRecord = fd_data._2__create_task;`|
|Subflow input|`fd_data.subflow_inputs.`*subflow-input-name*|`var reqItem = fd_data.subflow_inputs.requested_item;`|
|Trigger|`fd_data.trigger.`*trigger-data-pill*|`var incident = fd_data.trigger.current;`|

## General guidelines

Follow these general guidelines to create reusable and maintainable inline scripts.

-   **Write inline script for small non-reusable logic**

    Use inline script format or modify the data for specific inputs and use cases. For standard and reusable input data conversions and formatting operations, select a transform function instead.

-   **Review available transform functions**

    Workflow Studio provides a list of standard transform functions for data conversions and formatting operations. Rather than write and maintain a custom script solution, select an existing transform function if one is available.

-   **Call script includes from inline script**

    Call a script include from your inline script to reduce the amount of code you write and also to maintain common code in a single location. Use the class constructor to call your script include. For more information about creating a script include, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

    ```
    var si = new MyScriptInclude();
    si.functionOne();
    ```

-   **Create custom actions or subflows for reusable code rather than inline script**

    Create custom actions or subflows for reusable or complex data logic such as changing the data type of source data. You may also want to provide custom actions or subflows for flow designers who are not comfortable with code.

-   **Avoid duplicating action and flow functionality**

    Avoid writing inline script that duplicates action and flow functionality. For example, rather than write inline script to perform record operations, use the create and update record baseline actions.

-   **Avoid data type changes**

    Avoid runtime errors by verifying that your inline script provides information in the same data type as the input or output expects.

-   **Create variables by declaring them with the var keyword**

    Use the `var` keyword to declare variables so that they remain within the proper JavaScript scope. When you create a variable by assigning it a value, JavaScript may attach it to the global object, which can result in variable values persisting outside of the local scope and causing errors.

-   **Process records outputs with For Each flow logic and the flow data object**

    Inline script can only access the **records** output of a Look Up Records action from For Each flow logic. Add a Look Up Records action to the flow to generate the records output. Add a For Each flow logic to the flow to process each record in the records output. Create an inline script reference to the For Each flow logic using the fd\_data and item objects. For example, this reference assumes that the For Each flow logic is the second item in your flow outline `fd_data._2__for_each.item`.

-   **Use type ahead suggestions to generate references to flow and action data.**

    Create references to flow and action data using the fd\_data object. The script editor displays type ahead suggestions for existing flow and action data when you type `fd_data`. Select a suggestion to build references to flow and action data.

    **Note:** Refer to record data in a For Each flow logic using the **item** object.

-   **Scope loop counters**

    Script loops don't have a maximum number of iterations, so loops execute infinitely when there is not a valid exit condition.

    To make sure that there is a valid exit condition, use scope loop counters in inline scripts or in script steps within an action. Add `var` to`for (i=0; i< length; i++)` and get `for (var i=0; i< length; i++)`


## Licensing considerations

Inline scripts that call integration APIs are subject to Integration Hub licensing.

## Code editor

The code editor provides text editor support for inline scripts.

The code editor has these features for the supported language services and [Inline scripts](inline-scripts.md).

-   Syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes
-   Auto-suggestions and auto-completions

![Code editor in Workflow Studio](../../../script/general-scripting/image/monaco-editor.png "Code editor")

## Editing tips

-   To insert a fixed space anywhere in your code, press Tab.
-   To indent a single line of code, click in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab. To decrease the indentation, press Shift+Tab.
-   To remove one tab from the start of a line of code, click in the line and press Shift+Tab.
-   To declare variables, use the `var` keyword so that they remain within the proper JavaScript scope.

**Parent Topic:**[Building flows](flows.md)

