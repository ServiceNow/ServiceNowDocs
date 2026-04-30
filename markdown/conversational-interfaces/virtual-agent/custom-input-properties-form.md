---
title: Custom input properties sheet
description: Use this sheet to define a custom input control in Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-11-05"
reading_time_minutes: 1
keywords: [Virtual Agent, custom, input, properties]
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Custom input properties sheet

Use this sheet to define a custom input control in Virtual Agent.

## Custom input properties sheet

<table id="table_jmw_bn2_dmb"><thead><tr><th>

Custom input property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom Control Definition

</td><td>

List of custom control definitions for the controls.Select the definition that defines how the control is rendered for the channel in which it runs. If you need to add a custom control definition, click the **Custom control definitions** link.

</td></tr><tr><td>

Generate Control Data Function

</td><td>

Script function that provides the data used to render the custom control. For example, if you're creating a slider input control, you would define the values for the slider. These values include the slider minimum and maximum values, slide default values, icon used in the slider, and so on.

</td></tr><tr><td>

Transcript Function

</td><td>

Script function that provides the message recorded in the transcript. For example, a message for an input control could confirm that the control is rendered with specific data values.

</td></tr><tr><td>

Response Handler Function

</td><td>

Script function that defines how the input response is handled on the conversation server.

</td></tr><tr><td>

Response Transcript Function

</td><td>

Script function that provides the message for the input control response that is recorded in the conversation transcript.

</td></tr><tr><td>

Non-supported channel response message

</td><td>

Default fallback message that is displayed when a user is running the control on an unsupported channel.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced \(optional\)

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

</td></tr></tbody>
</table>