---
title: Localize the bot messages
description: Localize the bot messages to receive them in a language of your choice during your conversations with the bot.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Localize the bot messages

Localize the bot messages to receive them in a language of your choice during your conversations with the bot.

## Before you begin

Role required: virtual\_agent\_admin

## Procedure

1.  Navigate to the provider channel identity record of your bot and select the **Bot Messages** tab.

    Confirm that the values for those bot messages are accurate.

2.  Navigate to the Messages \[`sys_ui_message.list`\] table and select **New**.

    **Note:** Before creating a new message, ensure that the message you want to create is not already created.

3.  On the form, fill in the details.

    |Field name|Description|
    |----------|-----------|
    |Key|Message for the record. Make sure that this matches with the bot message value in step 1. If you want to create multiple translations for the same message in different languages, add each translated message individually.|
    |Language|Your preferred language for the conversation/message.|
    |Message|The equivalent of the key message translated into your preferred language.|

4.  Select **Submit**.


## Result

Start a new conversation with the bot. You will notice that the translated message is displayed by the bot in user’s preferred Microsoft Teams language, if you have already provided the translation for that language.

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

