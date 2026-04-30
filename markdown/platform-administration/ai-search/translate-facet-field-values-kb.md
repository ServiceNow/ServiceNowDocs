---
title: Configure translation for knowledge article reference field values in facets
description: Specify whether facets should display knowledge article reference field values in the search user's session language. If you disable translation, facets display knowledge article reference field values in your instance's default language.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer]
---

# Configure translation for knowledge article reference field values in facets

Specify whether facets should display knowledge article reference field values in the search user's session language. If you disable translation, facets display knowledge article reference field values in your instance's default language.

## Before you begin

Role required: ais\_admin

## About this task

By default, the search results page displays facets for knowledge article reference fields using translated field values in the search user's session language. If no translated field value is available for the search user's session language, the knowledge article facet instead displays the field value in your instance's default language.

As an example, if you search from a Japanese session on an English-language instance, the KB Category facet displays field values in Japanese using Japanese translated field values. If a field value has no Japanese translation, the KB Category facet falls back to displaying that field value in English.

Search administrators can disable this translation behavior for knowledge article reference fields. With translation disabled, search users will see knowledge article facet field values in the instance's default language instead of in their session language.

To learn more about facets, see [Create a facet in an AI Search application configuration](create-facet-ais.md). For details on translated field values, see [System Localization](../../localization/concept/system-localization-landing.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the Knowledge Table indexed source record in form view by selecting its name.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|index\_translated\_reference\_fields|
    |Value|false|

    **Note:** To re-enable translation for facets, so that knowledge article reference field values appear in the user's session language when translated field values are available, set the index\_translated\_reference\_fields attribute's value back to **true**, its default value. For more information on the index\_translated\_reference\_fields attribute, see [Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md#).

5.  Select **Submit**.

    The updated attribute value appears in the indexed source's Advanced Configuration related list. If you changed the index\_translated\_reference\_fields attribute's value, a `Re-index is needed for configuration change to take effect` informational message appears.

6.  If you changed the index\_translated\_reference\_fields attribute's value, select **Index All Tables** to reindex content for the Knowledge Table indexed source.

    For more details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).


## Result

Facets for knowledge article reference fields display field value translations in the user's session language.

**Note:** If you set the index\_translated\_reference\_fields attribute's value back to `true` and see knowledge article reference field values displayed in the instance's default language in facets, check whether translations of these field values exist for the user's session language.

**Parent Topic:**[Internationalization support for AI Search](../concept/international-language-support-ais.md)

