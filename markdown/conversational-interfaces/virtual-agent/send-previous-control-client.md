---
title: Send previous control to client
description: Provide the ability to send previous control to client.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Send previous control to client

Provide the ability to send previous control to client.

There are two ways to send previous control back from the server when a client requests:

-   In inbound transformation, set `validation_message` in result. Previous control will be sent again with message provided in `validation_message`.
-   In inbound transformer, set `send_prev_control` in result to true, previous control will be sent again. Use this method for Multi-Step controls.

Example script:

```
(function execute (inputs, outputs) {
  var result = {};
  var request_context = inputs.request_context;
  var typed_value = request_context ['typed_value'];
  if (typed_value.index0f("#") > -1)
    result["validation_message"] = "Invalid character, please don't enter special character '#'";
  result["value"] = typed_value;
  result["search_text"] = "";
  outputs.result - result;
})(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

