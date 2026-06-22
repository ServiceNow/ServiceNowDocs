---
title: Configure subflow conversational settings
description: Configure conversation settings to make a subflow available to conversational interfaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/configure-subflow-conversation-settings.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-03-03"
reading_time_minutes: 5
breadcrumb: [Conversational subflows, Exploring subflows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Configure subflow conversational settings

Configure conversation settings to make a subflow available to conversational interfaces.

## Before you begin

Role required:

-   admin or flow\_designer
-   virtual\_agent\_admin

**Important:** Edit the **Now Assist Panel - Platform \(default\)** assistant and make sure that the Subflows and actions skill is assigned to the assistant. For information about editing an assistant, see [Manage LLM virtual agents on the Assistants screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/manage-llm-va.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  From the list of all subflows, select the subflow that you want to configure.

4.  Click the more actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions menu\) and select **Conversational settings**.

5.  Configure the general settings.

    \[Omitted image "conversational-settings-subflow-general-01.png"\] Alt text: Example general settings for the Send SMS subflow.

    |Field|Description|
    |-----|-----------|
    |Is conversational|The option to make the subflow available to conversational interfaces. When enabled, you can call the subflow from a conversation.|
    |Subflow skill name|The name that a virtual agent displays for the skill in the list of available topics.|
    |Subflow skill description|The search terms and keywords that someone might use in a conversation to call this subflow. The more descriptive the skill, the better AI Search can be in matching it to an utterance.|
    |Assistants where subflow is discoverable|The list of virtual assistants where this subflow is discoverable.|
    |Roles which can access this|The roles you must have to access this subflow from a virtual agent.|

6.  Configure the subflow inputs and outputs.

    \[Omitted image "conversational-settings-50.png"\] Alt text: Example inputs and outputs of the Send SMS subflow.

<table id="table_lnb_4lx_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate descriptions

</td><td>

Option to generate descriptions for the conversational inputs and outputs of the subflow by using generative AI. Now Assist generates a description for all the inputs and outputs where the description field is empty. Regenerating the descriptions does not overwrite descriptions that you previously saved.The AI-generated fields are marked with the AI icon \[Omitted image "icon-ai-generated.png"\].

</td></tr><tr><td>

Show/hide checkbox

</td><td>

Controls the visibility of a subflow input or output in a conversation. Select the field if you want to make the field visible in the conversation.\[Omitted image "conversational-show-hide.png"\] Alt text: Screen displaying the show-hide checkboxes for fields.

To hide a mandatory field, you must provide a default value for the field.

</td></tr><tr><td>

Conversational inputs

</td><td>

The list of subflow inputs that are available to conversational interfaces.

</td></tr><tr><td>

Default value

</td><td>

Provides a default value for the conversational input.During a conversation, users can provide their own value or proceed with the default value.

**Tip:**

You can pass an input value without user interaction by assigning a default value and making the input field hidden.

</td></tr><tr><td>

Describe this input

</td><td>

The search terms and keywords that someone might use in a conversation to set this input. The more descriptive the input, the better AI Search can be in matching it to an utterance. You must provide a description for mandatory inputs.

</td></tr><tr><td>

Override with reference

</td><td>

The option to look up and insert an existing value from a selected table and reference field. Rather than require users to manually type in a value, this option allows users to select from a list of existing record values. When run, the input uses the value that the user selected from the list.

 This option is available for inputs with the Email, GUID, Integer, Long, Long Integer String, String, and String \(Full UTF8\) data types.

**Note:** The Document ID and Reference data types are not valid options, because the system automatically overrides these input types with a list of display values as defined by the table's reference field. For more information about display values and reference fields, see [Display values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/c_DisplayValues.md).

 Turning on this option displays the **Table** and **Reference field** options.

 \[Omitted image "override-with-reference.png"\] Alt text: Example of Table and the Reference fields after selecting the override with reference option.

</td></tr><tr><td>

Table

</td><td>

The table containing the reference field that you want to use to display a list of existing values. For example, the User \[sys\_user\] table contains string fields to select a user by name.

</td></tr><tr><td>

Reference field

</td><td>

The field whose existing record values you want to display as a list of options. This input displays a list of options based on the reference field's data type. The data type of the reference field you select should match the data type of the input. Select a field that contains both meaningful and unique values. For example, if you have a string input for user names, then select a string field such as name from the User \[sys\_user\] table. In a conversation, the input displays a list of string user names to choose from such as `Abel Tuter` or `Beth Anglin`.

**Note:** This option is not available for inputs with the GUID data type, because each table already has a unique field that stores its Sys ID value.

 \[Omitted image "example-input-string-user-name-01.png"\] Alt text: Example conversation where a string input shows a list of user names to choose from.

 For more information about display values and reference fields, see [Display values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/c_DisplayValues.md).

</td></tr><tr><td>

Conversational outputs

</td><td>

The list of subflow outputs that are available to conversational interfaces.

</td></tr><tr><td>

Describe this output

</td><td>

The search terms and keywords that someone might use in a conversation to set this output. The more descriptive the output, the better AI Search can be in matching it to an utterance. You must provide a description for mandatory outputs.

</td></tr></tbody>
</table>7.  Configure conversational advanced settings.

    \[Omitted image "conversational-settings-advanced.png"\] Alt text: Example of advanced settings.

    |Field|Description|
    |-----|-----------|
    |Include in discovery|The option to make this subflow discoverable from a virtual agent.|
    |Include in list of topics|The option to include this subflow in the list of available topics.|
    |Promote skill|The option to display this subflow higher in the list when someone asks to see all available skills.|
    |Use autonomous mode|The option to create, view, update, or delete records without asking for a confirmation.|
    |Enable follow-up|The option to retain the context of previous conversations so that the users can ask follow-up questions, provide additional details, and continue the conversation.|
    |Channels|The list of default channels in which this subflow is available.|

8.  Select **Save and close**.


**Parent Topic:**[Conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/conversational-subflows.md)

**Parent Topic:**[Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/subflows.md)

