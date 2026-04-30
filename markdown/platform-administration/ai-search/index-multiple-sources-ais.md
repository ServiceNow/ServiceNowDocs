---
title: Perform a full table index or reindex for multiple AI Search indexed sources
description: Make content from multiple internal indexed sources searchable by performing a full table index. This procedure indexes existing records from the source tables and any child tables configured for indexing. You can manually reindex content from internal indexed sources by repeating this procedure.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Indexing content from indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Perform a full table index or reindex for multiple AI Search indexed sources

Make content from multiple internal indexed sources searchable by performing a full table index. This procedure indexes existing records from the source tables and any child tables configured for indexing. You can manually reindex content from internal indexed sources by repeating this procedure.

## Before you begin

Your indexed sources must be active and internal \(referring to ServiceNow AI Platform® tables\). To index content from indexed sources for external documents, see [Indexing and searching external content in AI Search](../concept/external-content-ais.md).

Role required: ais\_admin

## About this task

Once you define an indexed source, AI Search begins automatically indexing to reflect changes to records in the selected source table and its specified child tables. The results of all record create, update, and delete operations in these tables are reflected in the search index. AI Search doesn't index content from unmodified records in these tables until you perform a full table index.

Use this procedure to index searchable content from existing records in indexed sources, or to manually reindex content for indexed sources that have already been indexed.

If an indexed source contains unindexed records, the Indexed Sources list displays an informational message and marks the new source with an alert triangle icon ![](../image/icon-alert-triangle.png). A similar informational message appears on the Indexed Source form. Make sure to perform a full table index for each indexed source that displays the alert triangle icon.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Select the indexed sources with content that you want to make searchable.

    To select all indexed sources on the page, follow the instructions for your list version in [Perform actions on selected items in a list](https://www.servicenow.com/docs/access?context=configure-use-list-functions&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

3.  In the **Actions on selected rows…** menu, select **Index All Tables**.

    The Indexed Source History page for the last selected index appears. A message reports that AI Search has queued an indexing task for the indexed source.

4.  Refresh the Indexed Source History form page to monitor the progress of the indexing task.

    When the task completes, the **Ingestion State** field shows **indexed**.

5.  To return to the list of indexed sources, select the back icon ![](../../../use/using-forms/image/FormBackUI15.png).


## Result

AI Search indexes content from existing records in the indexed sources. Indexing continues on a scheduled basis. You don't need to repeat this task for the indexed sources unless you want to reindex their content before the next scheduled indexing run.

## What to do next

Define search sources to make searchable content from indexed sources available in user search experiences. For details on creating search sources, see [Create a search source for AI Search](create-search-source-ais.md).

**Parent Topic:**[Indexing content from AI Search indexed sources](../concept/indexing-content-ais.md)

