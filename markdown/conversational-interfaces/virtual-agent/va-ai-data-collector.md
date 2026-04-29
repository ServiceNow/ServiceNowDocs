---
title: Input Collector user input control
description: Use the Input Collector control to gather data for use by Now Assist in conversations that use large language model \(LLM\) topic discovery.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, Designer, Input Collector, User input, control, node, LLM, Now Assist, Large Language Model]
breadcrumb: [Assistant Designer user input controls, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Input Collector user input control

Use the Input Collector control to gather data for use by Now Assist in conversations that use large language model \(LLM\) topic discovery.

## Overview

For an overview of the Input Collector from a user perspective, watch this video.

Virtual Agent Designer Input Collector user input control video

## Input Collector properties

The Input Collector is only available for topics that use LLM discovery.

The Input Collector can hold up to 5 of any of the LLM user inputs aside from another Input Collector. To collect more than 5 user inputs, place multiple Input Collector nodes in sequence or adjust the Value of the **com.glide.cs.va\_input\_collector\_max\_nodes** property in the System Properties \[sys\_properties\] table.

You can reorder nodes inside the Input Collector on both the canvas and table views. To reorder nodes on the canvas, select a given node inside the Input Collector and drag it up or down in the list. You can add or remove nodes from an Input Collector, or nodes between multiple Input Collectors, by selecting a node and dragging it into or out of an Input Collector node on the canvas. To reorder nodes in an Input Collector in the table view, select a given node in the list, then select the up or down arrow next to the node.

Specify the flow action properties for the node that you want to create.

<table id="ai-data-collector-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this node in the topic flow.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Additional instructions for LLM

</td><td>

Further instructions to the LLM, such as adding data formats, restrictions, or default values for user responses. You can create additional instructions in plain language, input a script, or define conditions with the data pill picker.

</td></tr><tr><td>

Confirmation message

</td><td>

Toggle switch to display a summary of collected inputs to the user at the end of a conversation. If Summary message is activated, the Virtual Agent, when activated, presents the information that you have entered and asks if everything is correct. Select **Yes** to continue the chat or **No** to restart collecting user input. You can also reply by typing a response in the chat window, to confirm or deny the summary or to change your answer. This option is active by default, and shows an enabled icon ![](../images/bluecheck.png) when activated.

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
</table>## Example Input Collector capability

![Basic properties include the node name. Advanced options include Additional instructions to LLM, Confirmation messages, and Hide this node.](../images/ai-data-collector-properties.png)

## Input Collector canvas view

![Input collector canvas view, holding text and static choice input nodes. You can move nodes by selecting and dragging them inside, out of, or within the Input collector.](../images/input-collector-canvas-view.png)

## Input Collector table view

![Input collector table view, showing text and static choice nodes, with up and down arrows to reorder nodes inside the collector.](../images/input-collector-table-view.png)

## Channel support

|Channel|LLM support|NLU/keyword support|Constraints|
|-------|-----------|-------------------|-----------|
|Web UI|Not supported|Supported|None|
|Mobile UI|Not supported|Supported|None|
|Now Assist panel|Not supported|Supported|None|
|Microsoft Teams|Supported|Supported|None|
|Slack|Not supported|Not supported|Not applicable|
|Workplace|Not supported|Not supported|Not applicable|
|Facebook Messenger|Not supported|Not supported|Not applicable|
|SMS Twilio|Supported|Not supported|Not applicable|
|LINE|Not supported|Not supported|Not applicable|
|WhatsApp \(powered by Twilio\)|Supported|Not supported|Not applicable|
|WhatsApp|Not supported|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not supported|Not applicable|
|Alexa \(Voice\)|Not supported|Not supported|Not applicable|

**Parent Topic:**[Assistant Designer user input controls](va-user-inputs.md)

