---
title: Configure subflow conversational settings
description: Configure conversation settings to make a subflow available to conversational interfaces.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 6
breadcrumb: [Building subflows, Use, Workflow Studio, Build workflows]
---

# Configure subflow conversational settings

Configure conversation settings to make a subflow available to conversational interfaces.

## Before you begin

Role required:

-   admin or flow\_designer
-   now.assist.creator

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  From the list of all subflows, select the subflow that you want to configure.

4.  From the side panel, open **Conversational settings** \(![Option on the side panel to open conversational settings.](../images/conversational-settings-icon-z.png)\).

5.  Select the skill that you want to edit, or create a new skill.

6.  Configure the general settings.

    ![Example general settings for the Send SMS subflow.](../images/general-settings-conv-sublow-z.png)

<table id="table_rfk_qjx_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate skill metadata

</td><td>

Option to generate descriptions for the conversational skill, inputs, and outputs of the subflow by using generative AI. Workflow Studio generates a description for all the inputs and outputs where the description is empty. Regenerating the descriptions does not overwrite existing descriptions of any of the fields. **Tip:** This field is disabled if none of the description is field is empty.

The AI-generated fields are marked with the AI icon ![](../images/icon-ai-generated.png).

</td></tr><tr><td>

Is conversational

</td><td>

The option to make the subflow available to conversational interfaces. When enabled, you can call the subflow from a conversation through the skill.

</td></tr><tr><td>

Subflow skill name

</td><td>

The name that a virtual agent displays for the skill in the list of available topics.

</td></tr><tr><td>

Subflow skill description

</td><td>

The search terms and keywords that someone might use in a conversation to call this subflow. The more descriptive the skill, the better AI Search can be in matching it to an utterance. **Tip:** You can enter the description manually or use generative AI. To generate the description with generative AI, make sure that the field is empty and select **Generate skill metadata** ![Generate skill metadata icon.](../images/generate-skill-metadata-icon.png).

</td></tr><tr><td>

Assistants where subflow is discoverable

</td><td>

The list of virtual assistants where this subflow is discoverable.

</td></tr><tr><td>

Roles which can access this

</td><td>

The roles you must have to access this subflow from a conversation. During a conversation, the subflow displays the skill only to users who have the specified roles. You must specify the role in the subflow settings and in the Conversational settings. By default, users must have the sn\_conv\_fa.csa\_email\_write role to create records in the sys\_email table.

</td></tr></tbody>
</table>7.  Configure the subflow inputs and outputs.

    ![Example inputs and outputs of the Send SMS subflow.](../images/conversational-subflow-input-output-z.png)

<table id="table_lnb_4lx_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show/hide checkbox

</td><td>

Controls the visibility of an input or output in a conversation. Select the checkbox if you want to make the field visible in the conversation.![Option to select the visibility of inputs in a conversation.](../images/conversational-input-checkbox-z.png)

For example, you can take the message text as an input from the user during the conversation or you can have a default text and hide the input field during the conversation.

For a mandatory field, the checkbox is disabled until you specify a default value.

</td></tr><tr><td>

Conversational inputs

</td><td>

The list of subflow inputs that are available to conversational interfaces.

</td></tr><tr><td>

Describe this input

</td><td>

The search terms and keywords that someone might use in a conversation to set this input. The more descriptive the input, the better AI Search can be in matching it to an utterance. You must provide a description for mandatory inputs. **Tip:** You can enter the description manually or use generative AI. To generate the description with generative AI, make sure that the field is empty and select **Generate skill metadata** ![Generate skill metadata icon.](../images/generate-skill-metadata-icon.png).

</td></tr><tr><td>

Default value

</td><td>

Provides a default value for the conversational input.During a conversation, users can provide their own value or proceed with the default value.

**Tip:**

You can pass an input value without user interaction by assigning a default value and making the input field hidden.

</td></tr><tr><td>

Override with reference

</td><td>

The option to look up and insert an existing value from a selected table and reference field. Rather than require users to manually type in a value, this option allows users to select from a list of existing record values. When run, the input uses the value that the user selected from the list.

 This option is available for inputs with the Email, GUID, Integer, Long, Long Integer String, String, and String \(Full UTF8\) data types.

**Note:** The Document ID and Reference data types are not valid options, because the system automatically overrides these input types with a list of display values as defined by the table's reference field. For more information about display values and reference fields, see [Display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 Turning on this option displays the **Table** and **Reference field** options.

</td></tr><tr><td>

Table

</td><td>

The table containing the reference field that you want to use to display a list of existing values. For example, the User \[sys\_user\] table contains string fields to select a user by name.

</td></tr><tr><td>

Reference field

</td><td>

The field whose existing record values you want to display as a list of options. This input displays a list of options based on the reference field's data type. The data type of the reference field you select should match the data type of the input. Select a field that contains both meaningful and unique values. For example, if you have a string input for user names, then select a string field such as name from the User \[sys\_user\] table. In a conversation, the input displays a list of string user names to choose from such as `Abel Tuter` or `Beth Anglin`.

**Note:** This option is not available for inputs with the GUID data type, because each table already has a unique field that stores its Sys ID value.

 ![Example conversation where a string input shows a list of user names to choose from.](../images/example-input-string-user-name-01.png)

 For more information about display values and reference fields, see [Display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 You can use condition in the filter to limit the records that are referenced in this field. The filter helps you reduce the number of records from the referenced table and provide the most relevant options in the conversation.

 ![Option to apply filter for records in the Reference field.](../images/reference-field-filter-z.png)

</td></tr><tr><td>

Conversational outputs

</td><td>

The list of subflow outputs that are available to conversational interfaces.

</td></tr><tr><td>

Describe this output

</td><td>

The search terms and keywords that someone might use in a conversation to set this output. The more descriptive the output, the better AI Search can be in matching it to an utterance. You must provide a description for mandatory outputs. **Tip:** You can enter the description manually or use generative AI. To generate the description with generative AI, make sure that the field is empty and select **Generate skill metadata** ![Generate skill metadata icon.](../images/generate-skill-metadata-icon.png).

</td></tr></tbody>
</table>8.  Configure conversational advanced settings.

    ![Example advanced settings for the Send SMS subflow.](../images/conversational-subflow-advanced-setting-z.png)

<table id="table_erk_nmx_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Include in discovery

</td><td>

The option to make this subflow discoverable from a virtual agent.

</td></tr><tr><td>

Include in list of topics

</td><td>

The option to include this subflow in the list of available topics.

</td></tr><tr><td>

Promote skill

</td><td>

The option to display this subflow higher in the list when someone asks to see all available skills.

</td></tr><tr><td>

Use autonomous mode

</td><td>

The option to create, view, update, or delete records without asking for a confirmation.

</td></tr><tr><td>

Enable follow up

</td><td>

The option to retain the context of previous conversations so that the users can ask follow-up questions, provide additional details, and continue the conversation.

</td></tr><tr><td>

Show errors from subflow and actions

</td><td>

The option to show error messages from the subflow in the conversation.If this field is selected, when the subflow encounters an error during a conversation, it displays a specific error message based on what is specified in the subflow. If this field is not selected, the subflow displays a generic error message.

</td></tr><tr><td>

Channels

</td><td>

The list of default channels in which this subflow is available.To learn more about channels, see [Channels in conversational interfacesChannels in conversational interfaces](https://www.servicenow.com/docs/access?context=ci-channels-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>9.  Save the skill.

    You can also test the skill by selecting **Save and test**.


**Parent Topic:**[Building subflows](../concept/subflows.md)

