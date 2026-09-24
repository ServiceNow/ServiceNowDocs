---
title: Script bot response control
description: Use the Script bot response control in a Virtual Agent topic to run a script that returns a single response or a multi-part response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-script-output.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Assistant Designer bot responses, Assistant Designer interface reference, Reference, Virtual Agent, Conversational Interfaces]
---

# Script bot response control

Use the Script bot response control in a Virtual Agent topic to run a script that returns a single response or a multi-part response.

Use the Script bot response control when creating a more complex response that relies on scripted calculations or requires a multi-part response. Scripted output can include text, image, cards, links, and HTML to create a versatile response.

## Script bot response control properties

<table id="table_l2x_5jn_vdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

The name that identifies this Script bot response control node in the topic flow.

</td></tr><tr><td>

Script output type

</td><td>

The type of output returned by the script, either single-part or multi-part.

</td></tr><tr><td>

Script response message

</td><td>

The script that generates the selected output type.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Channel support

|Channel|Support|Constraints|
|-------|-------|-----------|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|SMS Twilio|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Google Chat|Supported|None|

## Example script

In this example, the script calculates the time two hours from the current time and outputs a multi-part message that includes this information.

```
(function execute() {
      var gdt = new GlideDateTime();
      var gt = new GlideTime();
      gdt.addSeconds(7200);
      gt = gdt.getTime();
      var multiOutMsg = new sn_cs.MultiPartOutMsg();
      multiOutMsg.addPlainTextPart('Thank you for submitting an incident.');
      multiOutMsg.addPlainTextPart('You should receive a response from a technician by ' + gt.getByFormat('HH:mm'));
      return multiOutMsg;
})()
```

## Example Script bot response control

**Note:** Asset library controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Script properties

</th><th>

Script bot response output

</th></tr></thead><tbody><tr><td>

\[Omitted image "va-script-output-properties.png"\] Alt text: Basic properties include the node name, script output type, and the script itself.

</td><td>

\[Omitted image "va-script-output-web.png"\] Alt text: A sample script output in a chat window that reads, "This is my script output."

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-bot-responses.md)

