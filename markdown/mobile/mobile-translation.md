---
title: Create translation records for mobile
description: Create records on the Translated Name / Field table to translate elements of your mobile app that are not natively translated.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Localization on mobile devices, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create translation records for mobile

Create records on the Translated Name / Field table to translate elements of your mobile app that are not natively translated.

## Before you begin

Role required: admin

Use these steps to add translations for your mobile device that are not already translated by your mobile device's native translation settings. To see which elements need to be manually translated, switch your mobile device's native language to the language you are working on, and view your mobile apps to see which values remain in English. Use the steps below to translate the remaining values.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Translated Name / Fields** &gt; **.**

2.  Click **New** to create a new Translated Name / Fields record.

3.  On the form, fill in the fields.

<table id="table_q1y_m4b_2mb"><thead><tr><th>

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

The element on the table to be translated. See the table below for element names for each translatable element.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Repeat the steps to create a record for each language you want to support on your instance.


**Parent Topic:**[Localization on mobile devices](../concept/localization-mobile-device.md)

