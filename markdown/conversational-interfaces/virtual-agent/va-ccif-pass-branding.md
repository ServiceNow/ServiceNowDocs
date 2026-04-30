---
title: Pass branding to a chat client
description: Pass custom branding to your custom chat integration.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Pass branding to a chat client

Pass custom branding to your custom chat integration.

See [Set up your Virtual Agent bot's branding](../../conversational-interfaces/task/ac-configure-chat-branding.md) for more information about branding. Use `sn_cs.VASystemObject.getSettings` to apply branding.

Example script:

```
va_sms_twilio_adapter_default_text_outbound_transformer
(function execute(inputs, outputs) {
  try {
    var richControl = inputs.rich_control;
    var branding = sn_cs.VASystemObject.getSettings("default_branding"); // new
    var header = "(" + branding["header_label"] + ") "; // new
    outputs.result = header; // new
    outputs.result += richControl['label'];
  } catch(e){
    gs.error('Error in default text outbound transformer: ' + e.message);
    throw e; 
  } 
})(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

