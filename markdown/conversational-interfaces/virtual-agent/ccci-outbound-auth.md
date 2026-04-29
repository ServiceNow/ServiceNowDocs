---
title: Outbound authentication using a token
description: Pass an outbound token from the authentication API to the sender script.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Outbound authentication using a token

Pass an outbound token from the authentication API to the sender script.

Secure fields contain the `maskType` metadata field as "SECURE". The client can handle the following script appropriately.

Example: Outbound authentication token script

```
(function execute(inputs, outputs) {
    try {
        var results = inputs.result;
        
        var sendInputs = {
            app_inbound_id : inputs["app_inbound_id"],
            channel_user_id: inputs["channel_user_id"],
            messages: JSON.stringify(results)
        };

        sn_fd.FlowAPI.startSubflowQuick('sn_va_sms_twilio.va_sms_twilio_adapter_send_sms', sendInputs);
        //return sn_fd.FlowAPI.executeActionQuick('sn_va_sms_twilio.va_sms_twilio_adapter_sender_handler', sendInputs);


    } catch (e) {
        gs.error("Messages: " + JSON.stringify(sendInputs));
        gs.error("Error is twilio sms sender : " + e.message);
    }
})(inputs, outputs);
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

