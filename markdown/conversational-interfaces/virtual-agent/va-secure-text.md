---
title: Secure Text user input control
description: The Secure Text control provides a means to encrypt sensitive information provided as simple text or other formats. Use this control to encrypt sensitive information in topics that use large language model \(LLM\) discovery.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Assistant Designer user input controls, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Secure Text user input control

The Secure Text control provides a means to encrypt sensitive information provided as simple text or other formats. Use this control to encrypt sensitive information in topics that use large language model \(LLM\) discovery.

Use this control to gather and encrypt user information for topics using large language model \(LLM\) topic discovery. The Secure Text input also avoids sensitive information from being sent through an LLM.

## Secure Text user input control properties

<table id="table_khb_p5y_11c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Secure Text user input control node in the topic flow.

</td></tr><tr><td>

Prompt

</td><td>

Text string or script that returns text. This value is used only when the default value isn’t specified. For example: `What is your password?`

</td></tr><tr><td>

Input format

</td><td>

Text format that is validated when a user enters certain text items. When the input isn’t valid, the bot asks the user to reenter the text.

 Choose the format of the text item to be validated:

 -   Text: Any text string \(no validation\).
-   Email: Format that consists of an email prefix \(user name\), the @ symbol, and domain.
-   IP address \(IPV4, IPV6\): Data communication delivery format for internet Protocol version 4 or version 6.
-   Phone number \(E.164\): Internationally recognized standard phone number format.
-   URL: Web address format.
-   Custom: A script that provides a validation rule for a custom text format. The script should include related error messages that are displayed when the expected format isn’t entered.

 For phone and IP address format examples, see E.164 phone formats and IP address field types.

</td></tr><tr><td>

Hash function

</td><td>

The method digest algorithm based on the standard WS-Security specification.

</td></tr><tr><td>

Encryption salt

</td><td>

Random data that is used as an additional input to a one-way function that hashes data.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Default value

</td><td>

A value for the user response to the prompt. For example, if you already know the user name, the default value might be `(Script Variables > Last username)`.

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`

</td></tr><tr><td>

Default value confirmation

</td><td>

Message that asks the user to verify that the value in the Default value field is correct. This message is used instead of a value in the Prompt field. For example: `Are you (Script Variables > Username)?`

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr><tr><td>

Skip reprompting

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip reprompting in the conversation. When a preceding node is revisited through a topic loopback or [Dialog Act](../concept/c_dialog-acts.md), the Virtual Agent bypasses this node and automatically retain its original value.

</td></tr></tbody>
</table>## Example Secure Text user input control

<table id="table_ykg_dvy_11c"><thead><tr><th>

Input properties

</th><th>

Input prompt

</th></tr></thead><tbody><tr><td>

![Secure Text user input basic properties include node name, prompt, input format, hash function, and encryption salt. Advanced options include Default value, Confirmation message, and Hide or skip this node.](../images/va-secure-text-input.png "Secure Text input control basic properties")

</td><td>

![Secure Text input shown in the web client. The text reads, “What is your first and last name?” and the user response is automatically hidden.](../images/va-secure-text-input-web.png "Web UI Secure Text user input prompt")

</td></tr></tbody>
</table>## Channel support

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None.|
|Mobile UI|Supported|None.|
|Now Assist panel|Supported|None.|
|Microsoft Teams|Supported|None.|
|Slack|Supported|Slack users can edit text previously entered in a conversation. However, Virtual Agent processes messages as they’re first entered. If a Slack user edits text input, such as a comment to update a case, then Virtual Agent doesn’t evaluate the edited update.|
|Workplace|Supported|None.|
|Facebook Messenger|Supported|The maximum character limit is 5000 characters.|
|SMS Twilio|Supported|None.|
|LINE|Supported|The maximum character limit is 5000 characters.|
|WhatsApp|Supported|None.|
|Apple Messages for Business|Supported|None.|
|Alexa \(Voice\)|Supported|For screen devices, character limits may apply. For more information, see the [Alexa developer documentation](https://developer.amazon.com/en-US/docs/alexa/custom-skills/display-interface-reference.html).|

**Parent Topic:**[Assistant Designer user input controls](va-user-inputs.md)

