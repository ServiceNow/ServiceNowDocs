---
title: LLM Text bot response control
description: Use this control to write a prompt description that will dynamically create an output message to the user in conversations that use large language model \(LLM\) topic discovery.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assistant Designer bot responses, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# LLM Text bot response control

Use this control to write a prompt description that will dynamically create an output message to the user in conversations that use large language model \(LLM\) topic discovery.

## LLM Text bot response control properties

The Text bot response is available on the palette when you work with topics that use LLM topic discovery.

<table id="table_m2v_xmj_h1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this LLM Text bot response control node in the topic flow.

</td></tr><tr><td>

Tell the LLM how to respond

</td><td>

What sort of message you want the LLM to send to the user. For example, `Greet the user in a friendly, professional manner`. You can create messages using plain text, scripts, or conditions defined with the data pill picker.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Text bot response control

![Basic properties include the node name and how you want the LLM to respond. Advanced options include Hide this node.](../images/va-ai-response-llm-properties.png)

**Parent Topic:**[Assistant Designer bot responses](va-bot-responses.md)

