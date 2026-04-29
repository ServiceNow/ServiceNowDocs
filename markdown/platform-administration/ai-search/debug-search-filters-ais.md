---
title: Debug search source and content security filters
description: Use the Session Log to view search source and content security filters applied to results for a search query. Administrators can use this approach to verify search source filters and content security settings.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Debug search source and content security filters

Use the Session Log to view search source and content security filters applied to results for a search query. Administrators can use this approach to verify search source filters and content security settings.

## Before you begin

Role required: admin

## About this task

Enable session debugging for AI Search to view debug log messages for search source and content security filters. Each debug log message shows the filters that AI Search applies to determine which records appear in a search query's results.

## Procedure

1.  To enable session debugging for AI Search, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug AI Search**.

2.  Navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug Log**.

    The Session Log opens.

3.  Use the [Search Preview UI for AI Search](../../../use/dashboards/application-content-packs/ai-search-preview.md#) to submit the search query of interest.

    **Note:** To debug content security filters for another user, specify their name in the Search Preview UI's user impersonation tool.

4.  To see the search source filters applied for your search queries, filter the Session Log entries for `AIS:search sources`.

    ![Sample search source filter message.](../image/debug-search-source-filter.png)

5.  To see the content security filters applied when evaluating access to search results for the current \(or impersonated\) ServiceNow AI Platform® user, filter the Session Log entries for `security query`.

    ![Sample content security filter messages.](../image/debug-content-security-filter.png)


## What to do next

If a search source's filters exclude records that should be searchable, modify those filters. For details, see [Create a search source for AI Search](create-search-source-ais.md).

If content security filters prevent the user from seeing search results that should be accessible, correct the access control settings for the affected source records and then reindex content for the relevant indexed source. For details on content security settings, see [Content security in AI Search](../concept/content-security-ais.md). To reindex content, follow the steps from [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Administering AI Search](../concept/administer-ais.md)

