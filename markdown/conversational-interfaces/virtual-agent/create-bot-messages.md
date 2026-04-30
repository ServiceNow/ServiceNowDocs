---
title: Create bot messages
description: Create channel-specific bot messages.Use the bot messages API to implement channel-specific bot messages.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create bot messages

Create channel-specific bot messages.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channel Integrations** &gt; **Connections** and select a connection.

2.  In the **Provider Channel Identity** tab, select a provider channel identity.

3.  Select **New** in the **Bot Messages** table.

4.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your bot message|
    |Value|Text displayed when a bot message is triggered|
    |Description|Description of the bot message, such as Welcome message or Instructional message for image upload|
    |Message Type|Default selection is Bot Message|
    |Provider Channel Identity|Select the Provider Channel Identity|

5.  Select **Submit**.


**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

## Bot message implementation

Use the bot messages API to implement channel-specific bot messages.

### Bot message API

Use the following API to incorporate bot messages into your custom chat integration.

Example: Bot message implementation

```
function getBotMessage(providerId, inboundId, botMessageName) {
    // fetch the bot message using bot messages api
    var botMessages = sn_cs.VASystemObject.getAllBotMessages(providerId, inboundId);
    if (botMessages && botMessages[botMessageName]) {
        var botMessage = botMessages[botMessageName];
        botMessage = botMessage.trim();
        if (botMessage) {
            return botMessage;
        }
    }
}
```

