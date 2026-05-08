---
title: Virtual Agent translation tables
description: Virtual Agent uses the \[sys\_translated\_text\] and \[sys\_ui\_message\] tables to store translated text.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent translation tables

Virtual Agent uses the \[sys\_translated\_text\] and \[sys\_ui\_message\] tables to store translated text.

<table id="table_c1f_l12_lpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Translated Text \[sys\_translated\_text\]

</td><td>

Stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).The \[sys\_cs\_topic\] table contains the English keywords and topic titles. It pulls translations from the \[sys\_translated\_text\] table.

 For details about translating text content into different languages, see Translated text table and Translating text fields.

</td></tr><tr><td>

Message \[sys\_ui\_message\]

</td><td>

Stores expert translations for messages in Virtual Agent topics.Pre-built topics have already been translated, but you must provide translations for any content you create for your instance. For more information about the Message table, see Message table.

</td></tr><tr><td>

Text Translations for Dynamic Translation \[sys\_cs\_dynamic\_translation\_text\]

</td><td>

Stores copies of the translations found in the Message \[sys\_ui\_message\] table and previously dynamically translated messages.This view-only table is only available when the Dynamic Translation for Virtual Agent plugin is installed and the Dynamic Translation in Virtual Agent feature is enabled. This table is cleared every 24 hours to ensure that the most up-to-date translations stored in the Message \[sys\_ui\_message\] table are being referenced. For more information about how the Text Translations for Dynamic Translation \[sys\_cs\_dyamic\_translation\_text\] table works with Dynamic Translation in Virtual Agent, see [Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](../concept/dynamic-lang-detection-translation-enhanced-chat.md).

</td></tr></tbody>
</table>**Parent Topic:**[Localizing Virtual Agent conversations](../concept/localize-va-topic.md)

