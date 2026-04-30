---
title: Translate knowledge articles using Dynamic Translation
description: Use machine translation to automatically translate knowledge articles into different languages.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Bulk Translation for Dynamic Translation, Bulk Translation for knowledge articles, Use translation management, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate knowledge articles using Dynamic Translation

Use machine translation to automatically translate knowledge articles into different languages.

## Before you begin

[Add a custom Localization Framework setting to enable machine translation](con-lf-dynamic-translations.md).

Role required: Localization requester to request translations

## About this task

Dynamic Translation uses the ServiceNow® Localization Framework to translate knowledge articles into different locales without any manual intervention.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles**.

2.  Select the articles you want translated.

3.  Select **Request Translations**.

    **Note:** .Check the validation list to ensure that all articles to be translated have been validated. For more information, see [Bulk Translation for knowledge articles](bulk-translation.md).

4.  In the **Request Translations** dialog box, select the languages into which you want the articles translated.

5.  Select **Submit**.

    Dynamic Translation automatically initiates a translation process and creates a translated article.


## Result

The selected articles are translated in selected languages and marked as version 0.01. The article can be accessed from the Knowledge \[kb\_knowledge\] table.

**Parent Topic:**[Use Bulk Translation for Dynamic Translation](bts-for-dynamic-translations.md)

