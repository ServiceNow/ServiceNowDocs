---
title: Typing indicators
description: Display a typing indicator when a bot or live agent is preparing a response to a requester.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Typing indicators

Display a typing indicator when a bot or live agent is preparing a response to a requester.

When Virtual Agent processes a request, the Start typing indicator action is called. When Virtual Agent completes the request processing, the End typing indicator action is called before Virtual Agent processes any output or input controls.

These actions call the defaultText control outbound transformation. The following example shows how the typing indicator is handled in the defaultText control outbound transformation.

Example: Typing indicator script

```
(function execute(inputs, outputs) {
    try {
        var richControl = inputs.rich_control;
        var actionType = richControl.type;
        if(actionType == 'StartTypingIndicatorActionMsg'){
            outputs.result = '{activity:{type: "typing" }}'
        }else if(actionType == 'EndTypingIndicatorActionMsg'){
            outputs.result = '{activity:{type: "message" , text: "Finished typing"}}'
        }
       /* Handle other type of control */
    } catch (e) {
        gs.error("Error in default action outbound transformer : " + e.message);
        throw e;
    }
})
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

