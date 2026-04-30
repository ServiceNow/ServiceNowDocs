---
title: Configure a language as reading from right to left
description: Use the Text Direction field to configure a language that reads from right to left, such as Hebrew.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Translating to an unsupported language, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a language as reading from right to left

Use the Text Direction field to configure a language that reads from right to left, such as Hebrew.

## Before you begin

Activate the languages that your users need. For more information, see [Activate a language](t_ActivateALanguage.md).

Role required: admin

## About this task

Right-to-left language support is available only in the main user interface and on live feed. Other user interfaces and applications, such as the graphical Workflow Editor, reporting, CMS, chat, and the ServiceNow documentation sites, are not supported.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Languages**.

2.  Select **New**.

3.  Enter the **Name** of the language, such as Hebrew.

4.  Enter the [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code for the language.

    For example, Hebrew is `he`.

5.  In the Text Direction field, select **Right-to-Left**.

6.  Select **Submit**.


