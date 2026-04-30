---
title: Searching translated content
description: Understand how AI Search searches translated fields and documents.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer]
---

# Searching translated content

Understand how AI Search searches translated fields and documents.

The ServiceNow AI Platform® includes two categories of translated content:

1.  Translated fields, such as translations of Catalog Item record fields.
2.  Translated documents \(long text and HTML values\), such as translations of knowledge article records.

The default AI Search matching behavior differs for these two types of content.

## Translated fields

When you search content that includes translated fields, AI Search matches and displays field translations in your ServiceNow AI Platform session language. If a field lacks a translation in the session language, AI Search instead falls back to matching against the English-language field value. For example, if your session language is Japanese, AI Search returns Japanese field translations where present on a Catalog Item record, but returns English values for Catalog Item fields that have no Japanese translation.

To learn more about how the ServiceNow AI Platform handles translated fields, see [Translating individual UI strings](../../localization/concept/c_TranslateIndFieldLabelsAndValues.md).

If you insert or update field translation records in the Translated Text \[sys\_translated\_text\] table, reindex content from the relevant indexed source to make AI Search use the new translations. For details on reindexing content, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](../task/index-multiple-sources-ais.md).

**Note:** AI Search doesn't support translated fields on the Knowledge \[kb\_knowledge\] table. This behavior has the following effects.

-   Search queries don't match translated versions of kb\_knowledge translated fields.
-   Search results don't display translated versions of kb\_knowledge translated fields.
-   [Search application facets](../task/create-facet-ais.md) don't display translated versions of kb\_knowledge translated fields.

## Translated documents

When searching content with translated documents, by default AI Search only matches documents in the user's ServiceNow AI Platform session language. For example, a Japanese user search only matches knowledge articles in Japanese, excluding all knowledge articles in other languages.

Starting in the Utah release, you can configure a filter condition for globally searchable knowledge articles. Articles that satisfy this condition can be matched by searches in any language. For information on this setting, see [Configure globally searchable knowledge articles](../task/configure-global-srch-kb-articles.md).

Beginning in the Tokyo release, you can set a fallback language for each language enabled in your ServiceNow AI Platform instance. When a fallback language is configured for the user's session language, AI Search returns search results in both languages. For more details, see [AI Search interaction with fallback languages](interaction-fallback-language-ais.md).

You can configure a global fallback locale to make AI Search match documents in the instance locale's language as well as the user's session language. This configuration works best when you want to make all English-language documents globally searchable. To learn more about configuring a global fallback locale, see [Enable a global fallback locale for translated content](../task/enable-global-fallback-lang-ais.md).

**Parent Topic:**[Internationalization support for AI Search](international-language-support-ais.md)

