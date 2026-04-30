---
title: Set the default source for search context
description: You can decide which source to set as the default search source.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set the default source for search context

You can decide which source to set as the default search source.

## Before you begin

Role required: admin

## About this task

-   If you set an additional resource as the default source that source is considered the default search source.
-   If you don't mark any additional resource as the default source, then the searcher source is considered the default search source.
-   If you don't have a searcher and you have not marked any additional resource as the default source, the default is the additional resource with the lowest value in the **Order** field.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Search Contexts**.

2.  Open the search context record to change its default source.

3.  To set an additional resource as the default search source:

    1.  Click the Additional Resource Configuration related list.

    2.  Select and hold \(or right-click\) the search resource configuration record and click **Set as Default Search**.

4.  To set a searcher source as the default search source:

    1.  Click the **Set Searcher as the Default Search** related link to set **Searcher** as the default search source.

        **Note:** The **Set Searcher as the Default Search** related link appears only if an additional resource is the default search source.

    2.  To search all searcher sources or a specific searcher source from the list, select **All**.

        **Note:** The **Searcher default search** field appears only when the **Searcher** field contains more than one source.


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

