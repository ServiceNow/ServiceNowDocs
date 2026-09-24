---
title: \(Legacy\) Date Time user input control
description: Use the Date Time user input control in a Virtual Agent topic to enable the user to select a calendar date, time \(hours and minutes\), or both.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-date-time-input-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Virtual Agent, Designer, Date, Time, User input, control, node, day, hour, minute, calendar]
breadcrumb: [User input controls for NLU, Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Date Time user input control

Use the Date Time user input control in a Virtual Agent topic to enable the user to select a calendar date, time \(hours and minutes\), or both.

The Date Time user input control accepts inputs from a calendar selection, or by entering plain language in the Virtual Agent chat window. If you type your answer, the Virtual Agent accepts different inputs depending on how your region handles dates. For example, if you're in the United States, the input control supports the MM-DD-YYYY format, while a user in Spain enters the date in DD-MM-YYYY format.

## Date Time user input control properties for NLU topic discovery

<table id="table_nff_y1b_3db"><thead><tr><th>

Date Time property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies this node in the topic flow.

</td></tr><tr><td>

Variable Name

</td><td>

Name of the variable that stores the user response to this prompt. The variable name is automatically created from the **Node name** property.

</td></tr><tr><td>

Prompt

</td><td>

Prompt or question for the user. The prompt can be either a text string or a script that returns text. This value is used only when the default value is not specified. For example: `What's your name?`

</td></tr><tr><td>

NLU entity\[NLU topic discovery only\]

</td><td>

Option to associate an NLU entity with the node. If an NLU entity is associated with the input variable for this node, Virtual Agent can slot-fill the specified value based on the user's utterance. Select an entity from the list of entities associated with the topic intent.

 When you specify an entity for the node, the Do not ask users to confirm recognized entity toggle switch is displayed. When enabled, users are not prompted to confirm the extracted entity.

</td></tr><tr><td>

Input format

</td><td>

Type of Date Time control to be displayed. Select one of the following formats:

-   **Date**: Shows only the monthly calendar for the user to select the date.
-   **DateTime**: Shows both a monthly calendar and time picker.
-   **Time**: Shows only the time picker for the user to select the time \(hours and minutes\).

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Default value

</td></tr><tr><td>

Predefine a value for user input

</td><td>

Predefined value for the user response to the question or prompt. The response defined in the **Default value confirmation** field asks the user to confirm the default value. If the user responds with `no`, the value becomes null. The default value can be either a text string or a script that returns text. For example, if you're using dot-walking, the default value might be: `Script Variables > Last username`. Or if you're using a script, the default value might be: `{{vaScripts.lastUsername}}`.

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`

</td></tr><tr><td>

Default value confirmation

</td><td>

Message that asks the user to verify that the value in the **Default value** field is correct. This message is used instead of a value in the **Prompt** field. It can contain either a text string or a script that returns text. For example, if you're using dot-walking: `Are you (Input Variables > Username)?` Or if you're using a script, the confirmation message might be: `Are you {{vaScripts.lastUsername}}?`.

</td></tr><tr><td class="sub-head" colspan="2">

Conversation switching

</td></tr><tr><td class="sub-head" colspan="2">

This section is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td>

Turn on to let users change the subject

</td><td>

Option to enable NLU prediction for this node. If enabled, users can enter text to answer questions, regardless of the type of input control being used. Virtual Agent uses this utterance to match another existing intent, letting the user switch topics.

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr><tr><td>

Skip reprompting if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip reprompting in the conversation. When a preceding node is revisited through a topic loopback or Dialog Act, Virtual Agent bypasses this node and automatically retains its original value.

</td></tr></tbody>
</table>## Example Date Time user input control for NLU topic discovery

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Input properties

</th><th>

Date Time prompt

</th></tr></thead><tbody><tr><td>

\[Omitted image "va-datetime-properties.png"\] Alt text: Basic properties include the node name, prompt, input format, and NLU entity.

</td><td>

\[Omitted image "va-datetime-native.png"\] Alt text: In the Web client, a calendar pop-up lets the user choose a date and time.

</td></tr></tbody>
</table>## Channel support

|Channel|NLU/keyword support|Constraints|
|-------|-------------------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|SMS Twilio|Not supported|Not applicable|
|LINE|Supported|None|
|WhatsApp|Supported|None|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Supported|For best results, enable NLU at the node.|

**Parent Topic:**[\(Legacy\) Virtual Agent Designer user input controls for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-user-inputs-nlu.md)

