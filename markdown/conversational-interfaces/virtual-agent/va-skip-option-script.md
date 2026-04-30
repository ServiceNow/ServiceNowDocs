---
title: Implement a skip option
description: Use a rich control to provide the option for users to skip a question.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Implement a skip option

Use a rich control to provide the option for users to skip a question.

Use the rich control `\nType SKIP to skip question` to provide the option for a user to skip a question. There are two ways to configure a skip option:

-   In the provider attributes script, use `_skip_internal` to trigger a contextual action service to skip the question.
-   Map a contextual action for the provider and use `//request_context.contextual_action = "SKIP"` to skip the question. See [Contextual actions for custom chat integrations](contextual-actions.md#) to learn more about mapping user inputs to contextual actions.

Example script:

```
va_sms_twilio_adapter_default_text_outbound_transformer
(function execute(inputs, outputs) {
  try {
    var richControl = inputs.rich_control;
    outputs.result = richControl['label'];
    if (richControl['required'] === false && richControl['uiType'] != "OutputText") { // new
      outputs.result += "\nType SKIP to skip question"; // new
    } // new
  } catch(e){
    gs.error('Error in default text outbound transformer: ' + e.message);
    throw e; 
  }
})(inputs, outputs);
va_sms_twilio_adapter_provider_attributes
(function execute(inputs, outputs) {
    try {
        var headers = (inputs.headers);
        var payload = (inputs.payload);
        var smsUtil = new VASMSTwilioUtil();
        outputs.token = JSON.stringify(smsUtil.getToken(headers, payload));
        var data = payload.data;
        var request_context = {}; 
        if (data['MediaUrl0']) {
            var attachment_value = {};
            attachment_value.url = data['MediaUrl0'];
            attachment_value.content_type = data['MediaContentType0'];
            attachment_value.name = smsUtil.getFileName(attachment_value.url , attachment_value.content_type);
            request_context.attachment_value = attachment_value;
        } else {
           var b = data['Body']; // new
           request_context.typed_value = b; // new
           if (b === "SKIP") { // new
             request_context.typed_value = "_skip_internal"; // new
             //request_context.contextual_action = "SKIP"; // new
           } // new
        }
        outputs.request_context = request_context;
        outputs.provider_user_id = data.From;
    } catch (e) {
        gs.error("Error in va_sms_twilio_adapter_provider_attributes : " + e.message);
    }
})(inputs, outputs);
contextual_action (all new)
(function execute(inputs, outputs) {
  var contextual_action = inputs.request_context.contextual_action;
  if (contextual_action === "SKIP") {
      sn_cs.VASystemObject.skipOptionalQuestion(inputs.conversation_id);
  }
})(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

