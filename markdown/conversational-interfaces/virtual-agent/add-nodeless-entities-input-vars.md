---
title: Add nodeless NLU entities as input variables to a topic
description: You can add nodeless NLU entities as input variables to a topic if NLU is enabled for Virtual Agent. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Nodeless, NLU, Natural Language Understanding, entity, input, variables, topic, slot-filled, Virtual Agent, Variables]
breadcrumb: [Creating a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Add nodeless NLU entities as input variables to a topic

You can add nodeless NLU entities as input variables to a topic if NLU is enabled for Virtual Agent. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

If a custom control prompts a user for a date and the user mentioned a date in their initial utterance, you can capture that without prompting the user again. To prompt the user when not slot-filled, use input controls.

For more information about NLU entities, see Entities. For more information about system entities, see [NLU system entities](../reference/nlu-system-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Open a topic and view the **Flow** tab.

3.  In the sidebar, select the Variables tab, and select the **Input** icon ![](../images/icon-plus-clear.png).

4.  On the form, fill in the fields.

<table id="table_ncp_hnp_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input Types

</td><td>

Data type of the input. The fields on the dialog box change according to your choice.-   **String**: Alphanumeric text. Shows the **Input format** field. Choose plain text or a conforming rule, depending on the type of data.
-   **True/False**: Boolean value, either yes or no.
-   **Date Time**: Date, time, or both. Shows the **Input format** field.
-   **Static Choice**: Defined user choices. Shows **Display name** and **Value to store** field pairs.
-   **Dynamic Choice**: Choice of table records. Shows **Populate choices by**, **Table**, and **Filter choices** fields. The value can be either conditional or scripted.
 For details, see [Input data types in Virtual Agent topics](../reference/va-data-types.md).

</td></tr><tr><td>

Name

</td><td>

Name of the variable for the entity.Variable names must be unique within the scope of a topic. The name appears as a variable when used in dot walking.

</td></tr><tr><td>

NLU Entity

</td><td>

The NLU entity associated with the node.This could be a pre-built Virtual Agent entity that you import into the model, a system entity \(such as DURATION, TIME, or MONEY\), or a custom entity that you created.

</td></tr><tr><td class="sub-head" colspan="2">

String data type properties

</td></tr><tr><td>

Input format

</td><td>

Text format that is validated when a user enters certain text items. If the user doesn't enter the expected format, an error message indicates that the format is not valid and asks the user to reenter the text.

 Choose the format of the text item to be validated:

-   Text: Any text string \(no validation\)
-   Email: Format that consists of an email prefix \(user name\), @ symbol, and domain.
-   IP address \(IPV4, IPV6\): Data communication delivery format for Internet Protocol version 4 or version 6.
-   Phone number \(E.164\): Internationally recognized standard phone number format.
-   URL: Web address format
-   Custom: Script that provides a text validation rule for a custom text format and the related error messages displayed when the expected format is not entered.
**Note:** For phone and IP address format examples, see E.164 phone formats and IP address field types.

</td></tr><tr><td class="sub-head" colspan="2">

Date Time data type properties

</td></tr><tr><td>

Input format

</td><td>

Type of Date Time control to be displayed. Select one of the following formats:-   **Date**: Shows only the monthly calendar for the user to select the date.
-   **DateTime**: Shows both a monthly calendar and time picker.
-   **Time**: Shows only the time picker for the user to select the time \(hours and minutes\).


</td></tr><tr><td class="sub-head" colspan="2">

Static Choice data type properties

</td></tr><tr><td>

Choices\[For Static Choice data type\]

</td><td>

Enter two or more choices as follows:-   **Display name**: Short phrase or text that appears to the user for that choice.
-   **Value to store**: The string that is stored in the variable when the corresponding choice is selected.


</td></tr><tr><td class="sub-head" colspan="2">

Dynamic Choice data type properties

</td></tr><tr><td>

Populate choices by

</td><td>

Type of dynamic variable to be used. Select one of the following options: -   **Record**: Returns records from the table selected. The values for these options are GlideRecord objects.
-   **Script**: Expression that returns an array of options.


</td></tr><tr><td>

Table\[Record values only\]

</td><td>

If you selected **Record** as the method to populate choices, select the table to be searched.

</td></tr><tr><td>

Filter choices\[Record values only\]

</td><td>

Select one of the following:-   **Condition Builder**: Creates a filter used to select a subset of records from the table.
-   **Script**: Defines the enumeration list for the options \(choice list\) to be displayed. The name value pair is stored as a string object.


</td></tr></tbody>
</table>5.  Select **Save**.

    NLU entities appear alongside topic input variables in the Variables sidebar.

    ![NLU entities appear with input variables in the Variables sidebar. A copy icon appears alongside the view icon.](../images/nlu-entities-input-palette.png)

    **Note:**

    You can remove a slot-filled value to prompt the user again \(unbind it from the initial input value\). For more information, read about the vaInputs.myvar.unbindEntity\(\); method in [Virtual Agent scripts](../concept/virtual-agent-scripts.md).


**Parent Topic:**[Creating a Virtual Agent topic](create-virtual-agent-topic.md)

