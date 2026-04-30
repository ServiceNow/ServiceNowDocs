---
title: Language filtering for external content
description: AI Search filters search results from external content connectors, showing only results in the user's session language, fallback language, and global fallback locale language.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer]
---

# Language filtering for external content

AI Search filters search results from external content connectors, showing only results in the user's session language, fallback language, and global fallback locale language.

When you have the External Content Connectors application installed, AI Search applies language-based filtering to search results retrieved by your external content connectors. For an external content search result to be displayed, it must include content in one of the following languages:

-   The search user's ServiceNow AI Platform® session language
-   The fallback language for the search user's ServiceNow AI Platform session language \(if configured\)
-   The language for the global fallback locale \(if configured\)

As an example, if the session language is Canadian French, with French configured as the fallback language and English configured as the global fallback locale language, searches only return external content results that contain Canadian French, French, and English content. External content search results which only contain content in other languages do not appear in the search results list.

**Note:** AI Search can detect multiple languages when indexing content from external source system documents, so a single external content search result may be tagged with multiple languages. As an example, a document in Japanese that contains a section in English might be tagged as including both Japanese and English content. This document would appear in the search results from the previous example because it contains content in English. For more information on language detection at indexing time, see [Internationalization support for AI Search](international-language-support-ais.md).

To learn about configuring and using connectors to make content from external source systems searchable, see [External Content Connectors](../reference/ext-cont-connectors-landing-page.md). For details on fallback languages and the global fallback locale, see [AI Search interaction with fallback languages](interaction-fallback-language-ais.md) and [Enable a global fallback locale for translated content](../task/enable-global-fallback-lang-ais.md).

**Parent Topic:**[Internationalization support for AI Search](international-language-support-ais.md)

