---
title: Perform a full table index or reindex for a single AI Search indexed source
description: Make content from an internal indexed source searchable by performing a full table index. This procedure indexes existing records from the source table and any child tables configured for indexing. You can manually reindex content from an internal indexed source by repeating this procedure.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Indexing content from indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Perform a full table index or reindex for a single AI Search indexed source

Make content from an internal indexed source searchable by performing a full table index. This procedure indexes existing records from the source table and any child tables configured for indexing. You can manually reindex content from an internal indexed source by repeating this procedure.

## Before you begin

Your indexed source must be active and internal \(referring to a ServiceNow AI Platform® table\). To index content from an indexed source for external documents, see [Indexing and searching external content in AI Search](../concept/external-content-ais.md).

Role required: ais\_admin

## About this task

Once you define an indexed source, AI Search begins automatically indexing to reflect changes to records in the selected source table and its specified child tables. The results of all record create, update, and delete operations in these tables are reflected in the search index. AI Search doesn't index content from unmodified records in these tables until you perform a full table index.

Use this procedure to index searchable content from existing records in an indexed source, or to manually reindex existing content for an indexed source that has already been indexed.

If an indexed source contains unindexed records, the Indexed Sources list displays an informational message and marks the new source with an alert triangle icon ![](../image/icon-alert-triangle.png). A similar informational message appears on the Indexed Source form. Make sure to perform a full table index for each indexed source that displays the alert triangle icon.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source with content that you want to make searchable.

3.  Select **Index All Tables**.

    The Generate Text Index dialog box appears.

4.  If you want AI Search to allow indexing of updates to individual records in the source table while the table indexing event is running, select the **Non blocking index** option.

    **Note:** With this option deselected, AI Search defers indexing of updates to individual records in the source table until after the table indexing event finishes. The index may not reflect the latest contents for updated records until the deferred record indexing events finish.

5.  Select **OK**.

    The Indexed Source History page appears. A message reports that AI Search has queued an indexing task for the indexed source.

6.  To monitor the progress of the indexing task, refresh the Indexed Source History form page.

    When the task completes, the **Ingestion State** field shows **indexed**.

7.  To return to the list of indexed sources, select the back icon ![](../../../use/using-forms/image/FormBackUI15.png).


## Result

AI Search indexes content from existing records in the indexed source. Indexing continues on a scheduled basis. You don't need to repeat this task for the indexed source unless you want to reindex its content before the next scheduled indexing run.

## What to do next

Define search sources to make searchable content from the indexed source available in user search experiences. For details on creating search sources, see [Create a search source for AI Search](create-search-source-ais.md).

**Parent Topic:**[Indexing content from AI Search indexed sources](../concept/indexing-content-ais.md)

