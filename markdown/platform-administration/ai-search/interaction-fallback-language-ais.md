---
title: AI Search interaction with fallback languages
description: When a fallback language is configured for the user's session language, AI Search searches translated documents in both languages. Search uses the appropriate stop word, synonym, and typo handling dictionaries for the fallback language.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search interaction with fallback languages

When a fallback language is configured for the user's session language, AI Search searches translated documents in both languages. Search uses the appropriate stop word, synonym, and typo handling dictionaries for the fallback language.

Starting in the Tokyo release, you can set a fallback language for each language enabled in your instance. The system uses this fallback language for elements of user interface text that aren't translated in the specified language. For details on configuring fallback languages, see [Set a fallback language](../../localization/task/set-fallback-language.md).

If you set a fallback language for the user's ServiceNow AI Platform® session language, AI Search returns results for translated content, such as knowledge articles, in both the session language and your configured fallback language. When searching content in the fallback language, AI Search uses the stop word, synonym, and typo handling dictionaries for the fallback language.

As an example, suppose you configure Spanish as the fallback language for Mexican Spanish. With this configuration, users searching in Mexican Spanish sessions can find knowledge articles in both Mexican Spanish and Spanish. AI Search uses the Mexican Spanish and Spanish dictionaries and result improvement rules when matching articles in Mexican Spanish. It uses the Spanish dictionaries and result improvement rules when matching articles in Spanish.

![Diagram showing es-MX user session language and es fallback language.](../image/diagram-fallback-language.png "Search result languages with a fallback language")

If you configure a global fallback locale in addition to a fallback language, AI Search returns matching results for translated content in the user's session language, the fallback language, and the global fallback locale's language. As an example, suppose you configure French as the fallback language for Canadian French, and also configure English as the global fallback locale. Users searching in Canadian French sessions can search knowledge articles in Canadian French, French, and English.

![Diagram showing fr-CA user session language, fr fallback language, and en global fallback locale.](../image/diagram-fallback-language-locale.png "Search result languages with a fallback language and a global fallback locale")

For details on configuring a global fallback locale, see [Enable a global fallback locale for translated content](../task/enable-global-fallback-lang-ais.md).

**Parent Topic:**[Internationalization support for AI Search](international-language-support-ais.md)

