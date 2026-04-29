---
title: Create translation records for mobile
description: Create records on the Translated Name / Field table to translate elements of your mobile app that aren't natively translated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server-side localization, Localization, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create translation records for mobile

Create records on the Translated Name / Field table to translate elements of your mobile app that aren't natively translated.

## Before you begin

Role required: admin

Use these steps to add translations for your mobile device that aren't already translated by your mobile device's native translation settings. To see which elements must be manually translated, switch your mobile device's native language to the language you're working on. Then view your mobile apps to see which values remain in English. To translate the remaining values, follow the procedural steps in the next section.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Translated Name / Fields**

2.  Select **New** to create a Translated Name / Fields record.

3.  On the form, fill in the fields.

<table id="table_tfs_qpw_mhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label \(translate\)

</td><td>

Translated text that users see on the translated item.

</td></tr><tr><td>

Language

</td><td>

Two-character ISO language code for this translated text.

</td></tr><tr><td>

Value

</td><td>

Original English value that causes this translated text to be displayed.

</td></tr><tr><td>

Table

</td><td>

Select a table depending on the element to be translated:-   For Screen names, use **sys\_sg\_screen**
-   For Launcher names, use **sys\_sg\_applet\_launcher**
-   For Function names, use **sys\_sg\_button\_instance**
-   For global search placeholder text, use **sys\_sg\_global\_search**
-   For search source names, use **sys\_search\_source**


</td></tr><tr><td>

Element

</td><td>

The element on the table to be translated. Refer to [Translation values for mobile element](../reference/mobile-translation-reference.md) for the element names of each translatable element.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Repeat the steps to create a record for each language you want to support on your instance.


**Parent Topic:**[Server-side localization](../concept/localization-server-side.md)

