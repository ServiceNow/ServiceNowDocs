---
title: Synchronous authentication of messages
description: Inbound message authentication is performed before the message is added to the hybrid queue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/ccci-synch-auth-msgs.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Synchronous authentication of messages

Inbound message authentication is performed before the message is added to the hybrid queue.

This code has to be implemented in the provider attribute script. For more information, see [Virtual Agent action scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-action-scripts.md).

Example: Synchronous authentication of messages

```
var validated = sn_cs.VASystemObject.validateMessage(providerApp.sysId, payload, JSON.stringify(headers));
if (validated === false) {
    response.setStatus(401);
    response.setContentType("test/xml")
    var writer = response.getStreamWriter();
    writer.writeString(
```

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-features-custom-chat-integrations.md)

