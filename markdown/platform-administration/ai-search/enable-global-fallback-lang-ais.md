---
title: Enable a global fallback locale for translated content
description: Configure AI Search to match translated documents in a global fallback locale's language as well as the user's session language.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable a global fallback locale for translated content

Configure AI Search to match translated documents in a global fallback locale's language as well as the user's session language.

## Before you begin

Role required: ais\_admin

## About this task

By default, when searching content with translated documents, AI Search only matches indexed records in the user's ServiceNow AI Platform® session language. For example, a search in a Japanese user session only matches knowledge articles in Japanese, excluding all articles in other languages.

You can configure AI Search to apply a global fallback locale to user searches. When you enable this option, AI Search matches records in the language from the ServiceNow AI Platform instance's locale \(or another locale that you specify\) as well as matching records in the user's session language. As an example, if you set English as the global fallback locale, users searching in Japanese sessions can see knowledge article results in both Japanese and English.

![Diagram showing ja user session language and en global fallback locale language.](../image/diagram-global-fallback-locale.png "Search result languages with a global fallback locale")

**Note:** The global fallback locale works best when you want to make all English-language records globally searchable. To make other sets of records globally searchable, see [Configure globally searchable knowledge articles](configure-global-srch-kb-articles.md).

When you enable the global fallback locale option for search, AI Search determines the global fallback locale as follows:

1.  If the value of the **glide.ais.translate.global\_fallback\_locale** system property is a valid locale identifier string, such as **en**, **en-US**, or **fr**, AI Search uses the matching locale as the global fallback locale.
2.  Otherwise, AI Search uses the ServiceNow AI Platform instance's locale, as specified by the value of the **glide.system.locale** system property, as the global fallback locale.
3.  If the **glide.system.locale** system property's value isn't a valid locale, AI Search uses English as the global fallback locale.

For more details on ServiceNow AI Platform locales and their associated languages, see [Configuring locales](../../localization/concept/c_DefineLocales.md#).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **AI Search**.

2.  Select the option for the **Enable global language fallback** \(**glide.ais.translate.enable\_global\_language\_fallback**\) system property.

3.  Select **Save**.

4.  Add the **glide.ais.translate.global\_fallback\_locale** system property and set its value to the locale that you want AI Search to use as the global fallback locale.

    For instructions on adding this system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).


## Result

AI Search searches translated document content in the global fallback locale's language as well as the user's session language.

**Note:** When searching the Catalog Item table, AI Search ignores the instance locale. Catalog searches only match documents in the user's ServiceNow AI Platform session language.

**Parent Topic:**[Internationalization support for AI Search](../concept/international-language-support-ais.md)

