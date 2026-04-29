---
title: Custom output properties sheet
description: Use this sheet to define a custom response control in Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual Agent, custom output, response control]
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Custom output properties sheet

Use this sheet to define a custom response control in Virtual Agent.

## Custom output properties sheet

<table id="table_jmw_bn2_dmb"><thead><tr><th>

Custom response property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom Control Definition

</td><td>

List of custom control definitions for the controls.Select the definition that defines how the control is rendered for the channel in which it runs.

</td></tr><tr><td>

Generate Control Data Function

</td><td>

Script function that provides the data used to render the custom control. For example, if you're creating a slider input control, you would define the values for the slider. These values include the slider minimum and maximum values, slide default values, icon used in the slider, and so on.

</td></tr><tr><td>

Transcript Function

</td><td>

Script function that provides the message recorded in the transcript. For example, a message for an input control could confirm that the control is rendered with specific data values.

</td></tr><tr><td>

Non-supported channel response message

</td><td>

Default fallback message that is displayed when a user is running the control on an unsupported channel.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>