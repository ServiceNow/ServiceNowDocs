---
title: Index AI Search for notifications
description: Make content from multiple internal indexed sources searchable by performing a full table index. This procedure indexes existing records from the source tables and any child tables configured for indexing.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate AI Search for Notifications, Preferences in Next Experience, Notification Preferences, Notifications, Configure core features, Administer]
---

# Index AI Search for notifications

Make content from multiple internal indexed sources searchable by performing a full table index. This procedure indexes existing records from the source tables and any child tables configured for indexing.

## Before you begin

Your indexed sources must be active and internal \(referring to ServiceNow AI Platform tables\). To index content from indexed sources for external documents, see [Indexing and searching external content in AI Search](../../ai-search/concept/external-content-ais.md).

Role required: ais\_admin

## About this task

Once you define an indexed source, AI Search begins automatically indexing to reflect changes to records in the selected source table and its specified child tables. The results of all record create, update, and delete operations in these tables are reflected in the search index. AI Search doesn't index content from unmodified records in these tables until you perform a full table index

Follow these steps to index searchable content from existing records in indexed sources. Use the same steps to manually reindex content for indexed sources that have already been indexed.

If an indexed source contains unindexed records, the Indexed Sources list displays an informational message and marks the new source with an alert triangle icon. A similar informational message appears on the Indexed Source form. Make sure to perform a full table index for each indexed source that displays the alert triangle icon.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Search for **Platform Notifications V1** and **Platform Notifications V2**.

3.  In the **Actions on selected rows…** menu, select **Index All Tables**.

    The Indexed Source History page for the last selected index appears. A message reports that AI Search has queued an indexing task for the indexed source.

4.  Refresh the Indexed Source History form page to monitor the progress of the indexing task.

    When the task completes, the **Ingestion State** field shows **indexed**.


**Parent Topic:**[Activate AI Search for Notifications](activate-ai-search-for-notifications-plugin.md)

