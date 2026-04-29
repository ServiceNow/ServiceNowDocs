---
title: Create a custom search matcher for global search
description: Customize the global search experience to return exact match search results from a specified table and column \(field\). You can configure custom search matchers for search terms with prefixes followed by numbers, such as INT470271, or for numeric search terms with delimiter characters, such as 525-326-3827 or 2016/01/08.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom search matcher for global search

Customize the global search experience to return exact match search results from a specified table and column \(field\). You can configure custom search matchers for search terms with prefixes followed by numbers, such as `INT470271`, or for numeric search terms with delimiter characters, such as `525-326-3827` or `2016/01/08`.

## Before you begin

You must have Next Experience enabled.

AI Search must be configured as the search engine for global search. For details on configuring AI Search as the search engine for global search, see [AI Search for Next Experience](../concept/ais-next-experience-app.md).

**Note:** If your instance was originally created running Utah or a later family release, AI Search is automatically configured as the search engine for global search.

Role required: ais\_admin

## About this task

To customize exact-matching behavior in global search, you can define a custom search matcher. The matcher specifies a Java regular expression pattern that AI Search compares search queries to, plus a table and a column \(field\) from that table. When a search query exactly matches the regular expression pattern, the custom matcher triggers and global search only returns exact-match results from the specified table and column.

Custom search matchers take precedence over the default AI Search exact match functionality for tables with prefixes defined in the Number \[sys\_number\] table. If a global search query doesn't match any custom search matcher's regular expression pattern, AI Search falls back to evaluating the query for exact matches in tables with defined prefixes.

**Note:** Users with the admin role can disable this fallback behavior by setting the value of the **glide.ais.custom\_matcher.legacy\_fallback\_enabled** system property to **false**. With this value set, if a search query doesn't match any custom search matcher's regular expression patterns, AI Search treats it as a normal full-text search, ignoring exact matches in tables with defined prefixes.

To learn how AI Search evaluates global search queries for exact matches, see [Using global search with AI Search for Next Experience](../concept/using-ais-next-experience-app.md).

## Procedure

1.  Navigate to **AI Search** &gt; **Search Experience** &gt; **Global Search Custom Matchers**.

2.  Select **New**.

3.  On the Custom Matcher form, fill in the **Name**, **Table**, and **Column** fields.

    For a description of the field values, see [Custom Matcher form](../reference/custom-matcher-form-ais.md).

4.  Populate the form's **Regex** field.

    1.  Select **Generate Regex**.

    2.  In the pop-up window, select the option that more closely matches the values you expect to see in the specified **Column**.

    3.  When prompted, enter the value prefix or select the value numeric delimiter.

    4.  Close the pop-up window by selecting **Submit**.

5.  Select **Submit.**

6.  Navigate to the Custom matchers for Search Applications table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `m2m_search_context_config_custom_matcher.list`.

    3.  Press Enter.

        The Custom matchers for Search Application \[m2m\_search\_context\_config\_custom\_matcher\] table opens in list view.

7.  For each search application that you want to use your custom matcher with, including global search, link the matcher to the application.

    1.  Select **New**.

    2.  On the Custom matchers for Search Application form, fill in the fields.

<table id="table_rdp_5lh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom matcher

</td><td>

The name of your custom search matcher.

</td></tr><tr><td>

Order

</td><td>

Evaluation order for your custom search matcher in the context of the specified AI Search application. Matchers with lower **Order** values are evaluated first.

</td></tr><tr><td>

Search context config

</td><td>

The name of the search application configuration record for the AI Search application that you want to link your custom search matcher to. For global search, select the **\[AIS\] Next Experience Search Configuration** record.

</td></tr></tbody>
</table>    3.  Select **Submit**.

        A linkage record for your custom search matcher and the selected AI Search application appears in the Custom matchers for Search Application \[m2m\_search\_context\_config\_custom\_matcher\] table.


**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)

