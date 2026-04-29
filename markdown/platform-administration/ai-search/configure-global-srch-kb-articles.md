---
title: Configure globally searchable knowledge articles
description: Define an encoded query for knowledge articles that you want to make searchable in any language.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure globally searchable knowledge articles

Define an encoded query for knowledge articles that you want to make searchable in any language.

## Before you begin

Role required: ais\_admin

## About this task

By default, AI Search only matches translated content records, such as knowledge articles, that are in the user's ServiceNow AI Platform® session language. For example, a user searching from a Spanish user session only matches Spanish knowledge articles. For full details on this restriction, see [Searching translated content](../concept/searching-translated-content-ais.md).

**Note:** If you've configured a global fallback locale, search can match translated content records in that locale's language as well as in the user's session language. For more details on this approach, see [Enable a global fallback locale for translated content](enable-global-fallback-lang-ais.md).

To enable users to search for knowledge articles in any language, you can define an encoded query as the value of the **glide.ais.global\_searchable\_filter.kb\_knowledge** system property. Records that match this query are globally searchable, meaning they bypass the normal language filters and can be matched regardless of the search's language. As an example, a user searching from a German user session can match English or Japanese knowledge articles as long as they match the encoded query.

![Diagram showing de user session language and * globally searchable articles in any language.](../image/diagram-globally-searchable.png "Search result languages with globally searchable articles")

**Note:** To generate knowledge article query strings for your encoded query, you can navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **All** and follow the steps found in [Generate an encoded query string through a filter](https://www.servicenow.com/docs/access?context=t_GenEncodQueryStringFilter&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US). For descriptions of encoded query syntax and operators, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) and [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Open the **glide.ais.global\_searchable\_filter.kb\_knowledge** system property record.

3.  In the **Value** field, enter a filter expression specifying the knowledge articles that you want to make globally searchable.

4.  Select **Update**.


## Result

Knowledge articles that match your encoded query can be returned as results for user searches in any language.

## Make knowledge articles in the Email category globally searchable

Here is an example that defines the encoded query `kb_category=5681bf8bff0221009b20ffffffffff95` to make knowledge articles in the Email category globally searchable.

![glide.ais.global_searchable_filter.kb_knowledge system property form with value kb_category=5681bf8bff0221009b20ffffffffff95.](../image/global-kb-sys-prop-query-example.png "Email category encoded query for knowledge articles")

**Parent Topic:**[Internationalization support for AI Search](../concept/international-language-support-ais.md)

