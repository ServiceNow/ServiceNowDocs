---
title: Grouped Choice user input control
description: Use the Grouped Choice user input control in a Virtual Agent topic to list multiple groups of choices in one message.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Assistant Designer user input controls, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Grouped Choice user input control

Use the Grouped Choice user input control in a Virtual Agent topic to list multiple groups of choices in one message.

## Grouped Choice list display

The Grouped Choice list prompts users to select related choices in one message through the default **Select a choice** button. You can enable multi-select for each choice's group and also provide images and short descriptions to create a richer user experience. Users are presented with groups of choices where they're required to submit one selection before returning to the Virtual Agent topic.

Inputs are recorded on the Interactions \[interactions\] table. For more information, see [Virtual Agent interaction records](../concept/va-interactions.md).

## Grouped Choice user input control properties

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Grouped Choice user control node in the topic flow.

</td></tr><tr><td>

Prompt

</td><td>

Prompt or question for the user. The prompt can be either a text string or a script that returns text. For example: `Please select your meal preference.`

</td></tr><tr><td>

Group name

</td><td>

Name that identifies the grouped choice list in the property sheet. Add one \(required\) or multiple groups of related choices. Users must select one choice out of all groups.Use short phrases in your choice lists.

</td></tr><tr><td>

Choices

</td><td>

Number of choices added to each group.

</td></tr><tr><td class="sub-head" colspan="2">

Add a group of choices dialog box

</td></tr><tr><td class="sub-head" colspan="2">

This dialog box only appears after **Add** is selected.

</td></tr><tr><td>

Group name

</td><td>

Name that identifies the grouped choice list in the property sheet. A limit of 40 characters for choice list labels exists. The **Variable name** field is automatically generated from the group name. This read-only variable name appears in all lower-case text and substitutes any spaces in the group name for underscores. If multiple lists with the same name exist, the variable name is appended with `_1`, `_2`, `_3`, and so on. Use this variable in your conversation flow to retrieve user responses for each group within the Grouped Choice node.

</td></tr><tr><td>

Display as

</td><td>

Group heading title that appears in the rendered client.

</td></tr><tr><td>

Display name

</td><td>

Choice name that is displayed to users. At least two unique choices are required.

</td></tr><tr><td>

Value

</td><td>

String that is stored in the variable when the corresponding choice is selected. This value is automatically generated from the display name, but you can edit the field as needed.

</td></tr><tr><td>

Image

</td><td>

Option to an add image for the choice.Individual choice images are entered after you select **Add details**.

 To set this field, do one of the following:

-   Specify the URL link by either entering the link text, using a data pill, or using a script.
-   Upload an image file by selecting **Upload Image**.

</td></tr><tr><td>

Description

</td><td>

Option to provide additional information about the choice.

 Individual choice descriptions are entered after you select **Add details**.

For example: If the grouped choice list is about passengers selecting airplane amenities, like headphones, you could include a description about the type of headphones such as `Over-ear wired headphones`.

</td></tr><tr><td>

Allow the user to select more than one choice

</td><td>

Option to allow users to choose multiple options from the choice list by selecting **Yes**.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Customize group selection

</td></tr><tr><td>

Update title

</td><td>

Option to customize the title of the grouped choice's prompt button. A limit of 40 characters for choice list labels exists. If this field is left empty, the default title that users see is `Select a choice`.

</td></tr><tr><td>

Image

</td><td>

Option to add an image for the grouped choice's prompt button.To set this field, do one of the following:

-   Specify the URL link by either entering the link text, using a data pill, or using a script.
-   Upload an image file by selecting **Upload Image**.

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`.

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Grouped Choice user input control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Input properties

</th><th>

List prompt

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, prompt, and the list of possible choices.](../images/va-grouped-choice-properties-sheet.png "Grouped choice input control basic properties")

 

![Group choice properties include an internal name and the way this group should display to the user. Each choice consists of a name, value, image, and description.](../images/va-grouped-choice-dialog-box.png)

</td><td>

![A chat window displays the default "Select a choice" button. The list of choices appears when the user selects it.](../images/va-grouped-choice-default-button.png "Web UI Grouped Choice list default prompt")

 ![A chat window displays a custom button. It reads, "Select flight information" and includes a photo of an airplane.](../images/va-grouped-choice-customized-button.png "Web UI Grouped Choice list with customized title and image")

 ![An example list of choices. The first prompts the user to select the class type for their flight. The second asks the user to select a meal type.](../images/va-grouped-choice-user-example.png "Web UI Grouped Choice list")

</td></tr></tbody>
</table>## Channel support

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Not supported|Not applicable|
|Now Assist panel|Supported|None|
|Microsoft Teams|Not supported|Not applicable|
|Google chat|Not supported|Not applicable|
|Slack|Not supported|Not applicable|
|Workplace|Not supported|Not applicable|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp \(powered by Twilio\)|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Not supported|Not applicable|

**Parent Topic:**[Assistant Designer user input controls](va-user-inputs.md)

